# ✈️ Airline Sentiment Analysis

Análise de sentimentos em avaliações de companhias aéreas utilizando Processamento de Linguagem Natural (NLP) e Machine Learning.

## Sobre o Projeto

Este projeto realiza análise automatizada de sentimentos em 5 mil avaliações de passageiros de companhias aéreas, permitindo identificar padrões de satisfação, insatisfação e principais pontos de melhoria no setor de aviação.

### 🎯 Objetivos

- Classificar automaticamente avaliações em **positivas**, **negativas** ou **neutras**
- Analisar a correlação entre sentimento detectado e nota atribuída pelo usuário
- Comparar desempenho de diferentes companhias aéreas
- Identificar padrões e tendências nas experiências dos passageiros
## Tecnologias Utilizadas

- **Python 3.13.0**
- **Transformers (Hugging Face)** - Modelo DistilBERT multilíngue para classificação de sentimentos
- **Pandas** - Manipulação e análise de dados
- **Plotly** - Visualizações interativas
- **Google Colab** - Ambiente de desenvolvimento

## Dataset

**Fonte:** [Airline Reviews Dataset](https://www.kaggle.com/datasets/juhibhojani/airline-reviews)

- **Total de avaliações:** 23.171
- **Amostra analisada:** 5.000 avaliações (seleção aleatória)
- **Idioma:** Inglês
- **Período:** Avaliações históricas de múltiplas companhias aéreas

## Modelo Utilizado

**Modelo:** `lxyuan/distilbert-base-multilingual-cased-sentiments-student`

- Baseado em DistilBERT (versão otimizada do BERT)
- Suporta múltiplos idiomas
- Fine-tuned para análise de sentimentos
- Retorna label (positive/negative/neutral) e score de confiança

**Parâmetros:**
- Max length: 512 tokens
- Truncation: True (para avaliações longas)
## Análises Realizadas

### ✅ Concluídas

1. **Distribuição de Sentimentos**
   - Classificação de todas as avaliações em positivo/negativo/neutro
   - Visualização da proporção de cada categoria
   - **Resultado:** 63.7% negativas, 31.4% positivas, 4.9% neutras

2. **Correlação: Nota vs Sentimento Detectado**
   - Análise da relação entre a nota numérica (1-9) e o sentimento identificado pelo modelo
   - Heatmap mostrando distribuição cruzada
   - **Insight:** Forte correlação entre notas baixas (1-3) e sentimento negativo; notas altas (8-9) predominantemente positivas

## Como Executar

### Pré-requisitos

```bash
pip install pandas plotly transformers torch
```

### Execução

1. Clone o repositório:

```bash
git clone https://github.com/httpsemilly/airline-sentiment-analysis.git
cd airline-sentiment-analysis
```

2. Execute o notebook no Google Colab ou Jupyter:

```bash
jupyter notebook "airline-sentiment-analysis.ipynb"
```

## Estrutura do Projeto


```
airline-sentiment-analysis/
│
├── airline-sentiment-analysis.ipynb
├── airline_reviews.csv
├── results_with_sentiment.csv
├── images/                                       
│   ├── sentiment_distribution.png
│   └── rating_vs_sentiment.png
└── README.md
```

## Próximos Passos

1. **Dashboard Interativo:** Desenvolvimento de aplicação Streamlit para exploração dinâmica dos dados
2. **Análise por Companhia:** Ranking de companhias aéreas por sentimento médio
3. **Extração de Aspectos:** Identificar quais aspectos específicos (comida, atendimento, pontualidade) geram mais insatisfação
4. **Análise Temporal:** Verificar se sentimentos melhoraram/pioraram ao longo do tempo
5. **Comparação de Modelos:** Testar outros modelos (BERT, RoBERTa) e comparar performance
## Autor

**Emilly Cavalcante**
- GitHub: [@httpsemilly](https://github.com/httpsemilly)
- LinkedIn: [Emilly Cavalcante](https://linkedin.com/in/emillycavalcante)
- Email: emilly.menezescs@gmail.com
## Licença

Este projeto está sob a licença MIT. Veja o arquivo [LICENSE](LICENSE) para mais detalhes.

---

**Status:** 🚧 Em desenvolvimento ativo
