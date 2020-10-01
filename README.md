В ходе лабораторной работы мы обучали нейросеть с разным количеством слоев, нейроном на каждом слое и скоростью обучения.
На графиках видно, что при увеличении количества слоев, уменьшается скорость сходиомсти. 
Так же значение скорости влияет на обучение. Слишком маленькое или слишком большое значение приведет к большому количеству ошибок (что видно на 4 и 4 нейронной сети)

Нейросеть 1
============

    tf.keras.layers.Input(shape=(224,224,3)),
    tf.keras.layers.Conv2D(filters=8, kernel_size=3),
    tf.keras.layers.MaxPool2D(),
    tf.keras.layers.Conv2D(filters=8, kernel_size=3),
    tf.keras.layers.MaxPool2D(),
    tf.keras.layers.Flatten(),
    tf.keras.layers.Dense(NUM_CLASSES, activation=tf.keras.activations.softmax)
        
    lr = 0.000001
Метрики точности
-----------------
![hfhf](https://github.com/baliffagh/SMOMI/blob/Lab2/graph/2.1.trainaccuracy.PNG)
![hfhf](https://github.com/baliffagh/SMOMI/blob/Lab2/graph/2.1.valaccuracy.PNG)

Функции потерь
--------------
![hfhf](https://github.com/baliffagh/SMOMI/blob/Lab2/graph/2.1.trainloss.PNG)
![hfhf](https://github.com/baliffagh/SMOMI/blob/Lab2/graph/2.1.valloss.PNG)

Нейросеть 2
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
        
        lr = 0.000001
Метрики точности
-----------------
![hfhf](https://github.com/baliffagh/SMOMI/blob/Lab2/graph/2.2.trainaccuracy.PNG)
![hfhf](https://github.com/baliffagh/SMOMI/blob/Lab2/graph/2.2.valaccuracy.PNG)

Функции потерь
--------------
![hfhf](https://github.com/baliffagh/SMOMI/blob/Lab2/graph/2.2.trainloss.PNG)
![hfhf](https://github.com/baliffagh/SMOMI/blob/Lab2/graph/2.2.valloss.PNG)

Нейросеть 3
============

        tf.keras.layers.Input(shape=(224,224,3)),
        tf.keras.layers.Conv2D(filters=8, kernel_size=3),
        tf.keras.layers.MaxPool2D(),
        tf.keras.layers.Conv2D(filters=16, kernel_size=3),
        tf.keras.layers.MaxPool2D(),
        tf.keras.layers.Conv2D(filters=8, kernel_size=3),
        tf.keras.layers.MaxPool2D(),
        tf.keras.layers.Flatten(),
        tf.keras.layers.Dense(NUM_CLASSES, activation=tf.keras.activations.softmax)
        
        lr = 0.0000001
Метрики точности
-----------------
![hfhf](https://github.com/baliffagh/SMOMI/blob/Lab2/graph/2.3.trainaccuracy.PNG)
![hfhf](https://github.com/baliffagh/SMOMI/blob/Lab2/graph/2.3.valaccuracy.PNG)

Функции потерь
--------------
![hfhf](https://github.com/baliffagh/SMOMI/blob/Lab2/graph/2.3.trainloss.PNG)
![hfhf](https://github.com/baliffagh/SMOMI/blob/Lab2/graph/2.3.valloss.PNG)

Нейросеть 4
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
        
        lr = 0.0001
Метрики точности
-----------------
![hfhf](https://github.com/baliffagh/SMOMI/blob/Lab2/graph/2.4.trainaccuracy.PNG)
![hfhf](https://github.com/baliffagh/SMOMI/blob/Lab2/graph/2.4.valaccuracy.PNG)

Функции потерь
--------------
![hfhf](https://github.com/baliffagh/SMOMI/blob/Lab2/graph/2.4.trainloss.PNG)
![hfhf](https://github.com/baliffagh/SMOMI/blob/Lab2/graph/2.4.valloss.PNG)

Нейросеть 5
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
        
        lr = 0.0000000001
Метрики точности
-----------------
![hfhf](https://github.com/baliffagh/SMOMI/blob/Lab2/graph/2.5.trainaccuracy.PNG)
![hfhf](https://github.com/baliffagh/SMOMI/blob/Lab2/graph/2.5.valaccuracy.PNG)

Функции потерь
--------------
![hfhf](https://github.com/baliffagh/SMOMI/blob/Lab2/graph/2.5.trainloss.PNG)
![hfhf](https://github.com/baliffagh/SMOMI/blob/Lab2/graph/2.5.valloss.PNG)
