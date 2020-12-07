# mathjax-experiment

Please refer to the [Github repository](https://github.com/tonghuikang/mathjax-experiment) for the [source](https://raw.githubusercontent.com/tonghuikang/mathjax-experiment/master/README.md) of this [example](https://tonghuikang.github.io/mathjax-experiment/).

This uses [MathJax](https://github.com/mathjax/MathJax).

I followed these [instructions](http://csega.github.io/mypost/2017/03/28/how-to-set-up-mathjax-on-jekyll-and-github-properly.html) instructions to make it work.

You just need to append these three lines of [javascript](https://docs.mathjax.org/en/latest/web/start.html) [code](https://docs.mathjax.org/en/latest/input/tex/delimiters.html) to your markdown file.

```
<script src="https://polyfill.io/v3/polyfill.min.js?features=es6"></script>
<script type="text/javascript" id="MathJax-script" async src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-chtml.js"></script>
<script>window.MathJax = {tex: {inlineMath: [['$', '$'], ['\\(', '\\)']]}};</script>
```

You can append it to the Jekyll templates if you know how to do it.

There was also a [KaTeX](https://katex.org/) parser, but I was not able to use it render [inline](https://tonghuikang.github.io/mathjax-experiment/) equations while making use of `\textcolor`.



# Basic Example

Following is an example of inline and displayed $\LaTeX$ typesetting.

When $a \neq 0$, there are two solutions to $ax^2 + bx + c = 0$ and they are

$$
x = {-b \pm \sqrt{b^2-4ac} \over 2a}
$$


<div style="page-break-after: always;"></div>
# Stress Testing

However, the parsing may not work for various reasons. We test it inline - encoded between two single dollar signs, and displayed - encoded between two double dollar signs.


### Vertical symbol

In markdown, vertical symbols were used to delimit the table. It is recommended to use `\vert` in math expression.

You observe a subset $S$ with $|S|$ elements such that its weights is larger than the limit. The **knapsack cover inequality** prevents you from choosing all of these elements, you can choose at most $|S| - 1$ elements from $S$.

$$
\sum_{j \in S} x_j \leq |S| - 1 = |S| - 1
$$


### Curly braces

In TeX, curly braces are used as parenthesis and needs to be escaped. However, even after escaping, some math parses still ignore it. The workaround is to use `\lbrace` and `\rbrace`

The **recursion** for the dynamic programming is $f(k) = 1-\min\{ 1, f_{k-1}, f_{k-2}, f_{k-6} \}$

$$
f(k) = 1-\min\{ 1, f_{k-1}, f_{k-2}, f_{k-6} \}
$$


### Textcolor

Some parsers does not have certain packages.

The task is to minimise $\dfrac{\textcolor{red}{\lambda}}{2}  \vert \vert \theta \vert \vert ^2 + \textcolor{red}{\dfrac{1}{n}\Sigma_{(x,y)} \xi_{x,y}}$

$$
f(\theta) = \dfrac{\textcolor{red}{\lambda}}{2}  || \theta || ^2 + \textcolor{red}{\dfrac{1}{n}\Sigma_{(x,y)} \xi_{x,y}}
$$


### Double underscores

In markdown, underscores were used mark emphasis. There are still issues parsing underscores from separate math expressions. I have not yet to find an workaround.

The objective function is $f(x) = x_1 + x_2$

$x_1$ is the number of oranges and $x_2$ is the number of apples
$$
f(x) = x_1 + x_2
$$

Data $\mathcal{S}$ is made up of training data $\mathcal{S}_n,$ validation data $\mathcal{S}_{val}$ or test data $\mathcal{S}_*$

Please let me know if you how to resolve this!




<script src="https://polyfill.io/v3/polyfill.min.js?features=es6"></script>
<script type="text/javascript" id="MathJax-script" async src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-chtml.js"></script>
<script>window.MathJax = {tex: {inlineMath: [['$', '$'], ['\\(', '\\)']]}};</script>