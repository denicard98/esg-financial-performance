# Impact of ESG Factors on Corporate Financial Performance

Dissertação de mestrado (MSc Business Analytics, ISCTE Business School). Estuda o impacto de fatores ESG (Environmental, Social, Governance) na performance financeira de empresas do S&P 500 entre 2019 e 2023, combinando econometria de painel com um modelo de machine learning.

## Objetivo

Testar se scores ESG (e as suas componentes E, S e G) explicam variação na performance financeira das empresas, e comparar o poder explicativo de uma abordagem econométrica clássica com o de um modelo não-linear.

## Metodologia

- **Dados:** painel de empresas do S&P 500, 2019–2023
- **Modelo econométrico:** regressão em painel com efeitos fixos (fixed-effects panel econometrics), para controlar heterogeneidade não observada entre empresas e ao longo do tempo
- **Modelo de machine learning:** Random Forest, para captar relações não-lineares entre variáveis ESG e performance financeira, e como validação/comparação face ao modelo econométrico
- **Ferramentas:** Python (pandas, statsmodels/linearmodels, scikit-learn)

## Estrutura do repositório

```
esg-financial-performance/
├── data/              # dados usados (ou script de recolha, se os dados não puderem ser redistribuídos)
├── notebooks/         # exploração de dados, modelo de painel, Random Forest
├── src/                # funções auxiliares reutilizadas nos notebooks
├── report/             # dissertação final / resumo executivo
└── README.md
```

## Principais resultados

<!-- TODO: resumir aqui, em 3-5 bullets, as conclusões da dissertação:
- que variáveis ESG (E, S, G) tiveram efeito estatisticamente significativo na performance financeira
- direção e magnitude do efeito
- como o Random Forest se comparou ao modelo de painel (ex.: variáveis mais importantes, poder preditivo)
-->

## Como reproduzir

```bash
pip install -r requirements.txt
jupyter notebook notebooks/
```

## Próximos passos

<!-- TODO: ex. "adicionar dados de 2024", "testar efeitos aleatórios como robustez", etc. -->

---
*Projeto académico — ISCTE Business School, 2024–2026.*
