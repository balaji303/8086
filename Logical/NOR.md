# 16bit Logical NOR

| Address | Mnemonics |
|---------|-----------|
| 0400 | MOV AX,25AB|
| 0403 | MOV BX,6316|
| 0406|OR AX,BX|
|0408|NOT AX|
|040A|MOV [1200],AX|
040E |HLT


#### OUTPUT:
| ADDRESS|DATA|
|---------|-----------|
1200 | 00
1201|88

#### Manual Calculation:

```
AX = 32AC - 0011 0010 1010 1100
BX = 45DF - 0100 0101 1101 1111
OR          0111 0111 1111 1111
NOT         1000 1000 0000 0000
            8    8    0    0
```

#### Truth Table

| x | y | xy |
|---|---|----|
0 | 0 | 1
0 | 1 | 0
1 | 0 | 0
1 | 1 | 0