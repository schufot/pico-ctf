# [Riddle Registry (Forensics, Easy)](https://play.picoctf.org/practice/challenge/530)

- Description: Hi, intrepid investigator! You've stumbled upon a peculiar PDF filled with what seems like nothing more than garbled nonsense. But beware! Not everything is as it appears. Amidst the chaos lies a hidden treasure—an elusive flag waiting to be uncovered. Find the PDF file here Hidden Confidential Document and uncover the flag within the metadata.
- Solution:
  - Author value in metadata is `cGljb0NURntwdXp6bDNkX20zdGFkYXRhX2YwdW5kIV9jOTk5ZTJhNH0=` which is Base64 encoded

```bash
schufot-picoctf@webshell:~$ echo cGljb0NURntwdXp6bDNkX20zdGFkYXRhX2YwdW5kIV9jOTk5ZTJhNH0= | base64 -d
picoCTF{puzzl3d_m3tadata_f0und!_c999e2a4}
```

- Flag: `picoCTF{puzzl3d_m3tadata_f0und!_c999e2a4}`
