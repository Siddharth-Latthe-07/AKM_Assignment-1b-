# AKM_Assignment-1b
## Problem Statement:- Create a text file with some sensitive text. Share this file with the other developer by encrypting it without a shared password. Else sharing the password itself can be tricky. The encryption should happen on the command line in a linux machine. Use docker if needed.
### In this problem, the overall workflow is as below:-

### Encryption Workflow:
  - Create a Text File:
    
    - Created a text file(sensitive.txt)
  - Generate a Random Symmetric Key:
  
    - This done through OpenSSL,to generate a random symmetric key and save it to a file. (key.txt)
   
  - Encrypt the Text File:

    - Use OpenSSL to encrypt the text file using the generated symmetric key.

      Save the encrypted file.(sensitive_data_encrypted.txt)
  - Sharing Encrypted File and Symmetric Key:

    - Share both the encrypted file and the symmetric key to desired person
### Decryption Workflow:
  - Decrypt the File:
    - Use OpenSSL to decrypt the encrypted file using the shared symmetric key.

      Save the decrypted content to a new file. (Decryption syntax:- openssl enc -d -aes-256-cbc -in sensitive_data_encrypted.txt -out sensitive_data_decrypted.txt -pass file:symmetric_key.txt)

  <img width="605" alt="Screenshot 2024-01-08 194737" src="https://github.com/Siddharth-Latthe-07/AKM_Assignment-1b-/assets/121747151/c57b05e5-c37d-44d4-9584-114e0dea7b81">
