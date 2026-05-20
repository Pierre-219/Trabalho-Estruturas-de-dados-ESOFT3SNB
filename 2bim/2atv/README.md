# Atividade Avaliativa 2 — Estruturas de Dados em C.
Gerenciador de inteiros usando listas encadeadas, desenvolvido em grupo para a disciplina de Estrutura de Dados da Unicesumar.
## Parte 1: Inserção em Posição Específica
**Responsável:** Pierre
### O que foi implementado
A função `void inserirPosicao(No **head, int valor, int posicao)` insere um novo nó em uma posição específica da lista encadeada.
### Como funciona
A função cobre 3 cenários:
1. **Posição inválida**: qualquer valor negativo ou além do tamanho da lista exibe uma mensagem de erro e encerra sem modificar a lista.
2. **Posição 0 (início)**: o novo nó passa a ser o novo `head`, apontando para o antigo primeiro elemento.
3. **Meio ou fim**: percorre a lista até o nó anterior à posição desejada e encaixa o novo nó entre ele e o próximo.
### Exemplo
Antes:  10 -> 20 -> 30 -> NULL
Depois: 10 -> 99 -> 20 -> 30 -> NULL  (inserção na posição 1)

## Parte 2:
**Responsavel**:

## Parte 3:
**Responsavel**:

## Parte 4:
**Responsavel**:

## Parte 5:
**Responsavel**:
