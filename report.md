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

![Code](images/1.jpg)

<pre>

</pre>

<p style="text-align: center;">Иллюстрация решения </p>





