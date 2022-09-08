## Множества и операции над ними
**Множество** - любая совокупность объектов (**элементов**) какой-либо природы.
Пусть $A$ и $B$ два множества.
- $A \subset B$ все элементы множества А являются элементами множества В
- $A = B \iff A \subset B$  и $B\subset A$
- $A \cup B = \{ x: x \in A \lor \ x \in B \}$
- $A \cap B = \{ x: x \in A \land \ x \in B \}$ 
- $A \setminus B = \{ x: x \in A \land x \notin B \}$
- $\bar{A} = \Omega \setminus A$
- $A \triangle B = (A \setminus B) \cup (B \setminus A)$
## Множество действительных чисел
Всякое действительное число $x$ представимо беcконечной десятичной дробью $\pm [ |x|], x_1 x_2 \dots$
где $[x]$ наибольшее целое число, не превосходящее $x$ и называемое целой частью числа $x$ 
## Аксиома непрерывности
Пусть $A$ и $B$ два непустых множества действительных чисел, такие что $\forall a \in A$ и $\forall b \in B$ $a<b$, тогда существует число $\lambda: \forall a\in A \land \forall b \in B \quad a \ge \lambda \ge b$
## Ограниченность числовых множеств
Наибольшим элементом множества $X$ называется элемент $x_{max}: x_{max} \in X; \forall x \in X \ x \le x_{max}$
Множество $X$ действительных чисел называется ограниченным сверху, если $\exists M: \forall x \in X  \land\ x\le M$
$M$ - верхняя грань или мажоранта
$\sup X$ - минимальная мажоранта или точная верхняя грань
$M_0 = \sup X$ равносильно, если
- $\forall x \in X \ x\le M_0$, т.е. $M_0$ верхняя граница множества $X$
- $\epsilon > 0 \ \exists x_\varepsilon \in X: \ x_\varepsilon > m_0 - \varepsilon$, т.е. эту границу нельзя улучшить

Наименьшим элементом множества $X$ называется элемент $x_{min}: x_{min} \in X; \forall x \in X \ x \ge x_{min}$
Множество $X$ действительных чисел называется ограниченным снизу, если $\exists M: \forall x \in X  \land\ x\ge M$
$M$ - нижняя грань или миноранта
$\inf X$ - максимальная миноранта или точная нижняя грань
$M_0 = \inf X$ равносильно, если
- $\forall x \in X \ x\ge M_0$, т.е. $M_0$ верхняя граница множества $X$
- $\epsilon > 0 \ \exists x_\varepsilon \in X: \ x_\varepsilon < m_0 + \varepsilon$, т.е. эту границу нельзя улучшить

## Числовые последовательности
**Числовая последовательность** $\{ x_n\}_{n \in N}$ - отображение, согласно которому каждому натуральному числу $n$ ставится в соответствие некоторое число $x_n$.

## Предел последовательности
Число $A$ называется пределом числовой последовательности $x_n$
На $\varepsilon - \delta$ языке
$$
\boxed{

( \lim_{n \to \infty}{x_{n}} = A ) := \forall \varepsilon > 0 \; \exists N \in \mathbb{N} \; \forall n > N \quad ( | x_{n} - A | < \varepsilon )

}
$$


Через окрестности
$$

\boxed{

( \lim_{n \to \infty}{x_{n}} = A ) := \forall V(A) \ \exists N \in \mathbb{N} \ \forall n > N \ ( x_{n} \in V(A) )
}

$$
При этом сама последовательность называется сходящейся.

#Теорема Если последовательность сходится, то ее предел единственен.
*Доказательство*.
$\square$ От противного. Пусть для некоторой последовательности  $\{ x_n \}_{n \in \mathbb{N}}$ имеет место: $\lim_{n \to \infty} x_n = A$ и $\lim_{n \to \infty} x_n = B$ . По определению
$$|x-a|<\varepsilon \quad |x-b|<\varepsilon$$
при $\varepsilon>0$, а это невозможно если $\varepsilon < \frac{b-a}{2}$. $\blacksquare$
## Ограниченность сходящейся числовой последовательности
Числовая последовательность называется **ограниченной сверху**, если $\exists M \in R: \forall n \in N \ x_n \le M$
Числовая последовательность называется **ограниченной снизу**, если $\exists m \in R: \forall n \in N \ x_n \ge m$
Числовая последовательность называется **ограниченной**, если $\exists m, M \in R: \forall n \in N \ m\le x_n \le M$

#Теорема Если последовательность сходится, то она ограничена.
*Доказательство*
Пусть $\lim_{n \to \infty} x_n = A$. Тогда $\forall \varepsilon > 0 \ \exists n_0(\varepsilon): \forall n \ge n_0 \quad |x_n - A| < \varepsilon$
Если взять, например, $\varepsilon = 1$, то при $n \ge n_0$ все $x_n \in (A-1; A+1)$. При этом все члены последовательности $x_1, x_2, \dots, x_{n_0 - 1}$ могут $\notin$ этому интервалу. Но таких точек конечное число. Поэтому $\exists \rho = \max_{1 \le i \le n_0 -1} |x_i - A|$. Тогда $\forall x_n (n \in N) \ x_n [A-R; A+R]$, где $R = \max{(1, \rho)}$.
## Свойства сходящихся числовых последовательностей, связанные с неравенствами
#Теорема Пусть даны две числовые последовательности $\{x_n\}$ и $\{y_n\}$, причем $\lim_{n \to \infty} x_n = A$ и $\lim_{n \to \infty} y_n = B$ и $A < B$. Тогда можно найти номер $n_0$, начиная с которого члены этих последовательностей будут удовлетворять неравенству.
$$x_n < y_n$$
*Доказательство*
Пусть $\varepsilon = \frac{B-A}{2}$. Тогда
$\exists n_1: \forall n \ge n_1 \quad A - \varepsilon < x_n < A + \varepsilon = \frac{A+B}{2}$  и
$\exists n_2: \forall n \ge n_2 \quad \frac{A+B}{2} = B - \varepsilon < y_n < B + \varepsilon$
Если положить $n_0 = \max{(n_1, n_2)}$, то для всех $n \ge n_0$ будут выполняться оба из указанных неравенств, а это означает, что для таких $n$ будет $x_n - y_n$.
#Следствие 
Если $\lim_{n \to \infty} x_n = A$ и $A < B$ ($A > B$), то, начиная с некоторого номера, все члены последовательности удовлетворяют неравенству $x_n < B$ ($x_n > B$).
*Доказательство*
Для доказательства достаточно в теореме взять стационарную последовательность $y_n = B$.
#Следствие Теорема отделимости последовательности
Если $\lim_{n \to \infty} x_n = A$ и $A>0$ ($A < 0$), то, начиная с некоторого номера, все члены последовательности будут больше (меньше) некоторого положительного (отрицательного) числа.

#Теорема о предельном переходе в неравенстве
Пусть $\lim_{n \to \infty} x_n = A$ и $\lim_{n \to \infty} y_n = B$, причем для всех натуральных значений $n$ выполняется неравенство  $x_n \le y_n$. Тогда $A \le B$.
*Доказательство*
$\square$  Допустим, что выполнено противоположное - $A > B$. Тогда по предыдущей теореме, начиная с некоторого номера, члены последовательности должны удовлетворять неравенству $x_n > y_n$, что противоречит условию. $\blacksquare$

#Теорема о трех последовательностях
Пусть даны три числовые последовательности $\{ x_n \}$, $\{y_n\}$ и $\{z_n\}$ такие, что при всех значениях $n$ выполняется неравенство
$$x_n \le y_n \le z_n$$
Если последовательности $\{ x_n \}$ и $\{ z_n \}$ сходятся, причем
$$\lim_{n \to \infty} x_n = \lim_{n \to \infty} z_n= A$$
тогда последовательность $\{ y_n \}$ также сходится и $\lim_\limits{n \to \infty} y_n = A$.
*Доказательство*
Возьмем произвольное положительное число $\varepsilon$.
Тогда
$\exists n_1: \exists n \ge n_1 \quad A - \varepsilon < x_n < A + \varepsilon$  и
$\exists n_2: \forall n \ge n_2 \quad B - \varepsilon < z_n < A + \varepsilon$

$$\lim_{n \to \infty} \sqrt[n]{n} = 1$$
#Теорема  Принцип вложенных отрезков Коши-Кантора
Для всякой системы вложенных отрезков существует по крайней мере одна точка, которая входит в каждый из этих отрезков. Причем, если при $n \to \infty$ длина $n$-го отрезка стремится к нулю, т.е. $\lim_{n \to \infty} (b_n - a_n) = 0$, то такая точка единственная.
Зорич стр. 65

## Бесконечно малые и бесконечно большие последовательности
Последовательность $\{ x_n \}_{n \in N}$ называется бесконечно малой, если
$$\lim_{n \to \infty} x_n = 0$$
$\{ x_n \}_{n \in N}$ бесконечно малая, если
$$\forall \varepsilon > 0 \ \exists n_0(\varepsilon): \forall n \ge n_0 \quad |x_n| < \varepsilon$$
#Теорема 
Для того чтобы число $A$ было пределом последовательности $\{x_n\}$ необходимо и достаточно, чтобы члены последовательности можно было представить в виде $x_n = A + \alpha_n$, где $\{a_n\}$ - бесконечно малая.
#Теорема Сумма бесконечно малых последовательностей есть бесконечно малая последовательность.
$\square$ $\lim_{n \to \infty} x_n = 0$ и $\lim_{n \to \infty} y_n = 0$. Возьмем $\varepsilon > 0$.
Найдем номер $n_1: \forall n \ge n_1 \quad |x_n| < \frac{\varepsilon}{2}$ и номер $n_2: \forall n \ge n_2 \quad |y_n| < \frac{\varepsilon}{2}$.
Тогда оба эти неравенства будут выполняться $\forall n \ge n_0 = \max{(n_1, n_2)}$ и $|x_n + y_n| \le |x_n| + |y_n| < \varepsilon$. $\blacksquare$ 
 