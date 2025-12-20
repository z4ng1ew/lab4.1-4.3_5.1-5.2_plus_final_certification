# 📉 Probability of Default (PD) Model using XGBoost

Данный проект демонстрирует методологию построения модели кредитного скоринга для оценки **вероятности дефолта (PD)** на основе публичного датасета аномальных финансовых транзакций (`creditcard.csv`). Из-за отсутствия реальных данных о кредитных дефолтах, в задаче условно принимается, что:

- `Class = 1` — событие дефолта (мошенническая транзакция)  
- `Class = 0` — отсутствие дефолта

Модель решает задачу **бинарной классификации с сильным дисбалансом классов** и может быть использована в целях:

- определения кредитных cut-off уровней,  
- расчёта ожидаемых потерь (Expected Loss),  
- сегментации клиентов по уровню риска.

---

## 🔍 Основные результаты

- **ROC AUC**: > 0.97 — высокая способность ранжирования риска  
- **F1-score (minor class)**: ~0.72  
- **Важные признаки**: `V14`, `V10`, `V4` и другие анонимизированные PCA-компоненты  
- Поддержка кастомных **cut-off стратегий** принятия решений  

---

## 🛠️ Используемые технологии

- **Язык программирования**: Python  
- **Библиотеки**:
  - `pandas`, `numpy` — обработка и анализ данных  
  - `scikit-learn` — предобработка, метрики (`StandardScaler`, `classification_report`, `roc_auc_score`)  
  - `xgboost` — обучение модели (`XGBClassifier`)  
  - `matplotlib`, `seaborn` — визуализация (ROC-кривая, важность признаков)  
- **Инструменты**: Jupyter Notebook  
- **Методы**:
  - Учёт дисбаланса классов через `scale_pos_weight`  
  - Масштабирование признаков  
  - ROC-анализ и cut-off стратегии  

---

## 📁 Структура проекта

```
.
├── creditcard.csv          # исходный датасет (Kaggle)
├── pd_model.ipynb          # основной Jupyter Notebook
└── README.md
```

> ⚠️ Датасет `creditcard.csv` не включён в репозиторий по лицензионным соображениям. Его можно скачать с [Kaggle](https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud).

---

## 📌 Как запустить

1. Установите зависимости:
   ```bash
   pip install pandas numpy scikit-learn xgboost matplotlib seaborn jupyter
   ```
2. Запустите Jupyter Notebook:
   ```bash
   jupyter notebook pd_model.ipynb
   ```

---

## 🏷️ GitHub Topics

```
credit-risk
default-prediction
xgboost
machine-learning
binary-classification
imbalanced-data
roc-auc
financial-risk
fraud-detection
jupyter-notebook
```

---

## 📚 Источники

- Датасет: [Credit Card Fraud Detection (Kaggle)](https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud)  
- Методология PD оценки: Basel II/III, кредитный скоринг

---

> 💡 Проект выполнен в учебных целях и не предназначен для прямого применения в production-среде без дополнительной валидации и регуляторной экспертизы.

