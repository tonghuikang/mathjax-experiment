# mathjax-experiment

Please refer to the [Github repository](https://github.com/tonghuikang/mathjax-experiment) for the [source](https://raw.githubusercontent.com/tonghuikang/mathjax-experiment/master/README.md) of this example.

This uses [MathJax](https://github.com/mathjax/MathJax).

I followed these [instructions](http://csega.github.io/mypost/2017/03/28/how-to-set-up-mathjax-on-jekyll-and-github-properly.html) instructions to make it work.

You will need to append three lines of javascript code for it to work. You can append it to the templates if you know how to do it.

<script src="https://polyfill.io/v3/polyfill.min.js?features=es6"></script>
<script type="text/javascript" id="MathJax-script" async src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-chtml.js"></script>
<script>window.MathJax = {tex: {inlineMath: [['$', '$'], ['\\(', '\\)']]}};</script>

Following is an example of inline and displayed $\LaTeX$ typesetting.

When $a \neq 0$, there are two solutions to $ax^2 + bx + c = 0$ and they are

$$
x = {-b \pm \sqrt{b^2-4ac} \over 2a}
$$

$f(k) = 1-\min\{ 1, f_{k-1}, f_{k-2}, f_{k-6} \}$

- The **recursion** $f(k) = 1-\min\{ 1, f_{k-1}, f_{k-2}, f_{k-6} \}$
- The **recursion** $f(k) = 1-\min\lbrace 1, f_{k-1}, f_{k-2}, f_{k-6} \rbrace$
- minimise $\dfrac{\textcolor{red}{\lambda}}{2}  || \theta || ^2 + \textcolor{red}{\dfrac{1}{n}\Sigma_{(x,y)} \xi_{x,y}}$
- minimise $\dfrac{\textcolor{red}{\lambda}}{2}  \vert  \vert \theta \vert  \vert ^2 + \textcolor{red}{\dfrac{1}{n}\Sigma_{(x,y)} \xi_{x,y}}$

$$\dfrac{\textcolor{red}{\lambda}}{2}  || \theta || ^2 + \textcolor{red}{\dfrac{1}{n}\Sigma_{(x,y)} \xi_{x,y}}$$