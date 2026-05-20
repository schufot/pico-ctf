# [bytemancy1 (General Skills, Easy)](https://play.picoctf.org/practice/challenge/762)

## Description

Can you conjure the right bytes? The program's source code can be downloaded here.
Connect to the program with netcat: $ nc foggy-cliff.picoctf.net 62060

## Solution

- Program's source code

```python
while(True):
  try:
    print('⊹──────[ BYTEMANCY-1 ]──────⊹')
    print("☍⟐☉⟊☽☈⟁⧋⟡☍⟐☉⟊☽☈⟁⧋⟡☍⟐☉⟊☽☈⟁⧋⟡☍⟐")
    print()
    print('Send me ASCII DECIMAL 101 1751 times, side-by-side, no space.')
    print()
    print("☍⟐☉⟊☽☈⟁⧋⟡☍⟐☉⟊☽☈⟁⧋⟡☍⟐☉⟊☽☈⟁⧋⟡☍⟐")
    print('⊹─────────────⟡─────────────⊹')
    user_input = input('==> ')
    if user_input == "\x65"*1751:
      print(open("./flag.txt", "r").read())
      break
    else:
      print("That wasn't it. I got: " + str(user_input))
      print()
      print()
      print()
  except Exception as e:
    print(e)
    break
```

- Hex `\x65` equals 101 in decimal
- ASCII decimal 101 equals character e
- "\x65" == "e"
- "\x65"*1751 == "e"*1751
- Program expects 1751 times `e`

```bash
schufot-academy@webshell:~$ python3 -c 'print("e"*1751)' | nc foggy-cliff.picoctf.net 62060
⊹──────[ BYTEMANCY-1 ]──────⊹
☍⟐☉⟊☽☈⟁⧋⟡☍⟐☉⟊☽☈⟁⧋⟡☍⟐☉⟊☽☈⟁⧋⟡☍⟐

Send me ASCII DECIMAL 101 1751 times, side-by-side, no space.

☍⟐☉⟊☽☈⟁⧋⟡☍⟐☉⟊☽☈⟁⧋⟡☍⟐☉⟊☽☈⟁⧋⟡☍⟐
⊹─────────────⟡─────────────⊹
==> picoCTF{h0w_m4ny_e's???_e0d51f4b}
```


## Flag

`picoCTF{h0w_m4ny_e's???_e0d51f4b}`
