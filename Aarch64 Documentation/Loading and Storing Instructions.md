**Notes:**
Loading means; storing data into a register from the memory


## Load Register Instruction

```arm-asm
.data
value: .quad 0x1234567890abcdef

.text
.global main
main:
	ldr x0, =value
	ldr x1, [x0]
	mov x0, #0
	ret
```

```arm-asm
ldr x0, =value
```
**Notes:**
Address of the 'value' variable is loaded into the 'x0' register. x0 now points to this variable.

```arm-asm
ldr x1, [x0]
```
**Notes:**
Data at the address in x0 is loaded into x1 register.

---

### Loading Different Sized Values

#### Loading byte(8 bits) sized value:
```arm-asm
ldrb w1, [x0]
```
**Notes:**
w1 register is used here instead of x1 because ldrb loads only 8 bit value from the memory. It loads the value to the lower part of the x1 register, which is the w1 register.

#### Loading half word(16 bits) sized value:
```arm-asm
ldrh w2, [x0]
```

#### Loading word(32 bit) sized value:
```arm-asm
ldr w3, [x0]
```

---

### Loading Signed Values
```arm-asm
ldrsb w4, [x0] // byte
ldrsh w5, [x0] // half word
ldrsw x6, [x0] // word
```
**Notes:**
==x== register is used for ==ldrsw== instruction because word is 32 bit and signed bit will be held after the 32 bit, hence passing to the 64 bit territory, meaning the upper half of the register.

---


## Store Register Instruction
**Notes:**
Storing means; storing data from a register into a memory location(e.g another register)
```arm-asm
str x0, [x1]
strb w0, [x2] // store a byte
strh w0, [x3] // store a half word
str w0, [x4] // store a word
```