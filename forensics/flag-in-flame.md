# [Flag in Flame (Forensics, Easy)](https://play.picoctf.org/practice/challenge/523)

- Description: The SOC team discovered a suspiciously large log file after a recent breach. When they opened it, they found an enormous block of encoded text instead of typical logs. Could there be something hidden within? Your mission is to inspect the resulting file and reveal the real purpose of it. The team is relying on your skills to uncover any concealed information within this unusual log. Download the encoded data here: Logs Data. Be prepared—the file is large, and examining it thoroughly is crucial .
- Solution:

```bash
schufot-picoctf@webshell:~$ base64 -d logs.txt > output_image
schufot-picoctf@webshell:~$ file output_image
output_image: PNG image data, 896 x 1152, 8-bit/color RGB, non-interlaced
```
  - output_image.png: <img width="896" height="1152" alt="output" src="https://github.com/user-attachments/assets/c7324754-63fc-4267-a7d8-91afbb7df815" />


- Flag: ``
- Explanation:
