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
    
    
    lr=0.0001
    
    
    lr=0.0000001
    
Задача 3.3 c
============

Создали веса MobileNetV2, предобученной на наборе данных imagenet
Применяя процедуру модификации весов согласно метода градиентного спуска ко всей нейронной сети обучили нейронную сеть с разными темпами обучения

Задача 3.3 d
============

Применяя процедуру модификации весов согласно метода градиентного спуска только к слоям классификатора обучили нейронную сеть с разными темпами обучения и сохранили полученую нейронную сеть

Задача 3.3 e
============

Применяя процедуру модификации весов согласно метода градиентного спуска ко всей нейронной сети, предобученной в пункте 3d обучили нейронную сеть с разными темпами обучения
