# Distopia Score Brasil: É possível prever tendências institucionais rumo a uma sociedade distópica?

## Visão Geral

Este projeto foi desenvolvido como MVP da disciplina de Machine Learning & Analytics da Pós-Graduação em Ciência de Dados e Analytics (PUC-Rio).

O objetivo foi investigar se indicadores institucionais e democráticos podem ser utilizados para construir e prever um índice sintético denominado **Distopia Score**.

A inspiração do projeto surgiu de conceitos presentes na obra *1984*, de George Orwell, utilizando indicadores relacionados à liberdade de expressão, independência judicial, participação da sociedade civil e qualidade democrática para representar quantitativamente tendências institucionais potencialmente associadas a cenários mais ou menos democráticos.

---

## Problema de Negócio

É possível utilizar indicadores institucionais do Brasil para prever a evolução de um índice sintético de deterioração democrática no ano seguinte?

---

## Hipóteses Investigadas

Antes da análise, foram consideradas as seguintes hipóteses:

### H1
Reduções na liberdade de expressão aumentam o Distopia Score.

### H2
O enfraquecimento do Estado de Direito está associado ao aumento do Distopia Score.

### H3
Menor participação da sociedade civil contribui para cenários institucionais mais distópicos.

### H4
O Distopia Score apresenta forte persistência temporal, tornando o histórico recente um importante preditor do futuro.

---

## Fonte dos Dados

Os dados utilizados foram obtidos a partir do projeto **Varieties of Democracy (V-Dem)**.

Base original:

https://www.v-dem.net/data/the-v-dem-dataset/

A base disponibilizada neste repositório corresponde a uma versão tratada da base original contendo apenas:

- Brasil
- Período de 2000 a 2025
- Variáveis utilizadas na construção do Distopia Score

---

## Variáveis Utilizadas

| Variável | Descrição |
|-----------|-----------|
| Democracia Liberal | Mede a qualidade das instituições democráticas |
| Liberdade de Expressão e Informação | Avalia liberdade de imprensa e acesso à informação |
| Estado de Direito | Mede a força e independência das instituições jurídicas |
| Participação da Sociedade Civil | Avalia o nível de participação e organização social |
| Controle Judicial do Executivo | Mede a capacidade do Judiciário de limitar abusos do Executivo |

---

## Construção do Distopia Score

O Distopia Score foi construído a partir da combinação de indicadores institucionais do V-Dem.

A ideia central não é medir a existência de um regime autoritário, mas sim criar um indicador experimental capaz de representar tendências institucionais associadas a cenários mais ou menos democráticos.

Valores mais elevados do Distopia Score representam contextos institucionais potencialmente mais próximos de características observadas em regimes autoritários ou menos democráticos.

---

## Metodologia

### 1. Análise Exploratória dos Dados

- Estatísticas descritivas
- Evolução temporal dos indicadores
- Análise de correlação entre variáveis

### 2. Engenharia de Atributos

- Construção do Distopia Score
- Criação da variável alvo para previsão do ano seguinte
- Organização da série temporal para modelagem

### 3. Modelagem Preditiva

Foram comparadas quatro abordagens:

- Baseline (Persistência Temporal)
- Regressão Linear
- Random Forest
- Random Forest com ajuste de hiperparâmetros (Grid Search)

---

## Métricas de Avaliação

Os modelos foram avaliados utilizando:

- MAE (Mean Absolute Error)
- RMSE (Root Mean Squared Error)
- R² (Coeficiente de Determinação)

---

## Principais Resultados

Os resultados mostraram que o Distopia Score apresenta forte persistência temporal.

O modelo Baseline obteve o melhor desempenho preditivo, superando os modelos mais complexos avaliados.

Esse resultado sugere que alterações institucionais tendem a ocorrer de forma gradual ao longo do tempo, dificultando que algoritmos de Machine Learning obtenham ganhos significativos quando comparados a uma estratégia simples baseada no valor observado no ano anterior.

Além disso, a análise exploratória evidenciou períodos de maior deterioração institucional e momentos de recuperação parcial, demonstrando que os indicadores selecionados conseguem capturar mudanças relevantes na dinâmica institucional brasileira.

---

## Limitações do Projeto

- Apenas 26 observações anuais foram utilizadas.
- O estudo está restrito ao Brasil.
- Foram utilizados apenas indicadores institucionais selecionados do V-Dem.
- Não foram incorporadas variáveis econômicas, sociais ou geopolíticas.

Dessa forma, os resultados devem ser interpretados como uma prova de conceito (MVP) e não como um sistema definitivo de previsão institucional.

---

## Possíveis Evoluções Futuras

- Inclusão de outros países latino-americanos.
- Ampliação da série histórica.
- Inclusão de indicadores econômicos e sociais.
- Aplicação de modelos específicos para séries temporais.
- Testes com algoritmos mais avançados, como XGBoost e LightGBM.

---

## Estrutura do Projeto

```text
mvp-distopia-brasil/
│
├── dataset/
│   ├── README.md
│   └── dados_brasil_vdem.csv
│
├── notebooks/
│   ├── README.md
│   └── Distopia_Score.ipynb
│
└── README.md
```

---

## Tecnologias Utilizadas

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-Learn
- Google Colab
- GitHub

---

## Resultado Acadêmico

Projeto desenvolvido para a disciplina de Machine Learning & Analytics da Pós-Graduação em Ciência de Dados e Analytics (PUC-Rio).

**Avaliação Final: 10/10**

Comentários do avaliador:

> "Trabalho muito bacana sobre a previsão da nossa democracia caminhar pra uma versão distópica como em 1984 de George Orwell. O MVP foi bem estruturado, documentado e avaliado, com todas as etapas contendo markdowns explicativos e que agregaram à discussão, tanto na parte exploratória quanto na preditiva."

---

## Autor

**Pedro Reis**

Pós-Graduação em Ciência de Dados e Analytics – PUC-Rio

GitHub: https://github.com/pedrohreisrj
