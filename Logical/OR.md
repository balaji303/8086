# 16bit Logical OR

| Address | Mnemonics |
|---------|-----------|
| 0400 | MOV AX,32AC|
| 0403 | MOV BX,45DF|
| 0406|OR AX,BX|
|0408|MOV [1200],AX|
040C |HLT


#### OUTPUT:
| ADDRESS|DATA|
|---------|-----------|
1200 | FF
1201|77

#### Manual Calculation:

```
AX = 32AC - 0011 0010 1010 1100
BX = 45DF - 0100 0101 1101 1111
            0111 0111 1111 1111
            7    7    F    F
```

#### Truth Table

| x | y | xy |
|---|---|----|
0 | 0 | 0
0 | 1 | 1
1 | 0 | 1
1 | 1 | 1