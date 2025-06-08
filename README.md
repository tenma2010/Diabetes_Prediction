# Predição de Diabetes por Machine Learning

# Descrição do Projeto

Este projeto tem como objetivo desenvolver um modelo de Machine Learning para prever a ocorrência de diabetes em pacientes, utilizando dados de saúde. A detecção precoce é fundamental para o tratamento eficaz da doença e a prevenção de complicações.

# Funcionalidades

•
Coleta e Análise de Dados: Carregamento do dataset diabetes.csv e análise exploratória para entender a distribuição e estatísticas dos dados.

•
Pré-processamento de Dados: Tratamento de valores ausentes (substituição de zeros por médias) e padronização das características para otimizar o desempenho do modelo.

•
Treinamento do Modelo: Utilização de um modelo de Support Vector Machine (SVM) para classificação.

•
Avaliação de Desempenho: Medição da acurácia do modelo no conjunto de dados de teste.

•
Sistema de Predição: Capacidade de prever a ocorrência de diabetes para novas entradas de dados.

# Tecnologias Utilizadas

•
Python

•
numpy

•
pandas

•
scikit-learn (StandardScaler, train_test_split, svm, metrics)

# Conjunto de Dados

O conjunto de dados utilizado é o diabetes.csv, que contém 768 instâncias e 9 atributos. As características incluem:

•
Pregnancies: Número de gestações

•
Glucose: Concentração de glicose no plasma a 2 horas em um teste oral de tolerância à glicose

•
BloodPressure: Pressão arterial diastólica (mm Hg)

•
SkinThickness: Espessura da dobra cutânea do tríceps (mm)

•
Insulin: Insulina sérica de 2 horas (mu U/ml)

•
BMI: Índice de massa corporal (peso em kg/(altura em m)^2)

•
DiabetesPedigreeFunction: Função de pedigree de diabetes (uma função que pontua a probabilidade de diabetes com base no histórico familiar)

•
Age: Idade (anos)

•
Outcome: Variável de classe (0 para não-diabético, 1 para diabético)

O dataset possui 500 casos de não-diabéticos (Outcome = 0) e 268 casos de diabéticos (Outcome = 1).

# Metodologia de Machine Learning

1. Coleta e Análise de Dados: O dataset diabetes.csv é carregado e são realizadas análises estatísticas básicas (.head(), .shape(), .describe(), .value_counts(), .groupby().mean()).

2. Pré-processamento de Dados:

  •
  Valores zero nas colunas Glucose, BloodPressure, SkinThickness, Insulin e BMI são substituídos pela média dos respectivos atributos, pois zero não é um valor clinicamente plausível para essas métricas.

  •
  Os dados são padronizados usando StandardScaler para garantir que todas as características contribuam igualmente para o modelo.



3. Divisão de Dados: O dataset é dividido em conjuntos de treino e teste usando train_test_split, com uma proporção de 80% para treino e 20% para teste.

4. Treinamento do Modelo: Um modelo de Support Vector Classifier (SVC) é treinado com os dados padronizados.

5. Avaliação do Modelo: A acurácia do modelo é calculada nos conjuntos de treino e teste para verificar o desempenho e identificar possível overfitting.

# Resultados e Avaliação

Após o treinamento e avaliação do modelo SVM, os seguintes resultados de acurácia foram obtidos:

•
Acurácia no conjunto de treino: Aproximadamente 78.6% (0.7862)

•
Acurácia no conjunto de teste: Aproximadamente 77.2% (0.7727)

Estes resultados indicam que o modelo tem um bom desempenho na predição de diabetes, com uma acurácia consistente tanto nos dados de treino quanto nos de teste, sugerindo que o modelo não está sofrendo de overfitting significativo.



