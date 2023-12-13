# Math Language Project

# **{mat}**

**POR: Alexandre Magno e Leonardo Scarlato**


**{mat}** consiste em uma linguagem de programação interpretada, com a finalidade de facilitar a escrita em português de operações matemáticas. Nesta linguagem, há palavras reservadas que representam operações que proximam a dialética matemática oral com o código. Assim, proporciando um espaço mais amigavél para estudos de ambas as ciências.

O público alvo dessa linguagem são de jovens no estágio de desenvolvimento do estudo matemático e de programação.

**{mat}** lidará com números pertencentes ao conjunto dos Racionais(Q). Contudo, na linguagem, trabalha-se com a separação entre inteiros e fracionarios.

### Gramática

```

<program> ::= Prog <declarations> <statements>

<declarations> ::= <declaration> <declarations> |
                   <declaration>

<declaration> ::= <type> Id = <expr>;

<type> ::= inteiro | fracionario

<statements> ::= <statement> <statements> |
                 <statement>

<statement> ::= <atrib> |
                <ifelse> |
                <while> |
                <for> |
                <function> |
                <callfunction> |
                <print>

<atrib> ::= Id = <expr> ;

<ifelse> ::= IfElse ( <expr> <comp> <expr> ) { <statements> } Else { <statements> }

<while> ::= While ( <expr> <comp> <expr> ) { <statements> }

<for> ::= For ( <atrib> ; <expr> <comp> <expr> ; <atrib> ) { <statements> }

<function> ::= Function Id ( <param> ) : <statements> 

<callfunction> ::= CallFunction Id ( <param> )

<print> ::= Print ( <expr> )

<expr> ::= <id> |
           <number> |
           <binary_op> |
           <unary_op> |
           <func_call>


<func_call> ::= Id ( <expr> )

<op> ::= + | - | * | / | raiz_de | elevado_a | fatorial | pi

<comp> ::= == | != | < | > | <= | >=

<param> ::= Id |
            Id , <param>

```

# Tokens

Para essa linguagem foram definidos tokens únicos e que correspondem à representação oral de algumas expressões matemáticas:

| Operação | Aplicação |
| ----- | --------- |
| Radiciação | 16 raiz_de 4 |
| Potenciação | 2 elevado_a 5 |
| Fatorial | 5 fatorial |
| $\Pi$ | 2 * pi * raio |


# Paradigma Funcional

A sintaxe para-se definir uma função é a seguinte:

        funcao id (parametro) : expressao ;

exemplo:

        funcao raiz_quadrada(x): x raiz_de 2;

As funções retornam o valor da expressão definida. A variável passada como parâmetro possui escopo local, logo, mesmo que haja outra variável de mesmo nome definida no código, não há interferencia entre elas.

