В ходе лабораторной работы мы используем сверточную нейронную сеть с разным количеством слоев и фильтров на каждом слое.

Нейросеть 1
============

    tf.keras.layers.Input(shape=(224,224,3)),
    tf.keras.layers.Conv2D(filters=8, kernel_size=3),
    tf.keras.layers.MaxPool2D(),
    tf.keras.layers.Conv2D(filters=8, kernel_size=3),
    tf.keras.layers.MaxPool2D(),
    tf.keras.layers.Flatten(),
    tf.keras.layers.Dense(NUM_CLASSES, activation=tf.keras.activations.softmax)
    
    epochs = 200
Тренировочные данные:
 -------
![.](https://github.com/baliffagh/SMOMI/blob/Lab2/graph/2.1trainaccuracy.PNG)
![.](https://github.com/baliffagh/SMOMI/blob/Lab2/graph/2.1trainloss.PNG)

Валидационные данные:
------
![.](https://github.com/baliffagh/SMOMI/blob/Lab2/graph/2.1valaccuracy.PNG)
![.](https://github.com/baliffagh/SMOMI/blob/Lab2/graph/2.1valloss.PNG)

Нейронная сеть с 2 слоями и 8 фильтрами на каждом слое обучилась, примерно за 150-170 эпох, после чего начала деградировать. Что мы может отследить по тому, что график потерь начал возростать, а точность начала падать

Нейросеть 2
============
     tf.keras.layers.Input(shape=(224,224,3)),
     tf.keras.layers.Conv2D(filters=8, kernel_size=3),
     tf.keras.layers.MaxPool2D(),
     tf.keras.layers.Conv2D(filters=8, kernel_size=3),
     tf.keras.layers.MaxPool2D(),
     tf.keras.layers.Conv2D(filters=8, kernel_size=3),
     tf.keras.layers.MaxPool2D(),
     tf.keras.layers.Flatten(),
     tf.keras.layers.Dense(NUM_CLASSES, activation=tf.keras.activations.softmax)
 
     epochs = 200
     
Метрики точности:
-----------
Оранжевый - тренировочные данные,
Синий - валидационные данные

![.](https://github.com/baliffagh/SMOMI/blob/Lab2/graph/2.2trainvalaccuracy200.PNG)

Функция потерь
------------
![.](https://github.com/baliffagh/SMOMI/blob/Lab2/graph/2.2trainvalloss200.PNG)

Для сети с 3 слоями и количеством фильтров равных 8 8 8, мы пытались так же обучить ее за 200 эпох, но этого оказалось мало. Как и 300 эпох соответственно.

       epochs = 300
     
Метрики точности:
-----------
Оранжевый - тренировочные данные,
Синий - валидационные данные

![.](https://github.com/baliffagh/SMOMI/blob/Lab2/graph/2.2trainvalaccuracy300.PNG)

Функция потерь
------------
![.](https://github.com/baliffagh/SMOMI/blob/Lab2/graph/2.2trainvalloss300.PNG)

После чего я стала обучать ее на 400 эпох, но получилось так, что она обучилась за 220-250 эпох, после чего начала деградировать. Это может быть связано со случайным начальным приближением. В одном случае мы попали в такую точку где у нас хорошо растет точность и падают потери, а в другом случает можем оказаться так далеко от самого локальнго минимума и нам понадобиться слишком много времени, что мы прийти к нему. Чем больше и лучше сеть, тем меньше шансов, что наши графики будут так отличаться, но так как наша сеть маленькая и не подходит для решения этой задачи, то такой "рандом" это обычная вешь.

    epochs = 400
     
Метрики точности:
-----------
Оранжевый - тренировочные данные
Синий - валидационные данные

![.](https://github.com/baliffagh/SMOMI/blob/Lab2/graph/2.2trainvalaccuracy400.PNG)

Функция потерь
------------
![.](https://github.com/baliffagh/SMOMI/blob/Lab2/graph/2.2trainvalloss400.PNG)

     epochs = 250
     
Тренировочные данные:
 -------
![.](https://github.com/baliffagh/SMOMI/blob/Lab2/graph/2.2trainaccuracy250.PNG)
![.](https://github.com/baliffagh/SMOMI/blob/Lab2/graph/2.2trainloss250.PNG)

Валидационные данные:
------
![.](https://github.com/baliffagh/SMOMI/blob/Lab2/graph/2.2valaccuracy250.PNG)
![.](https://github.com/baliffagh/SMOMI/blob/Lab2/graph/2.2valloss250.PNG)

Нейросеть 3
============  
        tf.keras.layers.Input(shape=(224,224,3)),
        tf.keras.layers.Conv2D(filters=32, kernel_size=3),
        tf.keras.layers.MaxPool2D(),
        tf.keras.layers.Conv2D(filters=16, kernel_size=3),
        tf.keras.layers.MaxPool2D(),
        tf.keras.layers.Conv2D(filters=8, kernel_size=3),
        tf.keras.layers.MaxPool2D(),
        tf.keras.layers.Flatten(),
        tf.keras.layers.Dense(NUM_CLASSES, activation=tf.keras.activations.softmax)
        
        epochs = 300
Тренировочные данные:
 -------
![.](https://github.com/baliffagh/SMOMI/blob/Lab2/graph/2.3trainaccuracy300.PNG)
![.](https://github.com/baliffagh/SMOMI/blob/Lab2/graph/2.3trainloss300.PNG)

Валидационные данные:
------
![.](https://github.com/baliffagh/SMOMI/blob/Lab2/graph/2.3valaccuracy300.PNG)
![.](https://github.com/baliffagh/SMOMI/blob/Lab2/graph/2.3valloss300.PNG)



Нейросеть 4
============  
        tf.keras.layers.Input(shape=(224,224,3)),
        tf.keras.layers.Conv2D(filters=32, kernel_size=3),
        tf.keras.layers.MaxPool2D(),
        tf.keras.layers.Conv2D(filters=16, kernel_size=3),
        tf.keras.layers.MaxPool2D(),
        tf.keras.layers.Conv2D(filters=8, kernel_size=3),
        tf.keras.layers.MaxPool2D(),
        tf.keras.layers.Conv2D(filters=8, kernel_size=3),
        tf.keras.layers.MaxPool2D(),
        tf.keras.layers.Flatten(),
        tf.keras.layers.Dense(NUM_CLASSES, activation=tf.keras.activations.softmax)
        
        epochs = 400
Тренировочные данные:
 -------
![.](https://github.com/baliffagh/SMOMI/blob/Lab2/graph/2.4trainaccuracy400.PNG)
![.](https://github.com/baliffagh/SMOMI/blob/Lab2/graph/2.4trainloss400.PNG)

Валидационные данные:
------
![.](https://github.com/baliffagh/SMOMI/blob/Lab2/graph/2.4valaccuracy400.PNG)
![.](https://github.com/baliffagh/SMOMI/blob/Lab2/graph/2.4valloss400.PNG)

Нейросеть 5
============

        tf.keras.layers.Input(shape=(224,224,3)),
        tf.keras.layers.Conv2D(filters=64, kernel_size=3),
        tf.keras.layers.MaxPool2D(),
        tf.keras.layers.Conv2D(filters=32, kernel_size=3),
        tf.keras.layers.MaxPool2D(),
        tf.keras.layers.Conv2D(filters=16, kernel_size=3),
        tf.keras.layers.MaxPool2D(),
        tf.keras.layers.Conv2D(filters=8, kernel_size=3),
        tf.keras.layers.MaxPool2D(),
        tf.keras.layers.Flatten(),
        tf.keras.layers.Dense(NUM_CLASSES, activation=tf.keras.activations.softmax)
        
        epochs = 400
Тренировочные данные:
 -------
![.](https://github.com/baliffagh/SMOMI/blob/Lab2/graph/2.5trainaccuracy400.PNG)
![.](https://github.com/baliffagh/SMOMI/blob/Lab2/graph/2.5trainloss400.PNG)

Валидационные данные:
------
![.](https://github.com/baliffagh/SMOMI/blob/Lab2/graph/2.5valaccuracy400.PNG)
![.](https://github.com/baliffagh/SMOMI/blob/Lab2/graph/2.5valloss400.PNG)

Нейросеть 6
============ 
        tf.keras.layers.Input(shape=(224,224,3)),
        tf.keras.layers.Conv2D(filters=8, kernel_size=3),
        tf.keras.layers.MaxPool2D(),
        tf.keras.layers.Conv2D(filters=16, kernel_size=3),
        tf.keras.layers.MaxPool2D(),
        tf.keras.layers.Conv2D(filters=32, kernel_size=3),
        tf.keras.layers.MaxPool2D(),
        tf.keras.layers.Conv2D(filters=64, kernel_size=3),
        tf.keras.layers.MaxPool2D(),
        tf.keras.layers.Flatten(),
        tf.keras.layers.Dense(NUM_CLASSES, activation=tf.keras.activations.softmax)
        
        epochs = 300
Тренировочные данные:
 -------
![.](https://github.com/baliffagh/SMOMI/blob/Lab2/graph/2.6trainaccuracy300.PNG)
![.](https://github.com/baliffagh/SMOMI/blob/Lab2/graph/2.6trainloss300.PNG)

Валидационные данные:
------
![.](https://github.com/baliffagh/SMOMI/blob/Lab2/graph/2.6valaccuracy300.PNG)
![.](https://github.com/baliffagh/SMOMI/blob/Lab2/graph/2.6valloss300.PNG)

