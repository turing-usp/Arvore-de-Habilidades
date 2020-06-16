<img src="https://i.ibb.co/DtHQ3FG/802x265-Logo-GT.png" width="500">

## Grupo Turing
# PCA

**Resumo**:
PCA é um algoritmo linear de redução de dados, ele tenta manter a variância entre os dados como critério para selecionar novas variáveis.

**Teoria**
Principal Components Analysis (PCA) é um algoritmo de Redução de Dimensionalidade simples e poderoso. Existem duas formas de aplicar o PCA: uma utilizando SVD (Singular Value Decomposition) e outra utilizando a Matriz de Covariância. A tabela a seguir mostra a principal diferença das duas formas:

|              | SDV                                                                             |                             Matriz de Covariância                            |   |   |
|--------------|---------------------------------------------------------------------------------|:----------------------------------------------------------------------------:|---|---|
| Vantagens    | Utiliza todos os dados de forma direta para calcular os componentes principais. | Baixo custo computacional.                                                   |   |   |
| Desvantagens | Maior custo computacional.                                                      | Utiliza apenas os dados de forma indireta (através da Matriz de Covariância. |   |   |
|              |                                                                                 |                                                                              |   |   |

Essa técnica busca encontrar uma nova representação de dados tal que a variância dessa nova representação seja mantida comparado aos dados iniciais. Cada componente dessa nova representação possui uma quantidade de informação dele (proporcional a variância) e a redução de dimensionalidade ocorre quando se descarta os Componentes de menor importância (i.e. menor informação/variância), restando apenas os Componentes Principais.

- **Links**:
    - [Turing Talks: Aprendizado Não Supervisionado | Redução de Dimensionalidade](https://medium.com/turing-talks/aprendizado-n%C3%A3o-supervisionado-redu%C3%A7%C3%A3o-de-dimensionalidade-479ecfc464ea)
    - [Machine Learning — Singular Value Decomposition (SVD) & Principal Component Analysis (PCA)](https://medium.com/@jonathan_hui/machine-learning-singular-value-decomposition-svd-principal-component-analysis-pca-1d45e885e491)
    - [Foundations of Machine Learning : Singular Value Decomposition (SVD)](https://medium.com/the-andela-way/foundations-of-machine-learning-singular-value-decomposition-svd-162ac796c27d)
    - [PCA: Application in Machine Learning](https://medium.com/apprentice-journal/pca-application-in-machine-learning-4827c07a61db)


---
**Grupo Turing**  
Grupo de Extensão da Universidade de São Paulo (USP)

[Email](mailto:turing.usp@gmail.com)   
[Facebook](https://www.facebook.com/grupoturing.usp)  
[Medium](https://www.medium.com/turing-talks)  
[LinkedIn](https://www.linkedin.com/company/grupo-turing)

