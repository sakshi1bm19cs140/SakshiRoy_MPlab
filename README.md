# SakshiRoy_MPlab
//MUPLAB_SUBTRACTION
.MODEL SMALL
.DATA
NUM1 DB 43
NUM2 DB 15
RES DB ?

.CODE
MOV AX,@DATA
MOV DS,AX

MOV AL,NUM1
SUB AL,NUM2
MOV RES,AL

MOV AH,4CH
INT 21H
END

//MUPLAB_MULTIPLICATION
.MODEL SMALL
.DATA
NUM1 DB 43
NUM2 DB 15
RES DW ?

.CODE
MOV AX,@DATA
MOV DS,AX

MOV AL,NUM1
MUL NUM2
MOV RES,AX

MOV AH,4CH
INT 21H
END

//MUPLAB_DIVISION
.MODEL SMALL
.DATA
NUM1 DW 1234
NUM2 DB 67
QUOT DB ?
REM DB ?

.CODE
MOV AX,@DATA
MOV DS,AX
MOV AL,NUM2
DIV NUM1
MOV QUOT,AL
MOV REM,AH

MOV AH,4CH
INT 21H
END
