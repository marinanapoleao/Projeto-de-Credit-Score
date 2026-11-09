# Projeto de Credit Score - Parte 1 - Processamento dos dados

## 📌 Sobre o Projeto

## 🎯 Objetivo

## 💻 Problema de Negócio / Pergunta de Pesquisa

## 📊 Fonte de Dados

## 🛠️ LINGUAGENS E BIBLIOTECAS

## 🔍 Metodologia

## 📈 Resultados e Métricas

## 💡 Principais Insights e Implicações


# Projeto de Credit Score - Naive Bayes

## 📌 Sobre o Projeto

Desenvolvimento de modelos de classificação utilizando o algoritmo Naive Bayes Gaussiano para analisar informações de clientes e realizar previsões relacionadas ao perfil de crédito.

O notebook apresenta três experimentos de classificação: um relacionado à previsão de Churn e outros dois relacionados à classificação de Credit Score alto e baixo.

## 🎯 Objetivo

Desenvolver modelos preditivos capazes de classificar clientes de acordo com seu perfil de crédito, identificando aqueles com maior probabilidade de cumprir compromissos financeiros e aqueles que podem representar maior risco de inadimplência.

A finalidade é fornecer informações que auxiliem instituições financeiras na tomada de decisões sobre empréstimos e financiamentos.

## 💻 Problema de Negócio / Pergunta de Pesquisa

Com base nas características cadastrais e financeiras dos clientes, é possível desenvolver um modelo de classificação capaz de identificar clientes com perfil de crédito alto ou baixo?

Essa classificação poderia auxiliar instituições financeiras na avaliação de riscos e na análise de concessão de crédito.

## 📊 Fonte de Dados

O notebook utiliza arquivos CSV previamente preparados no módulo 17 da EBAC, separados em bases de treinamento e teste.

*São apresentados três conjuntos de dados:*
- Base Churn: informações como Credit Score, idade, tempo de relacionamento com o banco, saldo, quantidade de produtos, cartão de crédito, atividade do cliente, salário e país.
- Base Credit Score High: informações demográficas e socioeconômicas, como idade, renda, quantidade de filhos, gênero, estado civil, propriedade de imóvel e escolaridade.
- Base Credit Score Low: utiliza estrutura de variáveis semelhante à base anterior.

Observação: o notebook não identifica a fonte original dos conjuntos de dados nem apresenta o link de obtenção das bases. Portanto, a informação disponível é que foram utilizadas bases CSV preparadas em uma etapa anterior do curso.

## 🛠️ LINGUAGENS E BIBLIOTECAS

- Python
- Pandas: carregamento e manipulação dos dados.
- NumPy: operações numéricas.
- Scikit-learn: implementação do modelo e avaliação.
- Gaussian Naive Bayes (GaussianNB): algoritmo de classificação.
- Plotly: visualização das matrizes de confusão.
- Seaborn e Matplotlib: bibliotecas importadas no notebook.
  
## 🔍 Metodologia

O trabalho foi desenvolvido em duas etapas principais:

Etapa 1 — Preparação dos dados (módulo anterior)

*Conforme descrito no próprio notebook, foram realizadas as seguintes atividades:*
- Tratamento dos dados e valores faltantes.
- Transformação de variáveis categóricas em numéricas.
- Balanceamento das classes de treinamento.
- Análise de correlação.
- Separação dos dados em conjuntos de treinamento e teste.

Etapa 2 — Modelagem e avaliação

*Nesta etapa, foram utilizadas as bases previamente preparadas para:*
1. Carregar os conjuntos de treinamento e teste.
2. Verificar o balanceamento das classes.
3. Instanciar e treinar modelos Gaussian Naive Bayes.
4. Realizar previsões para os dados de treinamento.
5. Avaliar os modelos utilizando acurácia, recall e matrizes de confusão.
6. Aplicar os modelos aos dados de teste.
7. Comparar os resultados de treinamento e teste.
   
## 📈 Resultados e Métricas

*Resultados para três experimentos:*

Modelo ————————	Acurácia treino ——— Recall treino —————— Acurácia teste —————— Recall teste

Naive Bayes — Churn ——— 58,55% —————— 63,45% ————————— 55,53% ———————— 64,80%

Naive Bayes — Score High — 99,40% —————— 98,81% ————————— 100% ————————— 100%

Naive Bayes — Score Low — 99,56% —————— 100% —————————— 100% ————————— 100%

*Detalhamento dos resultados:*
- Churn: o modelo apresentou acurácia de 55,53% no teste e recall de 64,80%, indicando uma quantidade significativa de classificações incorretas.
- Score High: apresentou acurácia e recall de 100% no teste, composto por 41 registros.
- Score Low: também apresentou acurácia e recall de 100% no teste, composto por 41 registros.
  
## 💡 Principais Insights e Implicações

O experimento relacionado a Churn apresentou desempenho limitado, demonstrando dificuldades na identificação correta das classes.

Os modelos de Score High e Score Low apresentaram resultados aparentemente excelentes, com 100% de acurácia e recall nos conjuntos de teste.

Entretanto, identifiquei um ponto técnico importante que precisa ser investigado antes de considerar esses resultados como evidência de capacidade preditiva:
- O conjunto de variáveis de entrada do modelo Score High contém a coluna Credit Score_low, enquanto a variável prevista é Credit Score_high.
- O conjunto de entrada do modelo Score Low contém a coluna Credit Score_high, enquanto a variável prevista é Credit Score_low.
Como essas variáveis representam classificações relacionadas ao próprio Credit Score, existe a possibilidade de vazamento de informação (data leakage). É necessário verificar como foram construídas e se derivam da variável-alvo.

Além disso, os conjuntos de teste de Score High e Score Low possuem somente 41 registros cada.

Portanto, os resultados perfeitos precisam ser reavaliados antes de serem utilizados como demonstração da capacidade de previsão do modelo.

Implicação para o negócio: a proposta do projeto é utilizar modelos preditivos para apoiar a avaliação de risco de crédito, contribuindo para decisões mais fundamentadas sobre empréstimos e financiamentos.

# Projeto de Credit Score - Árvore de Decisão

## 📌 Sobre o Projeto

## 🎯 Objetivo

## 💻 Problema de Negócio / Pergunta de Pesquisa

## 📊 Fonte de Dados

## 🛠️ LINGUAGENS E BIBLIOTECAS

## 🔍 Metodologia

## 📈 Resultados e Métricas

## 💡 Principais Insights e Implicações



## 👩‍💻 Sobre a Autora

Desenvolvido por Marina Napoleão — Cientista de Dados / Analista de Dados. 
### LinkedIn <https://www.linkedin.com/in/marina-napoleao/>
### GitHub <https://github.com/marinanapoleao> 
