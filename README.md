# Trabalho de Grafos: Flood Fill com DFS 

Este projeto tem como objetivo implementar o algoritmo Flood Fill utilizando exclusivamente a abordagem recursiva DFS (Depth-First Search) em Python. A ideia central é modificar uma região de uma imagem 1000x1000 pixels, substituindo a cor original por uma nova cor, considerando os 8 vizinhos (acima, abaixo, esquerda, direita e as diagonais).

## Descrição do Problema

Dada uma imagem representada por uma matriz 2D de inteiros (cada inteiro representa o valor de um pixel), o algoritmo deve:
- Receber as coordenadas do pixel inicial (sr, sc).
- Alterar a cor do pixel inicial e de todos os pixels conectados (8-direcionalmente) que possuem a mesma cor, substituindo-os por uma nova cor.
- Realizar a operação utilizando **exclusivamente recursão** para percorrer os pixels.

## Abordagem e Algoritmo

Para solucionar o problema, utilizamos uma função recursiva DFS para explorar todos os pixels conectados com a cor original:
1. **Verificação Inicial:**  
   Se o pixel inicial já possui a nova cor, nenhuma ação é necessária.
2. **Função DFS:**  
   A função recursiva realiza as seguintes verificações:
   - Confirma se o pixel atual está dentro dos limites da imagem.
   - Verifica se o pixel possui a cor alvo (cor original que deve ser alterada).
   - Caso as condições sejam satisfeitas, altera a cor do pixel e chama recursivamente a DFS para cada um dos 8 vizinhos:
     - Vizinhos em linha (cima, baixo, esquerda, direita) e diagonais (superior-esquerda, superior-direita, inferior-esquerda, inferior-direita).
3. **Tratamento de Borda:**  
   A verificação dos limites da matriz impede que a recursão acesse índices inválidos.

## Requisitos

- **Linguagem de Programação:** Python
- **Entrada:** Um arquivo ou função que forneça uma matriz 1000x1000 representando a imagem.
- **Saída:** A imagem modificada após a aplicação do algoritmo.

