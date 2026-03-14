# [Hidden in plainsight (Forensics, Easy)](https://play.picoctf.org/practice/challenge/524)

- Description: You’re given a seemingly ordinary JPG image. Something is tucked away out of sight inside the file. Your task is to discover the hidden payload and extract the flag. Download the jpg image here.
- Solution:

```bash
schufot-picoctf@webshell:~$ file img.jpg 
img.jpg: JPEG image data, JFIF standard 1.01, aspect ratio, density 1x1, segment length 16, comment: "c3RlZ2hpZGU6Y0VGNmVuZHZjbVE9", baseline, precision 8, 640x640, components 3

schufot-picoctf@webshell:~$ echo "c3RlZ2hpZGU6Y0VGNmVuZHZjbVE9" | base64 -d
steghide:cEF6endvcmQ=

schufot-picoctf@webshell:~$ echo "cEF6endvcmQ=" | base64 -d
pAzzword

schufot-picoctf@webshell:~$ steghide extract -sf img.jpg 
Enter passphrase: 
wrote extracted data to "flag.txt".
```

- Flag: ``
- Explanation:
