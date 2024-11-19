
# Transposition Cipher Project

## Overview
This project implements a **Transposition Cipher** — a classical encryption technique that rearranges the characters of a plaintext message to create ciphertext. The project includes functionality to encrypt, decrypt, and brute-force decrypt messages encrypted using the cipher.

---

## Features
- **Encryption**: Encrypt a plaintext message using a specified key.
- **Decryption**: Decrypt a ciphertext back to plaintext using the same key.
- **Hacking**: Brute-force decrypt an encrypted message by trying all possible keys.

---

## How It Works
The Transposition Cipher rearranges characters by dividing the message into columns based on the encryption key. The ciphertext is formed by concatenating the columns. To decrypt, the ciphertext is reconstructed row by row.

---

## Usage

### 1. Encryption
```python
cipher = TranspositionCipher(key=5)
plaintext = "This is a secret message"
encrypted = cipher.encrypt_message(plaintext)
print("Encrypted Message:", encrypted)
```

**Output**:
```
Encrypted Message: Tssessih iec et sarge
```

### 2. Decryption
```python
cipher = TranspositionCipher(key=5)
ciphertext = "Tssessih iec et sarge"
decrypted = cipher.decrypt_message(ciphertext)
print("Decrypted Message:", decrypted)
```

**Output**:
```
Decrypted Message: This is a secret message
```

### 3. Hacking (Brute Force Decryption)
```python
encrypted_message = "Tssessih iec et sarge"
hacked_results = hack_cipher(encrypted_message)
```

**Output** (Sample):
```
Key: 1, Decrypted Message: Tssessih iec et sarge
Key: 5, Decrypted Message: This is a secret message
Key: 10, Decrypted Message: Tece  sssh  igssatreie
...
```

---

## Files
- `transposition_cipher.py`: Contains the implementation of the `TranspositionCipher` class and the `hack_cipher` function.
- `README.md`: Documentation for the project.
