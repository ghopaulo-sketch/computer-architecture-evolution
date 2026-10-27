QP3 - Quais são os principais registradores do CISC?

*Registradores*: Os registradores são pequenas unidades de memória internas ao processador, com acesso muito mais rápido que a memória principal. Em arquiteturas CISC (como a x86), eles costumam ser organizados em categorias, cada uma com uma função específica na execução das instruções.

*Registradores de Propósito Geral*: Armazenam dados e endereços usados nas operações aritméticas, lógicas e de movimentação de dados. No x86 de 32 bits, os principais são EAX (acumulador), EBX (base), ECX (contador), EDX (dados), ESI (índice de origem) e EDI (índice de destino). Em geral, cada um tem funções preferenciais em certas instruções (por exemplo, o ECX como contador em laços).

*Registradores de Ponteiro de Pilha e Base*: O ESP (Stack Pointer) aponta para o topo da pilha e é alterado automaticamente pelas instruções PUSH e POP. O EBP (Base Pointer) serve de referência para acessar parâmetros e variáveis locais de uma sub-rotina.

*Registradores de Controle e Estado*: O EIP (Instruction Pointer, equivalente ao Program Counter) guarda o endereço da próxima instrução a ser executada. O EFLAGS (registrador de flags) guarda indicadores como Zero, Carry, Sign e Overflow, que refletem o resultado da última operação e são usados em desvios condicionais.

*Registradores de Segmento*: CS (código), DS (dados), SS (pilha), ES, FS e GS ajudam a organizar o acesso à memória em segmentos.

Fontes: Livro: Arquitetura e Organização de Computadores: Projetando para o Desempenho — William Stallings e Instituto de Matemática e Estatística da USP (IME-USP) Arquitetura de Computadores - https://eaulas.usp.br/portal/course.action?course=33377
