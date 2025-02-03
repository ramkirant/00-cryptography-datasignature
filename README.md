# Cryptography and Data Signature

Data Signatures are used to prevent man in the middle attacks when data is being transmitted over the internet. There are two types of man in the middle attacks. 

1. Passive Attack:
   When the Data is read without being modified, it is called Passive Attack
3. Active Attack:
   When the Data is read and also modified, it is called Active Attack.

## Encryption
Man in the middle attacks can be prevented by encrypting or decrypting our data. As a part of encryption, We convert our data to a cypher text using a key. As a part of decryption, this cypher text is converted back to data using the same key.  

There are two types of keys used in encrypton. 
1. Symmetric Key:

   As a part of Symmetric Key encryption, data is encrypted and decrypted using the same key. Symmetric Key encryption comes with a problem of defined a secure way of sharing the encryption key between multiple parties. For obvious reasons, this key cannot be shared over the internet so it has to happen offline. And the key needs to be shared everytime the key gets modified.

   Symmetric Key Algorithms

   a. AES (Advanced Encryption Standard)

   b. DES (Data Encryption Standard)
   
3. Asymmetric Key:

   As a part of Assymetric key encryption, data is encrypted and decrypted using different keys. There are two types of keys in Assymetric encryption. A public key and a private key. 

   a. The data that is encrypted using the public key has to be decrypted using the private key.
   
   b. The data that is encrypted using the private key has to be decrypted using the public key.

    The sender encrypts the data using the receivers public key and the receiver decrypts the data using his private key.

   Assymetric Key algorithms

   a. RSA (Rivest, Shamir, Adleman)

   b. ECC (Elliptic Curve Cryptography)

## Digital Signatures
Digital Signatures authenticates the identity of the entity that is transmitting the message.

Digital Signature is achieved by:

a. Sender encrypts the data using his own private key

b. Receiver decrypts the data using the sender's public key. 

By being able to decrypt the data using the sender's public key, The receiver would be ensured of the authenticity of the source of data. 

### How can we prevent both active and passive man in the middle attacks at the same time?

a. The sender encrypts the data using the receiver's public key. This prevents passive attacks. 

b. The sender would them encrypt the data using his own private key. Theis prevents active attacks. 

c. The receiver would decrypt the data using the sender's public key and verify the authenticity of the source of data.

d. The receiver would decrypt the data using his own private key to view the data. 
