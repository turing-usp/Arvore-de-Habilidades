<img src="https://i.ibb.co/DtHQ3FG/802x265-Logo-GT.png" width="500">

## Grupo Turing
# Curvilinear Distance Analysis

- **Resumo**:
é a técnica equivalente ao CCA (canonical Correlation Analysis) mas utilizando distância geométrica em vez de distância euclidiana. Essa mudança torna esse algoritmo mais poderoso na redução de dimensionalidade. A implementação dele está no notebook CDA.Foi implementado também um variante dessa técnica, que lida melhor com ruído nos dados. Essa implementação está no notebook CDA_v2.

- No notebook CDA, foi feito uma análise demonstrando o poder da técnica. Foram criados dados aleatórios: 1000 pontos de 2 dimensões e o objetivo era chegar em uma dimensão. Aplicando o algoritmo, o erro ficou cerca de 1100 no final das iterações. Um erro grande pois os dados não possuem dimensão intrínseca igual a um. Mudando a segunda dimensão para o cosseno da primeira, i.e., tornando a segunda variável uma função não linear da primeira, e aplicando o algoritmo novamente, obtemos um erro de 4.7e-11, um erro extremamente baixo.

---
**Grupo Turing**  
Grupo de Extensão da Universidade de São Paulo (USP)

[Email](mailto:turing.usp@gmail.com)   
[Facebook](https://www.facebook.com/grupoturing.usp)  
[Medium](https://www.medium.com/turing-talks)  
[LinkedIn](https://www.linkedin.com/company/grupo-turing)

