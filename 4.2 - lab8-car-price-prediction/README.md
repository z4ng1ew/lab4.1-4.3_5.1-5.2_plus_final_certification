
# Лабораторная работа №8: Прогнозирование цены автомобиля с помощью линейной регрессии

Данный проект реализует линейную регрессию для предсказания цены подержанных автомобилей Toyota на основе ключевых характеристик: года выпуска, пробега, налога, расхода топлива и объема двигателя.

## 📌 Описание

- Используются данные из файла `toyota.csv`.
- Сравниваются две модели:
  - **Модель 1**: все 5 числовых признаков.
  - **Модель 2**: исключён признак с высокой мультиколлинеарностью (`mileage`).
- Используется библиотека `scikit-learn` для построения моделей.
- Оценка качества моделей — коэффициент детерминации R².
- Визуализация результатов через диаграммы рассеяния и графики сравнения.

## 📦 Требования

- Python 3.8+
- Библиотеки:
  - pandas
  - numpy
  - scikit-learn
  - matplotlib
  - seaborn

Установка зависимостей:

```bash
pip install -r requirements.txt
```

## 📁 Структура проекта

```
.
├── lab8_car_price_prediction.ipynb   # Основной Jupyter Notebook
├── toyota.csv                       # Данные для анализа
└── README.md
```

## 📈 Результаты

- **Модель 1**: R² ≈ 0.76
- **Модель 2**: R² ≈ 0.74  
- Исключение признака `mileage` снижает R², но повышает устойчивость модели к мультиколлинеарности.

## 📊 Визуализация

Сравнительный график прогнозируемой и фактической цены сохраняется в `model_comparison.png`.

## 📚 Использованные материалы

- Набор данных: [Toyota Used Car Listings](https://www.kaggle.com/datasets/)
- Sklearn LinearRegression
- Оценка модели: коэффициент детерминации (R²)

## 🧪 Как запустить

1. Скачайте репозиторий:
   ```bash
   git clone https://github.com/ваш-ник/lab8-car-price-prediction.git
   cd lab8-car-price-prediction
   ```
2. Установите зависимости:
   ```bash
   pip install -r requirements.txt
   ```
3. Откройте Jupyter Notebook:
   ```bash
   jupyter notebook lab8_car_price_prediction.ipynb
   ```
4. Выполните все ячейки.

---

## 🏷️ Topics (для GitHub)

```
machine-learning linear-regression python jupyter-notebook data-analysis car-price-prediction sklearn
```

