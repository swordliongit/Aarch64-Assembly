
```arm-asm
// Comment
/*
Multi-line comment
*/

.data
var: .byte 0

.text
.global main
main:
	mov x0, #0
	ret

```

#### DIRECTIVES
```arm-asm
.data
```
**Notes:**
Directives define what type of data will follow, .data directive is for defining variables

```arm-asm
.global main
```
**Notes:**
.global directive indicates that the main label can be accessed from anywhere and also outside of this file too.

#### INSTRUCTION FORMAT
```csv
Label | Opcode | Operand | Comments

main:   mov      x0, #0
		ret
```