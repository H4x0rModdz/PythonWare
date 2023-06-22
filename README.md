# PythonWare

<p align="center">
  <img src="https://github.com/H4x0rModdz/PythonWare/blob/main/pythonware.jpg" alt="PythonWare Logo" width="200">
</p>

<p align="center">
  A Python ransomware developed by H4x0rModdz.
</p>

---

**WARNING: The use of this ransomware is strictly illegal and unethical. This project is for educational and demonstration purposes only. The author is not responsible for any misuse or illegal use of this application.**

---

## About PythonWare

PythonWare is a Python ransomware designed to encrypt files on an infected system and demand a ransom (bitcoins) to decrypt them.

The ransomware utilizes the `cryptography` library for file encryption and decryption, and the `os` module for file and directory manipulation.

## Functionality

The ransomware consists of two main scripts: `wolf.py` and `decrypt.py`.

### wolf.py

The `wolf.py` script locates and encrypts the files on the infected system. It follows these steps:

1. Locates all files in the current directory.
2. Generates an encryption key using the `Fernet.generate_key()` method from the `cryptography` library.
3. Stores the generated key in a file named `thekey.key`.
4. Iterates through the list of files and individually encrypts each file using the generated key.
5. Overwrites the original files with the encrypted files.
6. Displays a ransom message demanding the payment of 0.25 Bitcoins in exchange for the decryption key.

### decrypt.py

The `decrypt.py` script is responsible for decrypting the files after the ransom payment. It performs the following steps:

1. Locates all files in the current directory.
2. Reads the decryption key stored in the `thekey.key` file.
3. Prompts the user for a secret phrase to unlock the decryption process.
4. If the secret phrase provided by the user matches the expected phrase, proceeds with the decryption process.
5. Iterates through the list of files and individually decrypts each file using the stored key.
6. Overwrites the encrypted files with the original decrypted files.
7. Displays a success message indicating that the files have been decrypted.

## How to Use

1. Clone the PythonWare repository to your system:

   ```bash
   git clone https://github.com/H4x0rModdz/PythonWare.git

2. Install Cryptography
   
   ```bash
   pip install cryptography

3. Install Python3   
You can download the latest version of Python from the official [Python Downloads](https://www.python.org/downloads/) page.

<br/>

4. Run the wolf.py script to encrypt the files:

   ```bash
   python3 wolf.py
After execution, all files in the directory (excluding the ransomware scripts themselves) will be encrypted.

<br/>

5. After "paying" the ransom, run the decrypt.py script to decrypt the files:

   ```bash
   python3 decrypt.py

<br/>

6. Password? github.com/H4x0rModdz/PythonWare

<br/>

Please note that using ransomware is illegal and unethical. The above code is provided for educational purposes only and should not be used maliciously.
