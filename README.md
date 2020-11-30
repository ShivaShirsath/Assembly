# ReadyForAssemblyLanguage
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
> How To Run :

    Step 1 :
        Open Terminal in this Folder

    Step 2 :
        Using `edit` command for creating/editing `File.asm` like below
        `C : \ Download \ ReadyForAssembly > edit Main.asm`

    Step 3 :
        Save Edited file and Exit to terminal

    Step 4 :
        Using `masm` command for making the assembly to `File.obj` like below
        'C : \ Download \ ReadyForAssembly > masm Main.asm'

    Step 5 :
        Using `link` command for linking the objects to `File.exe` like below
        `C : \ Download \ ReadyForAssembly > link Main.obj`

    Step 6 :
        Using File name with extension `.exe' for Running the Executable like below
        `C : \ Download \ ReadyDorAssembly > Main.exe`

> OutPut :

![Output](/output/output.png)
