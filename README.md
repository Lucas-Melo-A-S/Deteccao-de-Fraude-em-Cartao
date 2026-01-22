# Detecção de Fraude em Cartões de Crédito — Modelo Orientado a Decisão

## 🎯 Objetivo

Construir um modelo de detecção de fraude orientado a decisão de negócio, maximizando o recall e mantendo a precision sob controle, de forma explícita e defensável, em um dataset extremamente desbalanceado (~0,17% de fraudes).

O foco não é apenas performance estatística, mas reduzir falsos positivos mantendo alta capacidade de captura de fraudes.


## 🔍 Dataset
	•	Fonte: Kaggle — Credit Card Fraud Detection (ULB)
	•	Features: variáveis numéricas anonimizadas via PCA (V1 a V28)
	•	Target: Class
	•	1 → Fraude
	•	0 → Transação legítima


## 🧠 Metodologia
	•	Split estratificado em:
	•	treino
	•	calibração
	•	teste (hold-out real)
	•	Pipeline leakage-safe
	•	XGBoost com hiperparâmetros conservadores (controle de overfitting)
	•	Calibração de probabilidades (Sigmoid)
	•	Definição explícita de threshold baseada em precisão-alvo
	•	Avaliação com:
	•	ROC-AUC
	•	PR-AUC
	•	KS
	•	Matriz de confusão


## 📊 Resultados Finais (Conjunto de Teste)
	•	Precision: ≈ 34%
	•	Recall: ≈ 85%
	•	ROC-AUC: ≈ 0.96
	•	PR-AUC: ≈ 0.69
	•	KS: ≈ 0.86

### Matriz de Confusão (teste):
	•	Verdadeiros Negativos (TN): ~85.053
	•	Falsos Positivos (FP): ~242
	•	Falsos Negativos (FN): ~22
	•	Verdadeiros Positivos (TP): ~126
	
	➡️ Resultado operacionalmente realista, com alto poder de captura de fraude e controle consciente de falsos positivos.


## 📁 Estrutura do Repositório
	•	data/ → dados brutos e datasets intermediários
	•	notebooks/ → análises exploratórias e pipeline explicada passo a passo
	•	src/ → código reutilizável para treino, calibração e avaliação


## 🚀 Principais Aprendizados
	•	Accuracy é enganosa em problemas de fraude
	•	Métricas de ranking (ROC-AUC) não são suficientes sem threshold explícito
	•	Calibração de probabilidades é essencial para decisões confiáveis
	•	A definição de threshold é uma decisão de negócio, não apenas técnica
	•	Modelos com métricas “perfeitas” geralmente escondem leakage ou overfitting


## ⚠️ Limitações
	•	Dataset totalmente anonimizado via PCA
	•	Padrões de fraude mais “limpos” que cenários produtivos reais
	•	Métricas como KS e Gini tendem a ser infladas em relação à produção


## 📌 Autor

Lucas Melo Silva
Data Science • Machine Learning • Modelagem Preditiva
