# classification-of-cancer
classification of lung cancers

В рамках выполнения работы «Классификация раковых образований» был выбран датасет luna 2016. Данный набор содержит в себе 890 снимков легких компьютерной томографии пациентов. КТ сканы — это трехмерные рентгеновские снимки, которые представлены в виде трехмерного массива одноканальных данных. Вместо привычного пикселя, в трехмерном пространстве используется воксель. Он занимает некоторый пространственный объем. Каждое его измерение — это расстояние. Так же, хочется отметить, что каждый воксель КТ имеет некоторое число, которое характеризует его средней массовой плотности. Чем ярче изображение, тем больше плотность вещества. Так кости или метал принимают белый цвет, а воздух — черный.

Наша модель будет состоять из 4 основных блоков, батчнормализации, а также последнего линейного слоя и функции Softmax, которая высчитывает вероятности  определения к тому или иному классу.
Мы будем использовать блок, в котором будет две свертки 3x3, после каждой свертки будет идти функция активации Relu. Сверточные содержат в себе padding, что позволяет сохранить размерность изображения. В конце каждого блока используется слой субдискретизации MaxPool, который уменьшает размерность нашего изображения в два раза. Так же наши сверки увеличивают число каналов. 

Результаты можно посмотреть в файле results.png
Модель обучалась 10 эпох
Было полученно приемлимое занчение recall метрики, однако precision получился невысоким
