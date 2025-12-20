# Классификация изображений одежды на Fashion-MNIST  
**Сравнение архитектур нейросетей для задачи классификации Fashion-MNIST (оптимизированная версия для CPU)**

![Fashion-MNIST](https://github.com/zalandoresearch/fashion-mnist/raw/master/doc/img/fashion-mnist-sprite.png)

## 📌 Описание  
Проект направлен на сравнение трёх архитектур нейронных сетей на датасете **Fashion-MNIST** (альтернатива классическому MNIST с изображениями модной одежды):  

1. **Полносвязная нейронная сеть (MLP)**  
2. **Лёгкая свёрточная нейронная сеть (CNN)**  
3. **Оптимальная CNN для CPU** (с Batch Normalization, Dropout и адаптивным learning rate)  

Цель — достичь точности **не менее 90%** на тестовой выборке, при этом оптимизируя время обучения для CPU.

---

## 📊 Результаты

| Архитектура                | Точность на тесте | Время обучения |
|---------------------------|-------------------|----------------|
| **Оптимальная CNN**       | **0.9289**        | 12.02 мин      |
| Лёгкая CNN                | 0.9121            | 2.26 мин       |
| Полносвязная сеть (MLP)   | 0.8852            | 0.28 мин       |

✅ **Задача выполнена успешно**: достигнута точность **92.89%**, что превосходит требуемый порог в **90%**.

![Примеры предсказаний лучшей модели](attachment:prediction_examples.png)

---

## 🧠 Используемые технологии и библиотеки

- **Python 3.12**
- **TensorFlow / Keras** — создание и обучение моделей
- **NumPy**, **Pandas** — обработка и манипуляции с данными
- **Matplotlib** — визуализация результатов
- **Jupyter Notebook** — среда разработки и отчёта
- **Fashion-MNIST** — стандартный датасет (70 000 изображений 28×28 в 10 классах одежды)

---

## 🔧 Архитектура лучших моделей

### 1. Оптимальная CNN (лучшая по точности)
- Conv2D → Conv2D → MaxPooling → BatchNorm → Dropout  
- Conv2D → Conv2D → MaxPooling → BatchNorm → Dropout  
- Flatten → Dense → BatchNorm → Dropout → Dense(10, softmax)  
- Optimizer: **Adam** с адаптивным learning rate  
- Время обучения: **~12 минут**

### 2. Лёгкая CNN
- Conv2D → MaxPooling → Dropout  
- Conv2D → MaxPooling → Dropout  
- Conv2D → MaxPooling → Dropout  
- Flatten → Dense → Dropout → Dense(10, softmax)  
- Optimizer: **Adam**  
- Время обучения: **~2.3 минуты**

### 3. Полносвязная сеть (MLP)
- Dense(256) → Dropout → Dense(128) → Dropout → Dense(10, softmax)  
- Optimizer: **Adam**  
- Время обучения: **~0.3 минуты**

---

## 📁 Структура проекта

```
.
├── fashion_mnist_cpu_optimized.ipynb   # Основной Jupyter Notebook
└── README.md                           # Документация (этот файл)
```


## 📌 GitHub Topics (для раздела Topics в репозитории)

```
tensorflow keras fashion-mnist neural-networks computer-vision deep-learning jupyter-notebook cnn cpu-optimization
```


---

## ✅ Заключение

- **Свёрточные нейросети значительно превосходят полносвязные** в классификации изображений.
- **Оптимизированная CNN с Batch Normalization и адаптивным learning rate** показала наилучший результат (92.89%).
- Даже **лёгкая CNN уверенно перевыполнила требование по точности**, при этом обучаясь всего за 2.3 минуты на CPU.
- Проект демонстрирует важность выбора архитектуры и техник регуляризации при решении задач компьютерного зрения на CPU.

---

> 💡 **Примечание**: Все модели обучались **без GPU**, что делает результаты особенно релевантными для CPU-сценариев.

