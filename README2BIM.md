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



# Atividade 2
## Thaylor e Antonio




# Atividade 3
## Bruno
