# Análise e Predição de Notas IMDB de Filmes

## 🎬 Descrição do Problema de Negócio

Este projeto tem como objetivo analisar um conjunto de dados de filmes do IMDB e desenvolver um modelo de machine learning capaz de prever a nota IMDB de filmes com base em suas características. O estudo busca responder perguntas importantes do setor cinematográfico, como:

1. **Qual filme você recomendaria para uma pessoa que você não conhece?**
2. **Quais são os principais fatores que estão relacionados com alta expectativa de faturamento de um filme?**
3. **Quais insights podem ser tirados com a coluna Overview? É possível inferir o gênero do filme a partir dessa coluna?**

## 🚀 Como Executar o Projeto

### 1. Instalação das Dependências

Primeiro, crie um ambiente virtual e instale as dependências necessárias:

```bash
# Criar ambiente virtual
python -m venv venv

# Ativar ambiente virtual
# No Windows:
venv\Scripts\activate
# No Linux/Mac:
source venv/bin/activate

# Instalar dependências
pip install -r requirements.txt
```

As principais dependências incluem:
- pandas
- numpy
- scikit-learn
- matplotlib
- seaborn
- joblib

### 2. Estrutura do Projeto

```
├── data/
│   ├── raw/                 # Dados brutos
│   └── processed/           # Dados processados
├── notebooks/               # Notebooks Jupyter com análises
│   ├── 01-tratamento_dos_dados.ipynb
│   ├── 02-eda.ipynb
│   └── 03-modelagem.ipynb
├── models/                  # Modelos treinados
│   └── best_rf.pkl
├── requirements.txt         # Dependências do projeto
└── README.md
```

### 3. Execução das Análises

O projeto está organizado em três notebooks principais:

1. **Tratamento dos Dados** (`notebooks/01-tratamento_dos_dados.ipynb`):
   - Análise exploratória inicial
   - Limpeza e transformação dos dados
   - Tratamento de valores ausentes
   - Criação de flags para dados faltantes

2. **Análise Exploratória** (`notebooks/02-eda.ipynb`):
   - Análise univariada e multivariada
   - Análise de variáveis categóricas (gênero, diretor, atores)
   - Análise textual das sinopses usando NMF
   - Respostas às perguntas de negócio

3. **Modelagem Preditiva** (`notebooks/03-modelagem.ipynb`):
   - Preparação dos dados para modelagem
   - Treinamento de modelos (Regressão Linear, Random Forest)
   - Otimização de hiperparâmetros
   - Avaliação de desempenho

### 4. Executando os Notebooks

```bash
# Iniciar Jupyter Notebook
jupyter notebook

# Ou Jupyter Lab
jupyter lab
```

Navegue até a pasta `notebooks/` e execute os arquivos na ordem numerada.

## 📊 Estrutura dos Arquivos

### Dados de Entrada
- `data/raw/desafio_indicium_imdb.csv`: Conjunto de dados original com 999 filmes contendo:
  - Series_Title: Nome do filme
  - Released_Year: Ano de lançamento
  - Certificate: Classificação etária
  - Runtime: Duração do filme
  - Genre: Gênero(s) do filme
  - IMDB_Rating: Nota no IMDB
  - Overview: Sinopse do filme
  - Meta_score: Pontuação da crítica
  - Director: Diretor
  - Star1-4: Atores principais
  - No_of_Votes: Número de votos
  - Gross: Faturamento

### Dados Processados
- `data/processed/desafio_indicium_imdb_tratado.csv`: Dados após tratamento com:
  - Correção de tipos de dados
  - Tratamento de valores ausentes
  - Criação de flags para dados faltantes
  - Remoção de colunas desnecessárias

### Modelos
- `models/best_rf.pkl`: Modelo Random Forest otimizado salvo
