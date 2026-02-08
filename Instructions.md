# Instructions

##  Table

|      |  + 00  |  + 01  |  + 02  |  + 03  |  + 04  |  + 05  |  + 06  |  + 07  |
|-----:|:-------|:-------|:-------|:-------|:-------|:-------|:-------|:-------|
| 0x00 | BRK #  | ORA iX | hlt    | slo iX | dop zp | ORA zp | ASL zp | slo zp |
| 0x08 | PHP    | ORA #  | ASL A  | anc #  | top ab | ORA ab | ASL ab | slo ab |
| 0x10 | BPL r  | ORA iY | hlt    | slo iY | dop zX | ORA zX | ASL zX | slo zX |
| 0x18 | CLC    | ORA aY | nop    | slo aY | top aX | ORA aX | ASL aX | slo aX |
| 0x20 | JSR ab | AND iX | hlt    | rla iX | BIT zp | AND zp | ROL zp | rla zp |
| 0x28 | PLP    | AND #  | ROL A  | anc #  | BIT ab | AND ab | ROL ab | rla ab |
| 0x30 | BMI r  | AND iY | hlt    | rla iY | dop zX | AND zX | ROL zX | rla zX |
| 0x38 | SEC    | AND aY | nop    | rla aY | top aX | AND aX | ROL aX | rla aX |
| 0x40 | RTI    | EOR iX | hlt    | sre iX | dop zp | EOR zp | LSR zp | sre zp |
| 0x48 | PHA    | EOR #  | LSR A  | alr #  | JMP ab | EOR ab | LSR ab | sre ab |
| 0x50 | BVC r  | EOR iY | hlt    | str iY | dop zX | EOR zX | LSR zX | sre zX |
| 0x58 | CLI    | EOR aY | nop    | sre aY | top aX | EOR aX | LSR aX | sre aX |
| 0x60 | RTS    | ADC iX | hlt    | rra iX | dop zp | ADC zp | ROR zp | rra zp |
| 0x68 | PLA    | ADC #  | ROR A  | arr #  | JMP id | ADC ab | ROR ab | rra ab |
| 0x70 | BVS r  | ADC iY | hlt    | rra iY | dop zX | ADC zX | ROR zX | rra zX |
| 0x78 | SED    | ADC aY | nop    | rra aY | top aX | ADC aX | ROR aX | rra aX |
| 0x80 | dop #  | STA iX | dop #  | sax iX | STY zp | STA zp | STX zp | sax zp |
| 0x88 | DEY    | dop #  | TXA    | ane #  | STY ab | STA ab | STX ab | sax ab |
| 0x90 | BCC r  | STA iY | hlt    | sha iY | STY zX | STA zX | STX zY | sax zY |
| 0x98 | TYA    | STA aY | TXS    | shs aY | shy aX | STA aX | shx aY | sha aY |
| 0xA0 | LDY #  | LDA iX | LDX #  | lax iX | LDY zp | LDA zp | LDX zp | lax zp |
| 0xA8 | TAY    | LDA #  | TAX    | lax #  | LDY ab | LDA ab | LDX ab | lax ab |
| 0xB0 | BCS r  | LDA iY | hlt    | lax iY | LDY zX | LDA zX | LDX zY | lax zY |
| 0xB8 | CLV    | LDA aY | TSX    | las aY | LDY aX | LDA aX | LDX aY | lax aY |
| 0xC0 | CPY #  | CMP iX | dop #  |        | CPY zp | CMP zp | DEC zp |        |
| 0xC8 | INY    | CMP #  | DEX    | sbx #  | CPY ab | CMP ab | DEC ab |        |
| 0xD0 | BNE r  | CMP iY | hlt    |        | dop zX | CMP zX | DEC zX |        |
| 0xD8 | CLD    | CMP aY | nop    |        | top aX | CMP aX | DEC aX |        |
| 0xE0 | CPX #  | SBC iX | dop #  |        | CPX zp | SBC zp | INC zp |        |
| 0xE8 | INX    | SBC #  | NOP    | sbc #  | CPX ab | SBC ab | INC ab |        |
| 0xF0 | BEQ r  | SBC iY | hlt    |        | dop zX | SBC zX | INC zX |        |
| 0xF8 | SED    | SBC aY | nop    |        | top aX | SBC aX | INC aX |        |

###   Instructions

|      | + 0 | + 1 | + 2 | + 3 | + 4 | + 5 | + 6 | + 7 |
|-----:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
| 0x00 | BRK | ORA | hlt | slo | dop | ORA | ASL | slo |
| 0x08 | PHP | ORA | ASL | anc | top | ORA | ASL | slo |
| 0x10 | BPL | ORA | hlt | slo | dop | ORA | ASL | slo |
| 0x18 | CLC | ORA | nop | slo | top | ORA | ASL | slo |
| 0x20 | JSR | AND | hlt | rla | BIT | AND | ROL | rla |
| 0x28 | PLP | AND | ROL | anc | BIT | AND | ROL | rla |
| 0x30 | BMI | AND | hlt | rla | dop | AND | ROL | rla |
| 0x38 | SEC | AND | nop | rla | top | AND | ROL | rla |
| 0x40 | RTI | EOR | hlt | sre | dop | EOR | LSR | sre |
| 0x48 | PHA | EOR | LSR | alr | JMP | EOR | LSR | sre |
| 0x50 | BVC | EOR | hlt | sre | dop | EOR | LSR | sre |
| 0x58 | CLI | EOR | nop | sre | top | EOR | LSR | sre |
| 0x60 | RTS | ADC | hlt | rra | dop | ADC | ROR | rra |
| 0x68 | PLA | ADC | ROR | arr | JMP | ADC | ROR | rra |
| 0x70 | BVS | ADC | hlt | rra | dop | ADC | ROR | rra |
| 0x78 | SEI | ADC | nop | rra | top | ADC | ROR | rra |
| 0x80 | dop | STA | dop | sax | STY | STA | STX | sax |
| 0x88 | DEY | dop | TXA | ane | STY | STA | STX | sax |
| 0x90 | BCC | STA | hlt | sha | STY | STA | STX | sax |
| 0x98 | TYA | STA | TXS | shs | shy | STA | shx | sha |
| 0xA0 | LDY | LDA | LDX | lax | LDY | LDA | LDX | lax |
| 0xA8 | TAY | LDA | TAX | lax | LDY | LDA | LDX | lax |
| 0xB0 | BCS | LDA | hlt | lax | LDY | LDA | LDX | lax |
| 0xB8 | CLV | LDA | TSX | las | LDY | LDA | LDX | lax |
| 0xC0 | CPY | CMP | dop |     | CPY | CMP | DEC |     |
| 0xC8 | INY | CMP | DEX | sbx | CPY | CMP | DEC |     |
| 0xD0 | BNE | CMP | hlt |     | dop | CMP | DEC |     |
| 0xD8 | CLD | CMP | nop |     | top | CMP | DEC |     |
| 0xE0 | CPX | SBC | dop |     | CPX | SBC | INC |     |
| 0xE8 | INX | SBC | NOP | sbc | CPX | SBC | INC |     |
| 0xF0 | BEQ | SBC | hlt |     | dop | SBC | INC |     |
| 0xF8 | SED | SBC | nop |     | top | SBC | INC |     |

###   Addressing

|      | + 0 | + 1 | + 2 | + 3 | + 4 | + 5 | + 6 | + 7 |
|-----:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
| 0x00 | imp | i,X | kil | i,X | zp  | zp  | zp  | zp  |
| 0x08 | imp | #im | acc | #im | abs | abs | abs | abs |
| 0x10 | rel | i,Y | kil | i,Y | z,X | z,X | z,X | z,X |
| 0x18 | imp | a,Y | imp | a,Y | a,X | a,X | a,X | a,X |
| 0x20 | abs | i,X | kil | i,X | zp  | zp  | zp  | zp  |
| 0x28 | imp | #im | acc | #im | abs | abs | abs | abs |
| 0x30 | rel | i,Y | kil | i,Y | z,X | z,X | z,X | z,X |
| 0x38 | imp | a,Y | imp | a,Y | a,X | a,X | a,X | a,X |
| 0x40 | imp | i,X | kil | i,X | zp  | zp  | zp  | zp  |
| 0x48 | imp | #im | acc | #im | abs | abs | abs | abs |
| 0x50 | rel | i,Y | kil | i,Y | z,X | z,X | z,X | z,X |
| 0x58 | imp | a,Y | imp | a,Y | a,X | a,X | a,X | a,X |
| 0x60 | imp | i,X | kil | i,X | zp  | zp  | zp  | zp  |
| 0x68 | imp | #im | acc | #im | ind | abs | abs | abs |
| 0x70 | rel | i,Y | kil | i,Y | z,X | z,X | z,X | zX  |
| 0x78 | imp | a,Y | imp | a,Y | a,X | a,X | a,X | a,X |
| 0x80 | #im | i,X | #im | i,X | zp  | zp  | zp  | zp  |
| 0x88 | imp | #im | imp | #im | abs | abs | abs | abs |
| 0x90 | rel | i,Y | kil | i,Y | a,X | z,X | z,Y | z,Y |
| 0x98 | imp | a,Y | imp | a,Y | a,X | a,X | a,Y | a,Y |
| 0xA0 | #im | i,X | #im | i,X | zp  | zp  | zp  | zp  |
| 0xA8 | imp | #im | imp | #im | abs | abs | abs | abs |
| 0xB0 | rel | i,Y | kil | i,Y | z,X | z,X | z,Y | z,Y |
| 0xB8 | imp | a,Y | imp | a,Y | a,X | a,X | a,Y | a,Y |
| 0xC0 | #im | i,X | #im |     | zp  | zp  | zp  |     |
| 0xC8 | imp | #im | imp | #im | abs | abs | abs |     |
| 0xD0 | rel | i,Y | kil |     | z,X | z,X | z,X |     |
| 0xD8 | imp | a,Y | imp |     | a,X | a,X | a,X |     |
| 0xE0 | #im | i,X | #im |     | zp  | zp  | zp  |     |
| 0xE8 | imp | #im | imp | #im | abs | abs | abs |     |
| 0xF0 | rel | i,Y | kil |     | z,X | z,X | z,X |     |
| 0xF8 | imp | a,Y | imp |     | a,X | a,X | a,X |     |

###   Number of Bytes

|      | + 0 | + 1 | + 2 | + 3 | + 4 | + 5 | + 6 | + 7 |
|-----:|----:|----:|----:|----:|----:|----:|----:|----:|
| 0x00 |   2 |   2 |   ? |   2 |   2 |   2 |   2 |   2 |
| 0x08 |   1 |   2 |   1 |   2 |   3 |   3 |   3 |   3 |
| 0x10 |   2 |   2 |   ? |   2 |   2 |   2 |   2 |   2 |
| 0x18 |   1 |   3 |   1 |   3 |   3 |   3 |   3 |   3 |
| 0x20 |   3 |   2 |   ? |   2 |   2 |   2 |   2 |   2 |
| 0x28 |   1 |   2 |   1 |   2 |   3 |   3 |   3 |   3 |
| 0x30 |   2 |   2 |   ? |   2 |   2 |   2 |   2 |   2 |
| 0x38 |   1 |   3 |   1 |   3 |   3 |   3 |   3 |   3 |
| 0x40 |   1 |   2 |   ? |   2 |   2 |   2 |   2 |   2 |
| 0x48 |   1 |   2 |   1 |   2 |   3 |   3 |   3 |   3 |
| 0x50 |   2 |   2 |   ? |   2 |   2 |   2 |   2 |   2 |
| 0x58 |   1 |   3 |   1 |   3 |   3 |   3 |   3 |   3 |
| 0x60 |   1 |   2 |   ? |   2 |   2 |   2 |   2 |   2 |
| 0x68 |   1 |   2 |   1 |   2 |   3 |   3 |   3 |   3 |
| 0x70 |   2 |   2 |   ? |   2 |   2 |   2 |   2 |   2 |
| 0x78 |   1 |   3 |   1 |   3 |   3 |   3 |   3 |   3 |
| 0x80 |   2 |   2 |   2 |   2 |   2 |   2 |   2 |   2 |
| 0x88 |   1 |   2 |   1 |   2 |   3 |   3 |   3 |   3 |
| 0x90 |   2 |   2 |   ? |   2 |   2 |   2 |   2 |   2 |
| 0x98 |   1 |   3 |   1 |   3 |   3 |   3 |   3 |   3 |
| 0xA0 |   2 |   2 |   2 |   2 |   2 |   2 |   2 |   2 |
| 0xA8 |   1 |   2 |   1 |   2 |   3 |   3 |   3 |   3 |
| 0xB0 |   2 |   2 |   ? |   2 |   2 |   2 |   2 |   2 |
| 0xB8 |   1 |   3 |   1 |   3 |   3 |   3 |   3 |   3 |
| 0xC0 |   2 |   2 |   2 |     |   2 |   2 |   2 |     |
| 0xC8 |   1 |   2 |   1 |   2 |   3 |   3 |   3 |     |
| 0xD0 |   2 |   2 |   ? |     |   2 |   2 |   2 |     |
| 0xD8 |   1 |   3 |   1 |     |   3 |   3 |   3 |     |
| 0xE0 |   2 |   2 |   2 |     |   2 |   2 |   2 |     |
| 0xE8 |   1 |   2 |   1 |   2 |   3 |   3 |   3 |     |
| 0xF0 |   2 |   2 |   ? |     |   2 |   2 |   2 |     |
| 0xF8 |   1 |   3 |   1 |     |   3 |   3 |   3 |     |

###   Cycles

|      | + 0 | + 1 | + 2 | + 3 | + 4 | + 5 | + 6 | + 7 |
|-----:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
| 0x00 |   7 |   6 |   ? |   8 |   3 |   3 |   5 |   5 |
| 0x08 |   3 |   2 |   2 |   2 |   4 |   4 |   6 |   6 |
| 0x10 | 2-4 | 5,6 |   ? |   8 |   4 |   4 |   6 |   6 |
| 0x18 |   2 | 4,5 |   2 |   7 |   4 | 4,5 |   7 |   7 |
| 0x20 |   6 |   6 |   ? |   8 |   3 |   3 |   5 |   5 |
| 0x28 |   4 |   2 |   2 |   2 |   4 |   4 |   6 |   6 |
| 0x30 | 2-4 | 5,6 |   ? |   8 |   4 |   4 |   6 |   6 |
| 0x38 |   2 | 4,5 |   2 |   7 |   4 | 4,5 |   7 |   7 |
| 0x40 |   6 |   6 |   ? |   8 |   3 |   3 |   5 |   5 |
| 0x48 |   3 |   2 |   2 |   2 |   3 |   4 |   6 |   6 |
| 0x50 | 2-4 | 5,6 |   ? |   8 |   4 |   4 |   6 |   6 |
| 0x58 |   2 | 4,5 |   2 |   7 |   4 | 4,5 |   7 |   7 |
| 0x60 |   6 |   6 |   ? |   8 |   3 |   3 |   5 |   5 |
| 0x68 |   4 |   2 |   2 |   2 |   5 |   4 |   6 |   6 |
| 0x70 | 2-4 | 5,6 |   ? |   8 |   4 |   4 |   6 |   6 |
| 0x78 |   2 | 4,5 |   2 |   7 |   4 | 4,5 |   7 |   7 |
| 0x80 |   2 |   6 |   2 |   6 |   3 |   3 |   3 |   3 |
| 0x88 |   2 |   2 |   2 |   2 |   4 |   4 |   4 |   4 |
| 0x90 | 2-4 |   6 |   ? |   6 |   4 |   4 |   4 |   4 |
| 0x98 |   2 |   5 |   2 |   5 |   5 |   5 |   5 |   5 |
| 0xA0 |   2 |   6 |   2 |   6 |   3 |   3 |   3 |   3 |
| 0xA8 |   2 |   2 |   2 |   2 |   4 |   4 |   4 |   4 |
| 0xB0 | 2-4 | 5,6 |   ? |   5 |   4 |   4 |   4 |   4 |
| 0xB8 |   2 | 4,5 |   2 |   4 | 4,5 | 4,5 | 4,5 |   4 |
| 0xC0 |   2 |   6 |   2 |     |   3 |   3 |   5 |     |
| 0xC8 |   2 |   2 |   2 |   2 |   4 |   4 |   6 |     |
| 0xD0 | 2-4 | 5,6 |   ? |     |   4 |   4 |   6 |     |
| 0xD8 |   2 | 4,5 |   2 |     |   4 | 4,5 |   7 |     |
| 0xE0 |   2 |   6 |   2 |     |   3 |   3 |   5 |     |
| 0xE8 |   2 |   2 |   2 |   2 |   4 |   4 |   6 |     |
| 0xF0 | 2-4 | 5,6 |   ? |     |   4 |   4 |   6 |     |
| 0xF8 |   2 | 4,5 |   2 |     |   4 | 4,5 |   7 |     |


##  Details

###   Access

- LDA

|  Addressing  | OPE | Bytes | Cycles |
|:------------:|:---:|------:|:-------|
| #Immediate   | $A9 |     2 | 2      |
| ZeroPage     | $A5 |     2 | 3      |
| ZeroPage, X  | $B5 |     2 | 4      |
| Absolute     | $AD |     3 | 4      |
| Absolute, X  | $BD |     3 | 4 (5)  |
| Absolute, Y  | $B9 |     3 | 4 (5)  |
| (Indirect,X) | $A1 |     2 | 6      |
| (Indirect),Y | $B1 |     2 | 5 (6)  |

- LDX

|  Addressing  | OPE | Bytes | Cycles |
|:------------:|:---:|------:|:-------|
| #Immediate   | $A2 |     2 | 2      |
| ZeroPage     | $A6 |     2 | 3      |
| ZeroPage, Y  | $B6 |     2 | 4      |
| Absolute     | $AE |     3 | 4      |
| Absolute, Y  | $BE |     3 | 4 (5)  |

- LDY

|  Addressing  | OPE | Bytes | Cycles |
|:------------:|:---:|------:|:-------|
| #Immediate   | $A0 |     2 | 2      |
| ZeroPage     | $A4 |     2 | 3      |
| ZeroPage, X  | $B4 |     2 | 4      |
| Absolute     | $AC |     3 | 4      |
| Absolute, X  | $BC |     3 | 4 (5)  |

- STA

|  Addressing  | OPE | Bytes | Cycles |
|:------------:|:---:|------:|:-------|
| ZeroPage     | $85 |     2 | 3      |
| ZeroPage, X  | $95 |     2 | 4      |
| Absolute     | $8D |     3 | 4      |
| Absolute, X  | $9D |     3 | 5      |
| Absolute, Y  | $99 |     3 | 5      |
| (Indirect,X) | $81 |     2 | 6      |
| (Indirect),Y | $91 |     2 | 6      |

- STX

|  Addressing  | OPE | Bytes | Cycles |
|:------------:|:---:|------:|:-------|
| ZeroPage     | $86 |     2 | 3      |
| ZeroPage, Y  | $96 |     2 | 4      |
| Absolute     | $8E |     3 | 4      |

- STY

|  Addressing  | OPE | Bytes | Cycles |
|:------------:|:---:|------:|:-------|
| ZeroPage     | $84 |     2 | 3      |
| ZeroPage, X  | $94 |     2 | 4      |
| Absolute     | $8C |     3 | 4      |


###   Transfer

- TAX

|  Addressing  | OPE | Bytes | Cycles |
|:------------:|:---:|------:|:-------|
| Implied      | $AA |     1 | 2      |

- TAY

|  Addressing  | OPE | Bytes | Cycles |
|:------------:|:---:|------:|:-------|
| Implied      | $A8 |     1 | 2      |

- TXA

|  Addressing  | OPE | Bytes | Cycles |
|:------------:|:---:|------:|:-------|
| Implied      | $8A |     1 | 2      |

- TYA

|  Addressing  | OPE | Bytes | Cycles |
|:------------:|:---:|------:|:-------|
| Implied      | $98 |     1 | 2      |


###   Arithmetic

- ADC

|  Addressing  | OPE | Bytes | Cycles |
|:------------:|:---:|------:|:-------|
| #Immediate   | $69 |     2 | 2      |
| ZeroPage     | $65 |     2 | 3      |
| ZeroPage, X  | $75 |     2 | 4      |
| Absolute     | $6D |     3 | 4      |
| Absolute, X  | $7D |     3 | 4 (5)  |
| Absolute, Y  | $79 |     3 | 4 (5)  |
| (Indirect,X) | $61 |     2 | 6      |
| (Indirect),Y | $71 |     2 | 5 (6)  |

- DEC

|  Addressing  | OPE | Bytes | Cycles |
|:------------:|:---:|------:|:-------|
| ZeroPage     | $C6 |     2 | 5      |
| ZeroPage, X  | $D6 |     2 | 6      |
| Absolute     | $CE |     3 | 6      |
| Absolute, X  | $DE |     3 | 7      |

- DEX

|  Addressing  | OPE | Bytes | Cycles |
|:------------:|:---:|------:|:-------|
| Implied      | $CA |     1 | 2      |


- DEY

|  Addressing  | OPE | Bytes | Cycles |
|:------------:|:---:|------:|:-------|
| Implied      | $88 |     1 | 2      |

- INC

|  Addressing  | OPE | Bytes | Cycles |
|:------------:|:---:|------:|:-------|
| ZeroPage     | $E6 |     2 | 5      |
| ZeroPage, X  | $F6 |     2 | 6      |
| Absolute     | $EE |     3 | 6      |
| Absolute, X  | $FE |     3 | 7      |

- INX

|  Addressing  | OPE | Bytes | Cycles |
|:------------:|:---:|------:|:-------|
| Implied      | $E8 |     1 | 2      |

- INY

|  Addressing  | OPE | Bytes | Cycles |
|:------------:|:---:|------:|:-------|
| Implied      | $C8 |     1 | 2      |

- SBC

|  Addressing  | OPE | Bytes | Cycles |
|:------------:|:---:|------:|:-------|
| #Immediate   | $E9 |     2 | 2      |
| ZeroPage     | $E5 |     2 | 3      |
| ZeroPage, X  | $F5 |     2 | 4      |
| Absolute     | $ED |     3 | 4      |
| Absolute, X  | $FD |     3 | 4 (5)  |
| Absolute, Y  | $F9 |     3 | 4 (5)  |
| (Indirect,X) | $E1 |     2 | 6      |
| (Indirect),Y | $F1 |     2 | 5 (6)  |


###   Shift

- ASL

|  Addressing  | OPE | Bytes | Cycles |
|:------------:|:---:|------:|:-------|
| Accumulator  | $0A |     1 | 2      |
| ZeroPage     | $06 |     2 | 5      |
| ZeroPage, X  | $16 |     2 | 6      |
| Absolute     | $0E |     3 | 6      |
| Absolute, X  | $1E |     3 | 7      |

- LSR

|  Addressing  | OPE | Bytes | Cycles |
|:------------:|:---:|------:|:-------|
| Accumulator  | $4A |     1 | 2      |
| ZeroPage     | $46 |     2 | 5      |
| ZeroPage, X  | $56 |     2 | 6      |
| Absolute     | $4E |     3 | 6      |
| Absolute, X  | $5E |     3 | 7      |

- ROL

|  Addressing  | OPE | Bytes | Cycles |
|:------------:|:---:|------:|:-------|
| Accumulator  | $2A |     1 | 2      |
| ZeroPage     | $26 |     2 | 5      |
| ZeroPage, X  | $36 |     2 | 6      |
| Absolute     | $2E |     3 | 6      |
| Absolute, X  | $3E |     3 | 7      |

- ROR

|  Addressing  | OPE | Bytes | Cycles |
|:------------:|:---:|------:|:-------|
| Accumulator  | $6A |     1 | 2      |
| ZeroPage     | $66 |     2 | 5      |
| ZeroPage, X  | $76 |     2 | 6      |
| Absolute     | $6E |     3 | 6      |
| Absolute, X  | $7E |     3 | 7      |


###  Bitwise

- AND

|  Addressing  | OPE | Bytes | Cycles |
|:------------:|:---:|------:|:-------|
| #Immediate   | $29 |     2 | 2      |
| ZeroPage     | $25 |     2 | 3      |
| ZeroPage, X  | $35 |     2 | 4      |
| Absolute     | $2D |     3 | 4      |
| Absolute, X  | $3D |     3 | 4 (5)  |
| Absolute, Y  | $39 |     3 | 4 (5)  |
| (Indirect,X) | $21 |     2 | 6      |
| (Indirect),Y | $31 |     2 | 5 (6)  |

- BIT

|  Addressing  | OPE | Bytes | Cycles |
|:------------:|:---:|------:|:-------|
| ZeroPage     | $24 |     2 | 3      |
| Absolute     | $2C |     3 | 4      |

- EOR

|  Addressing  | OPE | Bytes | Cycles |
|:------------:|:---:|------:|:-------|
| #Immediate   | $49 |     2 | 2      |
| ZeroPage     | $45 |     2 | 3      |
| ZeroPage, X  | $55 |     2 | 4      |
| Absolute     | $4D |     3 | 4      |
| Absolute, X  | $5D |     3 | 4 (5)  |
| Absolute, Y  | $59 |     3 | 4 (5)  |
| (Indirect,X) | $41 |     2 | 6      |
| (Indirect),Y | $51 |     2 | 5 (6)  |

- ORA

|  Addressing  | OPE | Bytes | Cycles |
|:------------:|:---:|------:|:-------|
| #Immediate   | $09 |     2 | 2      |
| ZeroPage     | $05 |     2 | 3      |
| ZeroPage, X  | $15 |     2 | 4      |
| Absolute     | $0D |     3 | 4      |
| Absolute, X  | $1D |     3 | 4 (5)  |
| Absolute, Y  | $19 |     3 | 4 (5)  |
| (Indirect,X) | $01 |     2 | 6      |
| (Indirect),Y | $11 |     2 | 5 (6)  |


###  Compare

- CMP

|  Addressing  | OPE | Bytes | Cycles |
|:------------:|:---:|------:|:-------|
| #Immediate   | $C9 |     2 | 2      |
| ZeroPage     | $C5 |     2 | 3      |
| ZeroPage, X  | $D5 |     2 | 4      |
| Absolute     | $CD |     3 | 4      |
| Absolute, X  | $DD |     3 | 4 (5)  |
| Absolute, Y  | $D9 |     3 | 4 (5)  |
| (Indirect,X) | $C1 |     2 | 6      |
| (Indirect),Y | $D1 |     2 | 5 (6)  |

- CPX

|  Addressing  | OPE | Bytes | Cycles |
|:------------:|:---:|------:|:-------|
| #Immediate   | $E0 |     2 | 2      |
| ZeroPage     | $E4 |     2 | 3      |
| Absolute     | $EC |     3 | 4      |

- CPY

|  Addressing  | OPE | Bytes | Cycles |
|:------------:|:---:|------:|:-------|
| #Immediate   | $C0 |     2 | 2      |
| ZeroPage     | $C4 |     2 | 3      |
| Absolute     | $CC |     3 | 4      |


###  Branch

- BCC

|  Addressing  | OPE | Bytes | Cycles |
|:------------:|:---:|------:|:-------|
| Relative     | $90 |     2 | 2-4    |

- BCS

|  Addressing  | OPE | Bytes | Cycles |
|:------------:|:---:|------:|:-------|
| Relative     | $B0 |     2 | 2-4    |

- BEQ

|  Addressing  | OPE | Bytes | Cycles |
|:------------:|:---:|------:|:-------|
| Relative     | $F0 |     2 | 2-4    |

- BMI

|  Addressing  | OPE | Bytes | Cycles |
|:------------:|:---:|------:|:-------|
| Relative     | $30 |     2 | 2-4    |

- BNE

|  Addressing  | OPE | Bytes | Cycles |
|:------------:|:---:|------:|:-------|
| Relative     | $D0 |     2 | 2-4    |

- BPL

|  Addressing  | OPE | Bytes | Cycles |
|:------------:|:---:|------:|:-------|
| Relative     | $10 |     2 | 2-4    |

- BVC

|  Addressing  | OPE | Bytes | Cycles |
|:------------:|:---:|------:|:-------|
| Relative     | $50 |     2 | 2-4    |

- BVS

|  Addressing  | OPE | Bytes | Cycles |
|:------------:|:---:|------:|:-------|
| Relative     | $70 |     2 | 2-4    |


###  Jump

- BRK

|  Addressing  | OPE | Bytes | Cycles |
|:------------:|:---:|------:|:-------|
| Implied      | $00 |     2 | 7      |

- JMP

|  Addressing  | OPE | Bytes | Cycles |
|:------------:|:---:|------:|:-------|
| Absolute     | $4C |     3 | 3      |
| (Indirect)   | $6C |     3 | 5      |

- JSR

|  Addressing  | OPE | Bytes | Cycles |
|:------------:|:---:|------:|:-------|
| Absolute     | $20 |     3 | 6      |

- RTI

|  Addressing  | OPE | Bytes | Cycles |
|:------------:|:---:|------:|:-------|
| Implied      | $40 |     1 | 6      |

- RTS

|  Addressing  | OPE | Bytes | Cycles |
|:------------:|:---:|------:|:-------|
| Implied      | $60 |     1 | 6      |


###  Stack

- PHA

|  Addressing  | OPE | Bytes | Cycles |
|:------------:|:---:|------:|:-------|
| Implied      | $48 |     1 | 3      |

- PHP

|  Addressing  | OPE | Bytes | Cycles |
|:------------:|:---:|------:|:-------|
| Implied      | $08 |     1 | 3      |

- PLA

|  Addressing  | OPE | Bytes | Cycles |
|:------------:|:---:|------:|:-------|
| Implied      | $68 |     1 | 4      |

- PLP

|  Addressing  | OPE | Bytes | Cycles |
|:------------:|:---:|------:|:-------|
| Implied      | $28 |     1 | 4      |

- TSX

|  Addressing  | OPE | Bytes | Cycles |
|:------------:|:---:|------:|:-------|
| Implied      | $BA |     1 | 2      |

- TXS

|  Addressing  | OPE | Bytes | Cycles |
|:------------:|:---:|------:|:-------|
| Implied      | $9A |     1 | 2      |


###  Flags

- CLC

|  Addressing  | OPE | Bytes | Cycles |
|:------------:|:---:|------:|:-------|
| Implied      | $18 |     1 | 2      |

- CLD

|  Addressing  | OPE | Bytes | Cycles |
|:------------:|:---:|------:|:-------|
| Implied      | $D8 |     1 | 2      |

- CLI

|  Addressing  | OPE | Bytes | Cycles |
|:------------:|:---:|------:|:-------|
| Implied      | $58 |     1 | 2      |

- CLV

|  Addressing  | OPE | Bytes | Cycles |
|:------------:|:---:|------:|:-------|
| Implied      | $B8 |     1 | 2      |

- SEC

|  Addressing  | OPE | Bytes | Cycles |
|:------------:|:---:|------:|:-------|
| Implied      | $38 |     1 | 2      |

- SED

|  Addressing  | OPE | Bytes | Cycles |
|:------------:|:---:|------:|:-------|
| Implied      | $F8 |     1 | 2      |

- SEI

|  Addressing  | OPE | Bytes | Cycles |
|:------------:|:---:|------:|:-------|
| Implied      | $78 |     1 | 2      |


###  Other

- NOP

|  Addressing  | OPE | Bytes | Cycles |
|:------------:|:---:|------:|:-------|
| Implied      | $EA |     1 | 2      |
