# Projeto de Credit Score - Parte 1 - Processamento dos dados
<img width="1408" height="768" alt="Gemini_Generated_Image_9gnh6m9gnh6m9gnh" src="https://github.com/user-attachments/assets/948fe497-5225-4bb3-909b-aafd3058f6b4" />

## 📌 Sobre o Projeto

Desenvolvimento de um processo de preparação e análise exploratória de dados de clientes para um projeto de classificação de Credit Score.

O trabalho envolve o tratamento de dados faltantes, transformação de variáveis, análise estatística, identificação de possíveis outliers, investigação de correlações, análise do perfil dos clientes e balanceamento das classes.

A etapa prepara a base de dados para o desenvolvimento de modelos de Machine Learning capazes de classificar o perfil de crédito dos clientes.

## 🎯 Objetivo

Preparar e transformar uma base de dados bancária para possibilitar a construção de modelos preditivos de Credit Score.

*O projeto busca:*
- Melhorar a qualidade e consistência dos dados.
- Identificar padrões e relações entre características dos clientes e seus scores de crédito.
- Tratar variáveis numéricas e categóricas.
- Investigar correlações entre as variáveis.
- Balancear as classes da variável-alvo.
- Separar os dados em conjuntos de treinamento e teste.

## 💻 Problema de Negócio / Pergunta de Pesquisa

É possível identificar padrões no perfil demográfico e socioeconômico dos clientes que estejam associados ao seu nível de Credit Score?

Quais características dos clientes apresentam maior associação com a classificação do score de crédito e podem contribuir para o desenvolvimento de modelos preditivos?

*Contexto de negócio:*

O Credit Score representa uma pontuação relacionada à credibilidade financeira de um indivíduo e ao risco de inadimplência.

Instituições financeiras podem utilizar essas informações para apoiar decisões de concessão de crédito, aprovação de empréstimos e definição de condições de financiamento.

## 📊 Fonte de Dados

Arquivo utilizado: CREDIT_SCORE_PROJETO_PARTE1.csv

*A base apresenta:*
- 164 registros de clientes.
- 8 colunas.
- 3 variáveis numéricas.
- 5 variáveis categóricas.

*Descrição das variáveis:*

Variável — Descrição

Age — Idade dos clientes

Gender — Gênero

Income — Salário mensal

Education — Nível de escolaridade

Marital Status — Estado civil

Number of Children — Quantidade de filhos

Home Ownership — Tipo de residência: própria ou alugada

Credit Score — Classificação do score de crédito

*A variável-alvo é Credit Score, inicialmente dividida em três categorias:*
- High: score alto.
- Average: score médio.
- Low: score baixo.
  
## 🛠️ LINGUAGENS E BIBLIOTECAS

Python: linguagem utilizada para processamento e análise.

Pandas: manipulação, limpeza e transformação dos dados.

NumPy: operações numéricas.

Matplotlib: construção de gráficos.

Seaborn: visualizações estatísticas e matrizes de correlação.

Plotly Express: gráficos interativos.

Scikit-learn:
- Label Encoder.
- One-Hot Encoding.
- Train-Test Split.

Imbalanced-learn:
- SMOTE para balanceamento das classes.

SciPy: biblioteca científica importada no notebook.

## 🔍 Metodologia

*Etapa 1 — Pré-processamento dos dados*
- Inspeção das variáveis e identificação dos tipos de dados.
- Conversão da variável Income de texto para formato numérico.
- Identificação de valores ausentes.
- Tratamento dos 34 registros ausentes na variável Age, utilizando a mediana de 36 anos.
- Padronização das variáveis categóricas, convertendo os textos para letras minúsculas e removendo espaços desnecessários.
- Inspeção das categorias para identificar inconsistências.

*Etapa 2 — Análise exploratória dos dados (EDA)*

Análise univariada:
- Estatísticas descritivas das variáveis numéricas.
- Distribuição de idade, renda e quantidade de filhos.
- Visualização utilizando histogramas e boxplots.
- Investigação de possíveis outliers.

Análise bivariada:
- Relação entre idade e estado civil.
- Relação entre Credit Score e escolaridade.
- Relação entre renda e idade.
- Relação entre renda e Credit Score.
- Relação entre propriedade de imóvel e Credit Score.
- Investigação adicional das relações entre quantidade de filhos, gênero, renda e score de crédito.

*Etapa 3 — Preparação para Machine Learning*
- Análise de correlação entre variáveis numéricas.
- Aplicação de Label Encoding nas variáveis Gender, Marital Status e Home Ownership.
- Aplicação de One-Hot Encoding nas variáveis Education e Credit Score.
- Exclusão das colunas categóricas originais após a transformação.
- Conversão das variáveis booleanas em valores numéricos.
- Separação dos dados em treinamento e teste, utilizando 75% para treinamento e 25% para teste.
- Verificação da distribuição das classes.
- Aplicação do SMOTE exclusivamente nos conjuntos de treinamento.
- Exportação dos conjuntos preparados em arquivos CSV.
  
## 📈 Resultados e Métricas

O projeto apresenta resultados relacionados à qualidade dos dados, análise exploratória e preparação das bases para modelagem.

*7.1. Tratamento de dados*

Indicador — Resultado

Registros originais — 164

Valores ausentes em Age — 34

Percentual de valores ausentes em Age — 20,73%

Mediana utilizada no preenchimento — 36 anos

Valores ausentes após tratamento — 0

A variável Income também foi convertida de texto para formato numérico.

*7.2. Estatísticas descritivas*

Variável ——————— Média ——— Mediana ——— Mínimo ——— Máximo

Age ————————— 37,20 ———— 36 ————— 25 ————— 53

Income ——————— 83.765,24 ——— 83.750 ——— 25.000 ——— 162.500

Number of Children —— 0,65 ————— 0 ————— 0 —————— 3

## 💡 Principais Insights e Implicações

A análise exploratória identificou relações relevantes entre características socioeconômicas e a classificação de crédito dos clientes.

#### Renda e idade

Foi identificada uma correlação positiva de aproximadamente 0,62 entre idade e renda. A análise sugere que clientes mais velhos tendem a apresentar rendimentos mais elevados, embora essa relação não seja uma regra absoluta.

#### Renda e Credit Score

*O notebook identificou uma associação entre maior renda e score de crédito elevado:*
- Clientes com renda inferior a 40 mil aparecem associados ao score baixo.
- Clientes com renda entre 40 mil e 68 mil apresentam maior presença de score médio.
- Clientes com renda a partir de 80 mil aparecem associados ao score alto.

#### Escolaridade e Credit Score

*A análise identificou diferenças na distribuição do score conforme a escolaridade:*
- Clientes com mestrado e doutorado apresentam maior presença de score alto.
- Clientes com graduação e formação associada apresentam maior presença de score médio.
- Clientes com ensino médio apresentam maior presença de score baixo.

#### Propriedade de imóvel e Credit Score

Foi identificada uma associação entre possuir imóvel próprio e apresentar score elevado.

*Segundo a análise registrada:*
- 98,19% dos clientes com imóvel próprio apresentam score alto.
- 64,15% dos clientes que alugam imóvel apresentam score baixo.

#### Idade e estado civil

*A análise identificou diferenças na distribuição do estado civil conforme a idade:*
- Até 33 anos, aproximadamente 80% dos clientes são solteiros.
- A partir dos 34 anos, aproximadamente 70% são casados.

#### Quantidade de filhos e gênero

A base apresenta predominância de clientes sem filhos (59,15%). O notebook também observou diferenças na distribuição dos scores entre homens e mulheres, com maior presença masculina na categoria média e feminina na categoria baixa.

#### Implicações para o negócio

Os resultados demonstram como a análise de dados pode ajudar a identificar padrões no perfil socioeconômico dos clientes e suas associações com a classificação de crédito.

Esses padrões podem contribuir para a construção de modelos de classificação capazes de apoiar a avaliação de risco e a tomada de decisão das instituições financeiras.

# Projeto de Credit Score - Naive Bayes
<img width="1408" height="768" alt="Gemini_Generated_Image_vogaiivogaiivoga" src="https://github.com/user-attachments/assets/c28d33ee-b748-4080-84a9-c976264366bf" />


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
<img width="1408" height="768" alt="Gemini_Generated_Image_49jt2m49jt2m49jt" src="https://github.com/user-attachments/assets/f2237133-55a6-4aca-8a6d-4051f1727935" />

## 📌 Sobre o Projeto

Projeto de classificação utilizando o algoritmo de Árvore de Decisão para analisar o comportamento de clientes e identificar a ocorrência de churn (cancelamento ou saída de clientes).

O trabalho dá continuidade a um projeto anterior de pré-processamento e balanceamento de dados, no qual também foi aplicado o algoritmo Naive Bayes.

## 🎯 Objetivo

Desenvolver um modelo de classificação utilizando Árvore de Decisão para prever a ocorrência de churn, identificando clientes que permaneceram e clientes que deixaram a empresa.

Também foram avaliadas as principais variáveis que influenciam as previsões e comparado o desempenho do modelo com o algoritmo Naive Bayes.

## 💻 Problema de Negócio / Pergunta de Pesquisa

Como utilizar o histórico e as características dos clientes para identificar aqueles com maior probabilidade de cancelar ou deixar a empresa?

Quais variáveis apresentam maior influência na identificação do churn e como melhorar a capacidade de previsão do modelo?

## 📊 Fonte de Dados

Bases de dados de treinamento e teste, previamente tratadas no Projeto de Credit Score - Processamento dos dados.
Link: <https://github.com/marinanapoleao/Projeto-de-Credit-Score/blob/main/Projeto%20de%20Credit%20Score%20-%20Processamento%20dos%20dados.ipynb> 

Foram utilizadas:
- X_train_balanced.csv: variáveis independentes para treinamento.
- y_train_balanced.csv: variável-alvo para treinamento.
- X_test: variáveis independentes para teste.
- y_test: variável-alvo para teste.
  
## 🛠️ LINGUAGENS E BIBLIOTECAS

- Python.
- Pandas e NumPy: manipulação e análise dos dados.
- Matplotlib e Seaborn: visualização dos resultados.
- Scikit-learn:
  - DecisionTreeClassifier;
  - confusion_matrix;
  - accuracy_score;
  - classification_report;
  - plot_tree.
  
## 🔍 Metodologia

- Carregamento das bases de treinamento e teste, previamente tratadas e balanceadas.

- Verificação das variáveis e distribuição das classes.

- Treinamento do modelo de Árvore de Decisão utilizando o critério Gini e random_state=0.

- Avaliação do modelo utilizando acurácia, precisão, recall, F1-score e matriz de confusão.

- Visualização da estrutura da árvore e análise da importância das variáveis.

- Identificação das duas principais features: quantidade de produtos e idade.

- Construção de um segundo modelo utilizando somente essas duas variáveis.

- Comparação dos resultados entre a árvore completa, a árvore reduzida e o modelo Naive Bayes.

## 📈 Resultados e Métricas

*Modelo 1 — Árvore completa*

Acurácia: 79,30%

Recall — Churn: 56%

Precisão — Churn: 51%

F1-score — Churn: 53%

#### Matriz de confusão

Resultado ———————  Quantidade

Verdadeiros negativos ——— 16.798

Falsos positivos ——————  2.851

Falsos negativos —————— 2.310

Verdadeiros positivos ——— 2.968

*Modelo 2 — Árvore reduzida (Quantidade de Produtos + Idade)*

Acurácia: 85%

Recall — Churn: 52%

Precisão — Churn: 67%

F1-score — Churn: 59%

#### Matriz de confusão

Resultado ———————  Quantidade

Verdadeiros negativos ——— 18.309

Falsos positivos ——————  1.340

Falsos negativos —————— 2.520

Verdadeiros positivos ——— 2.758

## 💡 Principais Insights e Implicações

- A quantidade de produtos e a idade foram identificadas como as duas variáveis mais importantes para a previsão de churn.
- A árvore reduzida apresentou melhor desempenho geral, aumentando a acurácia de 79% para 85%.
- A precisão da classe churn aumentou de 51% para 67%, reduzindo os falsos positivos de 2.851 para 1.340.
- Entretanto, o recall da classe churn caiu de 56% para 52%, aumentando a quantidade de clientes que deixaram a empresa sem serem identificados pelo modelo.
- O Naive Bayes apresentou resultados inferiores de acurácia para churn, enquanto a Árvore de Decisão apresentou melhor desempenho geral.

*Implicação para o negócio:* o modelo pode auxiliar na identificação de padrões associados à saída de clientes, contribuindo para estratégias de retenção e ações preventivas. Entretanto, é importante considerar o equilíbrio entre identificar clientes que realmente podem sair e evitar classificações incorretas.

## 👩‍💻 Sobre a Autora

Desenvolvido por Marina Napoleão — Cientista de Dados / Analista de Dados. 
### LinkedIn <https://www.linkedin.com/in/marina-napoleao/>
### GitHub <https://github.com/marinanapoleao> 
