
### Defining Constants

```arm-asm
.equ buffer, 500
```
**Notes:**
1. buffer is a symbolic name for the value 500.
2. buffer can be changed to some other value.

### Hard Constants

```arm-asm
.equiv buffer, 2000
```
**Notes:**
buffer can't be changed to other value, compiler will throw error.