# Fernet Encryption Library

Flask uses a cryptographic algorithm called **Fernet** for session encryption and signing. Fernet is a symmetric encryption algorithm provided by the cryptography library, which is a dependency of Flask and Werkzeug.

Fernet is based on the AES (Advanced Encryption Standard) symmetric encryption algorithm and provides authenticated encryption, which ensures both confidentiality and integrity of the data. It uses a symmetric key (the secret key) to encrypt and decrypt the data.
Regarding the cryptographic signature, Fernet utilizes the HMAC (Hash-based Message Authentication Code) algorithm. HMAC is a widely-used mechanism for verifying the integrity and authenticity of a message. It combines a cryptographic hash function (such as SHA-256) with a secret key to generate a fixed-size signature.
In summary:

1. Encryption Algorithm: Fernet (based on AES)
2. Signature Algorithm: HMAC (using a cryptographic hash function)

These encryption and signature algorithms provide a strong level of security for session data in Flask. However, it's essential to ensure that the `app.secret_key` used for encryption is kept secret and adequately protected to maintain the integrity of the session data.