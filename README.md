# toy-aes
A toy Go implementation of AES.

This was for fun, to practice with Go, and to get to know AES in depth.

I've implemented this according to FIPS 197 (16-byte blocks, 10/12/14 rounds for 128/192/256 bit keys), but have set up vars to allow for tuning as with Rijndael.

I've chosen (for multiple reasons) to use predefined lookup tables for the S-boxes and MixColumns Galois Field multiplication. I'm doing Galois field exponentiation for the rcon() function during key expansion.