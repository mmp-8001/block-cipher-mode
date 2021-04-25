
# ECB (Electronic Code Book)  
All about ECB and it's serious weaknesses when used incorrectly.
  
* [Definition](#definition)  
* [Disadvantages](#disadvantages)
* [Encryption Diagram](#encryption-diagram)  
* [Decryption Diagram](#decryption-diagram)  
*  [Attacks](#attacks)  
* *  [Padding](#padding)  
  
## [Definition](#definition)  
The simplest of the encryption modes is the **electronic codebook** (ECB) mode. The message is divided into blocks, and each block is encrypted separately.

## [Disadvantages](#disadvantages)
The disadvantage of this method is a lack of diffusion. Because ECB encrypts identical plaintext blocks into identical ciphertext blocks, it does not hide data patterns well. ECB is not recommended for use in cryptographic protocols.

## [Encryption diagram](#encryption-diagram)  
![encryption diagram](https://upload.wikimedia.org/wikipedia/commons/thumb/d/d6/ECB_encryption.svg/601px-ECB_encryption.svg.png)

## [Decryption diagram](#decryption-diagram)  
![decryption diagram](https://upload.wikimedia.org/wikipedia/commons/thumb/e/e6/ECB_decryption.svg/601px-ECB_decryption.svg.png)

## [Attacks](#attacks)  
All attacks in ECB mode.

## [Padding](#padding)  
Suppose you can encrypt your input append to something important.
`plain_text = input + flag`
Take random string which have 15 characters as `input`.
Then `plain_text` which encrypt in first block has 1 char of flag.
As char is a byte we can find that first char of flag bye brute-forcing it.