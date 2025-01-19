# 16bit Logical NAND

| Address | Mnemonics |
|---------|-----------|
| 0400 | MOV AX,25AB|
| 0403 | MOV BX,7376|
| 0406|AND AX,BX|
|0408|NOT AX|
|040A|MOV [1200],AX|
040E |HLT


#### OUTPUT:
| ADDRESS|DATA|
|---------|-----------|
1200 | 5D
1201|DE

#### Manual Calculation:

```
AX = 25AB - 0010 0101 1010 1011
BX = 7376 - 0111 0011 1111 0110
AND         0010 0001 1010 0010
NOT         1101 1110 0101 1101
            D    E    5    D
```

#### Truth Table

| x | y | xy |
|---|---|----|
0 | 0 | 1
0 | 1 | 1
1 | 0 | 1
1 | 1 | 0