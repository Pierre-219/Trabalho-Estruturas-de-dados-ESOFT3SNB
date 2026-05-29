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
**Responsavel**:Thaylor


A função `buscarValor()` serve para procurar um número dentro de uma lista encadeada. Ela começa no primeiro nó da lista (`head`) e vai percorrendo os próximos nós um por um. A cada nó, compara o valor armazenado com o valor que está sendo procurado. Se encontrar, retorna a posição onde o valor está. Se chegar ao final da lista (`NULL`) sem encontrar o valor, retorna `-1`, indicando que ele não existe na lista. Por exemplo, na lista `10 -> 20 -> 30 -> NULL`, ao procurar o valor `20`, a função retorna `1`, pois ele está na segunda posição da lista (contando a partir de 0).


## Parte 3:
**Responsavel**: João Vittor Mulinari
# Inversão de Lista Encadeada em C
Este programa implementa a inversão de uma lista encadeada simples utilizando apenas ponteiros, sem criar uma nova lista ou utilizar vetores auxiliares.
## Funcionalidade
A função `inverterLista()` percorre a lista e altera a direção dos ponteiros, invertendo completamente a ordem dos elementos.

### Exemplo
Antes:
```txt
10 -> 20 -> 30 -> NULL
```
Depois:
```txt
30 -> 20 -> 10 -> NULL
```
## Conceitos Utilizados
* Estruturas (`struct`)
* Ponteiros
* Listas encadeadas
* Manipulação de memória dinâmica
* Algoritmo de inversão de lista

## Parte 4:
Antônio Henrique Kviatcovski:

A função dividirLista(No *head, No **lista1, No **lista2) tem como objetivo dividir uma lista encadeada em duas partes. Para isso, ela utiliza dois ponteiros: um ponteiro lento, que avança um nó por vez, e um ponteiro rápido, que avança dois nós por vez. 
Enquanto o ponteiro rápido percorre a lista, o lento se aproxima do meio. Quando o rápido chega ao final, o lento está posicionado no ponto de divisão da lista. Em seguida, o código separa a estrutura em duas listas independentes.

Por exemplo, em uma lista 10 -> 20 -> 30 -> 40 -> 50 -> NULL, a primeira lista resultante será 10 -> 20 -> 30 -> NULL e a segunda será 40 -> 50 -> NULL. Caso a quantidade de elementos seja ímpar, a primeira lista ficará com um elemento a mais. Essa abordagem é eficiente porque encontra o ponto de divisão sem precisar contar os elementos, percorrendo a lista apenas uma vez.


## Parte 5:
Bruno de carvalho:

# README - Playlist em C

## Descrição
Este programa em C implementa uma playlist de músicas utilizando uma lista duplamente encadeada circular.

A playlist permite navegar entre as músicas de forma contínua, avançando para a próxima ou retornando para a anterior.

--------------------------------------------------

## Funcionalidades
- Adicionar músicas na playlist
- Exibir todas as músicas
- Avançar para a próxima música
- Voltar para a música anterior
- Contar total de músicas
- Liberar memória da lista

--------------------------------------------------

## Estrutura Utilizada

typedef struct No {
    char musica[100];
    struct No *prox;
    struct No *ant;
} No;

Campos:
- musica → nome da música
- prox → ponteiro para próxima música
- ant → ponteiro para música anterior

--------------------------------------------------

## Conceitos Utilizados
- Structs
- Ponteiros
- Alocação dinâmica com malloc
- Liberação de memória com free
- Lista duplamente encadeada circular

--------------------------------------------------

## Compilação

gcc playlist.c -o playlist

--------------------------------------------------

## Execução

Windows:
playlist.exe

Linux/Mac:
./playlist

--------------------------------------------------

## Exemplo de Saída

Playlist:
[Rock] <-> [Jazz] <-> [Pop] <-> [Blues]

Total de musicas: 4

Tocando: Rock
Tocando: Jazz
Tocando: Pop
Tocando: Blues

Musica atual: Blues
