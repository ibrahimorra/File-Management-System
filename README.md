# File-Management-System

# Trabalho de CC6270 - Sistemas Operacionais

Sumário:
========

- [Grupo](#grupo)
- [Desenvolvimento](#desenvolvimento)
- [Entrega 1](#entrega-1)
- [Entrega 2](#entrega-2)
- [Entrega 3](#entrega-3)
- [Entrega 4](#entrega-4)
- [Entrega 5](#entrega-5)

# Grupo

|  Nome  |  R.A.  |
|  :---: |  :---: |
| Ibrahim Jamil Orra | 22.118.183-7 |
| Matheus Elias Cruz | 22.118.167-0 | 
| Pedro Henrique Silva Domingues  |  22.218.019-2  |
| Renan Martins | 22.118.025-0 |

# Desenvolvimento

Entregas realizadas:

- [x] Entrega 1
- [ ] Entrega 2 - falta thread e escalonamento
- [x] Entrega 3
- [x] Entrega 4
- [ ] Entrega 5

Organização detalhada dos processos realizados:
https://www.notion.so/Projeto-de-SO-b13890863847466e944f07cd94aa6080

# Entrega 1

__Tema__: Sistema de gerenciamento de arquivos

__Sistema Operacional__: Ubuntu

- Paralelo;
- Monousuario e multiusuario;
- Multitarefa; 
- Multiprocessado;
- Opera em lotes (batch).

__Hardware__: 

- Desktop AMD Ryzen 5 3400g 
- Colorful B550m Gaming Pro 
- 16 gb RAM DDR4 
- 1Tb Hard Disk 
- 500wats de potência

# Entrega 2

* _Processo_:

Um processo pode ser qualquer programa em execução. Uma entidade ativa que carrega atributos como memoria, estado do hardware e um id chamado de PID.
Processos possuem estados, os quais são:

__NEW__ - Está em estado de criação;

__READY__ - Está aguardando para ser direcionado a uma unidade de processamento;

__RUNNING__ - Suas instruções estão sendo executadas;

__WAITING__ - Em aguardo por um evento, como por exemplo uma entrada/saída de dados;

__TERMINATED__ - Sua execução foi finalizada;

* _Thread_:

threads são fluxos que ocorrem em paralelo dentro de um mesmo processo, cada uma possuindo seu próprio pc (Program Counter) para gerenciar quais instruções devem ser executadas a seguir. Assim como memoria para armazenamento de variáveis e uma pilha de execução para o histórico de execução.

* _Escalonamento de processo_:

Escalonamento de processos é a um susbsistema do sistema operacional, o qual decida qual processo poderá fazer o uso da cpu em um dado momento. Os algoritmos aplicados a este são responsáveis por todo o gerenciamento desta logistica.

----

Alguns exemplos de algoritmos de gerenciamento de processos são: Algoritmo do barbeiro e Jantar dos filósofos.

- algoritmo do barbeiro
	- Imagine uma barbearia (memória ram)
	- A barbearia recebe clientes (processos)
	- Se não há clientes, o barbeiro adormece 
	- Se a cadeira do barbeiro estiver livre o cliente vai ser atendido
	- O cliente espera pelo barbeiro se houver uma de espera vazia
	- Se não tive onde sentar, o cliente vai embora.

- algoritmo jantar dos filosofos
	- Uma mesa com cinco filósofos
	- Cada filosófo precisa de dois hashis para comer
	- Eles vão precisar compartilhar os hashis
	- Vão precisar considerar os hashis livres para poderem usar


No nosso projeto aplicaremos estes conhecimentos da seguinte forma:
1. Todo código que estiver rodando será um processo, independente de sua funcionalidade.
2. Threads serão utilizadas para gerenciar tarefas em plano de fundo enquanto o usuário permanece podendo utilizar a interface.
3. Não faremos uso direto de Escalonamento de processo, uma vez que o sistema operacional cumprirá todas as necessidades sob este aspecto.

# Entrega 3

Scripts serão aplicados para interagir com os códigos feitos em outras linguagens. Como exemplo, nosso grupo desenvolveu um script de instalação, o qual realiza tarefas como:

- Compilação dos codigos que estiverem na pasta src;
- Organização dos executaveis em uma pasta criada com o nome de "obj";
- Criação da estrutura de pastas na qual o usuário ira interagir;
- ...

# Entrega 4

A manipulação do sistema de arquivos foi realizada dentro do script de instalação, verificando a existencia, criando, removendo e aninhando pastas umas dentro de outras.
