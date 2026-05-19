# Explicações dos desafios da atividade 2
## Feito por Bruno de Carvalho:

## Desafio 1:
O código usa uma pilha para guardar os sinais de abertura ((, [, {). Quando aparece um sinal de fechamento, o programa checa se ele combina com o último que foi guardado. Se os pares baterem, ele limpa esse item e segue em frente; se estiverem errados ou sobrar algum sinal sem par no final, a frase é considerada inválida.

## Desafio 2:
O funcionamento desse código baseia-se na propriedade principal da pilha: o último a entrar é o primeiro a sair (LIFO).

A Estrutura (Pilha Dinâmica): Criamos uma estrutura onde cada "nó" guarda um caractere e um ponteiro para o próximo. Como usamos malloc, a pilha cresce conforme o tamanho da palavra digitada, sem desperdiçar espaço.

O Empilhamento (Push): O programa percorre a string do começo ao fim. Cada letra é colocada no topo da pilha. Se você digitar "CASA", o 'C' entra primeiro, depois o 'A', o 'S' e, por fim, o 'A' fica no topo.

A Inversão (Pop): Para inverter, começamos a retirar os elementos da pilha. Como o último 'A' de "CASA" era o topo, ele é o primeiro a sair e é colocado na primeira posição da string. Depois sai o 'S', o 'A' e o 'C'.

Sobrescrita: O código utiliza a própria variável da string original para guardar os caracteres que saem da pilha, economizando memória, já que os caracteres originais já estão salvos com segurança dentro dos nós da pilha.
