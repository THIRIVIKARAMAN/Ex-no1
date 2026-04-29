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

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|         1204            |          24              |
|         1205            |          68              |
|         1206            |          00              |
#### Manual Calculations
<img width="1600" height="1200" alt="image" src="https://github.com/user-attachments/assets/526307d9-155f-4a3c-92b0-77212d967860" />


---

## OUTPUT IMAGE FROM MASM SOFTWARE
<img width="753" height="467" alt="image" src="https://github.com/user-attachments/assets/26220551-9737-4bfb-9a4d-053c50be27d5" />


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
|         1204            |          00              |
|         1205            |          00              |


#### Manual Calculations
<img width="1600" height="1200" alt="image" src="https://github.com/user-attachments/assets/bfd18a83-0481-4326-b100-22b7e8511751" />

---


## OUTPUT SCREEN FROM MASM SOFTWARE
<img width="753" height="462" alt="image" src="https://github.com/user-attachments/assets/70fba460-a0c5-4c55-8576-27a1d3df2b09" />


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
|         1204            |          44              |
|         1205            |          51              |
|         1206            |          97              |
|         1207            |          0A              |

#### Manual Calculations
<img width="1200" height="1600" alt="image" src="https://github.com/user-attachments/assets/ae0781a2-5a8b-4c4a-aab3-175ad7031863" />

---

## OUTPUT SCREEN FROM MASM SOFTWARE
<img width="753" height="474" alt="image" src="https://github.com/user-attachments/assets/d1856e92-86ce-4ee3-9415-6ea4acdc8340" />


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
|         1204            |          01              |
|         1205            |          00              |
|         1206            |          00              |
|         1207            |          00              |

#### Manual Calculations
<img width="1600" height="1200" alt="image" src="https://github.com/user-attachments/assets/d8416817-b265-4c3a-8000-bf773467d55b" />

---
## OUTPUT FROM MASM SOFTWARE
<img width="753" height="501" alt="image" src="https://github.com/user-attachments/assets/9ee67af1-bf94-4ee4-aeda-ed3207a387c0" />


## RESULT

Thus, the Assembly Language Programs for 8086 to perform arithmetic operations (Addition, Subtraction, Multiplication, and Division) using both direct and indirect methods were successfully written and executed using MASM.

