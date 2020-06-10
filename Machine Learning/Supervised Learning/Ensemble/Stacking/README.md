<img src="https://i.ibb.co/DtHQ3FG/802x265-Logo-GT.png" width="500">

## Grupo Turing
# Ensemble Learning: Stacking

## Introdução
	
Stacking, também às vezes referenciado como blending, é uma técnica de ensemble learning que consiste em combinar múltiplos modelos passando suas predições a um “meta-modelo” que funcionará melhor do que os preditores individualmente. 

O conjunto de preditores usados como base é chamado de primeira camada e o “meta-modelo” de segunda camada, é possível adicionar mais camadas nessa técnica, porém nem sempre compensa fazê-lo, podendo chegar a iguais ou piores resultados. 


<img src="https://i.imgur.com/WNyxeOP.png" width="500">


## Processo de Criação
	
### 1-Preparar os datasets

* Selecionar features e target
* Fazer Data Cleaning
* Mudar variáveis categóricas para dummie variables
* Dividir em dataset treino e teste

### 2-Construir os preditores da primeira camada

* Construir os preditores (podem ser de tipos diferentes) da primeira camada
* Fit os modelos no dataset de treino

### 3-Adicionar as predições ao dataset

* Calcular as predições
* Adicionar elas ao dataset por concatenação

### 4-Construir o “meta-preditor” 

* Construir o preditor da segunda camada
* Treinar o preditor no dataset com as predições da primeira camada adicionadas

### 5-Usar o conjunto criado para a predição

* Faça a predição dos preditores da primeira camada no dataset de teste
* Concatene essas predições no dataset
* Utilize esse dataset para o preditor da segunda camada


## **Links**:
* [Stacking com redes neurais](https://machinelearningmastery.com/stacking-ensemble-for-deep-learning-neural-networks/
)

* [Código em python de stacking](https://medium.com/@rrfd/boosting-bagging-and-stacking-ensemble-methods-with-sklearn-and-mlens-a455c0c982de)


---
**Grupo Turing**  
Grupo de Extensão da Universidade de São Paulo (USP)

[Email](mailto:turing.usp@gmail.com)   
[Facebook](https://www.facebook.com/grupoturing.usp)  
[Medium](https://www.medium.com/turing-talks)  
[LinkedIn](https://www.linkedin.com/company/grupo-turing)

