# 16bit Logical XNOR

| Address | Mnemonics |
|---------|-----------|
| 0400 | MOV AX,45EF|
| 0403 | MOV BX,23B5|
| 0406|XOR AX,BX|
|0408|NOT AX|
|040D|MOV [1200],AX|
040E |HLT


#### OUTPUT:
| ADDRESS|DATA|
|---------|-----------|
1200 | A4
1201|99

#### Manual Calculation:

```
AX = 45EF - 0100 0101 1110 1111
BX = 23B5 - 0010 0011 1011 0100
            1001 1001 1010 0100
            9    9    A    4
```

#### Truth Table

| x | y | xy |
|---|---|----|
0 | 0 | 1
0 | 1 | 0
1 | 0 | 0
1 | 1 | 1