# Secret-Key-Encryption
Secret-Key-Encryption
|  Name   | Title |
| ------------- | ------------- |
| Asad Ali  | Secret-Key-Encryption  |

Instruction: https://seedsecuritylabs.org/Labs_16.04/PDF/Crypto_Encryption.pdf
# Task 1
- Step 1: . First create file ```article.txt```.The usage of tr is available in GNU documentations. -d means 'delete' and -cd means 'delete the complement of', so first we just keep the letters, spaces, and newlines as the plaintext.
```
touch article.txt
echo "This Is a Plain Text Which Is Converted into Cipher Text Using Subtitution" > article.txt
tr [:upper:] [:lower:] < article.txt > lowercase.txt
tr -cd ’[a-z][\n][:space:]’ < lowercase.txt > plaintext.txt
```

![task1a](https://github.com/Asad-Ali-Code/Secret-Key-Encryption/blob/main/task1a.PNG)

- Step 2: Use Python console to generate a permutation of a-z:
```
>>> import random
>>> s = "abcdefghijklmnopqrstuvwxyz"
>>> ''.join(random.sample(s,len(s)))
'jyqsfotweaurdlxkzgcbpnvhmi'
```

![task1b](https://github.com/Asad-Ali-Code/Secret-Key-Encryption/blob/main/task1b.PNG)

- Step 3: Encryption
```
$tr "abcdefghijklmnopqrstuvwxyz" "jyqsfotweaurdlxkzgcbpnvhmi" < plaintext.txt > ciphertext.txt
```

- Step 4: Decryption
```
$tr ’jyqsfotweaurdlxkzgcbpnvhmi’ ’abcdefghijklmnopqrstuvwxyz’ < ciphertext.txt > afterDecrypt.txt
```
