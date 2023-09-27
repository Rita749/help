### Задание

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
### Аналитическое решение

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
### Программное решение

```python
import matplotlib.pyplot as plt
import numpy as np
from sympy import *  

def sequence(n):
    return (-3*n**3 + 4*n**2 - 8*n - 6) / (4*n**2 + 2*n) #исходная последовательность

def plot_points(m):
    x = np.arange(1, m+1)
    y = sequence(x)

    # (k, 0) - blue colour
    plt.plot(x, np.zeros_like(x), 'bo', label='(k, 0)')

    # (0, x_k) - green color
    plt.plot(np.zeros_like(x), y, 'go', label='(0, x_k)')

    # (k, x_k) - red color
    plt.plot(x, y, 'ro', label='(k, x_k)')

    plt.xlabel('k')
    plt.ylabel('x_k')
    plt.legend()
    plt.grid()
    plt.show()

m = 20  # number of points
plot_points(m)

n = Symbol("n")  
a = limit((-3*n**3+4*n**2-8*n-6)/(4*n**2+2*n),n,oo)  
print(a) 

```
### График
![](https://raw.githubusercontent.com/Rita749/pictures/main/graphic.png)

<pre>

</pre>



### Заключение
В ходе лабораторной работы мы изучили тему числовые последовательности. Предоставили аналитическое и программные решения, показав, что они совпадают. А также продемонстрировали графически.

### Источники
1. Руководство по оформленитю Markdown файлов: [Электронный ресурс]. URL:
https://gist.github.com/Jekins/2bf2d0638163f1294637 (дата обращения 24.04.2023)
1. Балджы А.С., Хрипунова М.Б., Александрова И.А.. Математика на python: Учебное
пособие. - Москва,2018.- 77с. (дата обращения 24.04.2023)
1. Демидович Б.П. Сборник задач и упражнений по математическому анализу: Учебное
пособие. -  625с. (дата обращения 24.04.2023)
1. Криволапов С.Я, Хрипунова М.Б.. Математика на python: Учебное
пособие. - Москва,2022.- 455с. (дата обращения 24.04.2023)
1. Построение грайфиков по данным из файла: [Электронный ресурс]. URL:
https://habr.com/ru/articles/748282/ (дата обращения 24.04.2023) 





