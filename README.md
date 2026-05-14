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
### output table

<img width="1600" height="1083" alt="WhatsApp Image 2026-05-14 at 11 03 33 AM" src="https://github.com/user-attachments/assets/20684bdc-40c1-450f-adf6-16a0d80a458f" />


#### Manual Calculations
<img width="1600" height="1161" alt="WhatsApp Image 2026-05-14 at 11 03 32 AM" src="https://github.com/user-attachments/assets/cafcfa7b-1b1d-4cbc-80c0-f63f9fa56ce0" />



## OUTPUT IMAGE FROM MASM SOFTWARE
<img width="1600" height="1240" alt="WhatsApp Image 2026-05-14 at 11 06 30 AM (1)" src="https://github.com/user-attachments/assets/7e890dd0-99c0-49eb-8007-5232819bbab2" />



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

<img width="1600" height="1200" alt="WhatsApp Image 2026-05-14 at 11 07 31 AM" src="https://github.com/user-attachments/assets/b8b0b572-1cfa-41d6-9b05-09034d69ab67" />


#### Manual Calculations
<img width="1600" height="1200" alt="WhatsApp Image 2026-05-14 at 11 07 31 AM (1)" src="https://github.com/user-attachments/assets/ab5d4fea-14dd-4150-b4e6-53f3e340062b" />






## OUTPUT SCREEN FROM MASM SOFTWARE
<img width="1600" height="1075" alt="WhatsApp Image 2026-05-14 at 11 06 30 AM" src="https://github.com/user-attachments/assets/80e331cc-a9d4-416c-a1b6-1fda2d0634d7" />



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

<img width="1599" height="899" alt="WhatsApp Image 2026-05-14 at 11 09 31 AM" src="https://github.com/user-attachments/assets/8b50e97a-2e47-4741-976b-dc37bfa6b664" />

#### Manual Calculations
<img width="1599" height="899" alt="WhatsApp Image 2026-05-14 at 11 13 55 AM" src="https://github.com/user-attachments/assets/24185152-3f4d-4953-8700-540f5d82ade3" />


## OUTPUT SCREEN FROM MASM SOFTWARE
<img width="1600" height="1074" alt="WhatsApp Image 2026-05-14 at 11 06 30 AM (2)" src="https://github.com/user-attachments/assets/d8258e57-3d79-4625-98b2-3622340efe93" />



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
<img width="1599" height="899" alt="WhatsApp Image 2026-05-14 at 11 09 43 AM" src="https://github.com/user-attachments/assets/2e0e4c60-ae97-47f3-9ae1-fc55bd6ccc7e" />


#### Manual Calculations

<img width="1599" height="899" alt="WhatsApp Image 2026-05-14 at 11 10 16 AM" src="https://github.com/user-attachments/assets/25749c33-50e3-4071-b9f6-3d27c598add2" />

## OUTPUT FROM MASM SOFTWARE

<img width="1600" height="1099" alt="WhatsApp Image 2026-05-14 at 11 06 31 AM" src="https://github.com/user-attachments/assets/5ce2e05e-d72b-4f12-90df-623368736013" />




## RESULT

Thus, the Assembly Language Programs for 8086 to perform arithmetic operations (Addition, Subtraction, Multiplication, and Division) using both direct and indirect methods were successfully written and executed using MASM.

