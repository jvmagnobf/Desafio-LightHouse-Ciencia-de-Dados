# Desafio de Ciência de Dados: Previsão de Notas de Filmes IMDB

Este projeto explora um dataset com os 1000 filmes mais bem avaliados do IMDB para construir um modelo de Machine Learning capaz de prever a nota de um filme (`IMDB_Rating`) com base em suas características. O processo abrange desde a análise exploratória e limpeza dos dados até o treinamento, avaliação e salvamento de múltiplos modelos de regressão.

##  Dataset

O dataset utilizado é o `desafio_indicium_imdb.csv`, que contém informações sobre 1000 filmes, incluindo:
* Título, ano de lançamento, duração e gênero.
* Nota IMDB, Meta score e número de votos.
* Diretor, elenco principal e receita de bilheteria (Gross).

##  Etapas do Projeto

O notebook `DesafioIndiciumCD.ipynb` está estruturado com as seguintes etapas:

1.  **Análise Exploratória de Dados (EDA):** Investigação inicial para entender a estrutura, distribuições, correlações e valores ausentes nos dados.
2.  **Limpeza e Pré-processamento:** Conversão de tipos de dados (ex: `Runtime`, `Gross`), e tratamento de valores ausentes usando técnicas como imputação pela média, moda e regressão.
3.  **Engenharia de Features:**
    * **One-Hot Encoding:** Para variáveis categóricas com poucas categorias (`Genre`, `Certificate`).
    * **Análise de Correlação:** Para entender a influência de cada feature no alvo.
    * **Seleção de Features:** Remoção de colunas com baixa correlação para simplificar o modelo.
4.  **Normalização de Dados:** Aplicação da normalização Min-Max (`MinMaxScaler`) nas features numéricas para padronizar a escala dos dados.
5.  **Treinamento e Avaliação de Modelos:**
    * Treinamento de um modelo base de **Regressão Linear**.
    * Treinamento de um modelo mais avançado de **Random Forest Regressor**.
    * Comparação de desempenho entre os modelos usando as métricas MAE, MSE e R².
6.  **Uso do Modelo:** Demonstração de como usar o modelo treinado para prever a nota de um novo filme.
7.  **Salvando o Modelo:** Exemplo de como salvar o modelo final (`.pkl`) usando `joblib`.

##  Tecnologias Utilizadas

* Python 3
* Pandas
* Numpy
* Scikit-learn
* Matplotlib
* Seaborn
* Jupyter Notebook

##  Como Executar o Projeto

Para executar este projeto em sua máquina local, siga os passos abaixo.

### 1. Pré-requisitos

* Ter o [Python 3](https://www.python.org/downloads/) instalado.
* Ter o `pip` (gerenciador de pacotes do Python) instalado.

### 2. Estrutura dos Arquivos

Certifique-se de que o notebook e o dataset estejam na mesma pasta:
```bash
seu-projeto/
├── DesafioIndiciumCD.ipynb
├── desafio_indicium_imdb.csv
└── README.md
```

### 3. Instalação das Dependências

É altamente recomendado criar um ambiente virtual para isolar as dependências do projeto.

```bash
# 1. Navegue até a pasta do seu projeto pelo terminal
cd caminho/para/seu-projeto

# 2. Crie um ambiente virtual
python3 -m venv venv

# 3. Ative o ambiente virtual
# No macOS ou Linux:
source venv/bin/activate
# No Windows:
# venv\Scripts\activate

# 4. Instale as bibliotecas necessárias
pip install pandas scikit-learn matplotlib seaborn jupyterlab
```
### 4. Executando o Notebook

Com as dependências instaladas e o ambiente virtual ativado, inicie o Jupyter.
```bash
# Inicie o Jupyter Lab (recomendado)
jupyter lab

# Ou, se preferir, o Jupyter Notebook clássico
# jupyter notebook
```
