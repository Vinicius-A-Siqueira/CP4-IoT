# Projeto de Análise de Consumo de Energia

## Integrantes do grupo
- Vinicius Alves Siqueira | RM: 551939
- Kauan Felipe de Souza | RM: 557954
- Gabriel Camargo Ravanhani | RM: 557879

---

## 1. Objetivo
O projeto tem como objetivo analisar e explorar padrões de consumo de energia elétrica em residências, utilizando dois datasets:
1. **Individual Household Electric Power Consumption** (`household_power_consumption.txt`)
2. **Energy Dataset Complete** (`energydata_complete.csv`)

As análises incluem estatísticas descritivas, visualizações, séries temporais, correlações, normalização, PCA, clustering (K-Means), regressão e classificação.

---

## 2. Estrutura do projeto

### 2.1 Notebooks
Foram desenvolvidos notebooks Jupyter para implementação dos exercícios:

1. **Notebook.ipynb**  
   - Abrange exercícios 1 a 25 com o dataset `household_power_consumption.txt`.  
   - Inclui:
     - Leitura e inspeção de dados
     - Limpeza e tratamento de missing values
     - Estatísticas e gráficos (linha, histograma, séries temporais)
     - Criação de variáveis derivadas (`Total_Sub_metering`)
     - Filtragem por data, consumo médio diário/mensal
     - Correlação entre variáveis
     - Normalização Min-Max
     - K-Means clustering
     - Decomposição de séries temporais
     - Regressão linear simples

2. **Notebook.ipynb**  
   - Abrange exercícios 26 a 35 com o dataset `energydata_complete.csv`.  
   - Inclui:
     - Leitura e inspeção de dados
     - Histograma e séries temporais da variável `Appliances`
     - Correlações com variáveis ambientais
     - Normalização e PCA
     - Regressão linear múltipla
     - Random Forest Regressor
     - K-Means clustering
     - Classificação binária (alto/baixo consumo) com Logistic Regression e Random Forest
     - Avaliação de métricas (RMSE, R², accuracy, precision, recall, F1, matriz de confusão)

### 2.2 Workflow Orange3
Para a versão visual utilizando **Orange3**, foram implementados os exercícios 36 a 40:

- **36 – Importação e visualização inicial**
  - Widget: **CSV File Import → Data Table**
  - Visualização das primeiras linhas do dataset `household_power_consumption.txt`
  - Contagem de variáveis: 9 colunas
  - Contagem de registros: 2.075.259 linhas

- **37 – Amostragem de dados**
  - Widget: **Sample Data** (1% da base)
  - Comparação da distribuição de `Global_active_power` com a base completa

- **38 – Distribuição do consumo**
  - Widget: **Distribution**
  - Análise da concentração de consumo em valores baixos

- **39 – Relação entre variáveis elétricas**
  - Widget: **Scatter Plot**
  - X-axis: Voltage | Y-axis: Global_intensity
  - Observação de correlação moderada

- **40 – Clustering com K-Means**
  - Widget: **k-Means** (3 clusters) + **Scatter Plot**
  - Atributos: `Sub_metering_1`, `Sub_metering_2`, `Sub_metering_3`
  - Identificação de padrões distintos de consumo residencial

> Nota: Os widgets do Orange3 permitem exploração visual e interação dinâmica com os dados.

---

## 3. Instruções de uso

### 3.1 Notebooks
1. Coloque os arquivos dos datasets **na mesma pasta** do notebook:
2. Abra o notebook desejado (`.ipynb`) no Jupyter Notebook ou google colab.
3. Execute as células em ordem.
4. Verifique gráficos, outputs e análises.

### 3.2 Orange3
1. Abra o **Orange3 Canvas**.
2. Importe os datasets através do widget **CSV File Import**.
3. Conecte aos widgets conforme os exercícios 36–40.
4. Explore visualmente os dados e observe padrões, clusters e correlações.

---

## 4. Observações
- As análises foram realizadas considerando possíveis valores ausentes (`?` no primeiro dataset) e com tratamento adequado.
- A normalização Min-Max foi aplicada antes de PCA e K-Means para escalonamento correto.
- Modelos de regressão e classificação foram avaliados com métricas padrão: RMSE, R², Accuracy, Precision, Recall e F1-Score.
- A versão visual no Orange3 permite uma abordagem interativa complementar à execução em notebooks.

---

## 5. Referências
- [UCI Machine Learning Repository – Individual Household Electric Power Consumption](https://archive.ics.uci.edu/ml/datasets/individual+household+electric+power+consumption)
- [Energy Dataset Complete](https://archive.ics.uci.edu/ml/datasets/energy+consumption+in+household)
- [Orange3 Widget Catalog](https://orangedatamining.com/widget-catalog/)
