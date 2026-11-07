QP5 - O que mudou do 8086 para o x86-64 atual?

*Contexto*: O 8086, lançado pela Intel em 1978, foi o primeiro processador da família x86 e deu nome a ela. Era um processador de 16 bits. Desde então a arquitetura evoluiu em três grandes etapas: 16 bits (8086, 1978), 32 bits (80386, 1985) e 64 bits (x86-64, proposto pela AMD em 2003 e depois adotado pela Intel). Em todas elas foi mantida a compatibilidade com o código antigo, e por isso o x86 atual ainda carrega marcas do 8086.

*Tamanho dos registradores*: No 8086 todos os registradores tinham 16 bits: AX, BX, CX, DX (propósito geral), SI, DI (índice), BP, SP (ponteiros), além dos registradores de segmento CS, DS, SS, ES, do IP e do FLAGS. No 80386 eles foram estendidos para 32 bits (EAX, EBX, ..., EIP, EFLAGS). No x86-64 foram estendidos novamente para 64 bits, com nomes iniciados em "R" (RAX, RBX, RSP, RIP, RFLAGS). Os registradores antigos continuam acessíveis em partes menores (RAX, EAX, AX, AL).

*Quantidade de registradores*: O x86-64 passou de 8 para 16 registradores de propósito geral, com a adição de R8 a R15. Isso reduz o acesso à memória e facilita a passagem de parâmetros em registradores nas chamadas de função.

*Endereçamento de memória*: O 8086 tinha barramento de endereços de 20 bits e acessava até 1 MB de memória. Como os registradores tinham só 16 bits, a memória era dividida em segmentos de 64 KB e o endereço era formado por um par segmento:offset. O 80386 passou a oferecer endereçamento de 32 bits (4 GB) e o chamado *flat addressing*. O x86-64 usa endereços virtuais de 64 bits, com limite teórico de 16 EB. Os processadores atuais implementam bem menos que isso, na casa de 1 TB em muitos modelos.

*Modos de operação*: O 8086 tinha um único modo de funcionamento (modo real). O 80286 introduziu o modo protegido, com gerenciamento de memória mais avançado, e o 80386 incluiu o modo virtual-8086. O x86-64 trouxe o *long mode*, com um submodo de 64 bits e um *modo de compatibilidade* para executar aplicações de 32 bits. Processadores atuais ainda conseguem iniciar em modo real, como um 8086.

*Segmentação e modos de endereçamento*: No x86-64, a segmentação foi praticamente abandonada em favor de um espaço de endereçamento plano (os registradores FS e GS permanecem para usos específicos). Os modos de endereçamento ficaram mais regulares com o formato base + índice × escala + deslocamento, enquanto o 8086 tinha combinações mais restritas de registradores.

*Outras evoluções*: Os processadores modernos também ganharam memória cache, execução fora de ordem, múltiplos núcleos (a partir do Core 2, 2006) e instruções para multimídia (SIMD). Internamente, as instruções complexas do x86 são decompostas em operações mais simples, de modo semelhante ao RISC. Já o conjunto de instruções externo continua sendo CISC e compatível com o legado.

Fontes:
- Intel x86 Assembly, material de aula (KAIST) - https://softsec.kaist.ac.kr/depot/sangkilc/is561/03-assembly.pdf
- x86 segment registers in protected mode (Tech-Juice) - https://tech-juice.org/2011/08/27/x86-segment-registers-in-protected-mode/
- x64 vs. x86: Key Differences Explained (phoenixNAP) - https://phoenixnap.com/kb/x64-vs-x86
