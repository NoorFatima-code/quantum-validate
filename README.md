# quantum-validate

Input validators for Quantum Language: email, URL, password strength, Pakistani phone numbers and CNIC.

## Install

```
qpm install quantum-validate
```

## Usage

```
# @use quantum-validate

let email = "noor@example.com"

if QValidate.is_email(email) {
  print("Valid email")
}

print(QValidate.is_pk_phone("0300-1234567"))      # true
print(QValidate.is_cnic("35202-1234567-1"))       # true
print(QValidate.format_cnic("3520212345671"))     # 35202-1234567-1
print(QValidate.is_strong_password("Abcd@1234"))  # true
```

## API

- `is_email(s)`: true agar email format sahi ho
- `is_url(s)`: true agar `http://` ya `https://` URL sahi ho
- `is_strong_password(s)`: 8+ chars, upper, lower, digit aur special character
- `is_pk_phone(s)`: Pakistani mobile (`03XXXXXXXXX`, `+923XXXXXXXXX`, `923XXXXXXXXX`)
- `is_cnic(s)`: 13 digits ya `XXXXX-XXXXXXX-X` format
- `format_cnic(s)`: CNIC ko `XXXXX-XXXXXXX-X` me badalta hai, invalid par `""` deta hai

## License

MIT