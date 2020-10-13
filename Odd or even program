data segment
    msg1 db 'enter the number $'
    msg2 db 0ah, 'the number is odd $'
    msg3 db 0ah, 'the number is even $'
data ends
code segment
    assume cs:code, ds:data
    start:
    mov ax,data
    mov ds,ax
    mov dx,offset msg1
    mov ah,09h
    int 21h
    mov ah,01h
    int 21h
    sub al,30h
    mov cl,02h
    div cl
    cmp ah,00
    je loop1
    mov dx,offset msg2
    mov ah,09h
    int 21h
    jne x
    loop1: mov dx,offset msg3
    mov ax,09h
    int 21h
    x: mov ah,4ch
    int 21h
code ends
end start
