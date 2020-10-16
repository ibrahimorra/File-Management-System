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
- [x] Entrega 2
- [x] Entrega 3
- [x] Entrega 4
- [x] Entrega 5

Organização detalhada dos processos realizados:
https://www.notion.so/Projeto-de-SO-b13890863847466e944f07cd94aa6080

# Entrega 1

__Tema__: Sistema de gerenciamento de arquivos

__Área do conhecimento__: Nosso grupo propõe a criação de uma aplicação desktop para auxiliar usuários linux a fazer gestão de arquivos, tornando o uso e organização diária de algumas tarefas mais agil. 

Entre esta tarefas, pretendemos implementar:

- Um instalador para facilitar a geração dos executaveis e criação da estrutura na qual o nosso sistema irá interagir;
- Uma agenda para shell, na qual o usuário pode gerenciar e salvar seus contatos;
- Um sistema de backup agendado, no qual o usuário pode inserir uma data para o backup e as pastas que deseja salvar;
- Um sistema de organização de imagens auto-organizado, capaz de gerar uma arvore de diretórios e organizar estas imagens segundo a data de geração.

__Sistema Operacional__: Ubuntu

- Paralelo;
- Monousuario e multiusuario;
- Multitarefa; 
- Multiprocessado;
- Opera em lotes (batch).

Porque escolhemos o sistema operacional Ubuntu:

- É open-source e pode ser rodado nos desktops, ou até mesmo na nuvem, estamos estudando na disciplina de sistemas operacionais, que pode facilitar o desenvolvimento do projeto e nas aplicações dos comandos e conceitos vistos em aula.

__Hardware__: 

- Desktop AMD Ryzen 5 3400g 
- Colorful B550m Gaming Pro 
- 16 gb RAM DDR4 
- 1Tb Hard Disk 
- 500wats de potência

# Entrega 2

* _Processo_:

Um processo pode ser qualquer programa em execução que utilizam um certo espaço de memória em que possam ser executados. Uma entidade ativa que carrega atributos como memoria, estado do hardware e um id chamado de PID (Process IDentification), o UID (User IDentification) e também um GID (Group IDentification).
Processos possuem estados, os quais são:

__NEW__ - Está em estado de criação;

__READY__ - Está aguardando para ser direcionado a uma unidade de processamento;

__RUNNING__ - Suas instruções estão sendo executadas;

__WAITING__ - Em aguardo por um evento, como por exemplo uma entrada/saída de dados;

__TERMINATED__ - Sua execução foi finalizada;



* _Thread_:

Threads são fluxos que ocorrem em paralelo dentro de um mesmo processo, cada uma possuindo seu próprio pc (Program Counter) para gerenciar quais instruções devem ser executadas a seguir. Assim como memoria para armazenamento de variáveis e uma pilha de execução para o histórico de execução. Apesar de cada thread possuir seus proprios recursos, ela é iniciada com uma cópia de seu pai.

No nosso projeto, threads foram implementadas para fazer com que em paralelo a agenda, novo terminal seja aberto e a lista de contatos seja exibida. O código para tal pode ser encontrado em arquivo.c, na função nomeada "mostrar_agenda", aproximadamente linha 106.

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

Scripts são conjuntos de comandos que serão interpretados e utilizado para a realizaço de tarefas. No caso do linux, utilizamos o bash como interpretador shell.

No nosso projeto, scripts serão aplicados para interagir com o âmbiente do usuário, preparando esta para o uso do programa. Ou seja, compilando e movendo arquivos, gerando estruturas de pastas, etc. Em mais detalhes, alguns exemplos ja implementados são:

- Compilação de todos os códigos de linguagem C que estiverem na pasta src, independente do nome;
- Organização dos executaveis em uma pasta criada com o nome de "obj";
- Criação da estrutura de pastas na qual o usuário ira interagir;
- ...

Dentro do script, utilizamos técnicas aprendidas em aula, como loops (para varrer multiplos arquivos e executar o comando de compilação para cada um deles), criação de pastas, movimentação de arquivos, "echos" para interagir com o terminal indicando mensagens relevantes do processo, variáveis que auxiliam ma gestão e dinamismo do cdigo, etc.

# Entrega 4

A principal manipulação do sistema de arquivos foi realizada dentro do script de instalação, verificando a existencia, criando, removendo e aninhando pastas umas dentro de outras.


# Entrega 5

* _Número de partições_:

Estamos utilizando uma única partição para desenvolvermos a aplicação dentro do sistema operacional Ubuntu.

* _Espaço da aplicação_:

O espaço da aplicação é de 16KB, no entanto, na hora da criação da árvore de diretórios e na incrementação de usuários o espaço pode aumentar.

* _Tecnologia da aplicação_:
- UFS - Unix File System

Esse sistema de arquivos é mais conhecido por utilizar a estrutura de arquivos hierárquica, como uma árvore usada na organização dos arquivos e diretórios, dividido nos seguintes blocos abaixo.
	- Boot blocks: Contém informação que são iniciados separadamente do sistema de arquivos.
	- Super block: Contém informação necessária sobre o sistema de arquivos.
	- Cylinder groups: Tem a função de agirem como uma partição ou mini-partição.

* _Ambiente da aplicação_:

A aplicação utilizará apenas uma única partição, no ambiente operacional Ubuntu, portanto, vai ficar tudo na mesma plataforma.

