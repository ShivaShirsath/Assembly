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
   * Open Terminal in this Folder
   * Using `EDIT` command for creating/editing `.ASM` file as below
      > `C : \ TC \ BIN > EDIT MAIN.ASM`
   * Save Edited file and Exit to terminal
   * Using `TASM` command for making the assembly to object ( `.ASM` to `.OBJ` ) file as below
      > `C : \ TC \ BIN > TASM MAIN.ASM`
   * Using `TLINK` command for linking the objects to executable ( `.OBJ` to `.EXE` ) file as below
      > `C : \ TC \ BIN > TLINK MAIN.OBJ`
   * Using File name with extension `.EXE' for Running the Executable as below
      > `C : \ TC \ BIN > MAIN.EXE`

> OutPut :

![Output](output.png)

## Download : [DOS Box](DOS%20Box_1.1.1.apk?raw=true)
## Download Required Files : [TC zip](TC.zip?raw=true)
## Download Integreted : [Assembler](Assembler_2.0.apk?raw=true)
