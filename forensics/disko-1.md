# [DISKO 1 (Forensics, Easy)](https://play.picoctf.org/practice/challenge/505)

- Description: Can you find the flag in this disk image? Download the disk image here.
- Solution:

```bash
schufot-picoctf@webshell:~$ strings disko-1.dd | grep picoCTF
picoCTF{1t5_ju5t_4_5tr1n9_c63b02ef}
```

- Flag: `picoCTF{1t5_ju5t_4_5tr1n9_c63b02ef}`
- Explanation:
 - strings disko-1.dd: Scans the binary disk image file for readable ASCII strings
 - grep picoCTF: Filters out only the strings that contain picoCTF
