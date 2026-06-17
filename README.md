# MVP - Previsão do Distopia Score no Brasil

Projeto desenvolvido para a disciplina de Machine Learning & Analytics.

## Objetivo

Construir um indicador sintético denominado Distopia Score e avaliar sua capacidade de previsão utilizando indicadores institucionais do projeto V-Dem.

## Estrutura do Projeto

dataset/
- dados_brasil_vdem.csv

notebooks/
- Distopia_Score.ipynb

## Fonte dos Dados

Os dados utilizados neste projeto foram extraídos do dataset V-Dem (Varieties of Democracy).

A base disponibilizada neste repositório corresponde a uma versão reduzida e tratada da base original, contendo apenas:

- Brasil
- Período 2000–2025
- Variáveis utilizadas na construção do Distopia Score

Base original:
https://www.v-dem.net/data/the-v-dem-dataset/

## Modelos Avaliados

- Baseline
- Regressão Linear
- Random Forest
- Random Forest com Grid Search

## Resultado

O modelo Baseline apresentou o melhor desempenho para previsão de curto prazo do Distopia Score.
