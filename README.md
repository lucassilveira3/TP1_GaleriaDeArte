# Trabalho Prático 1
## Problema da Galeria de Arte

### 1.	Modelagem Computacional
Após a leitura e pesquisa sobre o assunto do trabalho, foi possível perceber o que seria necessário para implementar e conseguir resolver a parte sobre triangulação Ear-Clipping e, posteriormente, a 3-Coloração. Utilizando conceitos vistos em aula, além de pequenas ideias encontradas em artigos.

### 2.	Implementação
O programa foi desenvolvido na linguagem Python (por meio dos Jupyter Notebook) e a plotagem foi realizada utilizando Holoviews.
#### 2.1.	Estruturas de Dados
As estruturas de dados utilizadas foram listas e arrays (amplamente utilizados em Python, por se tratar de uma estrutura mais simples de se manipular.
#### 2.2.	Triangulação Ear-Clipping
Para realizar o Ear-Clipping, foram utilizadas algumas funções relacionadas a Geometria:
•	Produto Vetorial: verificação dos ângulos (maiores ou menores que 180º);

•	Área do triângulo: verificação se o ponto se encontrava dentro do triângulo;

•	Cálculo do ângulo interior: base da função para procurar as ear tips;
#### 2.2.1.	Função verificaEar
A função que procura e remove as ear tips funciona da seguinte forma:
•	Procurar a ear tip com menor ângulo;

•	Formar um triângulo com os vértices (Vi-1, Vi, Vi+1);

•	Remover o vértice Vi;

•	Atualizar as conexões entre os vértices e os status das ear tips restantes;

A função é executada diversas vezes, até restar apenas um triângulo (três vértices finais).
#### 2.3.	3-Coloração
A coloração dos vértices foi uma etapa mais complicada que a triangulação, porém ela foi realizada por meio da utilização dos vértices adjacentes e do algoritmo DFS (Depth-First Search).
#### 2.3.1.	Algoritmo DFS (Depth-First Search)
Após uma adaptação no algoritmo DFS, que antes realizava a busca em grafos, a coloração ficou mais simples. A DFS ou busca em profundidade, funciona em conjunto com os vértices adjacentes, buscando os vértices que não estão coloridos e que não fazem adjacência com outro vértice colorido da mesma cor.

Portanto, após colorir um vértice de vermelho, a função vai colorir outros vértices que, em conjunto, formam um triângulo. Sempre buscando evitar que vértices adjacentes sejam coloridos da mesma cor, a função é executada até todos os vértices estarem coloridos (ou até todos os triângulos possuírem as três cores em seus vértices).

### 3. Execução
Para executar o programa, deve-se inserir os vértices do polígono em ordem anti-horária e apenas executar todas as células do notebook.

### 4.	Conclusão
Por fim, destaco a importância de se aprender e saber utilizar os algoritmos geométricos, como também a manipulação de sequências. O trabalho prático em si teve suas complicações, porém, no fim, tudo se encaixou e funcionou corretamente.

## Referências
https://www.geometrictools.com/Documentation/TriangulationByEarClipping.pdf

https://arxiv.org/ftp/arxiv/papers/1212/1212.6038.pdf#:~:text=The%20ear%20clipping%20triangulation%20algorithm,newly%20formed%20triangle%20is%20valid

https://github.com/mrbaozi/triangulation

https://pt.wikipedia.org/wiki/Busca_em_profundidade
