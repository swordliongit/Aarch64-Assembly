**Notes:**
Shifting left multiplies the value by 2, shifting right divides by 2

## Logical Shift

**Format:**
```arm-asm
lsl destination, value to be shifted, shift amount
lsr `` ``
```


```arm-asm
mov x1, #4 // copy 4 into x1
lsl x2, x0, x1
```
**Notes:**
x0 is shifted by amount of x1( in this case, shift all the bits 4 times) and stored in the x2 register

0x11011011 << 4:

result:
1101 1011 0000

## Arithmetic Shift
**Notes:**
When shifting to right, previous bits are replaced by the sign bit

**Format:**
```arm-asm
asr destination, value to be shifted, shift amount
```

```arm-asm
1001 0110
1001 0110 >> 1: 1100 1011
1100 1011 >> 1: 1110 0101

0110 1001
0110 1001 >> 1: 0011 0100
```