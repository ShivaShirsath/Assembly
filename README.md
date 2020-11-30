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
`
C : \ Download \ ReadyForAssembly > edit Main.asm 
C : \ Download \ ReadyForAssembly > masm Main.asm 
C : \ Download \ ReadyForAssembly > link Main.obj 
C : \ Download \ ReadyDorAssembly > Main.exe 
`
> OutPut :

![Output](/output/output.png)
