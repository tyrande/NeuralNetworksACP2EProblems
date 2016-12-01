<!--
create time: 2016-10-27
Author: Alan
-->

# Introduction

## Models of a neuron

**1.1** An example of the logistic function is defined by

$$\varphi(v) = {1\over 1+exp(-av)}$$

whose limiting values are  $0$ and $1$. Show that the derivative of $$\varphi(v)$$ with respect to $$v$$ is given by

$${d\varphi\over dv} = {a\varphi(v)[1-\varphi(v)]}$$

What is the value of this derivative at the origin?

**Proof.**
$${d\varphi\over dv} = {d({1\over 1+exp(-av)})\over dv} = -{1\over (1+exp(-av))^2}{d(1+exp(-av))\over dv} $$
$$= -{-a exp(-av)\over (1+exp(-av))^2} = a\varphi(v){exp(-av)\over (1+exp(-av))} = a\varphi(v)[1-\varphi(v)]$$

**Solution.**
$${d\varphi(0)\over dv} = a\varphi(0)[1-\varphi(0)] = {a\over 4}$$

________

**1.2** An odd sigmoid function is defined by
$$\varphi(v) = {1-exp(-av)\over 1+exp(-av)} = {tanh({av\over 2})}$$
where tanh denotes a hyperbolic tangent. The limiting values of this second sigmoid function are $-1$ and $+1$. Show that the derivative of $\varphi(v)$ with respect to $v$ is given by
$${d\varphi\over dv} = {a\over 2}[1-\varphi^2(v)]$$
What is the value of this derivative at the origin? Suppose that the slope parameter $a$ is made infinitely large. What is the resulting form of $\varphi(v)$?

**Proof.**
$${d\varphi\over dv} = {d({1-exp(-av)\over 1+exp(-av)})\over dv} = {d({1\over 1+exp(-av)})\over dv} - {d({1\over exp(av)+1})\over dv}$$
$$= {a exp(-av)\over (1+exp(-av))^2} - {-1\over (1+exp(av))^2}{d(1+exp(av))\over dv}$$
$$= {a exp(-av)\over (1+exp(-av))^2} + {aexp(av)\over (1+exp(av))^2} = {2a exp(-av)\over (1+exp(-av))^2}$$
$$ {a\over 2}[1-\varphi^2(v)] = {a\over 2}[1-({1-exp(-av)\over {1+exp(-av)}})^2] = {2a exp(-av)\over (1+exp(-av))^2}$$

**Solution.**
$${d\varphi(0)\over dv} = {a\over 2}[1-\varphi^2(0)] = {a\over 2}$$
$$ lim\varphi(v) = lim({1-exp(-av)\over 1+exp(-av)}) $$
________

**1.3** Yet another odd sigmoid function is the algebraic sigmoid
$$ \varphi(v) = {v\over \sqrt{1+v^2}} $$
whose limiting values are $-1$ and $+1$. Show that the derivative of $\varphi(v)$ with respect to $v$ is given by
$$ {d\varphi\over dv} = {\varphi^3(v)\over v^3} $$
What is value of this derivative at the origin?

**Proof.**

**Solution.**

________

**1.4** Consider the following two functions:
(i) $$ \varphi(v) = {1\over \sqrt{2\pi}}\int exp(-{x^2\over 2})dx $$
(ii) $$ \varphi(v) = {2\over \pi} tan^{-1}(v) $$
Explain why both of these function fit the requirements of a sigmoid function. How do these two functions differ from each other?

**Proof.**

**Solution.**

________

**1.5** Which of the five sigmoid functions described from in Problems 1.1 to 1.4 would qualify as a cumulative (probability) distribution function? Justify your answer.

**Solution.**
