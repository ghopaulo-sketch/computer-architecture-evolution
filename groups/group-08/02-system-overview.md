# 2. QP1 -  Como a CPU interpreta o CISC?

## 2.1 Ciclo de Execução da CPU

Fetch — Paulo

Decode - A decodificação é uma etapa fundamental na arquitetura CISC, pois é responsável por interpretar as instruções recebidas pela CPU. Ela identifica o código da instrução, os registradores envolvidos, os dados e os modos de endereçamento. A partir dessa interpretação, a unidade de controle determina quais operações e sinais de controle devem ser enviados para os componentes do processador. Como a CISC possui muitas instruções e formatos diferentes, essa etapa pode ser mais complexa. Portanto, a decodificação  é essencial para transformar a instrução em ações que a CPU consiga executar corretamente. 

Micro-ops e Controle Interno — Após a instrução ser decodificada, a CPU divide a instrução CISC em pequenas operações internas chamadas micro-ops. Essas micro-operações são executadas em sequência para realizar a tarefa completa.
O controle interno é responsável por organizar e controlar essas etapas, enviando sinais para os registradores, memória e ULA (Unidade Lógica e Aritmética).

Write back / Gravação do resultado -  Depois da execução, o resultado é colocado no destino definido pela instrução, como um registrador ou uma posição de memória. No exemplo ADD AX, [1000h], o resultado da soma é colocado em AX. 

Execute — As unidades de execução realizam as operações necessárias, como cálculos, movimentação de dados ou acesso à memoria. Como a instrução é complexa, esse processo costuma exigir múltiplos ciclos de clock.


**Exemplo Prático**:
Exemplo ADD AX, [1000h], o resultado da soma é colocado em AX.

Considere a instrução ADD AX, [1000h]. Ela representa a soma do valor armazenado na posição de memória indicada com o conteúdo do registrador AX. AX = 10 Memória[1000h] = 5 

1. A CPU busca a instrução.
2. Decodifica a operação ADD e identifica AX e a referência à memória.
3. Organiza as operações internas necessárias.
4. Obtém o valor 5 da memória.
5. Executa 10 + 5 = 15
6. Grava o resultado em AX. Resultado: AX = 15.

