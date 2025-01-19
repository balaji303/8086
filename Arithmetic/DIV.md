# 16bit Division

| Address | Mnemonics |
|---------|-----------|
| 0400 | MOV AX,000E|
| 0403 | MOV BH,07|
| 0406|DIV BH|
|0408|MOV [1200],AH|
|0408|MOV [1201],AL|
0410 |HLT


#### OUTPUT:
| ADDRESS|DATA|
|---------|-----------|
1200 | 00
1201|02

#### Manual Calculation:

```
AX = 000E
BX = 07

AX = 0002
```