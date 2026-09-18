Impact of ESG Factors on Corporate Financial Performance
==========================================================

Dissertacao de mestrado (MSc Business Analytics, ISCTE Business School, 2024-2026), concluida em julho de 2026. Estuda o impacto de fatores ESG (Environmental, Social, Governance) na performance financeira de empresas do S&P 500 entre 2019 e 2023, combinando econometria de painel com um modelo de machine learning.

**Status: concluida.** Orientador: Doutor Ricardo Joao Lourenco Abreu (ISCTE).

## Objetivo

Testar se scores ESG (e as suas componentes E, S e G) explicam variacao na performance financeira das empresas, e comparar o poder explicativo de uma abordagem econometrica classica com o de um modelo nao-linear.

## Metodologia

- Dados: painel de empresas do S&P 500, 2019-2023 (Refinitiv Eikon), ~500 empresas / ~2500 observacoes anuais
- Modelo econometrico: regressao em painel com efeitos fixos de empresa e ano (fixed-effects panel econometrics)
- Modelo de machine learning: Random Forest, para captar relacoes nao-lineares entre variaveis ESG e performance financeira
- Variaveis dependentes: Tobin's Q, ROA, ROE
- Ferramentas: Python (pandas, statsmodels, linearmodels, scikit-learn), Google Colab

## Principais resultados

- Os modelos de painel com efeitos fixos **nao encontram efeito linear estatisticamente significativo** do ESG (agregado ou por pilares) sobre Tobin's Q, ROA ou ROE, resultado robusto a variaveis defasadas e a analise individual dos pilares
- O modelo **Random Forest** alcanca capacidade preditiva substancial fora da amostra (R2 ate 0,55 para o Tobin's Q; 0,37 para o ROA), superando claramente um modelo linear (OLS) com as mesmas variaveis — evidencia de relacoes nao lineares que os modelos lineares nao captam
- A **desagregacao por pilares (E, S, G)** supera sistematicamente o ESG Combined Score em capacidade preditiva
- A **analise setorial** revela efeitos de sinal oposto que se cancelam no efeito medio: positivo e significativo em Industrials, negativo em Real Estate
- A reduzida variacao intraempresa dos scores ESG (26% a 52% da variacao total, consoante o pilar) ajuda a explicar a ausencia de significancia nos modelos de efeitos fixos

## Estrutura do repositorio

```
esg-financial-performance/
├── notebooks/
│   └── Main_AnalysisTese_Organizado.ipynb   # notebook completo: dados, painel, regressoes, VIF, Random Forest
├── report/
│   └── Dissertacao_Denilson_Cardoso.pdf     # dissertacao final
└── README.md
```

## Como reproduzir

```
pip install pandas numpy linearmodels statsmodels scikit-learn scipy
jupyter notebook notebooks/Main_AnalysisTese_Organizado.ipynb
```

Nota: os dados (Refinitiv Eikon, acesso via biblioteca ISCTE) nao sao redistribuidos por licenciamento.

---

Projeto academico — ISCTE Business School, 2024-2026.
