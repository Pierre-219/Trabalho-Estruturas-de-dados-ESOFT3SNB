# Dicionário com Tabela Hash em C

**Disciplina:** Estrutura de Dados — Atividade Avaliativa 3  
**Curso:** Engenharia de Software  
**Instituição:** Unicesumar  

---

## Descrição

Sistema de dicionário implementado em linguagem C utilizando **Tabela Hash** com tratamento de colisões por **listas encadeadas**. O programa permite inserir, buscar e remover palavras com suas definições, além de exibir a estrutura da tabela e estatísticas de desempenho.

---

## Estrutura do Projeto

Todo o código está em um único arquivo `dicionario_completo.c`, organizado em seções identificadas por comentários:

| Seção no arquivo | Responsável | Conteúdo |
|---|---|---|
| STRUCTS | — | Definição de `No` e `TabelaHash` |
| PESSOA 1 | Pessoa 1 | Função hash (djb2) e inicialização da tabela |
| PESSOA 2 | Pessoa 2 | Inserção de palavras e definições |
| PESSOA 3 | Pessoa 3 | Busca e remoção de palavras |
| PESSOA 4 | Pessoa 4 | Exibição da tabela hash |
| PESSOA 5 | Pessoa 5 | Estatísticas, liberação de memória e menu principal |

---

## Como Compilar e Executar

### Terminal / Linux

```bash
gcc dicionario_completo.c -o dicionario
./dicionario
```

### GDB Online (gdbonline.com)

1. Acesse [https://www.onlinegdb.com/](https://www.onlinegdb.com/)
2. Selecione a linguagem **C**
3. Cole o conteúdo do arquivo `dicionario_completo.c` no editor
4. Clique em **Run**

---

## Funcionamento

### Função Hash

A função utilizada é baseada no algoritmo **djb2**:

```
hash = 5381
para cada caractere c da palavra:
    hash = hash * 31 + c
índice = hash % TAMANHO_TABELA
```

O tamanho da tabela é **13** (número primo), o que reduz a chance de colisões distribuindo melhor os índices.

### Tratamento de Colisões — Lista Encadeada

Quando duas palavras geram o mesmo índice (colisão), os registros são armazenados em uma **lista encadeada** dentro do mesmo bucket. A inserção sempre acontece no início da lista para garantir O(1) nessa operação.

```
Bucket[7] → "algoritmo" → "algebra" → NULL
```

### Estrutura de Dados

```c
// Nó da lista encadeada
typedef struct No {
    char palavra[100];
    char definicao[500];
    struct No *proximo;
} No;

// Tabela Hash
typedef struct {
    No *buckets[13];   // vetor de ponteiros para listas
    int total_elementos;
    int total_colisoes;
} TabelaHash;
```

---

## Funcionalidades

### 1 — Inserir Palavra
Calcula o índice com a função hash e insere o novo nó no início da lista do bucket correspondente. Se a palavra já existe, atualiza a definição.

### 2 — Buscar Palavra
Calcula o índice, percorre a lista encadeada do bucket procurando pela palavra. Retorna a definição se encontrada.

### 3 — Remover Palavra
Localiza o nó na lista encadeada, ajusta os ponteiros para contorná-lo e libera a memória com `free()`.

### 4 — Exibir Tabela
Percorre todos os 13 buckets mostrando o conteúdo de cada lista encadeada. Buckets vazios são sinalizados como `(vazio)`.

### 5 — Estatísticas

| Informação | Descrição |
|---|---|
| Total de elementos | Quantidade de palavras no dicionário |
| Total de colisões | Quantas vezes dois elementos ocuparam o mesmo bucket |
| Fator de carga | `elementos / tamanho_tabela` — indica o quão cheia está a tabela |
| Maior lista encadeada | Tamanho do bucket com mais elementos |

O **fator de carga ideal** fica abaixo de 0.75. Acima disso, muitas colisões degradam o desempenho de O(1) para O(n).

---

## Exemplo de Uso

```
=== DICIONÁRIO COM TABELA HASH ===

1 - Inserir palavra
Opção: 1
Palavra: algoritmo
Definição: Conjunto de instruções para resolver um problema
Palavra "algoritmo" inserida no índice 7.

Opção: 5

========================================
           ESTATÍSTICAS
========================================
Tamanho da tabela   : 13 buckets
Elementos inseridos : 1
Buckets ocupados    : 1
Total de colisões   : 0
Fator de carga      : 0.08
Maior lista encad.  : 1 elemento(s)
========================================
```

---

## Conceitos Utilizados

- **Structs** — para representar os nós e a tabela
- **Ponteiros** — para navegar e manipular a lista encadeada
- **Alocação dinâmica** — `malloc` e `free` para criar e destruir nós
- **Listas encadeadas** — para tratar colisões dentro de cada bucket
- **Modularização** — código dividido em arquivos `.c` separados por responsabilidade
