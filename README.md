# Assembly

> Program :

```asm
DATA SEGMENT

     MSG DB "Hello World !$"
     
DATA ENDS

CODE SEGMENT  
    ASSUME DS:DATA, CS:CODE
    
    START:
        MOV AX,DATA
        MOV DS,AX
        
            LEA DX,MSG
            MOV AH,9
            INT 21H
        
        MOV AH,4CH
        INT 21H
        
CODE ENDS

    END START
```

* How To Run :
 
   * Exit to terminal
   * Use `EDIT` command for creating / editing `.ASM` file as below
      * `C : \ TC \ BIN > EDIT MAIN.ASM`
   * Save Edited file & Exit to terminal
   * Use `TASM` command for making the assembly code to object code ( `.ASM` to `.OBJ` ) as below
      * `C : \ TC \ BIN > TASM MAIN.ASM`
   * Use `TLINK` command for linking the object code to executable code ( `.OBJ` to `.EXE` ) as below
      * `C : \ TC \ BIN > TLINK MAIN.OBJ`
   * Use file name with extension `.EXE' for Running the Executable file as below
      * `C : \ TC \ BIN > MAIN.EXE`

> OutPut :

![Output](output.png)

## Download : [DOS Box](DOS%20Box_1.1.1.apk?raw=true)
## Download Required Files : [TC zip](TC.zip?raw=true)
## Download Integreted : [Assembler](Assembler_2.0.apk?raw=true)
