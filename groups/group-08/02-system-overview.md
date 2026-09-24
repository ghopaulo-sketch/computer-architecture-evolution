# 2. QP1 -  Como a CPU interpreta o CISC?

## 2.1 Ciclo de Execução da CPU

Fetch — Paulo

Decode — Jose Vitor

# Micro-ops e Controle Interno
Após a instrução ser decodificada, a CPU divide a instrução CISC em pequenas operações internas chamadas micro-ops. Essas micro-operações são executadas em sequência para realizar a tarefa completa.
O controle interno é responsável por organizar e controlar essas etapas, enviando sinais para os registradores, memória e ULA (Unidade Lógica e Aritmética).

Exemplo: ADD AX, [1000h]
Se AX = 10 e a posição de memória [1000h] = 5, a CPU:

1. Busca o valor 5 na memória.
2. Envia os valores de AX e da memória para a ULA.
3. A ULA realiza a soma (10 + 5).
4. O resultado, 15, é gravado novamente no registrador AX.

Assim, uma única instrução CISC é executada por meio de várias operações internas coordenadas pelo controle da CPU.

Execute — As unidades de execução realizam as operações necessárias, como cálculos, movimentação de dados ou acesso à memoria. Como a instrução é complexa, esse processo costuma exigir múltiplos ciclos de clock.


No exemplo ADD AX, [1000h], o resultado da soma é colocado em AX.

Considere a instrução ADD AX, [1000h]. Ela representa a soma do valor armazenado na posição de memória indicada com o conteúdo do registrador AX. AX = 10 Memória[1000h] = 5 1. A CPU busca a instrução. 2. Decodifica a operação ADD e identifica AX e a referência à memória. 3. Organiza as operações internas necessárias. 4. Obtém o valor 5 da memória. 5. Executa 10 + 5 = 15. 6. Grava o resultado em AX. Resultado: AX = 15.

teste
