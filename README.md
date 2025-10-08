# Trabalho Corrigido - Gramática Jison para C

## Autor
**Andrei Alves Fracalossi**

## Descrição
Este arquivo contém uma gramática **Jison** projetada para analisar um subconjunto da linguagem C.  
Ele suporta:

- Declarações de variáveis simples e ponteiros
- Arrays (simples e multidimensionais) com ou sem inicializadores
- Inicializadores de structs e unions
- Declarações de `struct`, `union` e `enum`
- Funções com parâmetros e protótipos
- Operadores básicos e compostos (`+`, `-`, `*`, `/`, `%`, `+=`, `-=`, etc.)
- Controle de fluxo: `if`, `else`, `while`, `do-while`, `for`, `switch/case/default`
- Chamadas de funções (`printf`, `scanf` e outras)
- Expressões aritméticas, lógicas e de comparação
- Tipos qualificados (`const` e `volatile`)

O objetivo é fornecer um **parser capaz de gerar uma árvore sintática abstrata (AST)** para programas C simples, incluindo manipulação de structs, unions e arrays.

---

## Estrutura do Arquivo

- **Lexical analyzer (`%lex`)**: define tokens, literais, operadores e palavras reservadas do C.
- **Produções (`%%`)**:
  - `programa` - ponto de entrada da gramática
  - `diretivas` e `diretiva` - tratamento de `#include` e `#define`
  - `declaracoes` e `declaracao` - declarações de variáveis, structs, unions e enums
  - `struct_declaracao`, `union_declaracao`, `enum_declaracao` - declarações complexas
  - `tipo` - definição de tipos básicos, qualificados e compostos (`struct`)
  - `funcao` e `parametros` - declaração e protótipo de funções
  - `declaracao_simples` - variáveis, ponteiros e arrays, incluindo inicializadores
  - `initializer` e `initializer_list` - inicializadores de arrays e structs/unions
  - `comandos` e `comando` - comandos, expressões, loops, condições e chamadas de função
  - `expressao` - avaliação de expressões, cast, sizeof, operadores e acesso a arrays

---

## Exemplos de Código Aceitos

```c
#include <stdio.h>
#define MAX 100

struct Data {
    int id;
    char name[20];
};

union Number {
    int i;
    float f;
};

enum Color { RED, GREEN, BLUE };

int main() {
    struct Data data1 = {1, "John"};
    union Number n = {42};
    int arr[3] = {1, 2, 3};

    for (int i = 0; i < 3; i++) {
        printf("%d\n", arr[i]);
    }

    return 0;
}
