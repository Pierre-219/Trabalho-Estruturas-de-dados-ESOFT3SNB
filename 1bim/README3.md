# Explicação de Exercícios da atividade 3
## Feito por: Bruno de carvalho

## Desafio 1
À medida que os clientes chegam, eles são "amarrados" uns atrás dos outros usando ponteiros. O primeiro cliente fica no início e o último no fim,O atendimento sempre começa pelo início. Quando o primeiro cliente sai, o segundo da fila assume o lugar dele. Criamos uma variável (um cronômetro) que começa em zero. O primeiro da fila não espera nada. Assim que ele é atendido, o tempo que ele levou é somado ao cronômetro, que passa a ser o tempo de espera do próximo da fila,a ssim que um cliente termina seu atendimento, o "espaço" que ele ocupava na memória é apagado para manter o programa leve.

## Desafio 2
Quando um novo documento chega, o programa percorre a fila e o "encaixa" no lugar certo. Se ele for muito importante (prioridade 1), ele fura a fila até encontrar alguém tão importante quanto ele ou chegar no início.
Se dois documentos têm a mesma prioridade, o código garante que o que chegou primeiro fique na frente (usando o símbolo <= na comparação),Como a fila já está organizada por importância no momento da entrada, na hora de imprimir basta retirar sempre quem está no início.
