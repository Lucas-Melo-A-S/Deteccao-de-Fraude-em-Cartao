# Detecção de Fraude de Cartão de Crédito — Modelo Orientado a Precisão

## 🎯 Objetivo

Maximizar a precisão (precision) mantendo um recall razoável, minimizando falsos positivos em um dataset altamente desbalanceado (~0,17% de fraudes).

## 🔍 Dataset
	•	Fonte: Kaggle – Credit Card Fraud Detection (ULB)
	•	Features: variáveis numéricas transformadas via PCA
	•	Target: Class (1 = Fraude, 0 = Legítima)

## 🧠 Metodologia
	•	Split estratificado em treino / calibração / teste
	•	XGBoost com hiperparâmetros conservadores
	•	Calibração de probabilidades (Sigmoid)
	•	Seleção de threshold baseada em uma precisão-alvo
	•	Avaliação com ROC-AUC, PR-AUC e matriz de confusão

## 📊 Resultados Finais
	•	Precision ≈ 40%
	•	Recall ≈ 82%
	•	Falsos Positivos: 19 – 132 (dependendo do threshold)
	•	Solução robusta, interpretável e orientada a produção

## 📁 Estrutura do Repositório
	•	data/ → dados brutos e processados
	•	notebooks/ → análises passo a passo
	•	src/ → código reutilizável de modelagem e avaliação

## 🚀 Principais Aprendizados
	•	Accuracy é enganosa em problemas de fraude
	•	Ajuste de threshold é tão importante quanto a escolha do modelo
	•	Calibração é essencial para decisões confiáveis

## 📌 Autor
Lucas Melo Silva
Data Science & Machine Learning
