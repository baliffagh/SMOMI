В данной лаборатоной работе мы занимались обучением нейронных сетей с использованием техники Transfer Learning
Создали случайно инициализированную нейронную сеть MobileNetV2. Обучили данную сеть со случайным начальным приближением и разными темпами обучения

Задача 3.2
===========

    return tf.keras.applications.MobileNetV2(
    input_shape=(224,224,3),
    classes = NUM_CLASSES,
    include_top=True,
    weights=None)
    lr = 0.000001
    
Метрики точности:
 -------
 
Зеленый - валидационные данные, розовый - тренировочные данные
 
![.](https://github.com/baliffagh/SMOMI/blob/Lab3/graph/3.1.1trainvalaccuracy.PNG)

Функции потерь:
------

Зеленый - валидационные данные, розовый - тренировочные данные

![.](https://github.com/baliffagh/SMOMI/blob/Lab3/graph/3.1.1trainvalloss.PNG)
    
    lr=0.0001
    
Метрики точности:
 -------
 
Синий - валидационные данные, оранжевый - тренировочные данные
 
![.](https://github.com/baliffagh/SMOMI/blob/Lab3/graph/3.1.2trainvalaccuracy.PNG)

Функции потерь:
------

Синий - валидационные данные, оранжевый - тренировочные данные

![.](https://github.com/baliffagh/SMOMI/blob/Lab3/graph/3.1.2trainvalloss.PNG)
    
    lr=0.0000001
    
Метрики точности:
 -------
 
Синий - валидационные данные, оранжевый - тренировочные данные
 
![.](https://github.com/baliffagh/SMOMI/blob/Lab3/graph/3.1.3trainvalaccuracy.PNG)

Функции потерь:
------

Синий - валидационные данные, оранжевый - тренировочные данные

![.](https://github.com/baliffagh/SMOMI/blob/Lab3/graph/3.1.3trainvalloss.PNG)
    
Задача 3.3 c
============

Создали веса MobileNetV2, предобученной на наборе данных imagenet

Применяя процедуру модификации весов согласно метода градиентного спуска ко всей нейронной сети обучили нейронную сеть с разными темпами обучения

    lr=0.000001
    
Метрики точности:
 -------
 
Голубой - валидационные данные, Красный - тренировочные данные
 
![.](https://github.com/baliffagh/SMOMI/blob/Lab3/graph/3.2.1trainvalaccuracy.PNG)

Функции потерь:
------

Голубой - валидационные данные, Красный - тренировочные данные

![.](https://github.com/baliffagh/SMOMI/blob/Lab3/graph/3.2.1trainvalloss.PNG)

    lr=0.0001
    
Метрики точности:
 -------
 
Синий - валидационные данные, оранжевый - тренировочные данные
 
![.](https://github.com/baliffagh/SMOMI/blob/Lab3/graph/3.2.2trainvalaccuracy.PNG)

Функции потерь:
------

Синий - валидационные данные, оранжевый - тренировочные данные

![.](https://github.com/baliffagh/SMOMI/blob/Lab3/graph/3.2.2trainvalloss.PNG)

    lr=0.0000005
    
Метрики точности:
 -------
 
Синий - валидационные данные, оранжевый - тренировочные данные
 
![.](https://github.com/baliffagh/SMOMI/blob/Lab3/graph/3.2.3trainvalaccuracy.PNG)

Функции потерь:
------

Синий - валидационные данные, оранжевый - тренировочные данные

![.](https://github.com/baliffagh/SMOMI/blob/Lab3/graph/3.2.3trainvalloss.PNG)

Задача 3.3 d
============

Применяя процедуру модификации весов согласно метода градиентного спуска только к слоям классификатора обучили нейронную сеть с разными темпами обучения и сохранили полученую нейронную сеть

    lr=0.000001
    
Метрики точности:
 -------
 
 Синий - валидационные данные, оранжевый - тренировочные данные
 
![.](https://github.com/baliffagh/SMOMI/blob/Lab3/graph/3.3.1trainvalaccuracy.PNG)

Функции потерь:
------

Синий - валидационные данные, оранжевый - тренировочные данные

![.](https://github.com/baliffagh/SMOMI/blob/Lab3/graph/3.3.1trainvalloss.PNG)

    lr=0.0001
    
Метрики точности:
 -------
 
Голубой - валидационные данные, Красный - тренировочные данные
 
![.](https://github.com/baliffagh/SMOMI/blob/Lab3/graph/3.3.2trainvalaccuracy.PNG)

Функции потерь:
------

Голубой - валидационные данные, Красный - тренировочные данные

![.](https://github.com/baliffagh/SMOMI/blob/Lab3/graph/3.3.2trainvalloss.PNG)

    lr=0.0000005
    
Метрики точности:
 -------
 
Синий - валидационные данные, оранжевый - тренировочные данные
 
![.](https://github.com/baliffagh/SMOMI/blob/Lab3/graph/3.3.3trainvalaccuracy.PNG)

Функции потерь:
------

Синий - валидационные данные, оранжевый - тренировочные данные

![.](https://github.com/baliffagh/SMOMI/blob/Lab3/graph/3.3.3trainvalloss.PNG)

Задача 3.3 e
============

Применяя процедуру модификации весов согласно метода градиентного спуска ко всей нейронной сети, предобученной в пункте 3d обучили нейронную сеть с разными темпами обучения

    lr=0.000001
    
Метрики точности:
 -------
 
 Синий - валидационные данные, оранжевый - тренировочные данные
 
![.](https://github.com/baliffagh/SMOMI/blob/Lab3/graph/3.4.1trainvalaccuracy.PNG)

Функции потерь:
------

Синий - валидационные данные, оранжевый - тренировочные данные

![.](https://github.com/baliffagh/SMOMI/blob/Lab3/graph/3.4.1trainvalloss.PNG)

    lr=0.0001
    
Метрики точности:
 -------
 
Синий - валидационные данные, оранжевый - тренировочные данные
 
![.](https://github.com/baliffagh/SMOMI/blob/Lab3/graph/3.4.2trainvalaccuracy.PNG)

Функции потерь:
------

Синий - валидационные данные, оранжевый - тренировочные данные

![.](https://github.com/baliffagh/SMOMI/blob/Lab3/graph/3.4.2trainvalloss.PNG)

    lr=0.0000005
    
Метрики точности:
 -------
 
Синий - валидационные данные, оранжевый - тренировочные данные
 
![.](https://github.com/baliffagh/SMOMI/blob/Lab3/graph/3.4.3trainvalaccuracy.PNG)

Функции потерь:
------

Синий - валидационные данные, оранжевый - тренировочные данные

![.](https://github.com/baliffagh/SMOMI/blob/Lab3/graph/3.4.3trainvalloss.PNG)

