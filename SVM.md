# SVM

Hinge Loss + Kernel Trick = SVM

## Hinge loss

loss function
$$
l(f(x^n), \hat{y}^n) = max(0, 1 - \hat{y}^n f(x))
$$

If $\hat{y}^n = 1$

$$
\begin{split}
e(f(x^n), \hat{y}^n) &= max (0, 1 - f(x)) \\
\end{split}
$$

$l$ has minimum when $f(x) > 1$

If $\hat{y}^n = -1$

$$
\begin{split}
e(f(x^n), \hat{y}^n) &= max (0, 1 + f(x)) \\
\end{split}
$$

$l$ has minimum when $f(x) < -1$

## Linear SVM

- Step 1: Function (Model)
	- $f(x) = \sum_{i} w_ix_i + b = \begin{bmatrix}w \\ b\end{bmatrix} \cdot \begin{bmatrix}x \\ 1\end{bmatrix} = w^Tx$
- Step 2: Loss function
	- Loss function is convex
- Step 3: Gradient descent?

### Typical formulation

Let $l(f(x^n), \hat{y}^n) = \varepsilon^n$.

$$
\begin{split}
\varepsilon^n \ge& 0 \\
\varepsilon^n \ge& 1 - \hat{y}^nf(x) \\
\hat{y}^nf(x)\ge& 1 - \varepsilon^n \\
\end{split}
$$

1 in the right of inequation is margin, $\varepsilon^n$ is slack variable

This formulation is a quadratic programing  problem 

## reference 

[(2) ML Lecture 20: Support Vector Machine (SVM) - YouTube](https://www.youtube.com/watch?v=QSEPStBgwRQ)