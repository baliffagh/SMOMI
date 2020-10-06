В ходе лабораторной работы исследовала влияние методов аугментации данных на процесс обучения нейронной сети MobileNetV2 в контексте решения задачи классификации с использованием набора данных Intel Image Classification
С использованием лабораторной #3 обучила нейронную сеть использованием следующих техник аугментации данных и определила их оптимальные параметры:

1.Горизонтальное отражение
========================

    image = tf.image.random_flip_left_right(image)
Метрики точности
-
Синий - валидационные данные, оранжевый - тренировочные данные
![.](https://github.com/baliffagh/SMOMI/blob/Lab4/graph/4fliptrainvalacc.PNG)

Функции потерь
-
Синий - валидационные данные, оранжевый - тренировочные данные
![.](https://github.com/baliffagh/SMOMI/blob/Lab4/graph/4fliptrainvalloss.PNG)


2.Поворот на случайный угол
========================

    
Метрики точности
-
Синий - валидационные данные, оранжевый - тренировочные данные
![.]()

Функции потерь
-
Синий - валидационные данные, оранжевый - тренировочные данные
![.]()

3.Изменение яркости и контраста
========================
1 сеть
-
    image = tf.image.random_brightness(image, 0.6, seed=None)
    image = tf.image.random_contrast(image, 0.4, 1.4, seed=None)
Метрики точности
-
Синий - валидационные данные, оранжевый - тренировочные данные
![.](https://github.com/baliffagh/SMOMI/blob/Lab4/graph/4.1BCtrainvalacc.PNG)

Функции потерь
-
Синий - валидационные данные, оранжевый - тренировочные данные
![.](https://github.com/baliffagh/SMOMI/blob/Lab4/graph/4.1BCtrainvalloss.PNG)

2сеть
-

    image = tf.image.random_brightness(image, 0.5, seed=None)
    image = tf.image.random_contrast(image, 0.5, 1.5, seed=None)
Метрики точности
-
Синий - валидационные данные, оранжевый - тренировочные данные
![.](https://github.com/baliffagh/SMOMI/blob/Lab4/graph/4.2BCtrainvalacc.PNG)

Функции потерь
-
Синий - валидационные данные, оранжевый - тренировочные данные
![.](https://github.com/baliffagh/SMOMI/blob/Lab4/graph/4.2BCtrainvalloss.PNG)

3 сеть
-

    image = tf.image.random_brightness(image, 0.7, seed=None)
    image = tf.image.random_contrast(image, 0.3, 1.3, seed=None)
Метрики точности
-
Синий - валидационные данные, оранжевый - тренировочные данные
![.](https://github.com/baliffagh/SMOMI/blob/Lab4/graph/4.3BCtrainvalacc.PNG)

Функции потерь
-
Синий - валидационные данные, оранжевый - тренировочные данные
![.](https://github.com/baliffagh/SMOMI/blob/Lab4/graph/4.3BCtrainvalloss.PNG)

4.Добавление гауссового шума
========================
1 сеть
-
    with tf.name_scope('Add_gaussian_noise'):
        noise_img = image + tf.random.normal(shape=tf.shape(image), mean=0.0, stddev=(50)/(255), dtype=tf.float32)
        noise_img = tf.clip_by_value(noise_img, 0.0, 1.0)
Метрики точности
-
Синий - валидационные данные, оранжевый - тренировочные данные
![.](https://github.com/baliffagh/SMOMI/blob/Lab4/graph/4.1Gausstrainvalacc.PNG)

Функции потерь
-
Синий - валидационные данные, оранжевый - тренировочные данные
![.](https://github.com/baliffagh/SMOMI/blob/Lab4/graph/4.1Gausstrainvalloss.PNG)

2сеть
-
    with tf.name_scope('Add_gaussian_noise'):
        noise_img = image + tf.random.normal(shape=tf.shape(image), mean=0.0, stddev=(100)/(255), dtype=tf.float32)
        noise_img = tf.clip_by_value(noise_img, 0.0, 1.0)
Метрики точности
-
Синий - валидационные данные, оранжевый - тренировочные данные
![.](https://github.com/baliffagh/SMOMI/blob/Lab4/graph/4.2Gausstrainvalacc.PNG)

Функции потерь
-
Синий - валидационные данные, оранжевый - тренировочные данные
![.](https://github.com/baliffagh/SMOMI/blob/Lab4/graph/4.2Gausstrainvalacc.PNG)

3 сеть
-
    with tf.name_scope('Add_gaussian_noise'):
        noise_img = image + tf.random.normal(shape=tf.shape(image), mean=0.0, stddev=1.0, dtype=tf.float32)
        noise_img = tf.clip_by_value(noise_img, 0.0, 1.0)
Метрики точности
-
Синий - валидационные данные, оранжевый - тренировочные данные
![.](https://github.com/baliffagh/SMOMI/blob/Lab4/graph/4.3Gausstrainvalacc.PNG)

Функции потерь
-
Синий - валидационные данные, оранжевый - тренировочные данные
![.](https://github.com/baliffagh/SMOMI/blob/Lab4/graph/4.3Gausstrainvalacc.PNG)
