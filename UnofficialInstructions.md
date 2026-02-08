# Instructions

##  Table

|      |  + 00  |  + 01  |  + 02  |  + 03  |  + 04  |  + 05  |  + 06  |  + 07  |
|-----:|:-------|:-------|:-------|:-------|:-------|:-------|:-------|:-------|
| 0x00 |        |        | HLT    | SLO iX | DOP zp |        |        | SLO zp |
| 0x08 |        |        |        | ANC #i | TOP ab |        |        | SLO ab |
| 0x10 |        |        | HLT    | SLO iY | DOP zX |        |        | SLO zX |
| 0x18 |        |        | NOP    | SLO aY | TOP aX |        |        | SLO aX |
| 0x20 |        |        | HLT    | RLA iX |        |        |        | RLA zp |
| 0x28 |        |        |        | ANC #i |        |        |        | RLA ab |
| 0x30 |        |        | HLT    | RLA iY |        |        |        | RLA zX |
| 0x38 |        |        | NOP    | RLA aY | TOP aX |        |        | RLA aX |
| 0x40 |        |        | HLT    | SRE iX | DOP zp |        |        | SRE zp |
| 0x48 |        |        |        | ALR #i |        |        |        | SRE ab |
| 0x50 |        |        | HLT    | SRE iY | DOP zX |        |        | SRE zX |
| 0x58 |        |        | NOP    | SRE aY | TOP aX |        |        | SRE aX |
| 0x60 |        |        | HLT    | RRA iX | DOP zp |        |        | RRA zp |
| 0x68 |        |        |        | ARR #i |        |        |        | RRA ab |
| 0x70 |        |        | HLT    | RRA iY | DOP zX |        |        | RRA zX |
| 0x78 |        |        | NOP    | RRA aY | TOP aX |        |        | RRA aX |
| 0x80 | DOP #i |        | DOP #i |        |        |        |        |        |
| 0x88 |        | DOP #i |        | ANE #i |        |        |        |        |
| 0x90 |        |        | HLT    |        |        |        |        |        |
| 0x98 |        |        |        |        |        |        |        |        |
| 0xA0 |        |        |        |        |        |        |        |        |
| 0xA8 |        |        |        | LAX #i |        |        |        |        |
| 0xB0 |        |        | HLT    |        |        |        |        |        |
| 0xB8 |        |        |        |        |        |        |        |        |
| 0xC0 |        |        | DOP #i |        |        |        |        |        |
| 0xC8 |        |        |        | SBX #i |        |        |        |        |
| 0xD0 |        |        | HLT    |        | DOP zX |        |        |        |
| 0xD8 |        |        | NOP    |        | TOP aX |        |        |        |
| 0xE0 |        |        | DOP #i |        |        |        |        |        |
| 0xE8 |        |        |        | SBC #i |        |        |        |        |
| 0xF0 |        |        | HLT    |        | DOP zX |        |        |        |
| 0xF8 |        |        | NOP    |        | TOP aX |        |        |        |


###   Instructions

|      | + 0 | + 1 | + 2 | + 3 | + 4 | + 5 | + 6 | + 7 |
|-----:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
| 0x00 |     |     | HLT | SLO | DOP |     |     | SLO |
| 0x08 |     |     |     | ANC | TOP |     |     | SLO |
| 0x10 |     |     | HLT | SLO | DOP |     |     | SLO |
| 0x18 |     |     | NOP | SLO | TOP |     |     | SLO |
| 0x20 |     |     | HLT | RLA |     |     |     | RLA |
| 0x28 |     |     |     | ANC |     |     |     | RLA |
| 0x30 |     |     | HLT | RLA | DOP |     |     | RLA |
| 0x38 |     |     | NOP | RLA | TOP |     |     | RLA |
| 0x40 |     |     | HLT | SRE | DOP |     |     | SRE |
| 0x48 |     |     |     | ALR |     |     |     | SRE |
| 0x50 |     |     | HLT | SRE | DOP |     |     | SRE |
| 0x58 |     |     | NOP | SRE | TOP |     |     | SRE |
| 0x60 |     |     | HLT | RRA | DOP |     |     | RRA |
| 0x68 |     |     |     | ARR |     |     |     | RRA |
| 0x70 |     |     | HLT | RRA | DOP |     |     | RRA |
| 0x78 |     |     | NOP | RRA | TOP |     |     | RRA |
| 0x80 | DOP |     | DOP |     |     |     |     |     |
| 0x88 |     | DOP |     | ANE |     |     |     |     |
| 0x90 |     |     | HLT |     |     |     |     |     |
| 0x98 |     |     |     |     |     |     |     |     |
| 0xA0 |     |     |     |     |     |     |     |     |
| 0xA8 |     |     |     | LAX |     |     |     |     |
| 0xB0 |     |     | HLT |     |     |     |     |     |
| 0xB8 |     |     |     |     |     |     |     |     |
| 0xC0 |     |     | DOP |     |     |     |     |     |
| 0xC8 |     |     |     | SBX |     |     |     |     |
| 0xD0 |     |     | HLT |     | DOP |     |     |     |
| 0xD8 |     |     | NOP |     | TOP |     |     |     |
| 0xE0 |     |     | DOP |     |     |     |     |     |
| 0xE8 |     |     |     | SBC |     |     |     |     |
| 0xF0 |     |     | HLT |     | DOP |     |     |     |
| 0xF8 |     |     | NOP |     | TOP |     |     |     |

###   Addressing

|      | + 0 | + 1 | + 2 | + 3 | + 4 | + 5 | + 6 | + 7 |
|-----:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
| 0x00 |     |     | kil | i,X |     |     |     | zp  |
| 0x08 |     |     |     | #im | abs |     |     | abs |
| 0x10 |     |     | kil | i,Y | z,X |     |     | z,X |
| 0x18 |     |     | imp | a,Y | a,X |     |     | a,X |
| 0x20 |     |     | kil | i,X |     |     |     | zp  |
| 0x28 |     |     |     | #im |     |     |     | abs |
| 0x30 |     |     | kil | i,Y | ??? |     |     | z,X |
| 0x38 |     |     | imp | a,Y | a,X |     |     | a,X |
| 0x40 |     |     | kil | i,X |     |     |     | zp  |
| 0x48 |     |     |     | #im |     |     |     | abs |
| 0x50 |     |     | kil | i,Y | z,X |     |     | z,X |
| 0x58 |     |     | imp | a,Y | a,X |     |     | a,X |
| 0x60 |     |     | kil | i,X |     |     |     | zp  |
| 0x68 |     |     |     | #im |     |     |     | abs |
| 0x70 |     |     | kil | i,Y | z,X |     |     | z,X |
| 0x78 |     |     | imp | a,Y | a,X |     |     | a,X |
| 0x80 | #im |     | #im |     |     |     |     |     |
| 0x88 |     | #im |     | #im |     |     |     |     |
| 0x90 |     |     | kil |     |     |     |     |     |
| 0x98 |     |     |     |     |     |     |     |     |
| 0xA0 |     |     |     |     |     |     |     |     |
| 0xA8 |     |     |     | #im |     |     |     |     |
| 0xB0 |     |     | kil |     |     |     |     |     |
| 0xB8 |     |     |     |     |     |     |     |     |
| 0xC0 |     |     | #im |     |     |     |     |     |
| 0xC8 |     |     |     | #im |     |     |     |     |
| 0xD0 |     |     | kil |     | z,X |     |     |     |
| 0xD8 |     |     | imp |     | a,X |     |     |     |
| 0xE0 |     |     | #im |     |     |     |     |     |
| 0xE8 |     |     |     | #im |     |     |     |     |
| 0xF0 |     |     | kil |     | z,X |     |     |     |
| 0xF8 |     |     | imp |     | a,X |     |     |     |

###   Number of Bytes

|      | + 0 | + 1 | + 2 | + 3 | + 4 | + 5 | + 6 | + 7 |
|-----:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
| 0x00 |     |     |   1 |   2 |   2 |     |     |   2 |
| 0x08 |     |     |     |   2 |   3 |     |     |   3 |
| 0x10 |     |     |   1 |   2 |   2 |     |     |   2 |
| 0x18 |     |     |   1 |   3 |   3 |     |     |   3 |
| 0x20 |     |     |   1 |   2 |     |     |     |   2 |
| 0x28 |     |     |     |   2 |     |     |     |   3 |
| 0x30 |     |     |   1 |   2 |   2 |     |     |   2 |
| 0x38 |     |     |   1 |   3 |   3 |     |     |   3 |
| 0x40 |     |     |   1 |   2 |   2 |     |     |   2 |
| 0x48 |     |     |     |   2 |     |     |     |   3 |
| 0x50 |     |     |   1 |   2 |   2 |     |     |   2 |
| 0x58 |     |     |   1 |   3 |   3 |     |     |   3 |
| 0x60 |     |     |   1 |   2 |   2 |     |     |   2 |
| 0x68 |     |     |     |   2 |     |     |     |   3 |
| 0x70 |     |     |   1 |   2 |   2 |     |     |   2 |
| 0x78 |     |     |   1 |   3 |   3 |     |     |   3 |
| 0x80 |   2 |     |   2 |     |     |     |     |     |
| 0x88 |     |   2 |   2 |     |     |     |     |     |
| 0x90 |     |     |   1 |     |     |     |     |     |
| 0x98 |     |     |     |     |     |     |     |     |
| 0xA0 |     |     |     |     |     |     |     |     |
| 0xA8 |     |     |   2 |     |     |     |     |     |
| 0xB0 |     |     |   1 |     |     |     |     |     |
| 0xB8 |     |     |     |     |     |     |     |     |
| 0xC0 |     |     |   2 |     |     |     |     |     |
| 0xC8 |     |     |   2 |     |     |     |     |     |
| 0xD0 |     |     |   1 |     |   2 |     |     |     |
| 0xD8 |     |     |   1 |     |   3 |     |     |     |
| 0xE0 |     |     |   2 |     |     |     |     |     |
| 0xE8 |     |     |   2 |     |     |     |     |     |
| 0xF0 |     |     |   1 |     |   2 |     |     |     |
| 0xF8 |     |     |   1 |     |   3 |     |     |     |

###   Cycles

|      | + 0 | + 1 | + 2 | + 3 | + 4 | + 5 | + 6 | + 7 |
|-----:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
| 0x00 |     |     |   ? |   8 |   3 |     |     |   5 |
| 0x08 |     |     |     |   2 |   4 |     |     |   6 |
| 0x10 |     |     |   ? |   8 |   4 |     |     |   6 |
| 0x18 |     |     |   2 |   7 |   4 |     |     |   7 |
| 0x20 |     |     |   ? |   8 |     |     |     |   5 |
| 0x28 |     |     |     |   2 |     |     |     |   6 |
| 0x30 |     |     |   ? |   8 |   4 |     |     |   6 |
| 0x38 |     |     |   2 |   7 |   4 |     |     |   7 |
| 0x40 |     |     |   ? |   8 |   3 |     |     |   5 |
| 0x48 |     |     |     |   2 |     |     |     |   6 |
| 0x50 |     |     |   ? |   8 |   4 |     |     |   6 |
| 0x58 |     |     |   2 |   7 |   4 |     |     |   7 |
| 0x60 |     |     |   ? |   8 |   3 |     |     |   5 |
| 0x68 |     |     |     |   2 |     |     |     |   6 |
| 0x70 |     |     |   ? |   8 |   4 |     |     |   6 |
| 0x78 |     |     |   2 |   7 |   4 |     |     |   7 |
| 0x80 |   2 |     |   2 |     |     |     |     |     |
| 0x88 |     |   2 |   2 |     |     |     |     |     |
| 0x90 |     |     |   ? |     |     |     |     |     |
| 0x98 |     |     |     |     |     |     |     |     |
| 0xA0 |     |     |     |     |     |     |     |     |
| 0xA8 |     |     |   2 |     |     |     |     |     |
| 0xB0 |     |     |   ? |     |     |     |     |     |
| 0xB8 |     |     |     |     |     |     |     |     |
| 0xC0 |     |     |   2 |     |     |     |     |     |
| 0xC8 |     |     |   2 |     |     |     |     |     |
| 0xD0 |     |     |   ? |     |   4 |     |     |     |
| 0xD8 |     |     |   2 |     |   4 |     |     |     |
| 0xE0 |     |     |   2 |     |     |     |     |     |
| 0xE8 |     |     |   2 |     |     |     |     |     |
| 0xF0 |     |     |   ? |     |   4 |     |     |     |
| 0xF8 |     |     |   2 |     |   4 |     |     |     |


##  Details

###   HLT (JAM, KIL)

- CPU が停止する

|  Addressing  | OPE | Bytes | Cycles |
|:------------:|:---:|------:|:-------|
|              | $02 |     1 | ?      |
|              | $22 |     1 | ?      |
|              | $42 |     1 | ?      |
|              | $62 |     1 | ?      |
|              | $12 |     1 | ?      |
|              | $32 |     1 | ?      |
|              | $52 |     1 | ?      |
|              | $72 |     1 | ?      |
|              | $92 |     1 | ?      |
|              | $B2 |     1 | ?      |
|              | $D2 |     1 | ?      |
|              | $F2 |     1 | ?      |


###   NOP (DOP, TOP)

- 何もしないことを実行する

| MNE |  Addressing  | OPE | Bytes | Cycles |
|:---:|:------------:|:---:|------:|:-------|
| DOP | ZeroPage     | $04 |     2 | 3      |
| TOP | Absolute     | $0C |     3 | 4      |
| DOP | ZeroPage, X  | $14 |     2 | 4      |
| NOP | Implied      | $1A |     1 | 2      |
| TOP | Absolute, X  | $1C |     3 | 4      |
| DOP | ZeroPage, X? | $34 |     2 | 4      |
| NOP | Implied      | $3A |     1 | 2      |
| TOP | Absolute, X  | $3C |     3 | 4      |
| DOP | ZeroPage     | $44 |     2 | 3      |
| DOP | ZeroPage, X  | $54 |     2 | 4      |
| NOP | Implied      | $5A |     1 | 2      |
| TOP | Absolute, X  | $5C |     3 | 4      |
| DOP | ZeroPage     | $64 |     2 | 3      |
| DOP | ZeroPage, X  | $74 |     2 | 4      |
| NOP | Implied      | $7A |     1 | 2      |
| TOP | Absolute, X  | $7C |     3 | 4      |
| DOP | #Immediate   | $80 |     2 | 2      |
| DOP | #Immediate   | $82 |     2 | 2      |
| DOP | #Immediate   | $89 |     2 | 2      |
| DOP | #Immediate   | $C2 |     2 | 2      |
| DOP | ZeroPage, X  | $D4 |     2 | 4      |
| NOP | Implied      | $DA |     1 | 2      |
| TOP | Absolute, X  | $DC |     3 | 4      |
| DOP | #Immediate   | $E2 |     2 | 2      |
| DOP | ZeroPage, X  | $F4 |     2 | 4      |
| NOP | Implied      | $FA |     1 | 2      |
| TOP | Absolute, X  | $FC |     3 | 4      |


###   ALR (ASR)

- AND + LSR
- ALR #{imm} := AND #{imm} + LSR

|  Addressing  | OPE | Bytes | Cycles |
|:------------:|:---:|------:|:-------|
| #Immediate   | $4B |     2 | 2      |


###   ANC

- AND + ASL
- ANC #{imm} := AND #{imm} + ASL

|  Addressing  | OPE | Bytes | Cycles |
|:------------:|:---:|------:|:-------|
| #Immediate   | $0B |     2 | 2      |
| #Immediate   | $2B |     2 | 2      |


###   ANE

- A |= 0xEE, A &= X; A &= #{imm}

|  Addressing  | OPE | Bytes | Cycles |
|:------------:|:---:|------:|:-------|
| #Immediate   | $8B |     2 | 2      |


###   ARR

- AND + ROR
- ARR #{imm} := AND #{imm} + ROR

|  Addressing  | OPE | Bytes | Cycles |
|:------------:|:---:|------:|:-------|
| #Immediate   | $6B |     2 | 2      |


###   AXS (SBX)

- X = A & X - #{imm}

|  Addressing  | OPE | Bytes | Cycles |
|:------------:|:---:|------:|:-------|
| #Immediate   | $CB |     2 | 2      |


###   LAX

- A = X = ((A | 0xEE) & #{imm})
- A |= 0xFF; A &= ${imm}; X = A;

|  Addressing  | OPE | Bytes | Cycles |
|:------------:|:---:|------:|:-------|
| #Immediate   | $AB |     2 | 2      |


###   RLA

- ROL + AND
- RLA {adr} := ROL {adr} + AND {adr}

|  Addressing  | OPE | Bytes | Cycles |
|:------------:|:---:|------:|:-------|
| #Immediate   | N/A |  N/A  |        |
| ZeroPage     | $27 |     2 | 5      |
| ZeroPage, X  | $37 |     2 | 6      |
| Absolute     | $2F |     3 | 6      |
| Absolute, X  | $3F |     3 | 7      |
| Absolute, Y  | $3B |     3 | 7      |
| (Indirect,X) | $23 |     2 | 8      |
| (Indirect),Y | $33 |     2 | 8      |


###   RRA

- ROR + ADC
- RRA {adr} := ROR + ADC {adr}

|  Addressing  | OPE | Bytes | Cycles |
|:------------:|:---:|------:|:-------|
| #Immediate   | N/A |  N/A  |        |
| ZeroPage     | $67 |     2 | 5      |
| ZeroPage, X  | $77 |     2 | 6      |
| Absolute     | $6F |     3 | 6      |
| Absolute, X  | $7F |     3 | 7      |
| Absolute, Y  | $7B |     3 | 7      |
| (Indirect,X) | $63 |     2 | 8      |
| (Indirect),Y | $73 |     2 | 8      |


###   SBC

|  Addressing  | OPE | Bytes | Cycles |
|:------------:|:---:|------:|:-------|
| #Immediate   | $EB |     2 | 2      |


###   SHA(AHX), SHS (TAS,XAS), SHX, SHY

- SHA {adr} : {adr} <- A & X & H (AHX)
- SHS {adr} : S <- A & X, {adr} <- S & H (TAS, XAS)
- SHX {adr} : {adr} <- X & H
- SHY {adr} : {adr} <- Y & H

| MNE |  Addressing  | OPE | Bytes | Cycles |
|:---:|:------------:|:---:|------:|:-------|
| SHY | Absolute, X  | $9C |     3 | 5      |
| SHS | Absolute, Y  | $9B |     3 | 5      |
| SHX | Absolute, Y  | $9E |     3 | 5      |
| SHA | Absolute, Y  | $9F |     3 | 5      |


###   SLO

- ASL + ORA
- SLO {adr} := ASL + ORA {adr}

|  Addressing  | OPE | Bytes | Cycles |
|:------------:|:---:|------:|:-------|
| #Immediate   | N/A |  N/A  |        |
| ZeroPage     | $07 |     2 | 5      |
| ZeroPage, X  | $17 |     2 | 6      |
| Absolute     | $0F |     3 | 6      |
| Absolute, X  | $1F |     3 | 7      |
| Absolute, Y  | $1B |     3 | 7      |
| (Indirect,X) | $03 |     2 | 8      |
| (Indirect),Y | $13 |     2 | 8      |


###   SRE

- LSR + EOR
- SRE {adr} := LSR + EOR {adr}

|  Addressing  | OPE | Bytes | Cycles |
|:------------:|:---:|------:|:-------|
| #Immediate   | N/A |  N/A  |        |
| ZeroPage     | $47 |     2 | 5      |
| ZeroPage, X  | $57 |     2 | 6      |
| Absolute     | $4F |     3 | 6      |
| Absolute, X  | $5F |     3 | 7      |
| Absolute, Y  | $5B |     3 | 7      |
| (Indirect,X) | $43 |     2 | 8      |
| (Indirect),Y | $53 |     2 | 8      |
