# Atvidade 1
## Pierre e Joao
## Questão 1 — Fibonacci Recursivo Ingênuo
### Feito por Pierre

Calcula o n-ésimo termo de Fibonacci recursivamente e exibe o total de
chamadas realizadas para mostrar a ineficiência do método.

### Função `fib`

- **Caso base:** `n <= 1` — retorna o próprio `n`
- **Redução:** `fib(n) = fib(n-1) + fib(n-2)`, diminuindo `n` até o caso base
- **Contador:** `calls` é um ponteiro para o inteiro do `main` — todas as
  chamadas incrementam o mesmo valor sem precisar de variável global

### Por que é ineficiente
Os mesmos valores são recalculados várias vezes. O número de chamadas
cresce exponencialmente — `fib(40)` gera mais de 300 milhões de chamadas.

Autor: João Vittor Mulinari
# Fibonacci Recursivo em C

Programa em C que calcula o número de Fibonacci utilizando recursão e mostra o total de chamadas recursivas realizadas.

## Como funciona

1. O usuário digita um número `n`
2. O programa calcula `fib(n)`
3. Exibe o resultado e o número de chamadas recursivas

## Exemplo

```text
Digite n: 6

fib(6) = 8
Total de chamadas recursivas: 25
```

## Compilar

```bash
gcc fibonacci.c -o fibonacci
```

## Executar

Linux/Mac:
```bash
./fibonacci
```

Windows:
```bash
fibonacci.exe
```

## Conceitos utilizados

- Recursão
- Ponteiros
- Funções em C
- Sequência de Fibonacci


# Atividade 2
## Thaylor e Antonio




# Atividade 3
## Feito por: Bruno de Carvalho.

O usuário digita a quantidade de discos e o programa mostra todos os movimentos necessários para levar os discos da torre A até a torre C, usando a torre B como auxiliar.
A função resolverHanoi() funciona de forma recursiva:

move os discos menores para a torre auxiliar;
move o maior disco;
depois move os discos menores para a torre final.


O número mínimo de movimentos é:
2^n - 1


