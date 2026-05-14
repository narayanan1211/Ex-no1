# Arithmetic-operation-using-8086
# 8086 Assembly Language Programs for Arithmetic Operations

## AIM

To write and execute Assembly Language Programs to perform arithmetic operations for the 8086 microprocessor.

---

## APPARATUS REQUIRED

* Personal Computer with MASM Software

---

## 1. ADDITION

#### Algorithm

1. Initialize memory location in HL register.
2. Store 1st data.
3. Increment HL to enter 2nd data.
4. Move 2nd number to accumulator.
5. Decrement HL.
6. Add value in memory with accumulator.
7. Store result.
8. Stop.


## FLOW CHART
<img width="707" height="1024" alt="image" src="https://github.com/user-attachments/assets/b5a7062d-e294-47cd-9683-a40de25e82de" />


#### Program

```asm
CODE SEGMENT
ASSUME CS:CODE, DS:CODE
ORG 1000H
MOV CL,00H
MOV AX,1234H
MOV BX,1234H
ADD AX,BX
JNC L1
INC CL
L1:MOV SI,1200H
MOV [SI],AX
MOV [SI+2],CL
MOV AH,4CH
INT 21H
CODE ENDS
END
```

#### Output Table
<img width="1599" height="1013" alt="WhatsApp Image 2026-05-14 at 11 29 05 AM" src="https://github.com/user-attachments/assets/28148b84-7922-4b76-89b1-2e0fca69665e" />


#### Manual Calculations

<img width="1490" height="1440" alt="WhatsApp Image 2026-05-14 at 11 29 15 AM" src="https://github.com/user-attachments/assets/65d09c53-bc40-4b96-9f0b-b43352c3fe6e" />


## OUTPUT IMAGE FROM MASM SOFTWARE
<img width="1600" height="1240" alt="WhatsApp Image 2026-05-14 at 11 06 30 AM (1)" src="https://github.com/user-attachments/assets/4be03b79-fa29-46e5-a457-1d4c200c0d90" />


## 2. SUBTRACTION

#### Algorithm

1. Initialize memory and store 1st data.
2. Increment to get 2nd data.
3. Move 2nd data to accumulator.
4. Subtract memory content.
5. Store result.

## FLOWCHART

<img width="578" height="797" alt="image" src="https://github.com/user-attachments/assets/564c3c7a-33ce-4a1c-8920-beb5c24b9b47" />


#### Program
```asm
CODE SEGMENT
ASSUME CS: CODE, DS: CODE
ORG 1000H
MOV SI,2000H
MOV CL,00H
MOV AX,[SI]
MOV BX,[SI+02H]
SUB AX,BX
JNC L1
INC CL
L1:
MOV [SI+04H],AX
MOV [SI+06H],CL
MOV AH,4CH
INT 21H
CODE ENDS
END
```


#### Output Table
<img width="1599" height="1013" alt="WhatsApp Image 2026-05-14 at 11 29 05 AM" src="https://github.com/user-attachments/assets/25df8db4-fb8c-4582-add7-cacb155a5412" />



#### Manual Calculations

<img width="1490" height="1440" alt="WhatsApp Image 2026-05-14 at 11 29 15 AM" src="https://github.com/user-attachments/assets/8f5b0d7e-eccf-4e4a-bb03-7831fd45bb49" />



## OUTPUT SCREEN FROM MASM SOFTWARE
<img width="1600" height="1075" alt="WhatsApp Image 2026-05-14 at 11 06 30 AM" src="https://github.com/user-attachments/assets/3abc2737-b47a-4865-a06e-e285c6ce075b" />


## 3. MULTIPLICATION

#### Algorithm

1. Initialize memory and store operands.
2. Move operands to registers.
3. Multiply.
4. Store result.

##FLOWCHART

<img width="569" height="906" alt="image" src="https://github.com/user-attachments/assets/88be88ff-2896-4a88-b73d-84ccffd2fcf9" />



#### Program

```asm
CODE SEGMENT
ASSUME CS: CODE, DS: CODE
ORG 1000H
MOV SI,2000H
MOV DX,0000H
MOV AX,[SI]
MOV BX,[SI+02H]
MUL BX
MOV [SI+04H],AX
MOV [SI+06H],DX
MOV AH,4CH
INT 21H
CODE ENDS
END
```

#### Output Table
<img width="1600" height="1008" alt="WhatsApp Image 2026-05-14 at 11 29 42 AM" src="https://github.com/user-attachments/assets/8791c851-8c5e-4536-b8f8-305e5bfa9bd6" />


#### Manual Calculations

<img width="1600" height="1236" alt="WhatsApp Image 2026-05-14 at 11 29 57 AM" src="https://github.com/user-attachments/assets/89acf519-4474-4bbd-9ec3-b4eb5a29c38c" />


## OUTPUT SCREEN FROM MASM SOFTWARE
<img width="1600" height="1074" alt="WhatsApp Image 2026-05-14 at 11 06 30 AM (2)" src="https://github.com/user-attachments/assets/e8cfaa43-3246-4a6c-b256-5159e75870e2" />


## 4. DIVISION

#### Algorithm

1. Load memory location of operands.
2. Perform division.
3. Store result.

   ## FLOWCHART
<img width="1065" height="802" alt="image" src="https://github.com/user-attachments/assets/25b4a483-0d42-494b-8639-1af3ea17191b" />


#### Program

```asm
CODE SEGMENT
ASSUME CS: CODE, DS: CODE
ORG 1000H
MOV SI,2000H
MOV DX,0000H
MOV AX,[SI]
MOV BX,[SI+02H]
DIV BX
MOV [SI+04H],AX
MOV [SI+06H],DX
MOV AH,4CH
INT 21H
CODE ENDS
END
```

#### Output Table
<img width="1600" height="973" alt="WhatsApp Image 2026-05-14 at 11 30 37 AM" src="https://github.com/user-attachments/assets/71194e23-0abb-4a4d-9f51-b0fd2ec816f8" />


#### Manual Calculations
<img width="1600" height="426" alt="WhatsApp Image 2026-05-14 at 11 31 07 AM" src="https://github.com/user-attachments/assets/0e874e30-74d9-4a90-8d8b-2d037e0a9fe4" />


## OUTPUT FROM MASM SOFTWARE
<img width="1600" height="1099" alt="WhatsApp Image 2026-05-14 at 11 06 31 AM" src="https://github.com/user-attachments/assets/8ce1804a-a58b-41ee-b926-76f12cf6965d" />




## RESULT

Thus, the Assembly Language Programs for 8086 to perform arithmetic operations (Addition, Subtraction, Multiplication, and Division) using both direct and indirect methods were successfully written and executed using MASM.

