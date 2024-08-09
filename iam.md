# Discussion

1. What does IAM stand for? What does it mean?
    - Identity and Access Management -> framework of policies and technologies to ensure identification and correct access to resources
2. What's the difference between Authentication and Authorization?
    - Authentication: who are you?
    - Authorization: what can you do?
3. What are the main mechanisms for implementing Authentication in a FullStack Web App?
    - Username / Email + Password
    - JWTs
    - Sessions
    - Social Login
    - OAuth 2.0
4. What are: cookies, sessions, tokens?
    - cookies: stored in the resp headers in HHTP on the client side. You can set an expiration time to invalidate them .
    - sessions: stored on the server-side, higher protection through a more secure way to store them.
        -> FrontEnd Session: you use session from Flask, a specific type of cookie will be created for the browser. xyz.xyz.xyz
        -> Backend Session: data will be stored on the server side, and a cookie with the session ID will be created for the frontend. The cookie will look like this: bckjwgfhbwregi
        - Fernet is the encryption library used under the hood to secure sessions
            -> Has the cookie been tempered with?
            -> Can we decrypt the key using the secret?
    - tokens: pieces of data in JSON notation commonly, that will be stored on the client (i.e. browser)
5. How do we secure passwords so that we do not store bare text in the db? What package can we use in python to do so?
    - Hashing: plain text passed through a "meat-grinder" function, a certain amount of times, until it becomes unrecognizable.
    - Encrypting: Reversible process!!! You can always decrypt if you have the correct key. 
    - Bcrypt: Hashing + Salting -> Blowfish: 1999 Provos and Meziéres use the crypt existing function and the Blowfish cypher

## Lecture Goals
    1. User model with brcrypt and password_security
    2. Set up a session secret and enable sessions
    3. Set up signin, signup, signout routes and test them with Postman
