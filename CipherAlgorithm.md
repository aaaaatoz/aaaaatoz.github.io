#Common Cipher Algorithm
Cipher Algorithm is widely used in computer science and industry. Below are the common cipher algorithm
- One Way hash algorithm: MD5, SHA
- Symmetric-key algorithm: DES, AES
- ASymmetric-key algorithm: RSA


## MD5
MD5 is now widely used to generate a fix-length 128-bit (16-byte) hash value, typically expressed in text format as a 32 digit hexadecimal number, from a variable length of bytes (file). It has some weakness and not collision resistant.  now MD5 digests have been widely used in the software world to provide some assurance that a transferred file has arrived intact.

## SHA
SHA is quite similar to MD5 while it has bounch of algorithms as SHA-1, SHA-2, SHA-3 etc. it will generate 160 bit output msg SHA-1 or variable(224, 256, 512) bit output msg. compared with MD5, it is stronger and moden Web Browser encourage you use SHA-2 for SSL certification key generation.

## DES/3DES
DES and its Successor - 3DES has three parts:`key,data,mode`
- key is the 56 bit encryption/decryption key
- data is the raw data
- mode is either encryption or decryption
with these three elements - eg : key+raw data+encryption, we can generate a encrypted data stream and the receiver can get the use key + encrypted data + decrytion to get the raw data.
as the key is shared between the sender and receiver, 56 bit is too short so the algorithm has been abolished in industry.

## AES
similar to the DES but use longer key (128, 196, 256) and different algorithm. It is widely used in SSL or TLS communication.

## RSA
public-key cryptography or asymmetric cryptography needs a pair of keys called public key and private key. user can't get the private key from its' public key and visa versa. there are two typically usage for asymmetric cryptography.
- sender use the public key to encrypt the information and only the receiver with correct private key can decrypt the information. It is used to prevent critical information tapped by third party
- sender use the private key to encrypt the information and the receiver with public known public key can decrypt and confirm the information is exactly from the sender.