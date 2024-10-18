# Estudo de comando NASM
<p align="center">

<img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcReA0GB6oj4q0hWEIK1ujzZXMOemOz1l-gPQQ&s" width=170 heigth=170>

</p>
## primeiros comandos

* Programa hello world

```Assembly
 section .text
    _start:
    mov rax,1        ;prepara o sistema para fazer a escrita de um texto
    mov rdi,1        ;prepara a saida do texto na tela 
    mov rsi,mensagem ;imprimir ou exibir a mensagem na tela
    mov rdx,13       ;quantidade de caracteres
    syscall          ;chama o sistema para prepara saida 
    mov rax,60       ;chamada para a saida do sistema
    xor rdi,rdi      ;executar a saida do sistema
    syscall          ;invocar o sistema operacional para fechar

    section .data
    mensagem:db 'Hello,World',10   ;O valor 10 representa a quebra de linha 

```