В ходе лабораторной работы мы используем сверточную нейронную сеть с разным количеством слоев и нейронов на каждом слое.

Нейросеть 1
============

    tf.keras.layers.Input(shape=(224,224,3)),
    tf.keras.layers.Conv2D(filters=8, kernel_size=3),
    tf.keras.layers.MaxPool2D(),
    tf.keras.layers.Conv2D(filters=8, kernel_size=3),
    tf.keras.layers.MaxPool2D(),
    tf.keras.layers.Flatten(),
    tf.keras.layers.Dense(NUM_CLASSES, activation=tf.keras.activations.softmax)
        
Метрики точности
-----------------
![hfhf](https://github.com/baliffagh/SMOMI/blob/Lab2/graph/2.1.trainaccuracy.PNG)
![hfhf](https://github.com/baliffagh/SMOMI/blob/Lab2/graph/2.1.valaccuracy.PNG)

Функции потерь
--------------
![hfhf](https://github.com/baliffagh/SMOMI/blob/Lab2/graph/2.1.trainloss.PNG)
![hfhf](https://github.com/baliffagh/SMOMI/blob/Lab2/graph/2.1.valloss.PNG)

Первая нейронная сеть без внесения изменений.

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
        
Метрики точности
-----------------
![hfhf](https://github.com/baliffagh/SMOMI/blob/Lab2/graph/2.2.trainaccuracy.PNG)
![hfhf](https://github.com/baliffagh/SMOMI/blob/Lab2/graph/2.2.valaccuracy.PNG)

Функции потерь
--------------
![hfhf](https://github.com/baliffagh/SMOMI/blob/Lab2/graph/2.2.trainloss.PNG)
![hfhf](https://github.com/baliffagh/SMOMI/blob/Lab2/graph/2.2.valloss.PNG)

Мы дабавли еще один слой и мы видим, что точность упала. С добавлением слоя нам требуется бульшее количество эпох, что бы она дообучилась до уровня первой сети.

Нейросеть 3
============

        tf.keras.layers.Input(shape=(224,224,3)),
        tf.keras.layers.Conv2D(filters=32, kernel_size=3),
        tf.keras.layers.MaxPool2D(),
        tf.keras.layers.Conv2D(filters=8, kernel_size=3),
        tf.keras.layers.MaxPool2D(),
        tf.keras.layers.Conv2D(filters=8, kernel_size=3),
        tf.keras.layers.MaxPool2D(),
        tf.keras.layers.Flatten(),
        tf.keras.layers.Dense(NUM_CLASSES, activation=tf.keras.activations.softmax)
        
Метрики точности
-----------------
![hfhf](https://github.com/baliffagh/SMOMI/blob/Lab2/graph/2.3.trainaccuracy.PNG)
![hfhf](https://github.com/baliffagh/SMOMI/blob/Lab2/graph/2.3.valaccuracy.PNG)

Функции потерь
--------------
![hfhf](https://github.com/baliffagh/SMOMI/blob/Lab2/graph/2.3.trainloss.PNG)
![hfhf](https://github.com/baliffagh/SMOMI/blob/Lab2/graph/2.3.valloss.PNG)

С добавлением нейронов на слое, нейронная сеть обучается быстрее, но ей все еще не хватает эпох, что бы достичь лучшего результата.

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
        
Метрики точности
-----------------
![hfhf](https://github.com/baliffagh/SMOMI/blob/Lab2/graph/2.4.trainaccuracy.PNG)
![hfhf](https://github.com/baliffagh/SMOMI/blob/Lab2/graph/2.4.valaccuracy.PNG)

Функции потерь
--------------
![hfhf](https://github.com/baliffagh/SMOMI/blob/Lab2/graph/2.4.trainloss.PNG)
![hfhf](https://github.com/baliffagh/SMOMI/blob/Lab2/graph/2.4.valloss.PNG)

Мы снова добавили слой, точность снова упала и нужно гараздо больше эпох.

Нейросеть 5
============

        tf.keras.layers.Input(shape=(224,224,3)),
        tf.keras.layers.Conv2D(filters=32, kernel_size=3),
        tf.keras.layers.MaxPool2D(),
        tf.keras.layers.Conv2D(filters=16, kernel_size=3),
        tf.keras.layers.MaxPool2D(),
        tf.keras.layers.Conv2D(filters=16, kernel_size=3),
        tf.keras.layers.MaxPool2D(),
        tf.keras.layers.Conv2D(filters=8, kernel_size=3),
        tf.keras.layers.MaxPool2D(),
        tf.keras.layers.Flatten(),
        tf.keras.layers.Dense(NUM_CLASSES, activation=tf.keras.activations.softmax)
        
Метрики точности
-----------------
![hfhf](https://github.com/baliffagh/SMOMI/blob/Lab2/graph/2.5.trainaccuracy.PNG)
![hfhf](https://github.com/baliffagh/SMOMI/blob/Lab2/graph/2.5.valaccuracy.PNG)

Функции потерь
--------------
![hfhf](https://github.com/baliffagh/SMOMI/blob/Lab2/graph/2.5.trainloss.PNG)
![hfhf](https://github.com/baliffagh/SMOMI/blob/Lab2/graph/2.5.valloss.PNG)

С добавлением нейронов на слоях, у нас снова она обучается быстрее, но все еще не хватает эпох.

Можно сделать вывод, что для хорошего обучения с увеличением слоев нужно увеличивать количество эпох и количество нейронов на слоях.
