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
| ----------------------- | ------------------------ |
| 1200:12                 |1204:24                   |
| 1201:34                 |1205:68                   |
| 1202:12                 |1206:00                   |
| 1203:34                 |1207:C4                   |
#### Manual Calculations

(Add your calculation here)
![WhatsApp Image 2025-08-28 at 10 03 10_ce71bf9e](https://github.com/user-attachments/assets/d0342f80-493e-4ae6-9ecc-a4fb4e6e73a2)

---

## OUTPUT IMAGE FROM MASM SOFTWARE
<img width="636" height="428" alt="Screenshot 2025-08-21 120000" src="https://github.com/user-attachments/assets/90809216-1896-454b-9014-a0db16ef4433" />

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

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
| 1200:12                 |1204:00                   |
| 1201:34                 |1205:00                   |
| 1202:12                 |1206:00                   |
| 1203:34                 |1207:C4                   |
#### Manual Calculations

(Add your calculation here)

![WhatsApp Image 2025-08-28 at 10 06 34_b51b488a](https://github.com/user-attachments/assets/9cc9b2cf-32c4-4f50-bff7-130f0c950f45)

---


## OUTPUT SCREEN FROM MASM SOFTWARE
<img width="642" height="433" alt="Screenshot 2025-08-24 123315" src="https://github.com/user-attachments/assets/036ed336-0c2e-415f-b6ba-430f77349c34" />

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
| ----------------------- | ------------------------ |
| 1200:12                 |1204:44                   |
| 1201:34                 |1205:51                   |
| 1202:12                 |1206:97                   |
| 1203:34                 |1207:0A                   |


#### Manual Calculations

Add your calculation here)
![WhatsApp Image 2025-08-28 at 11 12 17_38f4e5b8](https://github.com/user-attachments/assets/cfb14122-5ff7-4a03-a4e7-28dae73b6e1c)
---

## OUTPUT SCREEN FROM MASM SOFTWARE
<img width="642" height="433" alt="Screenshot 2025-08-27 221001" src="https://github.com/user-attachments/assets/5dbee6c4-92ee-4b6d-a57f-ccab2f4c77e1" />

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
| ----------------------- | ------------------------ |
| 1200:12                 |1204:01                   |
| 1201:34                 |1205:00                   |
| 1202:12                 |1206:00                   |
| 1203:34                 |1207:00                   |
                       

#### Manual Calculations

(Add your calculation here)
![WhatsApp Image 2025-08-28 at 11 20 55_d846abb1](https://github.com/user-attachments/assets/28cfccf2-64aa-42de-ab44-a98316c0aead)
---
## OUTPUT FROM MASM SOFTWARE
<img width="642" height="433" alt="Screenshot 2025-08-27 223504" src="https://github.com/user-attachments/assets/a9067ff9-dc64-4d60-bd5f-e2371a1c1b0a" />

## RESULT

Thus, the Assembly Language Programs for 8086 to perform arithmetic operations (Addition, Subtraction, Multiplication, and Division) using both direct and indirect methods were successfully written and executed using MASM.
