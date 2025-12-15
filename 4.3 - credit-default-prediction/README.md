# Прогнозирование Кредитного Дефолта

Этот проект представляет собой модель машинного обучения для оценки вероятности дефолта (невыполнения обязательств) по кредиту на основе данных заемщика.

## Описание

Проект анализирует набор данных `German Credit Data` и использует два алгоритма машинного обучения:
1.  **Логистическая регрессия (Logistic Regression)**
2.  **Случайный лес (Random Forest)**

Модель оценивает вероятность дефолта для нового клиента, учитывая такие признаки, как возраст, пол, занятость, жилищные условия, состояние банковских счетов, сумму кредита, срок и цель кредита.

## Основные функции

*   **Визуализация данных:** Анализ распределения признаков и целевой переменной.
*   **Подготовка данных:** Кодирование категориальных переменных, масштабирование признаков.
*   **Обучение и сравнение моделей:** Сравнение производительности Logistic Regression и Random Forest.
*   **Оценка модели:** Использование метрик `ROC AUC`, `Precision`, `Recall` и `Classification Report`.
*   **Интерпретация модели:** Анализ важности признаков для модели Random Forest.
*   **Прогноз для нового клиента:** Готовая функция для оценки риска дефолта для новых заявок.

## Установка и запуск

1.  Клонируйте репозиторий:
    ```bash
    git clone https://github.com/your-username/credit-default-prediction.git
    cd credit-default-prediction
    ```
2.  Установите необходимые зависимости:
    ```bash
    pip install -r requirements.txt
    ```
3.  Запустите Jupyter Notebook и откройте файл `credit_default_prediction.ipynb`.

## Файлы в репозитории

*   `credit_default_prediction.ipynb`: Основной Jupyter Notebook с кодом и пояснениями.
*   `german_credit_data.csv`: Исходный набор данных.

## Используемые технологии

*   Python
*   Scikit-learn
*   Pandas
*   NumPy
*   Matplotlib
*   Seaborn
```

---

### Файл `requirements.txt`

На основе вашего кода, файл `requirements.txt` должен содержать:

```txt
pandas
numpy
matplotlib
seaborn
scikit-learn
```

---

### Topics для GitHub

```
machine-learning credit-risk credit-scoring jupyter-notebook python sklearn data-science classification random-forest logistic-regression
```