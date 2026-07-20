# Automatic Modulation Classification (AMC) com RadioML 2018.01A

Trabalho Final da disciplina **PGE00029 – Supervised Machine Learning**,
Programa de Pós-Graduação em Engenharia Elétrica Interunidades — UNESP.

**Autor:** Cleyslon Junio Pereira dos Santos
**Docente:** Prof. Dr. Alexandre da Silva Simões

## Objetivo

Classificação automática de modulação (AMC) utilizando o dataset
**RadioML 2018.01A**, comparando três abordagens supervisionadas:

- **KNN** (baseline)
- **MLP** (baseline)
- **CNN 1D** (modelo principal)

## Resultados (conjunto de teste)

| Modelo | Accuracy | F1 (macro) | Tempo de treino |
|--------|----------|------------|-----------------|
| KNN    | 0.2012   | 0.1945     | ~0.2 s          |
| MLP    | 0.1945   | 0.1698     | ~45.8 s         |
| CNN 1D | 0.5532   | 0.5640     | ~1005.6 s       |

## Estrutura do repositório

- `notebooks/` → notebook completo (Google Colab)
- `results/figures/` → figuras geradas (EDA, curvas de treino, matrizes de confusão, etc.)
- `results/metrics/` → métricas em CSV

## Dataset

RadioML 2018.01A (DeepSig) — **não incluído no repositório** por tamanho
(~21.45 GB). Necessário baixar separadamente.

## Como executar

1. Abrir o notebook em `notebooks/` no Google Colab.
2. Montar o Google Drive e apontar o caminho do dataset RadioML 2018.01A.
3. Executar as células em ordem (EDA → pré-processamento → KNN → MLP → CNN 1D → avaliação).

## Reprodutibilidade

Todos os experimentos usam semente fixa (`SEMENTE = 135`) para Python, NumPy e PyTorch (CPU/GPU).
