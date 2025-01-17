# 16bit Addition without Carry

| Address | Mnemonics |
|---------|-----------|
| 0400 | MOV AX,1234|
| 0403 | MOV BX,4321|
| 0406|ADD AX,BX|
|0408|MOV [1200],AX|
040C |HLT


#### OUTPUT:
| ADDRESS|DATA|
|---------|-----------|
1200 | 55
1201|55

#### Manual Calculation:

AX = 1234
BX = 4321

AX = 5555, so 1200 = 55 and 1201 = 55


# 16 bit addition with carry


| Address | Mnemonics |
|---------|-----------|
| 0400 | MOV DX,0000|
| 0403 | MOV AX,[1200]|
| 0407 | MOV BX,[1202]|
| 040B|ADD AX,BX|
|040C|JNC 0410|
040F |INC DX
0410|MOV [1204],AX
0412|MOV [1206],DX
0413|HLT

#### Input and Output

| Input ||| Output |
|-------|--------|-------|--------|
| Address | Data | Address | Data |
|-------|--------|-------|--------|
1200|54 04 | 1204 | 89 0A
1201 | 76 00 | 1205 | OD 00
1202 | 35 07 | 1206 | 01 00
1203 | 97 00| 1207 | 00 00

#### Manual Calculation

```
AX = 7654
BX = 9735
TOTAL = 0D89

DX = 0001
1204 = 89
1205 = OD
```