# Fashion MNIST: Сравнение архитектур нейросетей

![TensorFlow](https://img.shields.io/badge/TensorFlow-FF6F00?logo=tensorflow&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?logo=python&logoColor=white)
![Keras](https://img.shields.io/badge/Keras-D00000?logo=keras&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-F37626?logo=jupyter&logoColor=white)

Данный проект представляет собой сравнительный анализ трёх различных архитектур нейронных сетей для классификации изображений из датасета **Fashion MNIST** — набора из 70 000 чёрно-белых изображений 28×28 пикселей, представляющих 10 категорий одежды.

## 🎯 Цель

Достичь точности классификации на тестовой выборке **не менее 90%**, протестировав и сравнив следующие модели:

1. **Полносвязная нейронная сеть (MLP)**
2. **Базовая свёрточная нейронная сеть (CNN)**
3. **Оптимизированная CNN** с BatchNormalization, дополнительными свёрточными слоями и улучшенной стратегией обучения

## 📊 Результаты

| Архитектура           | Точность | Время обучения |
|----------------------|----------|----------------|
| Оптимизированная CNN | **93.69%** | ~14.5 мин      |
| Базовая CNN          | 91.90%   | ~4.9 мин       |
| Полносвязная сеть    | 88.56%   | ~0.4 мин       |

✅ **Задача выполнена**: лучшая модель (оптимизированная CNN) превысила требуемый порог точности в 90%.

## 🧠 Используемые технологии и инструменты

- **Python 3** — основной язык программирования
- **TensorFlow + Keras** — фреймворк для построения и обучения нейросетей
- **NumPy, Pandas** — обработка и манипуляция данными
- **Matplotlib** — визуализация графиков обучения
- **Jupyter Notebook** — среда разработки и документирования экспериментов

### Особенности моделей
- Использование **callback-функций**: `EarlyStopping`, `ModelCheckpoint`, `ReduceLROnPlateau`
- Применение **Dropout** и **Batch Normalization** для регуляризации
- Различные оптимизаторы: **Adam**, **RMSprop**
- Обработка данных: нормализация пикселей, one-hot encoding меток

## 📁 Структура проекта

- Единый Jupyter Notebook (`*.ipynb`)
- Сохранённые веса лучших моделей: `mlp_best.keras`, `cnn_best.keras`
- Визуализация кривых обучения и валидации

## ▶️ Как запустить

1. Установите зависимости:
   ```bash
   pip install tensorflow numpy pandas matplotlib jupyter
   ```
2. Запустите Jupyter Notebook:
   ```bash
   jupyter notebook
   ```
3. Откройте файл проекта и выполните все ячейки.

## 📌 GitHub Topics (для репозитория)

```
machine-learning
deep-learning
neural-network
tensorflow
keras
cnn
fashion-mnist
image-classification
jupyter-notebook
python
batch-normalization
dropout
model-comparison
computer-vision
```
