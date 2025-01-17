# 16bit Multiplication

| Address | Mnemonics |
|---------|-----------|
| 0400 | MOV AX,1234|
| 0403 | MOV BX,4321|
| 0406|MUL BX|
|0408|MOV [1200],AX|
|0408|MOV [1200],DX|
0410 |HLT


#### OUTPUT:
| ADDRESS|DATA|
|---------|-----------|
1200 | B4
1201|F4
1202|C5
1203|04

#### Manual Calculation:

```
AX = 1234
BX = 4321

AX = 04C5F4B4
```