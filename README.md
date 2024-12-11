# Multiple Cryptographic Functionalities

## Overview

This Python application integrates various cryptographic functionalities into a single interactive program. Users can perform encryption, decryption, hashing, digital signature generation/verification, and Message Authentication Code (MAC) generation.

Developed by **Alina Hasan**

---

## Features

1. **AES Encryption/Decryption**  
   Supports encryption and decryption using AES in ECB or CBC modes. Users can input plaintext/ciphertext, specify the AES mode, provide keys, and select the desired operation.

2. **RSA Encryption/Decryption**  
   Implements RSA for encrypting and decrypting messages. Users can generate RSA keys and perform encryption or decryption.

3. **Hashing**  
   Provides hashing functionalities using SHA1, SHA256, and MD5. Users can input data and select the hashing algorithm.

4. **Digital Signature using RSA**  
   Facilitates the creation and verification of digital signatures to ensure message integrity and authenticity.

5. **MAC Generation**  
   Supports generation of Message Authentication Codes using CMAC (Cipher Block Chaining-MAC) and HMAC (Hash-based Message Authentication Code).

---

## Installation

Before running the program, install the required cryptographic library:

```bash
pip install pycryptodome
```

---

## Usage

### Running the Application

Run the program in a Python environment. Upon execution, a menu will appear with the following options:

1. **AES Encryption/Decryption**
   
   - Choose ECB or CBC mode.
   - Specify whether to encrypt or decrypt.
   - Input the message and key.

2. **RSA Encryption/Decryption**
   
   - Generate RSA keys (private and public).
   - Choose encryption or decryption.
   - Input the required keys and message.

3. **Hashing**
   
   - Select the hashing algorithm (SHA1, SHA256, or MD5).
   - Input the message to hash.

4. **Digital Signature using RSA**
   
   - Generate a signature or verify an existing one.
   - Provide the necessary keys and message.

5. **MAC Generation**
   
   - Choose between CMAC and HMAC.
   - Input the message to generate the MAC.

6. **Exit**
   
   - Quit the application.

---

## Examples

### AES Encryption

- Mode: CBC
- Message: `HelloWorld`
- Key: `mysecretkey`

```plaintext
Encrypted text: b'\xab\xcd\xef...'
Decrypted text: HelloWorld
```

### RSA Encryption

- Generate keys:
  
  - Prime Numbers: `p = 17`, `q = 23`
  - Public Key (e, N): `(3, 391)`
  - Private Key (d): `275`

- Encrypt: `M = 42`
  
  ```plaintext
  Encrypted message: 180
  ```

- Decrypt: `C = 180`
  
  ```plaintext
  Decrypted message: 42
  ```

### Hashing

- Algorithm: SHA256
- Message: `SecureHash`

```plaintext
Hash Value: 7c2a55...e3a6f9
```

### Digital Signature

- Message: `VerifyThis`
- Signature: Generated using RSA private key.
- Verification: Valid or Invalid.

### MAC Generation

- Message: `AuthenticateMe`
- CMAC/HMAC: Generates a unique signature for the message.

---

## Implementation Details

### Modules Used

- `pycryptodome` for cryptographic functionalities.
- `hashlib`, `base64`, `os`, `hmac` for supporting utilities.

### Cryptographic Algorithms

- **AES**: Encryption/Decryption using block ciphers.
- **RSA**: Public/Private key cryptography for secure communication.
- **SHA1/SHA256/MD5**: Hash functions for integrity.
- **MAC**: Ensures authenticity using CMAC or HMAC.

### Input Validation

- Prime checking using `is_prime` function.
- Coprime validation for RSA key generation.

---

## Future Improvements

- Extend support for additional algorithms (e.g., DES, RSA-OAEP).
- Add a GUI for improved user experience.
- Provide more robust error handling for invalid inputs.

---

## License

This project is for academic purposes. Redistribution or commercial use is prohibited without permission.

---

## Contact

**Alina Hasan**  
Email: [alina.hasan@g.bracu.ac.bd]()  
ID: 20101301
