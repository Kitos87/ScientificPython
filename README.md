# ScientificPython
Зачётная задача "Метод Ньютона"

## 13. Метод Ньютона
*Метод Ньютона* нахождения корня уравнения $f(x) = 0$ заключается в итерациях вида
$$
x_{i+1} = x_i - \frac{f(x_i)}{f'(x_i)}.
$$
Написать функцию `mynewton(f, df, [x0, x1])`, реализующую метод Ньютона,
где 
`f` – строка, задающая правую часть $f(x)$ уравнения,
`df` – строка, задающая  $f'(x)$,
`[x0, x1]` – отрезок локализации.
Функция должна возвращать найденный корень с макимально возможной точностью.

Написать программу, тестирующую эту
функцию и сравнивающую ее с `scipy.optimize.newton`, `scipy.optimize.fsolve` на уравнениях:
$$
x^3 - 2x - 5 = 0, \qquad 0\le x \le 3
$$
(исторический пример Валлиса),
$$
\sin x = 0, \qquad 1 \le x \le 4,
$$
$$
x^3  = 0.001, \qquad -1 \le x \le 1,
$$
$$
\ln x + \frac{2}{3} = 0, \qquad 0 \le x \le 1,
$$
$$
\mathop{\rm sgn} (x-2)\, \sqrt{|x-2|} = 0, \qquad 1 \le x \le 4,
$$
$$
 \arctan x = \frac{\pi}{3}, \qquad 0 \le x \le 5,
$$
$$
\frac{1}{x - \pi} = 0, \qquad 0 \le x \le 5.
$$
Программа должна печатать таблицу, в которой указываются найденные функциями `mynewton`,
`scipy.optimize.newton`, `scipy.optimize.fsolve` решения, их относительные ошибки, и количества затраченных итераций.
Сравнить и следать выводы.

