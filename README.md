# Predição de Doença Cardíaca com Machine Learning

Projeto de Machine Learning aplicado à área da saúde,
comparando 4 modelos de classificação para predição de doença arterial 
coronariana, com foco em interpretabilidade clínica e análise de limiar 
de decisão.

## Sobre o dataset

O [Cleveland Heart Disease Dataset](https://archive.ics.uci.edu/dataset/45/heart+disease) 
foi escolhido por ser o benchmark mais utilizado na literatura de ML aplicado 
à cardiologia. Apesar das limitações conhecidas (303 pacientes, dados de 1988), 
suas variáveis têm significado clínico bem documentado e os resultados são 
comparáveis com a literatura existente.

O objetivo não é construir um modelo pronto para produção, mas demonstrar o 
raciocínio analítico completo, da EDA à interpretabilidade, num domínio de 
alto impacto.

## Estrutura

1. Carregamento e limpeza dos dados
2. Análise exploratória (EDA)
3. Pré-processamento
4. Modelagem — Regressão Logística, Árvore de Decisão, Random Forest, XGBoost
5. Avaliação do modelo final
6. Interpretabilidade — coeficientes e SHAP values
7. Conclusões clínicas

## Principais resultados

- **Melhor modelo:** Regressão Logística Otimizada (AUC-ROC: 0.9632)
- **Overfitting confirmado** em Random Forest e XGBoost (AUC treino = 1.0)
- **Limiar para triagem inicial:** 0.25-0.30 — 0 a 1 falso negativo
- **Limiar para confirmação diagnóstica:** 0.57 — F1 de 0.89 (equilíbrio ótimo)
- **Principais preditores:** número de vasos comprometidos, tipo de dor no 
  peito e resultado do teste de estresse com tálio

## Como executar

**Opção 1 — Google Colab (recomendado):**

[![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1nApc9JjPRjU7mjibykisZXq-ZuzgiSDw#scrollTo=uexabFf3r4VJ)

Todas as dependências são instaladas automaticamente na primeira célula.

**Opção 2 — Ambiente local:**
```bash
git clone https://github.com/meurii/heart-disease-ml-classification
cd heart-disease-ml-classification
pip install -r requirements.txt
jupyter notebook doenca_cardiaca_ML.ipynb
```

## Stack

Python · Pandas · NumPy · Scikit-learn · XGBoost · SHAP · 
Matplotlib · Seaborn · UCI ML Repository
