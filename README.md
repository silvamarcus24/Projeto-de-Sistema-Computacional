# Projeto-de-Sistema-Computacional
# ADR 001 – Implementação do Sistema de Playlist com Arquivo TXT em Linguagem C

## Status
Aceita

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
