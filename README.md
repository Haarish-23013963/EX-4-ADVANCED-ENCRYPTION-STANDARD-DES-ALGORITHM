# Ex-8-Implement-the-AES-Encryption-and-Decryption
## AIM :
To use Advanced Encryption Standard (AES) Algorithm for a practical application like URL Encryption.

## ALGORITHM :
Step 1: AES is based on a design principle known as a substitution–permutation.

Step 2: AES does not use a Feistel network like DES, it uses variant of Rijndael.

Step 3: It has a fixed block size of 128 bits, and a key size of 128, 192, or 256 bits.

Step 4: AES operates on a 4 × 4 column-major order array of bytes, termed the state.

## PROGRAM :
### NAME: HAARISH V
### REGISTER NO: 212223230067

```
#include <stdio.h>
#include <string.h>

void xor_encrypt_decrypt(char *input, char *key) {
    int input_len = strlen(input);
    int key_len = strlen(key);

    for (int i = 0; i < input_len; i++) {
        input[i] = input[i] ^ key[i % key_len]; 
    }
}

int main() {
    char url[256], key[256];

    // Asking for user input
    printf("Enter the URL/string to encrypt: ");
    fgets(url, sizeof(url), stdin);
    url[strcspn(url, "\n")] = '\0'; // Remove trailing newline from fgets

    printf("Enter the key for encryption: ");
    fgets(key, sizeof(key), stdin);
    key[strcspn(key, "\n")] = '\0'; // Remove trailing newline from fgets

    printf("Original URL: %s\n", url);

    xor_encrypt_decrypt(url, key);
    printf("Encrypted URL: %s\n", url);

    xor_encrypt_decrypt(url, key);
    printf("Decrypted URL: %s\n", url);

    return 0;
}
```
## OUTPUT:
![Screenshot 2025-04-21 091651](https://github.com/user-attachments/assets/93f6ba4f-64e7-416a-b88a-310a8dc39a7a)



## RESULT:
Hence,to use Advanced Encryption Standard (AES) Algorithm for a practical application like URL Encryption is done successfully.
