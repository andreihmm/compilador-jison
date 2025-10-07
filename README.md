# 🛠️ Mini Compilador em Jison

**Autor:** Andrei Alves Fracalossi  
**Arquivo principal:** `trabalho_corrigido.jison`  
**Descrição:** Este é um compilador simples desenvolvido com **Jison**, inspirado em uma linguagem de programação C-like. Ele é capaz de processar declarações de variáveis, ponteiros, estruturas condicionais, laços, funções e operações aritméticas/lógicas básicas.

---

## 📦 Funcionalidades

Este compilador suporta os seguintes recursos:

### ✅ Tipos de Dados
- `int`
- `float`
- `void`

### ✅ Variáveis
- Declaração de múltiplas variáveis na mesma linha.
- Inicialização opcional no momento da declaração.
- Suporte a ponteiros (`*`).

### ✅ Funções
- Declaração de funções com parâmetros tipados.
- Corpo da função com múltiplos comandos.
- Suporte ao `return`.

### ✅ Expressões Aritméticas
- Soma (`+`), Subtração (`-`), Multiplicação (`*`), Divisão (`/`).

### ✅ Operadores Relacionais e Lógicos
- Comparações: `==`, `!=`, `<`, `>`, `<=`, `>=`
- Lógicos: `&&`, `||`, `!`

### ✅ Comandos de Controle
- `if`, `else` (com ou sem blocos `{}`).
- `while`, `do-while`, `for` (**pendente de implementação funcional**).
- Blocos de comandos `{ ... }`.

### ✅ Entrada/Saída
- `print` para saída de valores.
- Suporte básico a strings e caracteres.

### ✅ Comentários
- Suporte a comentários de linha com `//`.

---

## 🚫 Limitações

Este compilador **não executa código real**, apenas **analisa e interpreta a estrutura sintática** e, em alguns casos, avalia expressões durante a análise (e.g., `3 + 5` é computado como `8`).

### ⚠️ Limitações atuais:

- **Não há verificação de escopo**: todas as variáveis são considera
