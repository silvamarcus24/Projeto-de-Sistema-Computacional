## Marcus Vinicius 
## Guilherme Montenegro
## Matheus Cavalcante
## Gustavo Saurim

# Projeto-de-Sistema-Computacional
# ADR 001 – Implementação do Sistema de Playlist com Arquivo TXT em Linguagem C 🔊

## Contexto
O projeto propõe a criação de um sistema de montagem automática de playlists musicais personalizadas. O sistema deve permitir a entrada de dados pelo usuário (nome da música, gênero, duração), armazená-los em um arquivo `.txt`, e gerar uma playlist com base no gênero desejado e no tempo total máximo informado.

## Decisão
A implementação será feita em **linguagem C**, com leitura e escrita de músicas em um **arquivo de texto** (`banco.txt`).  
O sistema buscará músicas no gênero escolhido e montará a playlist de forma sequencial até atingir o tempo máximo estipulado.

## Justificativas
- A linguagem C permite prática com entrada de dados, manipulação de arquivos e controle de fluxo.
- Uso de `.txt` facilita o armazenamento simples e reutilizável de dados.
- Permite simular um banco de dados básico sem uso de bibliotecas externas.
- O filtro por gênero e tempo estimula a lógica de seleção e controle acumulativo.

## Consequências
- Dados já existentes no `.txt` serão considerados na montagem da playlist.
- O sistema precisa validar os dados inseridos para evitar quebras na estrutura do arquivo.
- A leitura do arquivo deverá converter os dados em estruturas temporárias para filtragem e seleção.
- A playlist será composta por músicas ordenadas por entrada (ou pode ser aprimorado para ordenações específicas depois).

  ----

## Detalhamento das Escolhas da Arquitetura do Projeto

### (a) Quais as features que serão implementadas?
- Entrada de dados pelo usuário (nome da música, gênero, duração).
- Armazenamento das informações em um arquivo de texto (`banco.txt`).
- Leitura e conversão dos dados em estruturas temporárias (arrays ou structs).
- Filtro de músicas por gênero e tempo máximo total.
- Geração de playlist automaticamente com base nos critérios informados.
- Validação dos dados de entrada para garantir integridade da estrutura do arquivo.

### (b) Como será feito o armazenamento no banco do usuário?
- O "banco de dados" será um **arquivo `.txt`**, que armazenará as músicas em formato estruturado.
- Cada linha do arquivo conterá os dados de uma música: nome, gênero e duração.

### (c) Como será feita a comunicação entre o front-end e o back-end? E o banco de dados?
- O sistema será **monolítico** e **local**, o Front-end vai ser no próprio terminal do CodeBlocks contendo o "Menu" e vai ser lá que o usuário vai entrar com os dados. Já o Back-end seria o próprio programa C, que processa a lógica, manipula dados e responde às entradas do usuário na mesma aplicação.
- Toda interação ocorrerá via terminal (entrada e saída padrão).
- O "banco de dados" é acessado diretamente pelo programa em C como um arquivo `.txt`, sem intermediários.

