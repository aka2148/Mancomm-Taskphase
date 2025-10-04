# Question
Make an encryption and brute force decryption for hill cipher with known blocksize

## Solution
```
import numpy as np

matrix = np.array([[4, 4],
                   [7, 6]])

def hill_encrypt_2x2(plaintext, key):
    plaintext = ''.join(filter(str.isalpha, plaintext.upper()))
    # just ensuring that the string doesn't have any non-alphabetical characters

    if len(plaintext) % 2 != 0:
        plaintext += 'A'
        # padding the string if not divisible by 2 since our block size is 2

    ciphertext = ''

    for i in range(0, len(plaintext), 2):
        block = plaintext[i:i+2]
        # slicing the array to get the block

        P = np.array([[ord(block[0]) - ord('A')],
                      [ord(block[1]) - ord('A')]])
        # getting ascii values and subtracting ord('A') so that the mapping is like A=0, B=1 etc

        C = np.dot(key, P) % 26
        # multiplies our 2x2 key matrix with the 2x1 block which gives another 2x1 matrix which becomes part of ciphertext

        cipher_block = ''.join(chr(num[0] + ord('A')) for num in C)
        ciphertext += cipher_block

    return ciphertext

encrypted = hill_encrypt_2x2("taskphase", matrix)
print(encrypted)
```

