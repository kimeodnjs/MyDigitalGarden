---
title: LaTeX 문법 가이드
tags: [computer, markdown]
date: [2024-03-08]
---
>[!info]
> 필요할 때 마다 주기적으로 업데이트 되는 노트입니다. 더 자세한 내용은 [위키 백과](https://ko.wikipedia.org/wiki/%EC%9C%84%ED%82%A4%EB%B0%B1%EA%B3%BC:TeX_%EB%AC%B8%EB%B2%95) 참조

<br>
<br>
<br>

## 1. 사칙연산

^ecf543

<hr>

##### 입력

```latex
$x + y = 1$

$x - y = 1$

$x \times y = 1$

$x \div y = 1$
```

<br>
<br>

##### 출력

$x + y = 1$ 

$x - y = 1$

$x \times y = 1$

$x \div y = 1$

<br>
<br>
<br>

## 2. 분수
<hr>

##### 입력

```latex
$\frac{x}{y}$

$^x/_y$
```

<br>
<br>

##### 출력

$\frac{x}{y}$

$^x/_y$

<br>
<br>
<br>

## 3. 괄호
<hr>

##### 입력

```latex
$(x + y)$

$\{x + y\}$

$[x + y]$

$\lvert x + y \rvert$

$\langle x + y \rangle$

$\left(\frac{x}{y}\right)$

$\Bigg( \bigg( \Big( \big( ( ) \big) \Big) \bigg) \Bigg)$
```

<br>
<br>

##### 출력

$(x + y)$

$\{x + y\}$

$[x + y]$

$\lvert x + y \rvert$

$\langle x + y \rangle$

$\left(\frac{x}{y}\right)$

$\Bigg( \bigg( \Big( \big( ( ) \big) \Big) \bigg) \Bigg)$

<br>
<br>
<br>

## 4. 위 첨자, 아래 첨자
<hr>

##### 입력

```latex
$x^y$

$x_y$
```

<br>
<br>

##### 출력

$x^y$

$x_y$

<br>
<br>
<br>

## 5. 연속점
<hr>

##### 입력

```latex
$\dots$

$\cdots$

$\ldots$

$\vdots$

$\ddots$
```

<br>
<br>

##### 출력

$\dots$

$\cdots$

$\ldots$

$\vdots$

$\ddots$

<br>
<br>
<br>

## 6. 제곱근과 팩토리얼
<hr>

##### 입력

```latex
$\sqrt{x}$

$\sqrt[n]{x}$

$n! = 1 \times 2 \times 3 \times \ldots n$

$n! = \prod_{k=1}^n k$
```

<br>
<br>

##### 출력

$\sqrt{x}$

$\sqrt[n]{x}$

$n! = 1 \times 2 \times 3 \times \ldots n$

$n! = \prod_{k=1}^n k$

<br>
<br>
<br>

## 7. 행렬
<hr>

##### 입력

```latex
$$
A_{m,n} = 
\begin{matrix}
a_{1,1} & a_{1,2} & \cdots & a_{1,n} \\
a_{2,1} & a_{2,2} & \cdots & a_{2,n} \\
\vdots & \vdots & \ddots & \vdots \\
a_{m,1} & a_{m,2} & \cdots & a_{m,n}
\end{matrix}
$$

$$
\begin{bmatrix}
a & b \\
c & d
\end{bmatrix}
$$
```

<br>
<br>

##### 출력

$$
A_{m,n} = 
\begin{pmatrix}
a_{1,1} & a_{1,2} & \cdots & a_{1,n} \\
a_{2,1} & a_{2,2} & \cdots & a_{2,n} \\
\vdots & \vdots & \ddots & \vdots \\
a_{m,1} & a_{m,2} & \cdots & a_{m,n}
\end{pmatrix}
$$

$$
\begin{bmatrix}
a & b \\
c & d
\end{bmatrix}
$$

<br>
<br>
<br>

## 8. 적분
<hr>

##### 입력

```latex
$
\int_0^\infty \mathrm{e}^{-x}\, \mathrm{d}x
$
```

<br>
<br>

##### 출력

$
\int_0^\infty \mathrm{e}^{-x}\, \mathrm{d}x
$

<br>
<br>
<br>

## 9. 삼각함수
<hr>

##### 입력

```latex
$\cos(2\theta) = \cos^2\theta - \sin^2\theta$

$\pi \Pi \phi$

$90^\circ$
```

<br>
<br>

##### 출력

$\cos(2\theta) = \cos^2\theta - \sin^2\theta$

$\pi \Pi \phi$

$90^\circ$

<br>
<br>

## 10. 극한, 시그마, 로그
<hr>

##### 입력

```latex
$\lim_{x \to \infty} \exp(-x) = 0$

$\sum_{i=1}^{10} t_i$

$\displaystyle\sum_{i=1}^{10} t_i$

$\log_b a$
```

<br>
<br>

##### 출력

$\lim_{x \to \infty} \exp(-x) = 0$

$\sum_{i=1}^{10} t_i$

$\displaystyle\sum_{i=1}^{10} t_i$

$\log_b a$

<br>
<br>
<br>

## 11. 폰트
<hr>

##### 입력

```latex
ABCDEF
$\mathcal{ABCDEF}$
$\mathbb{ABCDEF}$
$\mathbf{ABCDEF}$
$\mathfrak{ABCDEF}$
$\mathrm{ABCDEF}$
$\mathit{ABCDEF}$
$\mathsf{ABCDEF}$
$\mathtt{ABCDEF}$
```

<br>
<br>

##### 출력

$\mathcal{ABCDEF}$
$\mathbb{ABCDEF}$
$\mathbf{ABCDEF}$
$\mathfrak{ABCDEF}$
$\mathrm{ABCDEF}$
$\mathit{ABCDEF}$
$\mathsf{ABCDEF}$
$\mathtt{ABCDEF}$

<br>
<br>
<br>

## 12. 벡터 및 확장 로마자
<hr>

##### 입력

```latex
$\mathring{A}$
$\hat{A}$
$\tilde{A}$
$\bar{A}$
$\acute{A}$
$\grave{A}$
$\check{A}$
$\breve{A}$
$\dot{A}$
$\ddot{A}$
$\vec{A}$
```

<br>
<br>

##### 출력

$\mathring{A}$
$\hat{A}$
$\tilde{A}$
$\bar{A}$
$\acute{A}$
$\grave{A}$
$\check{A}$
$\breve{A}$
$\dot{A}$
$\ddot{A}$
$\vec{A}$

<br>

> [!info]
> - 중괄호를 이용하여 복수의 문자에 지정할 수 있으나, 기호의 길이가 늘어나지 않으며 가운데 정렬로 출력된다.
> + tilde와 hat의 경우, 앞에 wide를 붙여 기호의 길이를 늘릴 수 있다.
> - 분음 기호 첨가에 따라 점이 삭제되는 $i, j$ 의 경우 \imath $\rightarrow \imath$ , \jmath $\rightarrow \jmath$ 를 이용한다.

<br>
<br>
<br>

## 13. 화살표
<hr>

##### 입력

```latex
$\Rrightarrow, \Lleftarrow$

$\Rightarrow, \Leftarrow$

$\rightarrow, \leftarrow$

$\nrightarrow, \nRightarrow, \nleftarrow, \nLeftarrow$

$\leftrightarrow, \longleftrightarrow$

$\uparrow, \downarrow$

$\nearrow, \swarrow, \nwarrow, \searrow$
```

<br>
<br>

##### 출력

$\Rrightarrow, \Lleftarrow$

$\Rightarrow, \Leftarrow$

$\rightarrow, \leftarrow$

$\nrightarrow, \nRightarrow, \nleftarrow, \nLeftarrow$

$\leftrightarrow, \longleftrightarrow$

$\uparrow, \downarrow$

$\nearrow, \swarrow, \nwarrow, \searrow$

<br>
<br>
<br>

## 14. 기타 연산자
<hr>

##### 입력

```latex
$\sim, \simeq, \eqsim, \cong, \ncong$

$\ne, \neq, \equiv, \risingdotseq$

$\cdot, \circ, \bullet, \otimes, \odot, \bigoplus, \bigodot$

$\approx, \le, \ge, \propto$

$\partial, \nabla$
```

<br>
<br>

##### 출력

$\sim, \simeq, \eqsim, \cong, \ncong$

$\ne, \neq, \equiv, \risingdotseq$

$\cdot, \circ, \bullet, \otimes, \odot, \bigoplus, \bigodot$

$\approx, \le, \ge, \propto$

$\partial, \nabla$

<br>
<br>
<br>

## 15. 공백
<hr>

##### 입력

```latex
$\,$

$\;$

$\quad$

$\qquad$
```

<br>
<br>

##### 출력

$\,$

$\;$

$\quad$

$\qquad$

<br>
<br>
<br>
