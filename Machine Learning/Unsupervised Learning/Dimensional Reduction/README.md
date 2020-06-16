<img src="https://i.ibb.co/DtHQ3FG/802x265-Logo-GT.png" width="500">


## Grupo Turing
# Dimensional Reduction


- **Resumo**:
 A tarefa dos algoritmos para Redução de Dimensionalidade é encontrar relações entre as variáveis do seu banco de dados, podendo assim diminuir o número de variáveis do problema. O algoritmo mais conhecido é o PCA.

- **Teoria**:
A análise de dados de grande dimensão busca identificar e eliminar redundâncias e, para isso, deve-se utilizar métodos/técnicas capazes de:

    * Estimar o número de variáveis ocultas.

    * Criar uma nova representação dos dados a fim de reduzir sua dimensão

    * Criar uma nova representação dos dados a fim de recuperar variáveis ocultas.

    Os algoritmos existentes para redução de dimensão atendem um ou dois itens dessa lista, nenhum consegue cumprir todos. Devido a tal limitação, costuma-se a utilizar dois ou três métodos combinados para tentar cumpri-los. 
    Cada técnica/método também possui algumas características que possuem um papel significante:

    * O modelo assumido dos dados.
    * O tipo de algoritmo que identifica os parâmetros do modelo.
    * A critéria a ser otimizada, que guia o algoritmo.

    Vamos falar sobre os critérios. O critério talvez mais importante é o erro de construção, como segue abaixo:


    <img src="https://imgur.com/TNOpiAS.png" width="500">  

    Onde que E{ } é o operador Esperança e dec e cod são funções de decodificação e codificação, respectivamente, definidas como:

    <img src="https://imgur.com/TyvsMzk.png" width="500">  


	Existem outros critérios, como o estatístico, que procura alguma projeção que preserve a variância observada inicialmente nos dados brutos. Se o objetivo for separar as variáveis ocultas, o critério pode ser a descorrelação; se o objetivo for preservar sua estrutura, a projeção deve manter as distâncias medidas no dados inicialmente.




- **Links**:
    - [Documentação so scikit learn sobre algoritmos de Dimensional Reduction](https://scikit-learn.org/stable/modules/unsupervised_reduction.html)
    - ["A beginner’s guide to dimensionality reduction in Machine Learning"](https://towardsdatascience.com/dimensionality-reduction-for-machine-learning-80a46c2ebb7e)
    - [Turing Talk sobre Dimensional Reduction](https://medium.com/turing-talks/aprendizado-n%C3%A3o-supervisionado-redu%C3%A7%C3%A3o-de-dimensionalidade-479ecfc464ea)


---
**Grupo Turing**  
Grupo de Extensão da Universidade de São Paulo (USP)

[Email](mailto:turing.usp@gmail.com)   
[Facebook](https://www.facebook.com/grupoturing.usp)  
[Medium](https://www.medium.com/turing-talks)  
[LinkedIn](https://www.linkedin.com/company/grupo-turing)

