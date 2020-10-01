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
