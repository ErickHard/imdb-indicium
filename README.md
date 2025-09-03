# 🎬 Projeto IMDB - Análise Exploratória e Previsão de Notas

Este projeto realiza **Análise Exploratória de Dados (EDA)**
Desenvolve um modelo de **Machine Learning**
Prever a nota do IMDB de filmes a partir de características como ano de lançamento, gênero, tempo de duração, número de votos e bilheteria.

## 📦 Instalação

1. **Clone este repositório** ou baixe os arquivos do projeto.
   ```bash
   git clone https://github.com/seu-repo/imdb-indicium.git
   cd imdb-indicium

2. Crie um ambiente virtual (recomendado)

python -m venv venv
source venv/bin/activate   # Linux/Mac
venv\Scripts\activate      # Windows

3. Instale as dependências

pip install -r requirements.txt

4. Coloque o dataset na pasta do projeto
O arquivo esperado é:

desafio_indicium_imdb (2).csv.csv

▶️ Execução do projeto

Abra o Jupyter Notebook e rode o projeto:

jupyter notebook

No navegador, abra o arquivo:

EDA_IMDB.ipynb

📊 Funcionalidades

Exploração e visualização dos dados (histogramas, scatterplots, correlação).

Limpeza e transformação das variáveis (ano, duração, bilheteria, gêneros).

Modelo de Random Forest Regressor para prever a nota do IMDB.

Salvamento do modelo treinado em arquivo .pkl

Exemplo de carregamento do modelo e previsão para um novo filme.

🧑‍💻 Uso do modelo salvo

Depois de executar, o modelo é salvo em modelo_imdb.pkl.
Você pode carregar e usar em qualquer script Python:

import joblib
import pandas as pd

# Carregamento do modelo
modelo = joblib.load("modelo_imdb.pkl")

# Exemplo de entrada
novo_filme = pd.DataFrame([{
    'Released_Year': 1994,
    'Runtime': 142,
    'Genre': 'Drama',
    'Meta_score': 80.0,
    'No_of_Votes': 2343110,
    'Gross': 28341469
}])

# Previsão 
print("Previsão IMDB:", modelo.predict(novo_filme)[0])

📌 Requisitos para execução do projeto

Python 3.9+

Pacotes usados e suas verções listados **requirements.txt**
---
# 📄 **requirements.txt**
```txt
pandas==2.2.2
numpy==1.26.4
matplotlib==3.9.0
seaborn==0.13.2
scikit-learn==1.5.0
jupyter==1.0.0
joblib==1.4.2
