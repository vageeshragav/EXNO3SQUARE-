# Square and Cube of a Number Using 8051 Microcontroller

## 8051 Square Program

### AIM
To write and execute an Assembly Language Program for finding the square of a given number using the 8051 microcontroller in Keil μVision software.

### APPARATUS REQUIRED
- Personal Computer
- Keil μVision IDE
- 8051 Microcontroller

### ALGORITHM
1. Start the program.
2. Read the input number from Port 0 (P0).
3. Move the input value into registers A and B.
4. Perform multiplication using the MUL AB instruction.
5. Store the lower byte of the result in Port 2 (P2).
6. Store the higher byte of the result in Port 3 (P3).
7. Stop the program.

### PROGRAM

```asm
ORG 0000H

MOV A,P0
MOV B,A
MUL AB

MOV P2,A
MOV P3,B

HERE: SJMP HERE

END
```

### OUTPUT

Example:

Input: 05H (5)

Square = 5 × 5 = 25

P2 = 19H (Lower Byte)

P3 = 00H (Higher Byte)

### RESULT
Thus, the square of the given number is calculated successfully using the 8051 microcontroller in Keil μVision software.

---

## 8051 Cube Program

### AIM
To write and execute an Assembly Language Program for finding the cube of a given number using the 8051 microcontroller in Keil μVision software.

### APPARATUS REQUIRED
- Personal Computer
- Keil μVision IDE
- 8051 Microcontroller

### ALGORITHM
1. Start the program.
2. Read the input number from Port 0 (P0).
3. Multiply the input number by itself to obtain the square.
4. Store the square's lower byte in register R6.
5. Multiply the square by the original input number.
6. Store the lower byte of the cube in Port 2 (P2).
7. Store the higher byte of the cube in Port 3 (P3).
8. Stop the program.

### PROGRAM

```asm
ORG 0000H

MOV A,P0
MOV B,A
MUL AB

MOV R6,A

MOV A,R6
MOV B,P0
MUL AB

MOV P2,A
MOV P3,B

HERE: SJMP HERE

END
```

### OUTPUT

Example:

Input: 05H (5)

Cube = 5 × 5 × 5 = 125

P2 = 7DH (Lower Byte)

P3 = 00H (Higher Byte)
<img width="936" height="558" alt="image" src="https://github.com/user-attachments/assets/fa715771-2e28-42c0-89c7-a537b7e1e036" />

### RESULT
Thus, the cube of the given number is calculated successfully using the 8051 microcontroller in Keil μVision software.

**Note:** The square program supports 8-bit input. The cube program above is intended for input values from 0 to 15 so that the result fits in 16 bits. P2 stores the lower byte and P3 stores the higher byte of the result.
