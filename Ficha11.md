# Ficha 11

## Problema 1.

Considere o campo vetorial $F:\mathbb{R}^2\to\mathbb{R}^2$ definido por $F(x,y)=(-2y,x)$ e o conjunto 

$$D=\{(x,y)\in\mathbb{R}^2 : x^2+y^2<1\,;\,y>\vert x\vert\}.$$ 

Calcule o trabalho realizado por $F$ ao longo da fronteira do conjunto $D$ no sentido anti-horário.

**Solução.**

Queremos calcular o trabalho realizado por $F$ ao longo de $\mathcal{C}$,
$$W=\int_{\mathcal{C}} \vec{F}\cdot d\vec{r}$$

<iframe src="https://www.geogebra.org/classic/njug6jft?embed" width="800" height="600" allowfullscreen style="border: 1px solid #e4e4e4;border-radius: 4px;" frameborder="0"></iframe>

Como podemos observar, é natural decompor $\mathcal{C}=\mathcal{C}_1\cup\mathcal{C}_2\cup\mathcal{C}_3$, como mostrado na figura, de maneira que 

$$W=\int_{\mathcal{C}} \vec{F}\cdot d\vec{r}=\int_{\mathcal{C}_1} \vec{F}\cdot d\vec{r} + \int_{\mathcal{C}_2} \vec{F}\cdot d\vec{r} + \int_{\mathcal{C}_3} \vec{F}\cdot d\vec{r}.\qquad\textit{``Divide et impera"}\quad (\textsf{Julio Cesar})$$

Não é dificil parametrizar cada uma destas componentes da curva $\mathcal{C}$ e calcular o trabalho total como a soma do trabalho realizado pelo campo de vetores $\vec{F}$ em cada componente. Porém, há uma forma mais direta de calcular o trabalho, usando o **Teorema de Green**. 

![Teorema de Green](https://raw.githubusercontent.com/jarpepegit/Tutoring/main/Francisco/TeoremaGreen.png)

Notemos que $\vec{F}=(F_1,F_2)=(-2y,x)$ é de classe $C^1$ no seu domínio, que é $\mathbb{R}^2$, e a região $D\subset\textsf{aberto}\subset\operatorname{Dom}(\vec{F})$. Logo, 

$$\int_{\mathcal{C}}\vec{F}\cdot d\vec{r} = \int\int_{D}\left(\frac{\partial F_2}{\partial x}-\frac{\partial F_1}{\partial y}\right) dD = \int\int_{D}\left(1-(-2)\right) dD = 3 \int\int_{D} dD = 3\operatorname{Area}(D) .$$

Claramente, convém usar coordenadas polares para calcular este integral duplo. Assim, temos que

$$\operatorname{Area}(D)=\int\int_{D} dD = \int_{\frac{\pi}{4}}^{\frac{3\pi}{4}}\int_{0}^1 r \,dr\,d\theta=\int_{\frac{\pi}{4}}^{\frac{3\pi}{4}}\tfrac{1}{2}r^2\Bigg|_{r=0}^{r=1}\,d\theta=\tfrac{1}{2}\theta\Bigg|_{\theta=\tfrac{\pi}{4}}^{\theta=\tfrac{3\pi}{4}}=\frac{1}{\cancel{2}}\frac{\cancel{2}\pi}{4}=\frac{\pi}{4}.$$

Logo, 

$$W=\oint_{\mathcal{C}}\vec{F}\cdot d\vec{r} =  \int\int_{D}\left(\frac{\partial F_2}{\partial x}-\frac{\partial F_1}{\partial y}\right) dD = 3\operatorname{Area}(D) = \frac{3\pi}{4}.$$

---

## Problema 5.
Considere o campo vetorial definido por
$$F(x,y,z) = \left(\frac{3y}{x^2+y^2}-2y, \frac{-3x}{x^2+y^2}+5x,z^2\right)$$

> a) Calcule o trabalho de $F$ ao longo do caminho $g(t)=(1,1,t)$, $t\in[0,5]$.

**Solução.**
$$\begin{split} W &=\int_{\mathcal{C}}\vec{F}\cdot d\vec{r}\\[2ex] 
&= \int_0^5 \left(\tfrac{3}{2}-2,-\tfrac{3}{2}+5,t^2\right)\cdot(0,0,1)\,dt \\[2ex] 
&= \int_0^5 t^2\,dt = \frac{t^3}{3}\Bigg|_{t=0}^{t=5}=\frac{5^3}{3}\end{split}.$$

---
> b) Calcule o trabalho de $F$ ao longo da curva dada pelas equações $y=1$, $x^2+z^2=1$, orientada num sentido à sua escolha.

**Solução.**

Claramente, a curva $\mathcal{C}$ em questão é uma circunferência de raio $1$, com centro em $(0,1,0)$, situada no plano $y=1$, paralelo ao plano $XZ$. Portanto, 

$$\begin{split} W &= \oint_{\mathcal{C}}\vec{F}\cdot d\vec{r}\\[2ex]
&= \int_0^{2\pi} \left(\tfrac{3}{\cos^2\theta+1}-2,\tfrac{-3\cos\theta}{\cos^2\theta+1}+5\cos\theta,\sin^2\theta\right)\cdot(-\sin\theta,0,\cos\theta)\,d\theta \\[2ex]
&= ...\textsf{uhmmm... não existe uma forma mais simples de calcular?}
\end{split}$$

![Cilindro intersectado com o plano](https://raw.githubusercontent.com/jarpepegit/Tutoring/main/Francisco/CilindroPlano.png)

O domínio do campo vetorial $F$ é $\mathbb{R}^3\setminus\{(0,0,z)\in\mathbb{R}^3: z\in\mathbb{R}\}$. O  campo $F$ é claramente de classe $C^1$ no seu domínio.  O caminho $\mathcal{C}$ situa-se dentro do domínio de $F$. Ele é **homotópico** ao caminho constante $(1,1,0)$. 

> *A circunferência* $\mathcal{C}$ *pode ser deformada continuamente, sem sair do domínio de* $F$, *até se tornar o ponto* $(1,1,0)$. 

Ora bem, uma vez que para um caminho constante cumpre-se que $d\vec{r}=\vec{r}\,'(t)\,dt = 0$, podemos concluir que:

> *O trabalho de qualquer campo vetorial sobre um caminho constante é zero.*

Como sabemos, o trabalho realizado por um campo vetorial sobre caminhos homotópicos $\mathcal{C}_1$ e $\mathcal{C}_2$ é invariante, isto é:

$$\int_{\mathcal{C}_1}\vec{F}\cdot d\vec{r}=\int_{\mathcal{C}_2}\vec{F}\cdot d\vec{r}$$

Logo, 

$$W=\int_{\mathcal{C}}\vec{F}\cdot d\vec{r} = 0.$$

----

Vamos a poner una matriz aqui
$$\begin{pmatrix}1 & 0 \\ 0 & 1\end{pmatrix}$$


> Written with [StackEdit](https://stackedit.io/).
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTE4NTA3NDg0MDgsNTAzMzgzODkwXX0=
-->