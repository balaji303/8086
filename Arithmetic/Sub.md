# 16bit Subtraction without Carry

| Address | Mnemonics |
|---------|-----------|
| 0400 | MOV AX,3242|
| 0403 | MOV BX,1111|
| 0406|SUB AX,BX|
|0408|MOV [1200],AX|
040C |HLT


#### OUTPUT:
| ADDRESS|DATA|
|---------|-----------|
1200 | 31
1201|21

#### Manual Calculation:

```
AX = 3242
BX = 1111

AX = 2131, so 1200 = 31 and 1201 = 21
```

# 16 bit Subtraction with carry


| Address | Mnemonics |
|---------|-----------|
| 0400 | MOV DX,0000|
| 0403 | MOV AX,[1200]|
| 0407 | MOV BX,[1202]|
| 040B|SUB AX,BX|
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
1200|67 | 1204 | 43
1201 | 54 | 1205 | CA
1202 | 23 | 1206 | 01
1203 | 8A| 1207 | 00

#### Manual Calculation

AX = 5467
BX = 8A23
TOTAL = CA44

DX = 0001
1204 = 44
1205 = CA