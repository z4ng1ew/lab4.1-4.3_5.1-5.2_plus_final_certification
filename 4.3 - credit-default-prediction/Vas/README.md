# 📊 Прогнозирование Вероятности Кредитного Дефолта

Этот проект демонстрирует построение и сравнение двух моделей машинного обучения — **Логистической регрессии** и **Random Forest** — для прогнозирования вероятности дефолта клиента по кредитной карте. В качестве данных используется публичный датасет **[UCI Credit Card](https://archive.ics.uci.edu/ml/datasets/default+of+credit+card+clients)**, содержащий информацию о 30 000 клиентах, включая демографические данные, историю платежей, балансы и суммы платежей.

Модель предназначена для:
- оценки кредитоспособности новых клиентов,
- расчёта вероятности дефолта (PD),
- сегментации клиентов по уровню риска.

---

## 🔍 Ключевые результаты

- **ROC AUC (Random Forest)**: **0.776**  
- **ROC AUC (Logistic Regression)**: **0.716**  
- **Кросс-валидация (RF)**: **0.780 ± 0.005**  
- **Точность (Accuracy)**: до **78.3%**  
- Поддержка интерактивного прогноза для новых клиентов

---

## 🛠️ Используемые технологии

- **Язык программирования**: Python  
- **Библиотеки**:
  - `pandas`, `numpy` — загрузка, обработка и анализ данных  
  - `scikit-learn` — масштабирование (`StandardScaler`), модели (`LogisticRegression`, `RandomForestClassifier`), метрики (`classification_report`, `roc_auc_score`, `confusion_matrix`)  
  - `imbalanced-learn (imblearn)` — балансировка классов (`SMOTE`)  
  - `matplotlib`, `seaborn` — визуализация результатов  
- **Методы**:
  - Feature Engineering (создание `PAY_MEAN`, `PAYMENT_RATIO`)  
  - Балансировка несбалансированных классов (SMOTE + `class_weight='balanced'`)  
  - Кросс-валидация (5-fold)  
  - ROC-анализ и матрица ошибок

---

## 📁 Структура проекта

```
.
├── UCI_Credit_Card.csv       # исходный датасет (не включён в репо)
├── credit_default_model.ipynb # основной Jupyter Notebook
└── README.md
```

> ⚠️ Датасет `UCI_Credit_Card.csv` не включён в репозиторий по лицензионным причинам. Его можно скачать с [официальной страницы UCI](https://archive.ics.uci.edu/ml/datasets/default+of+credit+card+clients).

---

## 📌 Как запустить

1. Установите зависимости:
   ```bash
   pip install pandas numpy scikit-learn matplotlib seaborn imbalanced-learn jupyter
   ```
2. Скачайте датасет и положите его в корневую папку проекта.
3. Запустите Jupyter Notebook:
   ```bash
   jupyter notebook credit_default_model.ipynb
   ```

---

## 🏷️ GitHub Topics 

```
credit-risk
default-prediction
machine-learning
random-forest
logistic-regression
imbalanced-data
roc-auc
feature-engineering
smote
jupyter-notebook
```

---

## 💡 Возможности

- **Интерактивный прогноз**: встроенная функция `predict_default_probability()` позволяет оценить риск для новых клиентов.
- **Диагностика модели**: визуализации включают ROC-кривые, матрицу ошибок, важность признаков и распределение предсказанных вероятностей.
- **Деловая рекомендация**: автоматическая классификация клиента на **низкий**, **средний** или **высокий** риск дефолта.

---

> 💡 Проект выполнен в учебных и исследовательских целях и не предназначен для прямого применения в production-среде без дополнительной валидации и регуляторной экспертизы.

