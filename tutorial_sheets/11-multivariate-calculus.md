<script type="text/x-mathjax-config">
  MathJax.Hub.Config({
    tex2jax: {
      inlineMath: [ ['$','$'], ["\\(","\\)"] ],
      processEscapes: true
    }
  });
</script>

<script type="text/javascript" async
  src="https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.7.5/MathJax.js?config=TeX-MML-AM_CHTML">
</script>
<script type="text/javascript" src="tutorialSheetScripts.js"> </script>
<script type="text/javascript" src="tutorialSheetGraphs.js"> </script>
<link rel="stylesheet" type="text/css" media="all" href="styles.css">

# Multivariate Calculus Tutorial Sheet, #11

### Additional resources
* [3Blue1Brown](https://www.youtube.com/playlist?list=PLZHQObOWTQDMsr9K-rj53DwVRMYO3t5Yr)

<br><br><br><br>

# Problem sheet
## Essential Questions
### Problem 1.
For each of the functions below, find all the first order partial derivatives:

(a) $f\left(x,y\right)=xy^3+x^2y^2$
<div class = "answer">
$$
\frac{\partial{}f}{\partial{}x}=y^3+2xy^2, \ \ \
\frac{\partial{}f}{\partial{}y}=3xy^2+2x^2y
$$
</div>

(b) $f\left(x,y\right)=xe^{2x+3y}$
<div class = "answer">
$$
\frac{\partial{}f}{\partial{}x}=e^{2x+3y}+2xe^{2x+3y}, \ \ \ \
\frac{\partial{}f}{\partial{}y}=3xe^{2x+3y}
$$
</div>

(c) $f\left(x,y\right)=\frac{x-y}{x+y}$
<div class = "answer">
$$
\frac{\partial{}f}{\partial{}x}=\frac{1\left(x+y\right)-1(x-y)}{ {(x+y)}^2}=\frac{2y}{ {(x+y)}^2}, \ \ \
\frac{\partial{}f}{\partial{}y}=\frac{-1\left(x+y\right)-1(x-y)}{ {(x+y)}^2}=\frac{-2x}{ {(x+y)}^2}
$$
</div>

(d) $f\left(x,y\right)=2x\sin{\left(x^2y\right)}$
<div class = "answer">
$$
\frac{\partial{}f}{\partial{}x}=2\sin{\left(x^2y\right)+4x^2y}\cos{(x^2y)},\ \
\frac{\partial{}f}{\partial{}y}=2x^3\cos{(x^2y)}
$$
</div>

(e) $f\left(x,y,z\right)=x\cos{z+x^2y^3e^z}$
<div class = "answer">
$$
\frac{\partial{}f}{\partial{}x}=\cos{z+2xy^3e^z, \ \ \
}\frac{\partial{}f}{\partial{}y}=3x^2y^2e^z, \ \ \ \
\frac{\partial{}f}{\partial{}z}=-x\sin{z}+x^2y^3e^z
$$
</div>
<div class = "workingout"><br><br><br><br><br><br><br><br></div>

### Problem 2.
For the function
$u\left(x,y\right)=\ln⁡(1+xy^2)$,
show that the second order partial derivative
$\frac{\partial^2 u}{\partial x \partial y}$
is equal to
$\frac{\partial^2 u}{\partial y \partial x}$
(note the order of differentiation) by calculating both ways.

<div class = "answer">
$$
\frac{\partial{}u}{\partial{}x}=\frac{y^2}{1+xy^2}
$$

$$
\frac{\partial^2 u}{\partial y \partial x}
= \frac{\partial}{\partial y} \frac{\partial u}{\partial x}
= \frac{2y\left(1+xy^2\right) - y^2(2xy)}{(1+xy^2)^2}
= \frac{2y+2xy^3-2xy^3}{(1+xy^2)^2}
= \frac{2y}{(1+xy^2)^2}
$$
    
$$
\frac{\partial u}{\partial y} = \frac{2 x y}{1+xy^2}
$$
    
$$
\frac{\partial^2 u}{\partial x \partial y}
= \frac{\partial}{\partial x} \frac{\partial u}{\partial y}
= \frac{(-2 x y)y^2}{((1+xy^2)^2} + \frac{2y}{1+xy^2}
= \frac{(-2 x y)y^2 + 2y\left(1+xy^2\right)}{(1+xy^2)^2}
= \frac{2y}{(1+xy^2)^2}
$$
</div>
<div class = "workingout"><br><br><br><br><br><br><br><br></div>

### Problem 3.
Find the turning points,
$[x_0, y_0, f(x_0,y_0)]$,
for the partial derivatives of the function
$f(x,y) = x e^{-x^2 - y^2}$.

<div class = "answer">
$$ f_x(x,y) = \frac{\partial f}{\partial x} = e^{-x^2 - y^2} + -2x^2 e^{-x^2 - y^2} $$

$$ f_y(x,y) = \frac{\partial f}{\partial y} = -2 x y e^{-x^2 - y^2} $$

$\Rightarrow{}$ for $f_x = 0$

$$ f_x = 1 + -2x^2 = 0 \Rightarrow x = \pm\frac{1}{\sqrt{2}} $$

$\Rightarrow{}$ for $f_y = 0$

$$ f_y = -2 x y = 0 \Rightarrow y = 0 $$

$$ \boxed{ f(\pm \frac{1}{\sqrt{2}}, 0) = \pm \frac{1}{\sqrt{2}} e^{-1/2} }$$
</div>
<div class = "workingout"><br><br><br><br><br><br><br><br></div>


-----------------------------------------------------------------------------------

## Challenging Questions
### Problem 4.
For functions $f(u, v)$, $u(x, y)$, and $v(x, y)$,
calculate the partial derivative $\frac{\partial f}{\partial y}$,
by direct substitution then the total derivative chain rule. Check that the approaches match.


(a) $ f(u, v) = \sin(u)\exp(-v), 
\quad 
u(x, y) = x / y, 
\quad v
(x, y) = x y $
<div class = "answer">
Direct substitution:    $f(x, y) = \sin(x / y)\exp(-x y)$

$$
\left(\frac{\partial f}{\partial y}\right)_x = -\frac{x e^{-x y} \cos(x/y)}{y^2} - x e^{-xy} \sin(x/y)
$$

<br>
$\Rightarrow{}$ Chain rule: $ \left(\frac{\partial f}{\partial y}\middle)_x
= \middle(\frac{\partial f}{\partial u}\middle)_v
    \middle(\frac{\partial u}{\partial y}\middle)_x + 
\middle(\frac{\partial f}{\partial v}\middle)_u
    \middle(\frac{\partial v}{\partial y}\right)_x $


\begin{align*}
\left(\frac{\partial f}{\partial u}\right)_v &= e^{-v} \cos u &
\left(\frac{\partial f}{\partial v}\right)_u &= -e^{-v} \sin u
\newline
\left(\frac{\partial u}{\partial y}\right)_x &= -\frac{x}{y^2} &
\left(\frac{\partial v}{\partial y}\right)_x &= x
\end{align*}

<br>
$$
\Rightarrow{} \boxed{ \left(\frac{\partial f}{\partial y}\right)_x
= -\frac{x e^{-x y} \cos(x/y)}{y^2} - x e^{-xy} \sin(x/y) }
$$
</div>

(b) $f(u, v) = u^2 + 2 u v + v^2,
\quad
u(x, y) = \sin(x + 5 y),
\quad
v(x, y) = \cos(x + 5 y)$

<div class = "answer">
$\Rightarrow$ Direct substitution:

$f(x, y) = 1 + 2 \sin(x + 5 y) \cos(x + 5 y)$


$$
\left(\frac{\partial f}{\partial y}\right)_x = 10 \cos^2(x + 5 y) - 10 \sin^2(x + 5 y)
$$


$\Rightarrow$ Chain rule

\begin{align*}
\left(\frac{\partial f}{\partial u}\right)_v &= 2 u + 2 v &
\left(\frac{\partial f}{\partial v}\right)_u &= 2 u + 2 v
\newline
\left(\frac{\partial u}{\partial y}\right)_x &= 5 \cos(x + 5y) &
\left(\frac{\partial v}{\partial y}\right)_x &= -5 \sin(x + 5 y)
\end{align*}

<br>
$$
\Rightarrow{} \boxed{ \left(\frac{\partial f}{\partial y}\right)_x
= 10 \cos^2(x + 5 y) - 10 \sin^2(x + 5 y) }
$$
</div>

(c) 
$f(u, v) = \frac{\arctan(u)}{1 + v^2},
\quad
u(x, y) = \sqrt{x y},
\quad
v(x, y) = x \ln(3 y)
$

<div class = "answer">
$\Rightarrow{}$ Direct substitution:

$f(x, y) = \frac{\arctan(\sqrt{x y})}{1 + (x \ln(3 y))^2}$

$$
\left(\frac{\partial f}{\partial y}\right)_x
= \frac{1}{(1+xy)(1+x^2 \ln(3 y)^2)}\frac{x}{2\sqrt{xy}} -\frac{2 x \ln(3 y) \arctan(\sqrt{x y})}{(1+x^2 \ln(3 y)^2)^2} x / y
$$

$\Rightarrow{}$ Chain rule:

\begin{align*}
\left(\frac{\partial f}{\partial u}\right)_v
&= \frac{1}{(1+u^2)(1+v^2)} 
&
\left(\frac{\partial f}{\partial v}\right)_u
&= -\frac{2 v \arctan(u)}{(1+v^2)^2}
\newline
\left(\frac{\partial u}{\partial y}\right)_x
&= \frac{x}{2\sqrt{xy}} 
&
\left(\frac{\partial v}{\partial y}\right)_x
&= x / y
\end{align*}

<br>

$$\Rightarrow{} \boxed{ \left(\frac{\partial f}{\partial y}\right)_x
= \frac{1}{(1+xy)(1+x^2 \ln(3 y)^2)}\frac{x}{2\sqrt{xy}} -\frac{2 x \ln(3 y) \arctan(\sqrt{x y})}{(1+x^2 \ln(3 y)^2)^2} x / y } $$
</div>

(d) $f(u, v) = \tanh(w u + v),
\quad
u(x, y) = \tanh(x a + y),
\quad
v(x, y) = y$

<div class = "answer">
$f(x, y) = \tanh(w \tanh(x a + y) + y)$


$$
\left(\frac{\partial f}{\partial y}\right)_x
= w \operatorname{sech}(w \tanh(x a + y) + y)^2
\operatorname{sech}(a x + y)^2 + 
\operatorname{sech}(w \tanh(x a + y) + y)^2
$$


$\Rightarrow{}$ Chain rule:

\begin{align*}
\left(\frac{\partial f}{\partial u}\right)_v &= 
w \operatorname{sech}(w u + v)^2
&
\left(\frac{\partial f}{\partial v}\right)_u
&= \operatorname{sech}(w u + v)^2
\newline
\left(\frac{\partial u}{\partial y}\right)_x &= 
\operatorname{sech}(a x + y)^2
&
\left(\frac{\partial v}{\partial y}\right)_x = 1
\end{align*}
   

$$
\boxed{ \left(\frac{\partial f}{\partial y}\right)_x
= w \operatorname{sech}(w \tanh(x a + y) + y)^2
    \operatorname{sech}(a x + y)^2 + 
    \operatorname{sech}(w \tanh(x a + y) + y)^2 }
$$

</div>
<div class = "workingout"><br><br><br><br><br><br><br><br></div>

### Problem 5.
If $f\left(x,y\right)=\sqrt[ 3 ]{x^3+y^3}$, find $f_x\left(a,0\right)$

<div class = "answer">
Note that by regular differentiation:}
$$
f'_x(x,y)=\frac{3x^2}{3(x^3+y^2)^{2/3}}
$$

$$
\boxed{ f'_x(a,0)=1 }
$$
</div>
<div class = "workingout"><br><br><br><br><br><br><br><br></div>

### Problem 6.
The ellipsoid $4x^2+2y^2+z^2=16$ intersects the plane $y=2$ in an ellipse. Find parametric equations for the tangent line to this ellipse at the point (1, 2, 2).

<div class = "answer">
The key is that since we are looking at the plane $y=2$, the slope is actually just $\frac{\partial{}z}{\partial{}x}$. So, we implicitly differentiate:

First, we need to find a function for $z$:

\begin{align*}
z^2 &= -4x^2-2y^2+16 
\newline
z &= \sqrt{-4x^2-2y^2+16}
\end{align*}

So we get:

$$ \frac{\partial{}z}{\partial{}x}=\frac{\partial{}}{\partial{}x} \sqrt{-4x^2-2y^2+16} $$

$$ \frac{df(u)}{dx}=\frac{df}{du}.\frac{du}{dx} $$

Let $u=-4x^2-2y^2+16$

$$ \frac{df}{du}=\frac{1}{2\sqrt{u}}\ \ \ \frac{du}{dx}=-8x $$

$$ \frac{\partial{}z}{\partial{}x}=\frac{1}{2\sqrt{u}} (-8x)=\frac{-8x}{2\sqrt{-4x^2-2y^2+16}} $$

Adding the values of x, y; we have:

$$ \frac{\partial{}z}{\partial{}x}=\frac{-8}{2\sqrt{4}}=-2 $$

The tangent line through that point, in the y = 2 plane, is:

$$ z = -2x + 4 $$

To get the parametric equation of the line, take $x = t$:

$$ \boxed{ x = t, \quad y=2, \quad z = -2t + 4 } $$
</div>
<div class = "workingout"><br><br><br><br><br><br><br><br></div>

### Problem 7.
Calculate the divergence ($\nabla \cdot$) and the curl ($\nabla \times$) of the following vector fields:

(a) ${x} = \begin{bmatrix}
    x \newline y \newline z \end{bmatrix}$
<div class = "answer">
For any column vector v:

$$ \nabla \cdot \mathbf{v} = 
\frac{\partial v_x}{\partial x} + 
\frac{\partial v_y}{\partial y} + 
\frac{\partial v_z}{\partial z}$$

$$\nabla\times\mathbf{v} = \begin{vmatrix}
\mathbf{i} & \mathbf{j} & \mathbf{k}
\newline
\frac{\partial}{\partial x}
& \frac{\partial}{\partial y}
& \frac{\partial}{\partial z}
\newline
v_x & v_y & v_z
\end{vmatrix} 
= \begin{bmatrix}
\frac{\partial v_z}{\partial y} - \frac{\partial v_y}{\partial z} \newline
\frac{\partial v_x}{\partial z} - \frac{\partial v_z}{\partial x} \newline
\frac{\partial v_y}{\partial x} - \frac{\partial v_x}{\partial y}
\end{bmatrix}
$$

<br>

$$ \boxed{ \nabla \cdot \mathbf{x} = 3, \ \ \ \nabla \times \mathbf{x} = \begin{bmatrix} 0 \newline 0 \newline 0 \end{bmatrix} } $$
</div>

(b) ${u} = \begin{bmatrix}
    -y \newline x \newline 3 z^2
    \end{bmatrix}$

<div class = "answer">
$$
\boxed{ \nabla \cdot \mathbf{u} = 6 z, \ \ \ \nabla \times \mathbf{u} = \begin{bmatrix} 0 \newline 0 \newline 2 \end{bmatrix} }
$$
</div>

(c) ${a} = \begin{bmatrix}
    0 \newline 0 \newline x z
    \end{bmatrix}$

<div class = "answer">
$$
\boxed{ \nabla \cdot \mathbf{a} = x, \ \ \ \nabla \times \mathbf{a} = \begin{bmatrix} 0 \newline -z \newline 0 \end{bmatrix} }
$$
</div>

(d) ${p} = \begin{bmatrix}
    x y z \newline x^2 + y^2 \newline -z
    \end{bmatrix}$

<div class = "answer">
$$
\boxed{ \nabla \cdot \mathbf{p} = y z + 2 y -1, \ \ \ \nabla \times \mathbf{p} = \begin{bmatrix} 0 \\ x y \\ 2x-xz \end{bmatrix} }
$$
</div>

(e) ${q} = \begin{bmatrix}
    \sin x \cos y \sin z \newline \cos x \sin y \sin z \newline \cos z
    \end{bmatrix}$

<div class = "answer">
$$\boxed{ \nabla \cdot \mathbf{q} = -\sin z + 2 \cos x \cos y \sin z, \ \ \ \nabla \times \mathbf{q} = \begin{bmatrix} -\cos x \sin y \cos z \newline \sin x \cos y \cos z \newline 0 \end{bmatrix} }$$
</div>
<div class = "workingout"><br><br><br><br><br><br><br><br></div>


-----------------------------------

## Exam Style Questions
### Problem 8.
Show that the function $u\left(x,y\right)=\ln⁡(1+xy^2)$ satisfies the partial differential equation:
$$ 2\frac{ {\partial{}}^2u}{ {\partial{}x}^2}+y^3\frac{ {\partial{}}^2u}{\partial{}y\partial{}x}=0 $$

<div class = "answer">
$$
\frac{\partial{}u}{\partial{}x}=\frac{y^2}{1+xy^2}\ ;\ \ \
\frac{ {\partial{}}^2u}{ {\partial{}x}^2}=-\frac{y^2}{ {\left(1+{xy}^2\right)}^2}.y^2=\frac{-y^4}{ {\left(1+{xy}^2\right)}^2}
$$

<br>
$$
\frac{ {\partial{}}^2u}{\partial{}y\partial{}x}=\frac{\partial{}}{\partial{}y}\left(\frac{\partial{}u}{\partial{}x}\right)=\frac{2y\left(1+xy^2\right)-y^2(2xy)}{ {(1+xy^2)}^2}=\frac{2y+2xy^3-2xy^3}{ { {(1+xy}^2)}^2}=\frac{2y}{ { {(1+xy}^2)}^2}
$$

<br>
$$ \boxed{
2\frac{ {\partial{}}^2u}{\partial{}x^2}+y^3\frac{ {\partial{}}^2u}{\partial{}y\partial{}x}=-\frac{2y^4}{ { {(1+xy}^2)}^2}+\frac{ {2y}^4}{ { {(1+xy}^2)}^2}=0 }
$$
</div>
<div class = "workingout"><br><br><br><br><br><br><br><br></div>

### Problem 9.
If $ g\left(s,t\right)=f(s^2-t^2,\ t^2-s^2) $ and $f$ is differentiable, show that $g$ satisfies the equation:}
$$ t\frac{\partial{}g}{\partial{}s}+s\frac{\partial{}g}{\partial{}t}=0 $$

<div class = "answer">
Let $x=s^2-t^2$ and $y=t^2-s^2$. Then $g(s,t)=f(x,y)$, and by the chain rule:

<br>
$$
\frac{\partial{}g}{\partial{}s}=\frac{\partial{}f}{\partial{}x}\frac{\partial{}x}{\partial{}s}+\frac{\partial{}f}{\partial{}y}\frac{\partial{}y}{\partial{}s}=(\frac{\partial{}f}{\partial{}x})(2s)+(\frac{\partial{}f}{\partial{}y})(-2s)
$$

<br>
$$
\frac{\partial{}g}{\partial{}t}=\frac{\partial{}f}{\partial{}x}\frac{\partial{}x}{\partial{}t}+\frac{\partial{}f}{\partial{}y}\frac{\partial{}y}{\partial{}t}=(\frac{\partial{}f}{\partial{}x})(-2t)+(\frac{\partial{}f}{\partial{}y})(2t)
$$

<br>
$$ \boxed{
t\frac{\partial{}g}{\partial{}s}+s\frac{\partial{}g}{\partial{}t}=(\frac{\partial{}f}{\partial{}x})(2st)+(\frac{\partial{}f}{\partial{}y})(-2st)+(\frac{\partial{}f}{\partial{}x})(-2st)+(\frac{\partial{}f}{\partial{}y})(2st)=0 }$$

</div>
<div class = "workingout"><br><br><br><br><br><br><br><br></div>


## Answers

<button type="button" onclick="displayAnswerButtons('block')">Show answer buttons</button>
<button type="button" onclick="displayAnswers('block')">Show all answers</button>
<button type="button" onclick="displayAnswers('none')">Hide all answers</button>
<br><br>
### For Printing
<button type="button" onclick="prepareForPrint('block')">Add whitespace</button>
<button type="button" onclick="prepareForPrint('none')">Remove whitespace</button>

<br><br>

# Next week, Partial Differential Equations!