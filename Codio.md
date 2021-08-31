# End of Module Assignment: OOP application of principles and concepts: En- and decryption of sensitve patient data

### Introduction
The queens medical centre is planning to introduce a web-based appointment and scheduling management information system (ASMIS) to improve patient care and efficiency.
To protect ASMIS and its data against cyber criminals, one suggestion mentioned in the security report was the encryption of sensitve patient data.

This program can en- and decrypt the name of patients, only leaving t

### Instruction
1. Write patients data (ID Number and Name) in PatientData.txt
2. Encrypt patients data with command: python3 Encrypt.py
3. View encrypted data in ProtectedData.txt
4. Decrypt patients data with command: python3 Decrypt.py
5. View decrypted data in DecryptedData.txt

### Description
It is a very simple encryption method based on a rotor encryption. The character is first converted to an ASCII value, then the position on the ASCII line is changed according to a secret key (for example pos+1).
Decryption only needs to subtract the ASCII value of the secret key.
This has of course several downsides


The secret key is converted into ASCII code, the text is converted into ASCII code, and the ASCII code of the secret key is used to cycle and accumulate the ASCII code of the text, and then converted into characters. If the length of the string exceeds 5, after transferring a string of secret keys, start from the beginning.
