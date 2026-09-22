# 2. QP1 -  Como a CPU interpreta o CISC?

## 2.1 Ciclo de Execução da CPU

Fetch — Paulo

Decode — Jose Vitor

Micro-ops e controle interno  - João Gabriel

Execute — Vitor Hugo

No exemplo ADD AX, [1000h], o resultado da soma é colocado em AX.

Considere a instrução ADD AX, [1000h]. Ela representa a soma do valor armazenado na posição de memória indicada com o conteúdo do registrador AX. AX = 10 Memória[1000h] = 5 1. A CPU busca a instrução. 2. Decodifica a operação ADD e identifica AX e a referência à memória. 3. Organiza as operações internas necessárias. 4. Obtém o valor 5 da memória. 5. Executa 10 + 5 = 15. 6. Grava o resultado em AX. Resultado: AX = 15.
