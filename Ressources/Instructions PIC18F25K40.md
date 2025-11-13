# Instructions PIC18F25K40

## BYTE-ORIENTED OPERATIONS
| Mnemonic / Operands                       | Description                          | Status Affected     |
|-------------------------------------------|--------------------------------------|---------------------|
| ADDWF f, d, a                             | Add WREG and f                       | C, DC, Z, OV, N     |
| ADDWFC f, d, a                            | Add WREG and CARRY bit to f          | C, DC, Z, OV, N     |
| ANDWF f, d, a                             | AND WREG with f                      | Z, N                |
| CLRF f, a                                 | Clear f                              | Z                   |
| COMF f, d, a                              | Complement f                         | Z, N                |
| CPFSEQ f, a                               | Compare f with WREG, skip =          | None                |
| CPFSGT f, a                               | Compare f with WREG, skip >          | None                |
| CPFSLT f, a                               | Compare f with WREG, skip <          | None                |
| DECF f, d, a                              | Decrement f                          | C, DC, Z, OV, N     |
| DECFSZ f, d, a                            | Decrement f, Skip if 0               | None                |
| DCFSNZ f, d, a                            | Decrement f, Skip if Not 0           | None                |
| INCF f, d, a                              | Increment f                          | C, DC, Z, OV, N     |
| INCFSZ f, d, a                            | Increment f, Skip if 0               | None                |
| INFSNZ f, d, a                            | Increment f, Skip if Not 0           | None                |
| IORWF f, d, a                             | Inclusive OR WREG with f             | Z, N                |
| MOVF f, d, a                              | Move f                               | Z, N                |
| MOVFF fs, fd                              | Move fs (source) to fd (destination) | None                |
| MOVWF f, a                                | Move WREG to f                       | None                |
| MULWF f, a                                | Multiply WREG with f                 | None                |
| NEGF f, a                                 | Negate f                             | C, DC, Z, OV, N     |
| RLCF f, d, a                              | Rotate Left f through Carry          | C, Z, N             |
| RLNCF f, d, a                             | Rotate Left f (No Carry)             | Z, N                |
| RRCF f, d, a                              | Rotate Right f through Carry         | C, Z, N             |
| RRNCF f, d, a                             | Rotate Right f (No Carry)            | Z, N                |
| SETF f, a                                 | Set f                                | None                |
| SUBFWB f, d, a                            | Subtract f from WREG with borrow     | C, DC, Z, OV, N     |
| SUBWF f, d, a                             | Subtract WREG from f                 | C, DC, Z, OV, N     |
| SUBWFB f, d, a                            | Subtract WREG from f with borrow     | C, DC, Z, OV, N     |
| SWAPF f, d, a                             | Swap nibbles in f                    | None                |
| TSTFSZ f, a                               | Test f, skip if 0                    | None                |
| XORWF f, d, a                             | Exclusive OR WREG with f             | Z, N                |

## BIT-ORIENTED OPERATIONS
| Mnemonic / Operands                       | Description                          | Status Affected     |
|-------------------------------------------|--------------------------------------|---------------------|
| BCF f, b, a                               | Bit Clear f                          | None                |
| BSF f, b, a                               | Bit Set f                            | None                |
| BTFSC f, b, a                             | Bit Test f, Skip if Clear            | None                |
| BTFSS f, b, a                             | Bit Test f, Skip if Set              | None                |
| BTG f, b, a                               | Bit Toggle f                         | None                |

## CONTROL OPERATIONS
| Mnemonic / Operands                       | Description                          | Status Affected     |
|-------------------------------------------|--------------------------------------|---------------------|
| BC n                                      | Branch if Carry                      | None                |
| BN n                                      | Branch if Negative                   | None                |
| BNC n                                     | Branch if Not Carry                  | None                |
| BNN n                                     | Branch if Not Negative               | None                |
| BNOV n                                    | Branch if Not Overflow               | None                |
| BNZ n                                     | Branch if Not Zero                   | None                |
| BOV n                                     | Branch if Overflow                   | None                |
| BRA n                                     | Branch Unconditionally               | None                |
| BZ n                                      | Branch if Zero                       | None                |
| CALL k, s                                 | Call subroutine                      | None                |
| CLRWDT -                                  | Clear Watchdog Timer                 | TO, PD              |
| DAW -                                     | Decimal Adjust WREG                  | C                   |
| GOTO k                                    | Go to address                        | None                |
| NOP -                                     | No Operation                         | None                |
| POP -                                     | Pop top of return stack (TOS)        | None                |
| PUSH -                                    | Push top of return stack (TOS)       | None                |
| RCALL n                                   | Relative Call                        | None                |
| RESET -                                   | Software device Reset                | All                 |
| RETFIE s                                  | Return from interrupt enable         | GIE/GIEH, PEIE/GIEL |
| RETLW k                                   | Return with literal in WREG          | None                |
| RETURN s                                  | Return from Subroutine               | None                |
| SLEEP -                                   | Go into Standby mode                 | TO, PD              |


## LITERAL OPERATIONS
| Mnemonic / Operands                       | Description                          | Status Affected     |
|-------------------------------------------|--------------------------------------|---------------------|
| ADDLW k                                   | Add literal and WREG                 | C, DC, Z, OV, N     |
| ANDLW k                                   | AND literal with WREG                | Z, N                |
| IORLW k                                   | Inclusive OR literal with WREG       | Z, N                |
| LFSR f, k                                 | Move literal (12-bit) to FSR(f)      | None                |
| MOVLB k                                   | Move literal to BSR<3:0>             | None                |
| MOVLW k                                   | Move literal to WREG                 | None                |
| MULLW k                                   | Multiply literal with WREG           | None                |
| SUBLW k                                   | Subtract WREG from literal           | C, DC, Z, OV, N     |
| XORLW k                                   | Exclusive OR literal with WREG       | Z, N                |


## DATA MEMORY <-> PROGRAM MEMORY OPERATIONS
| Mnemonic / Operands                       | Description                          | Status Affected     |
|-------------------------------------------|--------------------------------------|---------------------|
| TBLR                                      | Table Read                           | None                |
| TBLRD                                     | Table Read with post-increment       | None                |
| TBLRD                                     | Table Read with post-decrement       | None                |
| TBLRD                                     | Table Read with pre-increment        | None                |
| TBLWT                                     | Table Write                          | None                |
| TBLWT                                     | Table Write with post-increment      | None                |
| TBLWT                                     | Table Write with post-decrement      | None                |
| TBLWT                                     | Table Write with pre-increment       | None                |

## Légende :
  - **`f`** : File register
  - **`d`** : Destination (W for WREG, F for File register)
  - **`a`** : Access bank
  - **`k`** : litteral
  - **`s`** : Update from shadow registers ?
  - **`n`** : relative address