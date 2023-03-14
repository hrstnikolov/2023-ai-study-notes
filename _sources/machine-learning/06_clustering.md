# 06 Clustering

## Въведение

**over-fitting** - моделът е обърнал ТОЛКОВА внимание на шума че го взел предвид и ще го предположи

Причини за голямо отклонение **high bias**:
1. Първоначално предположение е грешно. Например предположили сме че зависимостта в данните е линейно, но те не са.
2. Има bias в данните.

Можем да 'оправим' модел с high bias/variance или с модела или с данните.

Variance хващаме лесно, bias не можем.

биас = грешки от измерване

> For example, a facial recognition system can start to be racially discriminatory, or a credit application evaluation system can become gender-biased. 

> Imagine that I wanted to create an algorithm that decides whether an applicant gets accepted into a university or not and one of my inputs was geographic location. Hypothetically speaking, if the location of an individual was highly correlated with ethnicity, then my algorithm would indirectly favor certain ethnicities over others. This is an example of bias in AI.

**hyperopt** - библиотека за оптимизиране на хипер-параметри

Хипер-параметрите имат приоритет.

Съвети:
- за много записи мога да пропусна cross-validation
- 1М записи -> 30К за тестване (0.3%)

Validation set използваме за да изберем модел.

## Clustering Analysis

Търсим групи, бучки в данните.

Вид обучение без учител, неконтролирано обучение.

Нямаме loss ф-я защото нямаме наблюдаван изход $\tilde{y}$.

**Ego graph**
- граф, в който аз съм център
- например - приятели във facebook

В графите имахме **graph cliques**.
- силно свързани групи
- на български - клика

**Приложения** на клъстерирането
- сегментиране
	- отделяне на видове тъкани в медицината
	- на групи от хора с общи интереси в маркетинга
- пресъпления




## k-Means Clustering

Blobs
- точки получени от двумерни гаусови разпределения

kmeans работи бързо и лесно

Предположението на k-means е, че данните са в групи, хипер-сфери.

objective function
loss ф-я на k-Means - **cluster inertia**

**k-Means++**

средно квадратична грешка = MSE

k-Means++ - начин да инициализираме клъстерите малко по-добре

по-default - init='kmeans++'. 'init='random' само ако имаме причина.


Какво правим ако не знаем колко са клъстерите?
Определяме ги графично с elbow method.

Case: ако търсим аномалии, може да очакваме да силуетната графика да покаче че единият клъстер е много малък - това е този с аномалиите.

**Йерархично клъстериране** - удобно ако имаме йерархия от групи

**Агломеративно клъстериране**

Не може да предсказваме нови данни

Алгоритмите дотук са **базирани на прототипи** - центроидите, които избираме в началото.

## DBSCAN

Предполагаме че има Outlier-и. DBSCAN ги изключва от клъстерите.

радиус на действие

