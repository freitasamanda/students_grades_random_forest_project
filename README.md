# Student Grade Prediction
Análise de desempenho acadêmico e segmentação de estudantes com Random Forest e K-Means.

---

## Estrutura do Repositório

```
students_grades_random_forest_project/
├── student_grade_prediction copy.ipynb  # Testes estatísticos, modelagem RF & K-Means
├── student_grade_ses_dataset.csv        # Dataset (12.025 registros × 29 colunas)
├── DATA_DICTIONARY.md                   # Dicionário de dados, políticas de nulos e faixas
├── model_card.md                        # Model card do RF Regressor & K-Means
├── relatorio_executivo_rendimento_escolar.html  # Relatório executivo interativo
├── tables/                              # Tabelas analíticas exportadas (CSV)
├── viz/                                 # Gráficos e visualizações exportadas
├── requirements.txt                     # Dependências do projeto
└── index.html                           # Página de portfólio (GitHub Pages)
```

---

## Sobre o Projeto

Este projeto analisa os fatores associados ao desempenho acadêmico de estudantes e identifica perfis de risco por meio de modelos de Machine Learning supervisionado e não supervisionado.

### Objetivos
- Identificar as variáveis socioeconômicas e comportamentais com maior impacto na nota final.
- Construir um modelo preditivo de regressão com Random Forest.
- Segmentar estudantes em perfis de desempenho com K-Means para priorizar intervenções pedagógicas.

### Dataset
- **Fonte:** Kaggle — `student_grade_ses_dataset.csv`
- **Registros:** 12.025
- **Features:** 29 colunas (variáveis socioeconômicas, comportamentais e acadêmicas)
- **Target:** `final_grade_pct` — percentual da nota final do estudante

---

## Metodologia

### 1. Análise Exploratória & Testes Estatísticos
- Medidas de posição e dispersão (média, mediana, desvio-padrão, CV).
- Testes bivariados com correção de Bonferroni.
- Testes t de Student e ANOVA para comparação de grupos.

### 2. Regressão Linear com Diagnóstico Robusto
- Seleção de features via VIF (Variance Inflation Factor).
- Modelagem cumulativa com critério AIC.
- Diagnóstico de resíduos e erros-padrão robustos HC3.

### 3. Random Forest Regressor
- Benchmark de modelos (OLS, Ridge, Lasso, RF).
- Importância por permutação (*Permutation Importance*).

### 4. Segmentação com K-Means
- Diagnóstico do número de clusters via curvas de cotovelo e silhueta.
- Perfilamento dos clusters e recomendações pedagógicas.

---

## Resultados

| Artefato | Descrição |
|---|---|
| [`relatorio_executivo_rendimento_escolar.html`](relatorio_executivo_rendimento_escolar.html) | Relatório executivo completo |
| [`DATA_DICTIONARY.md`](DATA_DICTIONARY.md) | Dicionário de dados |
| [`model_card.md`](model_card.md) | Model card dos modelos treinados |
| [`viz/`](viz/) | Visualizações exportadas |
| [`tables/`](tables/) | Tabelas analíticas em CSV |

---

## Dependências

```bash
pip install -r requirements.txt
```

Principais bibliotecas: `pandas`, `numpy`, `matplotlib`, `seaborn`, `scikit-learn`, `statsmodels`.

---

## Autora

**Amanda Freitas Carnaiba** — [Site pessoal](https://freitasamanda.github.io/)
