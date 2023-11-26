```
\documentclass[11pt]{article}
\usepackage[utf8]{inputenc}
\usepackage[russian]{babel}
\usepackage{amsmath}
\usepackage{amsfonts}
\usepackage{graphicx}
\pagestyle {empty}
\usepackage{wrapfig}
\usepackage{caption}
\usepackage{lipsum}
\usepackage{setspace}

\begin{document}

\begin{wrapfigure}{L}{0.45\textwidth}
\centering
\includegraphics[width=0.3\textwidth]{graph.png}
\caption*{Рис. 59}
\end{wrapfigure}


\noindent Производная функции (14.2) равна (см. пример 8 в п. 9.7)
\begin{equation*}
y' = 
\begin{cases} 
2x \sin \frac{1}{x} - \cos \frac{1}{x}, & \text{при } x \neq 0, \\
0, & \text{при } x = 0.
\end{cases}
\end{equation*}
Таким образом, функция (14.2) дифференцируема на всей числовой оси. При \( x = 0 \) ее производная имеет разрыв второго рода, поскольку
\begin{equation*}
\qquad \qquad \lim_{x \to 0} 2x \sin \frac{1}{x} = 0, \qquad \quad (14.4)
\end{equation*}
а второе слагаемое в выражении (14.3) для производной \( y' \) при \( x \neq 0 \), т.е. \( -\cos \frac{1}{x} \) не имеет предела при \( x \to 0 \). Кроме того, это слагаемое, изменяясь в любой односторонней окрестности точки \( x = 0 \) от \( -1 \) до \( +1 \), бесконечно много раз меняет в ней знак. Отсюда, в силу формул (14.3) и (14.4), следует, что и производная функции (14.2) в любой сколько угодно малой односторонней окрестности нуля также меняет знак. Общий характер поведения функции (14.2) изображен на рисунке 59.

Сформулируем теперь основанные на использовании производных высших порядков достаточные условия начала строгого экстремума, а также точек возрастания и убывания.

\textbf{Т Е О Р Е М А 4.} \textit {Пусть \( f \) в точке \( x_0 \) и функции \( f \) существующем производное до порядка \( n \geq 1 \) включительно, причем}
\begin{equation*}
\qquad \qquad \quad f^{(k)}(x_0) = 0 \quad \text{для } k = 1, 2, \ldots, n - 1, \quad f^{(n)}(x_0) \neq 0. \qquad  (14.5)
\end{equation*}
\textit {Тогда если \( n \) есть четное число, то функция \( f \) имеет в точке \( x_0 \) экстремум, и а именно максимум при \( f^{(2k)}(x_0) < 0 \) или минимум при \( f^{(2k)}(x_0) > 0 \). Если \( n \) есть нечетное число, то функция \( f \) не имеет в точке \( x_0 \) экстремума; в этом случае \( x_0 \) является точкой возрастания при} \( f^{(2k+1)}(x_0) > 0 \) \textit {или убывания при} \( f^{(2k+1)}(x_0) < 0 \). \\
Продолжим доказательству теоремы одно простое замечание: если в некоторой окрестности точки \( x_0 \) имеет место соотношение \( \beta(x) = o(\alpha(x)) \), \( x \to x_0 \), то существует такое \( \delta > 0 \), что при \( |x - x_0| < \delta \) справедливо неравенство

\[
|\beta(x)| \leq \frac{1}{2}|\alpha(x)|.
\]
\begin{center}
   \line(1,0){70}
\end{center}

\qquad \qquad \qquad \qquad \qquad \qquad \qquad \ \textit {360}


\end{document}
```
