# Bcrypt Notes

Bcrypt is a password hashing function designed by Niels Provos and David Mazières in 1999. It is based on the Blowfish symmetric block cipher algorithm and is specifically designed to hash passwords securely.
The key features of bcrypt include the use of a salt and an adaptive work factor, which make it resistant to brute-force attacks and rainbow table attacks.

Here's an overview of how the salt and hashing mechanism works in bcrypt:

1. Salt Generation: A salt is a random value used to add complexity to the hashing process. When hashing a password with bcrypt, a random salt is generated for each password. The salt is then stored together with the resulting hash.
2. Key Expansion: Bcrypt uses the Blowfish cipher to perform a key expansion step. The password, along with the salt, is used as the input to generate an encryption key for the cipher. The Blowfish algorithm repeatedly modifies the key based on the input data.
3. Adaptive Work Factor: Bcrypt allows you to specify a work factor, which determines the computational cost of the hashing algorithm. The work factor is a measure of how many iterations the algorithm should perform. A higher work factor increases the time it takes to compute the hash, making it more difficult for an attacker to perform a brute-force attack.
4. Hash Computation: Bcrypt iteratively applies the Blowfish algorithm, using the expanded key and the salt, to hash the password. The number of iterations is determined by the work factor.
5. Hash Output: The resulting hash, along with the salt and work factor, is stored in a format that includes all the necessary information for password verification. During password verification, bcrypt performs the same steps to compute a new hash using the provided password, salt, and work factor. It then compares the computed hash with the stored hash. If they match, the password is considered valid.