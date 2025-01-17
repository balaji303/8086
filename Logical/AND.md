# 16bit Logical AND

| Address | Mnemonics |
|---------|-----------|
| 0400 | MOV AX,32AC|
| 0403 | MOV BX,45DF|
| 0406|AND AX,BX|
|0408|MOV [1200],AX|
040C |HLT


#### OUTPUT:
| ADDRESS|DATA|
|---------|-----------|
1200 | 8C
1201|00

#### Manual Calculation:

```
AX = 32AC - 0011 0010 1010 1100
BX = 45DF - 0100 0101 1101 1111
            0000 0000 1000 1100
            0    0    8    C
```

#### Truth Table

| x | y | xy |
|---|---|----|
0 | 0 | 0
0 | 1 | 0
1 | 0 | 0
1 | 1 | 1