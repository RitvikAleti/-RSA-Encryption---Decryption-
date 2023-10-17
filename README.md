# RSA Encryption - Decryption

The RSA algorithm is a widely used cryptographic algorithm for secure communication, encryption, and digital signatures. It is named after its inventors, Ron Rivest, Adi Shamir, and Leonard Adleman. The RSA algorithm is based on the mathematical properties of large prime numbers and modular arithmetic. RSA Algorithm follows the below steps for encoding and decoding

1. Key Generation:
Two distinct prime numbers, p and q, are selected.
Their product, n = p * q, is calculated. This is the modulus used in encryption and decryption.
Euler's totient function of n, φ(n) = (p - 1) * (q - 1), is calculated. This function calculates the count of positive integers less than n that are coprime (have no common factors) with n.
An integer e is chosen, such that 1 < e < φ(n), and e is coprime with φ(n). This is the public exponent and will be part of the public key.
The modular multiplicative inverse of e modulo φ(n) is calculated. This is a number d such that (d * e) % φ(n) = 1. d is the private exponent and will be part of the private key.

2. Encryption:
The plaintext message is converted to a numeric representation. In RSA, this is often done using the ASCII values of the characters.
The ciphertext c is computed by raising the plaintext message m to the power of the public exponent e modulo n: c = (m^e) % n.

3. Decryption:
The ciphertext c is retrieved.
The plaintext message m is computed by raising the ciphertext to the power of the private exponent d modulo n: m = (c^d) % n.

Upon running the code of the given notebook, you will be prompted to enter the text to be encrypted along with encryption and decryption keys in the frame. I've used tkinter for demonstration.

![Screenshot 2023-07-12 171818](https://github.com/Ananya-Bompalli/RSA/assets/106391241/90c2b34c-5435-4329-91a3-27e16c28436e)

You will then have to select the encrypt option and enter the encryption key to get the encrypted text output

![Screenshot 2023-07-12 172723](https://github.com/Ananya-Bompalli/RSA/assets/106391241/8162dee0-300b-4a12-b669-5516accba8fd)                    ![Screenshot 2023-07-12 171855](https://github.com/Ananya-Bompalli/RSA/assets/106391241/7274b667-b5dc-4497-9655-f26f1ce9ceca)

To decrypt the encrypted message on the receiver side, The decrypted message and the decryption key must be given. 

![Screenshot 2023-07-12 173156](https://github.com/Ananya-Bompalli/RSA/assets/106391241/9aaf7dd4-b25f-40bb-a254-901292b4a307)     
Upon providing the decryption key, the decrypted message is displayed

![Screenshot 2023-07-12 172620](https://github.com/Ananya-Bompalli/RSA/assets/106391241/9d4d5af2-820b-4fe9-a056-edec91f852cc)   ![Screenshot 2023-07-12 171952](https://github.com/Ananya-Bompalli/RSA/assets/106391241/b9f9f710-1fd7-4d55-b41f-b97034122973)
