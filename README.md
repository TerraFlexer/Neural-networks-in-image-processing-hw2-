# Neural-networks-in-image-processing-hw2

Для выполнения задания использовалась сегментационная нейронная сеть с архитектурой Unet. Encoder слои были взяты с pretrained resnet34, decoder - самописные конволюции.
В качестве функции потерь использовалась BCEWithLogitsLoss().
Также был добавлен критерий остановки обучения, если среднее значение функции потерь за эпоху становилось меньше порога 0.006.

Обучение проводилось 20 эпох (если остановка не происходила раньше) по 40 попыток на каждой с использованием оптимизатора Adam.

Конечный результат для модели:
SiBaTrAcc final value: 0.805569581309087