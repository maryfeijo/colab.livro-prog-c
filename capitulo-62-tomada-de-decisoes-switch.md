# Capítulo 6.2: Tomada de Decisões - Switch

##### **Autor: **[**Ian Saud Soares**](https://github.com/iansaud)** **

#### Introdução

Basicamente Switch é um mecanismo para reduzir a utilização de diversos IF's e Else's o quer permitem diversas linhas de execução de código mediante uma condição. Com isso reduz a complexidade e facilita e muito entendimento da sua linha de código, é muito utilizado também para criação de menus em C/C++.

#### Algorítmo/Pseudocódigo

```c
possibilidade (variavel ou valor)
// Determina o Inicio
{
    caso (X): // Onde caso a variavel inserida anteriormente tenha valor igual a este, ele irã realizar a ação abaixo
    // Realiza uma ação
    caso (Z): // Onde caso a variavel inserida anteriormente tenha valor igual a este, ele irã realizar a ação abaixo
    // Realiza uma Ação

}
// Determina o Fim
```

Neste exemplo acima, podemos analisar que quando o compilador acessa o caso Switch, ele necessita de uma variável á  ser passada como parâmetro, esta que será comparada aos valores abaixo para entrar em cada situação listada abaixo.

#### Codigo utilizando If's Else's

```c
if (valor == X)
    // Realiza Ação
else
    if (valor == Z)
        //Realiza Ação
    else
        if (valor == Y)
            //Realiza Ação
        else
            if (valor == K)
                //Realiza Ação
```

Neste segundo exemplo utilizando If's e Else's encadeados podemos notar que o código fica bem mais complexo e cansativo para o leitor.

#### Código Utilizando Switch

```c
switch (valor)
{
    case valor1:
        //Realiza Ação
    break;
    case valor2:
        //Realiza Ação
    break;
    case valor3:
        //Realiza Ação
    break;
}
```

Também podemos definir uma ação padrão\(default\) para caso o valor passado não seja igual a nenhum dos cases listados anteriormente, abaixo um exemplo de uso

```c
switch (valor)
{
    case 1:
        printf("Voce digitou 1\n");
    break;
    case 2:
        printf("Voce digitou 2\n");

    break;
    case 3:
        printf("Voce digitou 3\n");

    break;
    default:
        printf("Voce digitou um numero que nao consta nas opcoes\n");

}
```

Agora um exemplo mais pratico de um código de um menu montado utilizando o switch case

```c
#include <stdio.h>

int main()
{    
    int menu;

    printf("Menu Seleções\n");
    printf("1 - Listar Cores Primarias\n");
    printf("2 - Listar Cores Secundarias");
    scanf("%d", &menu);

    switch (menu)
    {
        case 1:
            printf("Vermelho\n Amarelo\n Azul\n");
            break;
        case 2:
            printf("Laranja\n Verde\n Violeta\n");
            break;
        default:
            printf("Vc deve inserir um numero listado no menu 1 ou 2");
            break;
    }


}
```

#### Exercício

1- Utilizando a ferramenta switch case, crie um programa que diga receba do usuario um numero de 1 a 12 e o programa deve retornar ao usuario qual nome do mes. Exemplo: 1 = Janeiro

2 - Construa em  C uma mini calculadora utilizando Switch Case, onde o usuário deve selecionar se deseja fazer Soma, Subtração, Multiplicação ou Divisão e pedir ao usuário para inserir dois valores.

