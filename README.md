# Desafio de Ciência de Dados — Lighthouse 2025

Este repositório apresenta uma solução completa para o desafio proposto, envolvendo análise exploratória, estatística e modelagem preditiva sobre dados de filmes fornecidos em formato .csv.

## Como executar

1. **Clone o repositório:**

```bash
git clone https://github.com/afs-alice/lighthouse-data-science-challenge.git
cd lighthouse-data-science-challenge
```

2. **Instale os requisitos:**

```bash
# (Recomendado) Crie um ambiente virtual
python -m venv venv
source venv/bin/activate  # no Linux/macOS
venv\Scripts\activate  # no Windows

# Em seguida, instale as dependências
pip install -r requirements.txt
```

3. **Abra o notebook:**

Recomenda-se executar no [Google Colab](https://colab.research.google.com/) ou em ambiente Jupyter local.

```bash
jupyter notebook LH_CD_alice.ipynb
```

4. **Organize os dados:**

Garanta que o arquivo `desafio_indicium_imdb.csv` esteja dentro da pasta `/data`, conforme esperado no código:

```python
imdb_data = pd.read_csv("data/desafio_indicium_imdb.csv")
```


## Etapas da Solução

### Etapa 1 – Análise Exploratória e Limpeza
- Verificação e tratamento de tipos de dados
- Identificação de valores ausentes
- Conversões de colunas (ano, gross, runtime, etc.)
- Criação de novas variáveis (década, gênero principal, etc.)

### Etapa 2 – Análises Específicas
- **2a:** Recomendações com base em nota ponderada (método IMDB)
- **2b:** Fatores associados ao faturamento (correlação e agrupamentos)
- **2c:** Análise de palavras mais frequentes em sinopses por gênero

### Etapa 3 – Modelagem Preditiva
- Modelo de regressão para prever a nota do IMDB
- Utilização de Random Forest Regressor
- Transformações numéricas e categóricas via pipeline
- Métricas de avaliação: R², MAE e RMSE
- Teste com novo filme (The Shawshank Redemption)


## Modelo Treinado

O modelo final foi salvo no formato `.pkl` e pode ser carregado com:

```python
import joblib
modelo = joblib.load("modelo_imdb_alice.pkl")
```

---

