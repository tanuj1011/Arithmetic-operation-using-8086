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
ASSUME CS: CODE, DS: CODE
ORG 1000H
MOV SI,2000H
MOV CL,00H
MOV AX,[SI]
MOV BX,[SI+02H]
ADD AX,BX
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

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| 1200:12----------------------- | 1200:24------------------------ |
| 1201:34                      |   1205:68
  1202:12                          1206:00
  1203:34
#### Manual Calculations
![WhatsApp Image 2025-08-20 at 20 11 48_e5662f0c](https://github.com/user-attachments/assets/344b17c0-843c-42f9-bf89-9f5c3ef8bd96)

Add your calculation here)

---

## OUTPUT IMAGE FROM MASM SOFTWARE
<img width="640" height="480" alt="Screenshot (48)" src="https://github.com/user-attachments/assets/1b2522c8-ebae-4a93-bca1-521853d20203" />
<img width="640" height="480" alt="Screenshot (42)" src="https://github.com/user-attachments/assets/c1a8c59b-7ffc-4a51-abaf-c1d14fb23765" />



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
code segment
assume cs:code,ds:code
org 1000h
mov si,1200h
mov ax,[si]
mov bx,[si+02h]
mov cl,00h
sub ax,bx
jnc l1
inc cl
l1:mov[si+04h],ax
mov [si+06h],cl
mov ah,4ch
int 21h
code ends
end 

#### Output Table

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| 1200:12----------------------- | 1200:00------------------------ |
| 1201:34                      |   1205:00
  1202:12                          1206:00
  1203:34----------------------- | ------------------------ |


#### Manual Calculations
![WhatsApp Image 2025-08-20 at 20 12 18_0892d1d7](https://github.com/user-attachments/assets/58cc6f96-9f32-4db8-9295-9c46c9a550e9)

(Add your calculation here)

---


## OUTPUT SCREEN FROM MASM SOFTWARE
<img width="640" height="480" alt="Screenshot (49)" src="https://github.com/user-attachments/assets/8d231732-649f-4d73-8de4-b76c20de10eb" />
<img width="640" height="480" alt="Screenshot (44)" src="https://github.com/user-attachments/assets/0bbc94df-473f-47c2-bd0e-cacc50c29437" />



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

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
|  1200:12----------------------- | 1200:44----------------------- |
| 1201:34                      |   1205:51
  1202:12                          1206:97
  1203:34--------------------------1207:0A------------ | ------------------------ |

#### Manual Calculations

(![WhatsApp Image 2025-08-20 at 20 14 56_d883a811](https://github.com/user-attachments/assets/29b95e32-8bb6-4653-9d08-fa31dc3349c8)
Add your calculation here)

---

## OUTPUT SCREEN FROM MASM SOFTWARE
<img width="640" height="480" alt="Screenshot (53)" src="https://github.com/user-attachments/assets/15ffdf2d-2eb4-4235-a64e-da0b0fe3f6ba" />
<img width="640" height="480" alt="Screenshot (45)" src="https://github.com/user-attachments/assets/c9b73afc-ccab-49fb-977a-a66c5cbacf8c" />



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

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| 1200:12----------------------- | 1200:01----------------------- |
| 1201:34                      |   1205:00
  1202:12                          1206:00
  1203:34--------------------------1207:00--------------------------- | ------------------------ |

#### Manual Calculations
![WhatsApp Image 2025-08-20 at 20 14 57_76767a2f](https://github.com/user-attachments/assets/03d02df4-3270-4ae2-89d2-cb86bc1c52e3)

(Add your calculation here)

---
## OUTPUT FROM MASM SOFTWARE
<img width="640" height="480" alt="Screenshot (54)" src="https://github.com/user-attachments/assets/42ad1612-7a1e-43d2-bec3-7a1959e9f9a3" />
<img width="640" height="480" alt="Screenshot (47)" src="https://github.com/user-attachments/assets/1430f87c-f2fc-41f7-b785-ab613f19ed1a" />





## RESULT

Thus, the Assembly Language Programs for 8086 to perform arithmetic operations (Addition, Subtraction, Multiplication, and Division) using both direct and indirect methods were successfully written and executed using MASM.
