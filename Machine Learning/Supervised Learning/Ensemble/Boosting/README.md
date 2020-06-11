<img src="https://i.ibb.co/DtHQ3FG/802x265-Logo-GT.png" width="500">

## Grupo Turing
# Ensemble Learning: Boosting

## Introdução
	
Boosting é um tipo de ensemble learning que usa do aprendizado sequencial de
modelos de predição mais fracos, corrigindo os erros dos modelos anteriores, para criar um
mais forte. Seu objetivo é reduzir o alto viés que ocorreria no caso de se usar somente os
modelos fracos, para tal, devem ser usados modelos base com baixa variância e alto viés. O modelo razo mais comumente usado é a árvore de decisão.

## Tipos principais e como funcionam

### Adaboost (Adaptative Boosting)
Adaboost é um algoritmo de boosting que usa árvores de decisão de profundidade 1
chamados tocos (stumps) que serve tanto para classificação quanto para regressão. O primeiro
toco aplica uma divisão e o segundo verifica quais datapoints não foram classificados
corretamentes e aumenta o peso deles na função erro aplicada para que sejam mais
importantes nessa divisão, os corretamente classificados tem peso diminuído e o processo
segue em frente até tudo ser corretamente classificado com a junção desses . Os modelos
também têm pesos de acordo com seu sucesso para determinar sua influência no ensemble
final.

Prós:
* Flexível para ser combinado com outros algoritmos de ML
* Único parâmetro a ser melhorado é o T
* Pode ser usado com dados numéricos ou com texto

Cons:
* Modelos muito fracos podem levar a overfitting
* Algoritmo relativamente antigo e existem outras versões melhores atualmente
* Problemas com noise que é consistente

Exemplo de Classificador:

<img src="https://i.imgur.com/qBFAQ3X.jpg" width="500">

Exemplo de Regressor:

<img src="https://imgur.com/M2mM8Bm.jpg" width="500">


### Gradient Boosting
Assim como o Adaboost esse algoritmo também funciona sequencialmente
porém, ao invés de mudar os pesos dos erros, ele aplica o próximo modelo aos erros do
anterior. Ele utiliza então uma técnica conhecida como Gradient Descent nos parâmetros para os sucessivos modelos. Essa técnica, em linhas gerais, visa encontrar o mínimo global da função perda a partir da atualização dos parâmetros do modelo na direção de suas derivadas parciais.  

Prós:
* Alta performance
* Facilmente melhorado (tuning)
* Simples de programar

Cons:
* Uma pequena mudança na base de treino gera uma grande mudança no modelo
* Não é fácil entender as predições

Exemplo de Regressor:

<img src="https://imgur.com/ezVlCvA.jpg" width="500">

Exemplo de Classificador:

<img src="https://imgur.com/YkAJJl8.jpg" width="500">

<img src="https://imgur.com/HvaL0Qd.jpg" width="500">


### XGBoost (eXtreme Gradient Boosting)

XGboost é uma versão otimizada de gradient boosting usando diversas técnicas de programação, e.g. paralelismo, matriz esparsas e regularização, para agilizar o processamento e diminuir o overfitting.

Prós:
* Regularização
* Processamento em paralelo
* Pode lidar com valores faltantes
* Usa Cross Validation
* Faz um bom Tree Prunning (desconsiderar árvores com baixa importância no modelo)

Cons:
* Pode ser lento
* Pode criar um modelo complexo

Exemplo de Classificador:

<img src="https://imgur.com/ObJhH2x.jpg" width="500">

Exemplo de Regressor:

<img src="https://imgur.com/vpoMfeI.jpg" width="500">

## **Links Úteis**:

* https://towardsdatascience.com/boosting-algorithms-explained-d38f56ef3f30
* https://medium.com/greyatom/a-quick-guide-to-boosting-in-ml-acf7c1585cb5
* https://stats.stackexchange.com/questions/7813adjusting-sample-weights-in-adaboost
* https://www.edureka.co/blog/boosting-machine-learning/
* https://www.datacamp.com/community/tutorials/adaboost-classifier-python
* https://machinelearningmastery.com/boosting-and-adaboost-for-machine-learning/
* https://hub.packtpub.com/ensemble-methods-optimize-machine-learning-models/
* https://www.educba.com/adaboost-algorithm/



---
**Grupo Turing**  
Grupo de Extensão da Universidade de São Paulo (USP)

[Email](mailto:turing.usp@gmail.com)   
[Facebook](https://www.facebook.com/grupoturing.usp)  
[Medium](https://www.medium.com/turing-talks)  
[LinkedIn](https://www.linkedin.com/company/grupo-turing)

