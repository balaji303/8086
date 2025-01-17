# 16bit Logical AND

| Address | Mnemonics |
|---------|-----------|
| 0400 | MOV AX,89CD|
| 0403 | NOT AX|
|0405|MOV [1200],AX|
0409 |HLT


#### OUTPUT:
| ADDRESS|DATA|
|---------|-----------|
1200 | 32
1201|76

#### Manual Calculation:

```
AX = 89CD - 1000 1001 1100 1101
            0111 0110 0011 0010
            7    6    3    2
```

#### Truth Table

| x | y |
|---|---|
0 | 1 |
1 | 0 |

