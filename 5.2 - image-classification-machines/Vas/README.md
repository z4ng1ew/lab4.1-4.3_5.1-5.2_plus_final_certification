# 🧥 Fashion MNIST Image Classification with CNN

Этот проект решает задачу классификации изображений одежды из датасета **Fashion MNIST** с использованием сверточной нейронной сети (CNN), реализованной на **TensorFlow/Keras**. Модель достигает высокой точности (~92%) за счёт оптимизированной архитектуры, аугментации данных и стратегий регуляризации.

![Fashion MNIST](https://github.com/zalandoresearch/fashion-mnist/raw/master/doc/img/fashion-mnist-sprite.png)



Сылка на датасет - (https://www.kaggle.com/datasets/alxmamaev/flowers-recognition?spm=a2ty_o01.29997173.0.0.4b295171Xm0kYC) 

## 📌 Особенности

- Точность на валидации до **92%**
- Поддержка аугментации данных (`ImageDataGenerator`)
- Использование Batch Normalization и Dropout для борьбы с переобучением
- Динамическое изменение learning rate (`ReduceLROnPlateau`)
- Ранняя остановка обучения (`EarlyStopping`)
- Оптимизированная CNN-архитектура для изображений 28×28

## 🛠️ Используемые технологии

- **Python** 3.x
- **TensorFlow** / **Keras**
- **NumPy**, **Pandas**
- **Matplotlib** (визуализация)
- **Jupyter Notebook** (для разработки)

## 📦 Установка

1. Клонируйте репозиторий.
2. Установите зависимости:
   ```bash
   pip install -r requirements.txt
   ```

   Пример `requirements.txt`:
   ```
   tensorflow>=2.10.0
   numpy>=1.21.0
   pandas>=1.3.0
   matplotlib>=3.4.0
   ```

## ▶️ Запуск

Запустите Jupyter Notebook или Python-скрипт:

```bash
jupyter notebook fashion_mnist_cnn.ipynb
```

Или:
```bash
python fashion_mnist_cnn.py
```

## 🏗️ Архитектура модели

```python
Input(shape=(28, 28, 1))
→ Conv2D(32) → BatchNorm → Conv2D(32) → MaxPool → Dropout(0.25)
→ Conv2D(64) → BatchNorm → Conv2D(64) → MaxPool → Dropout(0.25)
→ Flatten()
→ Dense(128) → BatchNorm → Dropout(0.5)
→ Dense(10, softmax)
```

- Общее количество параметров: **468 714**
- Оптимизатор: **Adam** (с динамическим LR)
- Функция потерь: **Categorical Crossentropy**

## 📈 Результаты обучения

- **Точность на трейне**: ~90.5%
- **Точность на валидации**: ~92.0%
- **Batch size**: 128
- **Epochs**: до 35 (с ранней остановкой)

## 📚 Датасет

[Fashion-MNIST](https://github.com/zalandoresearch/fashion-mnist) — замена классическому MNIST, содержащая 70 000 изображений (28×28) 10 классов одежды:
- T-shirt/top
- Trouser
- Pullover
- Dress
- Coat
- Sandal
- Shirt
- Sneaker
- Bag
- Ankle boot

## 🏷️ GitHub Topics

Добавьте к репозиторию следующие топики:

```
tensorflow
keras
cnn
image-classification
fashion-mnist
deep-learning
computer-vision
neural-network
python
machine-learning
```
