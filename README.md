# AES
 Basic AES128 encryption algorithm using GF28 objects in C++.

## Overview
This class implements an AES 128 algorithm where the intermediate states are objects of type gf28, which stand for elements in a galois field GF(2^8). The objects support correct addition and multiplication, hence the implementation here is identical in form to the Rijndael algorithm description. This adds only readability of the code in comparison other implementations. This class is based on the work by SergeyBel (https://github.com/SergeyBel).

The gf28 class itself is hosted at https://github.com/jevillegasd/GF2-8

## Use
```c++
 #include "AES.h"
 uint8_t key[16] = { 0x11, 0x22, 0x33, 0x44}; // The class will automaticaly expand the key when declared.
 uint8_t plain_text0[16] = "This is secret.";
 
 AES aes(key);
 aes.Cipher(plain_text);
 aes.Decipher(plain_text);

```
