<img src="https://i.ibb.co/DtHQ3FG/802x265-Logo-GT.png" width="500">

## Grupo Turing
# Decision Tree (Regressão)

- **Resumo**:
Como dito no texto da árvore da parte de decision tree, esse modelo funciona a partir de divisões binárias do dataset em subcategorias de elementos mais “parecidos” entre si. Sendo a diferença entre o algoritmo de classificação e o de regressão a predição feita, na regressão é predito um valor enquanto na classificação uma categoria.


Exemplo:

<img src="https://imgur.com/euctHYr.png" width="500">

Mas o que se ganha com maior semelhança entre os dados? A resposta é um maior conhecimento sobre aquele dataset observado. Pode-se dizer, portanto, que o objetivo das separações ou cortes é obter um Ganho de Informação


<img src="https://imgur.com/bdbtF5h.png" width="500">


**E qual a definição de Ganho de Informação (IG)?**

O IG é o quanto aprendemos/podemos tirar de informação com base na feature utilizada para a separação. Sendo o objetivo do modelo a maximização desse aprendizado sobre o dataset.

Sua definição matemática para o uso na modelagem é a seguinte:


                                       IG = H(x) - H(x|a)


Sendo: 
*  H(x) a entropia do nó pai ou estado atual, definido por:

                H(x) = - ∑i=1 p(x)*log2p(x), sendo p(x) a proporção de exemplos em relação a todo o conjunto

* H(x|a) a entropia dos nós gerados ou próximo estado, definido por:

                 H(x|a) = W(L)*H(L) + W(R)*H(R), sendo W peso do nó que é igual ao número de elementos sobre o número de elementos do nó pai , H a entropia do nó filho, L o nó esquerdo e R o nó direito

**E como o Regression Tree usa o IG?**

O uso de IG para otimizar a árvore é computacionalmente caro e não prático para resultados rápidos, por isso, os modelos de predição usam outros parâmetros relacionados ao ganho de informação, mais versáteis para seus objetivos. A árvore de classificação costuma usar o próprio conceito de entropia ou um conceito de estatística chamado índice Gini. Porém a Regressão utiliza medidas mais adequada para seu uso numérico, usualmente elas envolvem o termo (y - ŷ)² (onde ŷ é a média dos targets dos elementos pertencentes ao dataset analisado), sendo a mais comum o erro quadrático médio, que é dado por:


                                       MSE = (1/n)*∑i=1(yi-ŷi)²

**Como construir uma árvore de regressão?**

Criar uma árvore de decisão é, em suma, criar um método recursivo de dividir datasets em 2. Para isso é usado um método chamado divisão binária (binary splitting), que nesse contexto só significará uma divisão em 2 grupos, e um algoritmo ganancioso (greedy).

O algoritmo testa todas as opções de divisões possíveis (o que só é alcançável devido a divisão binária) e checa qual tem o maior MSE. DEfinido o corte mais eficiente ele é aplicado e o processo se repete nos nós filhos.

É importante notar que o algoritmo ganancioso não gera necessariamente a opção ótima, pois um corte menos eficiente num processo pode levar a um melhor corte em seguida. Porém seus resultados são rápidos e muito próximos do melhor, motivo suficiente para ser usado.

É importante também ter  noção de que, quando parar a recursão. Existem diversos parâmetros usados para definir o tempo de parada, incluindo hiperparâmetros como a profundidade da árvore. A decisão do que usar e quando parar cabe ao criador mas existem alguns padrões de criação com seus motivos.
	
Os motivos são, em geral, ligados ao fato de que árvores muito grandes tendem a se adaptar ao ruído do dataset e perder sua capacidade produtiva.

Entre os critérios de parada mais usados estão:

* Determinar um máximo de nós
* Determinar um mínimo de elementos em nós pais ou filhos para os cortes
* Deixar a árvore se dividir até todos os elementos de um dataset terem o mesmo target ou só haver 1 elemento no dataset e fazer uma poda (prunning) para evitar sobre-ajuste

**Processo de Poda**

A capacidade de predição da árvore pode ser melhorada ainda mais a partir de um método chamado poda (prunning). Ele consiste em retirar os galhos que trazem pouco ganho de informação ao modelo, a partir disso diminuir a complexidade da árvore e, por conseguinte, diminuir o sobre-ajuste.

As regras da poda são :
* Parar quando o número de folhas for menor que um limite
* Parar quando a medida de erro das folhas forem menor que o limite
* Parar quando o número de elementos em cada folha for menor que um limite

**Decision Tree Regression em Python**

<img src="https://imgur.com/EXeWyTd.png" width="500">

Esse é um exemplo bem simples e recomenda-se que olhe as documentações anexadas nos links para maiores detalhes.

- **Links Úteis**:
    - [Lecture de Harvard sobre o assunto](http://www.stats.ox.ac.uk/~flaxman/HT17_lecture13.pdf)
    - [Decision Tree. It begins here.](https://medium.com/@rishabhjain_22692/decision-trees-it-begins-here-93ff54ef134)
    - [Explicação detalhada sobre Information Gain](https://www.thelearningmachine.ai/tree-id3)
    - [Using Decision Trees for Regression Problems](https://acadgild.com/blog/using-decision-trees-for-regression-problems)

---
**Grupo Turing**  
Grupo de Extensão da Universidade de São Paulo (USP)

[Email](mailto:turing.usp@gmail.com)   
[Facebook](https://www.facebook.com/grupoturing.usp)  
[Medium](https://www.medium.com/turing-talks)  
[LinkedIn](https://www.linkedin.com/company/grupo-turing)
