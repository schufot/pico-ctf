# [hashcrack (Cryptography, Easy)](https://play.picoctf.org/practice/challenge/475) - 

- Description: A company stored a secret message on a server which got breached due to the admin using weakly hashed passwords. Can you gain access to the secret stored within the server?
- Solution:
  ```bash
  schufot-picoctf@webshell:~$ nc verbal-sleep.picoctf.net 60626
  Welcome!! Looking For the Secret?
  
  We have identified a hash: 482c811da5d5b4bc6d497ffa98491e38
  Enter the password for identified hash:
  ```
  - `482c811da5d5b4bc6d497ffa98491e38`: MD5 hash, which is 32 hexadecimal characters
  - `https://crackstation.net/` reveals for it `password123`
  
  ```bash
  Enter the password for identified hash: password123
  Correct! You've cracked the MD5 hash with no secret found!
  
  Flag is yet to be revealed!! Crack this hash: b7a875fc1ea228b9061041b7cec4bd3c52ab3ce3
  Enter the password for the identified hash:
  ```
  - `b7a875fc1ea228b9061041b7cec4bd3c52ab3ce3`: SHA-1 hash, 40 characters
  - `https://crackstation.net/` reveals for it `letmein`
  
  ```bash
  Enter the password for the identified hash: letmein
  Correct! You've cracked the SHA-1 hash with no secret found!
  
  Almost there!! Crack this hash: 916e8c4f79b25028c9e467f1eb8eee6d6bbdff965f9928310ad30a8d88697745
  Enter the password for the identified hash:
  ```
  - `916e8c4f79b25028c9e467f1eb8eee6d6bbdff965f9928310ad30a8d88697745`: SHA-256 hash, 64 characters
  - `https://crackstation.net/` reveals for it `qwerty098`
  
  ```bash
  Enter the password for the identified hash: qwerty098
  Correct! You've cracked the SHA-256 hash with a secret found. 
  The flag is: picoCTF{UseStr0nG_h@shEs_&PaSswDs!_5b836723}
  ```
- Flag: `picoCTF{UseStr0nG_h@shEs_&PaSswDs!_5b836723}`
- Explanation:
