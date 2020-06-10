<img src="https://i.ibb.co/DtHQ3FG/802x265-Logo-GT.png" width="500">

## Grupo Turing
# Ensemble Learning: Bagging

## 1-Introdução
	
Bagging é um método de ensemble learning que utiliza bootstrapping, criação de modelos em paralelo e sua agregação para montar um modelo definitivo, o que justifica seu nome: “bootstrap aggregating”. O objetivo de usá-lo é diminuir a variância dos modelos bases, os quais, normalmente, são Decision Trees com grandes profundidades.

## 2-Bootstrapping, o conceito base

Bootstrap consiste na técnica de tirar várias amostras de um conjunto de dados e usá-las para tirar informações sobre o conjunto todo como média e desvio padrão. Nós, porém, usaremos essa técnica para melhorar nossas predições. Um detalhe importante do bootstrapping é que toda amostra nova retirada retorna alguns dos seus componentes ao grupo original e troca por outros, isso é chamado amostragem com retorno (é possível retirar a mesma   observação mais de uma vez).

O processo pode ser explicado nas seguintes etapas:
* Escolher o número de amostras para fazer
* Escolher o tamanho da amostra
* Para cada amostra, retirar (com retorno) com o tamanho definido e calcular suas estatísticas
* Calcule as médias das estatísticas de todas as amostras montadas

## 3-Explicação do funcionamento

De acordo com o artigo “Bagging Predictors” escrito por Leo Breiman em 1994, modelos de bagging são métodos para gerar múltiplas versões de um preditor e usar esses de forma agregada para construir um mais forte.

Consideremos um dataset de N observações independentes, o objetivo é, a partir de datasets menores de combinações desses N, construir um modelo melhor do que seria construído com o conjunto todo somente.

Se o retorno dos modelos é uma informação numérica então o procedimento adotado é a média. Se o retorno dos modelos é uma classificação então o método de agregação é uma votação.

O processo de criação pode ser resumido assim:

* Escolher o número de amostras a serem feitas
* Escolher o tamanho das amostras
* Tirar as amostras com retorno e treinar os modelos nelas
* Aplicar todos os modelos ao dataset que se deseja fazer uma previsão
* Tirar a média das previsões, esta será a previsão final

Esse processo também pode ser usado para checar o quanto um modelo é bom apenas mudando um pouco os passos finais. Faz-se uma avaliação dos modelos numa base de teste e tira-se a média das estatísticas obtidas, assim chegando a uma conclusão sobre o modelo em si.

## 4-Aplicação

O mais importante a se considerar quando usar essa técnica de ensemble learning é se o modelo base é instável. Ser instável significa que uma pequena alteração no dataset de treino gera grandes mudanças nas previsões feitas pelo modelo. É mais um motivo pelo qual árvores de decisão são comumente usadas dessa forma. 

É importante notar que bagging funciona com bons preditores, enquanto com os ruins, pode piorar ainda mais  o resultado.

## 5-Desvantagens

* Perda da facilidade de interpretação (o modelo final não é o modelo base e por isso não é tão fácil interpretá-lo)
* Complexidade computacional (os múltiplos modelos base ao mesmo tempo são computacionalmente caros)

## 6-Código
 
* [Construção desde a base de um modelo com bagging em python](https://machinelearningmastery.com/implement-bagging-scratch-python/)

* [Exemplo de Bagging para classificação](https://www.geeksforgeeks.org/ml-bagging-classifier/)

* [Exemplo de Bagging para Regressão no fim do post](https://medium.com/turing-talks/turing-talks-24-modelos-de-predi%C3%A7%C3%A3o-ensemble-learning-aa02ce01afda)

* [Mexer com Random Forest e seus hiperparâmetros](https://medium.com/turing-talks/turing-talks-18-modelos-de-predi%C3%A7%C3%A3o-random-forest-cfc91cd8e524)


## 7-Inspiração do texto

* [Texto que dá uma análise mais matemática por trás da técnica](https://www.stat.cmu.edu/~ryantibs/datamining/lectures/24-bag.pdf)

* Artigo muito famoso de 1994 sobre Bagging: "[Bagging Predictors" de Leo Breiman](https://link.springer.com/content/pdf/10.1023%2FA%3A1018054314350.pdf)

- **Turing Talks**:
    - [TURING TALK - Random Forest](https://medium.com/turing-talks/turing-talks-18-modelos-de-predi%C3%A7%C3%A3o-random-forest-cfc91cd8e52)

    - [TURING TALK - Ensamble Learning](https://medium.com/turing-talks/turing-talks-24-modelos-de-predi%C3%A7%C3%A3o-ensemble-learning-aa02ce01afda)


---
**Grupo Turing**  
Grupo de Extensão da Universidade de São Paulo (USP)

[Email](mailto:turing.usp@gmail.com)   
[Facebook](https://www.facebook.com/grupoturing.usp)  
[Medium](https://www.medium.com/turing-talks)  
[LinkedIn](https://www.linkedin.com/company/grupo-turing)

