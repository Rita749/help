## <p style="text-align: center;">Бюджетное учреждение высшего образования Ханты-Мансийского автономного округа – Югры</p>

# <p style="text-align: center;">«СУРГУТСКИЙ ГОСУДАРСТВЕННЫЙ УНИВЕРСИТЕТ»</p>

## <p style="text-align: center;">Политехнический институт</p>
---
<p style="text-align: center;">Кафедра прикладной математики</p>


<p style="text-align: center;">ФИО ОБУЧАЮЩЕГОСЯ</p>

# <p style="text-align: center;">ТЕМА ИНДИВИДУАЛЬНОГО ЗАДАНИЯ</p>

<p style="text-align: center;">Дисциплина «Математический анализ»</p>
<p style="text-align: center;">направление 01.03.02 «Прикладная математика и информатика»</p>
<p style="text-align: center;">направленность (профиль): «Технологии программирования и анализ данных»</p>
<pre>

</pre>

<p style="text-align: right;">Преподаватель: &nbsp&nbsp&nbsp&nbsp&nbsp&nbsp&nbsp&nbsp&nbsp&nbsp&nbsp&nbsp&nbsp&nbsp&nbsp&nbsp&nbsp </p>
<p style="text-align: right;">Должность, степень ФИО</p>

<p style="text-align: right;">Студент гр. № &nbsp&nbsp&nbsp&nbsp&nbsp&nbsp&nbsp&nbsp&nbsp&nbsp&nbsp&nbsp&nbsp&nbsp&nbsp&nbsp&nbsp&nbsp&nbsp&nbsp&nbsp </p>
<p style="text-align: right;">ФИО &nbsp&nbsp&nbsp&nbsp&nbsp&nbsp&nbsp&nbsp&nbsp&nbsp&nbsp&nbsp&nbsp&nbsp&nbsp&nbsp&nbsp&nbsp&nbsp&nbsp&nbsp&nbsp&nbsp&nbsp&nbsp&nbsp&nbsp&nbsp&nbsp&nbsp&nbsp&nbsp&nbsp&nbsp&nbsp&nbsp&nbsp</p>
<pre>

</pre>

<p style="text-align: center;">Сургут 20__ г.</p>

---
<pre>

</pre>

### Лабораторная работа №1. Числовые последовательности.

#### Задание
Вычислить пределы данных числовых последовательностей двумя способами: 
- аналитически 
- используя библиотеки Python для символьных вычислений. 

Для каждой числовой последовательности $\{x_k\}_1^\infty$ на одном рисунке построить (используя графические пакеты Python) следующие множества точек:

k = 1,...,m
- (k, 0) ~ синий цвет
- (0, $x_k$) ~ зеленый цвет
- (k, $x_k$) ~ красный цвет

В случае, если последовательность сходится, построить на соответствующем рисунке точку (оранжевый цвет) изображающую предел последовательности $\{x_k\}_1^\infty$.

Для сходящихся последовательностей, для заданного $\epsilon>0$ найти такой номер $n(\epsilon)$, начиная с которого $|x_k-A|<\epsilon, ∀k≥n(\epsilon)$

<pre>

</pre>
<p style="text-align: center;">Аналитическое решение</p>

$\lim_{n\rightarrow+\infty}(\frac{-3n^3+4n^2-8n-6}{4n^2+2n})=...$
  - $\lim_{n\rightarrow+\infty}(-3n^3+4n^2-8n-6)=-\infty$
  - $\lim_{n\rightarrow+\infty}(4n^2+2n)=+\infty$

Т.к. выражение $\frac{-\infty}{+\infty}$ является неопределенностью, преобразуем его:

$\lim_{n\rightarrow+\infty}(\frac{-3n^3+4n^2-8n-6}{4n^2+2n}) = \lim_{n\rightarrow+\infty}(\frac{n^2(-3n+4-\frac{8}{n}-\frac{6}{n^2})}{n^2(4+\frac{2}{n})})=\lim_{n\rightarrow+\infty}(\frac{-3n+4-\frac{8}{n}-\frac{6}{n^2}}{4+\frac{2}{n}})=...$

Вычисляем числитель:
- $\lim_{n\rightarrow+\infty}(-3n+4-\frac{8}{n}-\frac{6}{n^2})=...$
   - $\lim_{n\rightarrow+\infty}(-3n+4-\frac{8}{n})=-\infty$
   - $\lim_{n\rightarrow+\infty}(\frac{6}{n^2})=0$
   - 
$=>\lim_{n\rightarrow+\infty}(-3n+4-\frac{8}{n}-\frac{6}{n^2})=-\infty$

Вычисляем знаменатель:
- $\lim_{n\rightarrow+\infty}(4+\frac{2}{n})=4$

$\lim_{n\rightarrow+\infty}(\frac{-3n^3+4n^2-8n-6}{4n^2+2n})=\frac{-\infty}{4}=-\infty$

Ответ: $-\infty$

<pre>

</pre>
<p style="text-align: center;">Программное решение</p>

\```  
from sympy import *  
import numpy as np  
import matplotlib.pyplot as plt  
n = Symbol("n")  
a = limit((-3*n**3+4*n**2-8*n-6)/(4*n**2+2*n),n,oo)  
print(a)   
x = np.arange(-50, 50, 1)  
f = (-3*x**3+4*x**2-8*x-6)/(4*x**2+2*x)  
plt.plot(x, f)  
plt.xlabel('Ось х') #Подпись для оси х  
plt.ylabel('Ось y') #Подпись для оси y  
plt.title('Первый график') #Название  
plt.grid(True)  
plt.show()  

\```

![Code](images/1.jpg)

<pre>

</pre>

<p style="text-align: center;">Иллюстрация решения </p>

### Заключение
В ходе лабораторной работы мы изучили тему числовые последовательности. Предоставили аналитическое и программное решения, показав, что они совпадают. А также продемонстрировали графически.

### Источники
1. Руководство по оформленитю Markdown файлов: [Электронный ресурс]. URL:
https://gist.github.com/Jekins/2bf2d0638163f1294637 (дата обращения 24.04.2023)
2. Балджы А.С., Хрипунова М.Б., Александрова И.А.. Математика на python: Учебное
пособие. - Москва,2018.- 77с. (дата обращения 24.04.2023)
3. Демидович Б.П. Сборник задач и упражнений по математическому анализу: Учебное
пособие. -  625с. (дата обращения 24.04.2023)
4. Криволапов С.Я, Хрипунова М.Б.. Математика на python: Учебное
пособие. - Москва,2022.- 455с. (дата обращения 24.04.2023)
5. Построение грайфиков по данным из файла: [Электронный ресурс]. URL:
https://habr.com/ru/articles/748282/ (дата обращения 24.04.2023)






