# Ficha 8.

## Problema 2b)

O nosso erro foi representar incorretamente a região. De facto, a região $\mathcal{D}$ nas perspectivas cartesiana e polar é dada por

$$\boxed{\begin{array}{c}\underline{\textsf{cartesiana}} \\[3ex] x\le y\le \sqrt{2-x^2} \\[2ex] 0\le x\le 1\end{array}}\qquad \boxed{\begin{array}{c}\underline{\textsf{polar}} \\[3ex] \dfrac{\pi}{4}\le \theta\le \dfrac{\pi}{2} \\[2ex] 0\le r\le \sqrt{2}\end{array}}$$

<iframe src="https://www.geogebra.org/classic/nkx6ysuv?embed" width="800" height="600" allowfullscreen style="border: 1px solid #e4e4e4;border-radius: 4px;" frameborder="0"></iframe>

Desta forma, segue-se que

$$\underbrace{\displaystyle\int_0^1\left(\displaystyle\int_x^{\sqrt{2-x^2}}\dfrac{1}{1+x^2+y^2}dy\right)dx}_{\textsf{cartesianas}} = \underbrace{\displaystyle\int_{\frac{\pi}{4}}^{\frac{\pi}{2}}\left(\displaystyle\int_0^{\sqrt{2}}\dfrac{1}{1+r^2}\,\,{\color{red}r}\,\, dr\right)d\theta}_{\textsf{polares}}=\frac{\pi\ln 3}{8}.$$

---

## Problema 3

a) Já tínhamos determinado as imagens dos vértices do triângulo $T$. Estes são, do vértice $A=(0,0)$, a imagem é $A'=(0,0)$, do vértice $B=(1,0)$, a imagem é $B'=(2,1)$, do vértice $C=(0,2)$, a imagem é $C'=(2,-2)$. Para ter uma ideia cabal da região $S$, imagem via a transformação $x=2u+v$, $y=u^2 -v$, só precisamos saber como se transformam os segmentos que conformam a fronteira do triângulo $T$. Assim, por exemplo, o segmento $AB$ ($0\le u\le 1$, $v=0$) do triângulo $T$, tem como imagem os pontos $x=2u$, $y=u^2$. Portanto, $y=\frac{1}{4}x^2$. Procedemos similarmente com os outros segmentos fronteira do triângulo $T$. Temos assim que

![Prob2bFicha8](https://raw.githubusercontent.com/jarpepegit/Tutoring/main/Francisco/Prob2bFicha8.png)


b) Antes de avançar com a solução desta parte, recordemos que o  valor absoluto do Jacobiano da transformação associada é 	 $$ \boxed{\vert J(u,v)\vert=\left\vert\operatorname{det}\begin{pmatrix}x_u & x_v \\ y_u & y_v\end{pmatrix}\right\vert = \vert x_uy_v-x_vy_u\vert = \vert -2-2u\vert = 2(1+u)}$$
Ora bem, comecemos

$$\begin{split}\displaystyle\int\int_S\dfrac{1}{\sqrt{x+y+1}}\,dxdy &= \displaystyle\int\int_T\dfrac{1}{\sqrt{2u+v+u^2-v+1}}{\color{red}\vert J(u,v)\vert}\,dudv \\[2ex] &= \displaystyle\int\int_T\dfrac{1}{\sqrt{2u+u^2+1}}{\color{red}2(1+u)}\,dudv\\[2ex] &= \displaystyle\int\int_T\dfrac{1}{\sqrt{(u+1)^2}}{\color{red}2(1+u)}\,dudv\\[2ex] &=2\displaystyle\int\int_T\dfrac{1}{(u+1)}{\color{red}(1+u)}\,dudv \end{split} $$
Como $0\le u\le 1$, segue-se que $u+1>0$ . Logo, podemos concluir, usando a geometria do problema, que
$$\displaystyle\int\int_S\dfrac{1}{\sqrt{x+y+1}}\,dxdy \,\,=\,\, 2\displaystyle\int\int_T 1\,dudv \,\,=\,\, 2\operatorname{Area}(T) \,\,=\,\, 2$$

A **pior estratégia** teria sido calcular o integral do lado direito acima, usando os correspondentes limites de integração
$$2\displaystyle\int\int_T\dfrac{1}{(u+1)}{\color{red}(1+u)}\,du\,dv
\,\,=\,\,2\displaystyle\int_0^1\int_0^{2(1-u)} 1 \,dv\,du \,.$$

---

## Problema 4.
Considere o conjunto $$D=\left\{(x,y)\in\mathbb{R}^2:\quad 1<x+y<2\quad,\quad 0<x<y\right\}$$
e seja $f:D\to\mathbb{R}$ definida por $f(x,y)=(y^2-x^2)\cos(x+y)^4$.  Calcule $\int_Df$ utilizando uma transformação de coordenadas apropriada. Justifique cuidadosamente.

**Ideias** 

> - Olhando para as desigualdades na definição de $D$, podemos afirmar que a fronteira de $D$ está conformada por segmentos de recta. no plano $XY$. Portanto a nossa região é um quadrilátero, uma vez que temos a interseção de 4 desigualdades, todas elas sem sobreposição evidente. Mais ainda, dois equações de fronteira ($1=x+y$ e $x+y=2$) são paralelas, logo, a região deve ser um trapézio.
>  - Se usamos uma transformação é linear, podemos levar segmentos em segmentos. Se ainda a **trasformação linear** é **não degenerada** (Jacobiano com determinante não nulo) o tipo de quadrilátero é preservado, neste caso, transforma um **trapézio noutro trapézio** nas novas coordenadas. Caso contrário, transforma um trapézio num triângulo, ou ainda num segmento ou num ponto.

Olhando para a função $f(x,y)=(y^2-x^2)\cos(x+y)^4$, pensámos que a transformação que mais poderia facilitar o cálculo seria
$$\begin{array}{lcl}
u &=& x+y \\
v &=& -x+y
\end{array}$$
Porquê? Porque, por um lado, o determinante Jacobiano da transformação correspondente nas coordenadas $x,y$ é 
$$J(x,y)=\operatorname{det}\begin{pmatrix}u_x & u_y \\ v_x & v_y\end{pmatrix}=u_xv_y-u_yv_x=\operatorname{det}\begin{pmatrix}1 & 1 \\ -1 & 1\end{pmatrix}=2.$$
Logo, o determinante Jacobiano da inversa da transformação anterior nas coordenadas $u,v$ é
$$J(u,v)=\frac{1}{2}$$
Se olhamos para as imagens dos segmentos que formam a fronteira do trapézio via esta transformação, temos que 
$$D'= \left\{(u,v)\in\mathbb{R}^2:\quad 1<u<2\quad,\quad 0<v<u\right\}$$ Coloquemos os sistemas de eixos coordenados $XY$ e $UV$ sobrepostos para comparar $D$ com $D'$. Assim, temos que

<iframe src="https://www.geogebra.org/classic/rtt64mef?embed" width="800" height="600" allowfullscreen style="border: 1px solid #e4e4e4;border-radius: 4px;" frameborder="0"></iframe>

Por outro lado, $y^2-x^2=(y-x)(y+x)$ e, portanto, $f$ nas novas coordenadas é $f(u,v)=vu\,\cos u^4$. Desta forma, o integral que temos de calcular é 

$$\displaystyle\int_D f = \displaystyle\int\displaystyle\int_{D'} vu\,\cos u^4\,\tfrac{1}{2}du\,dv.$$

O problema é que, recordemos, ao tentar integrar usando, por exemplo, integração por partes, a coisa ficava ainda mais complexa...**sinal de alerta**, a transformação escolhida não é a mais apropriada. Portanto, temos de **procurar outra transformação** Que tal, desta vez tentar com

$$\begin{array}{lcl}
u &=& x+y \\
v &=& x
\end{array}$$

O determinante Jacobiano da transformação correspondente nas coordenadas $x,y$ é 

$$J(x,y)=\operatorname{det}\begin{pmatrix}u_x & u_y \\ v_x & v_y\end{pmatrix}=u_xv_y-u_yv_x=\operatorname{det}\begin{pmatrix}1 & 1 \\ 1 & 0\end{pmatrix}=-1.$$

Logo, 

$$J(u,v)=\frac{1}{-1}=-1$$ 

Nas novas coordenadas $(u,v)$, o trapézio $D''$ é dado por 

$$D''=\left\{(u,v)\in\mathbb{R}^2:\quad 1<u<2\quad,\quad 0<v<\frac{u}{2}\right\}$$

Colocando os sistemas de coordenadas $XY$ e $UV$ sobrepostos para comparar $D$ com $D''$, temos

<iframe src="https://www.geogebra.org/classic/e724gr5a?embed" width="800" height="600" allowfullscreen style="border: 1px solid #e4e4e4;border-radius: 4px;" frameborder="0"></iframe>

O integral que temos de calcular é

$$\begin{split}\int\int_D (y^2-x^2)\cos (x+y)^4 \,dx\,dy &= \int\int_{D''} (u^2-2uv)\cos u^4 \,du\,dv \\[2ex]
&= \int_1^2 \cos u^4\left(\int_0^{\frac{u}{2}} (u^2-2uv)\,dv\right)du\\[2ex]
&= \int_1^2 \cos u^4\left(u^2v-2u\frac{v^2}{2}\right)\Bigg|_{v=0}^{v=u/2}\,du\\[2ex]
&= \int_1^2 \cos u^4\left(\frac{u^3}{2}-\frac{u^3}{4}\right)\,du \\[2ex]
&= \int_1^2 \frac{1}{4}u^3\cos u^4\,du\\[2ex]
&= \frac{1}{16}\sin u^4\Bigg|_{u=1}^{u=2} = \frac{1}{16}(\sin 16-\sin 1).
\end{split}$$

---
## Problema 7.
Calcule o momento de inercia do sólido
$$ U=\Big\{(x,y,z)\in\mathbb{R}^3  :  y^2+z^2 \le 1\,;\, 0\le x\le (y^2+z^2)^{\frac{1}{4}}\,;y\ge 0\,;\,z\ge 0\Big\},$$
relativamente ao eixo $Ox$, e cuja densidade de massa é dada por $\sigma(x,y,z)=x(y^2+z^2)$.

**Solução.**

Dos apontamentos do Prof. João Pimentel, pág. 61, retirei o seguinte excerto:

![Momento de Inércia](https://raw.githubusercontent.com/jarpepegit/Tutoring/main/Francisco/MomentoDeInercia.png)

Logo, o momento de inércia do sólido em questão é

$$I_x=\int\,\int\,\int_U (y^2+z^2)\sigma(x,y,z)\,dV = \int\,\int\,\int_U x(y^2+z^2)^2\,dV$$

O sólido $U$ é mais simples de descrever em coordenadas **cilíndricas**

$$\begin{array}{lcl}
 y &=& r\cos\theta \\
 z &=& r\sin\theta \\
 x &=& x
\end{array}\quad\implies\quad U'=\Big\{(r,\theta,x)\in\mathbb{R}^3  :  \quad 0\le r\le 1\,\,;\,\,0\le x\le r^{\frac{1}{2}}\,\,;\,\,0\le\theta\le\frac{\pi}{2}\Big\} $$

De forma que,

$$\begin{split}
y^2+z^2=r^2 \\
dV = r\,dr\,d\theta\,dx
\end{split}$$

Portanto:

$$
I_x = \int_0^{\pi/2} \int_0^1 \int_0^{\sqrt{r}} (r^2)^2 \cdot x \cdot r\, dx\, dr\, d\theta
= \int_0^{\pi/2} \int_0^1 \int_0^{\sqrt{r}} r^4 x r\, dx\, dr\, d\theta
= \int_0^{\pi/2} \int_0^1 r^5 \left[\int_0^{\sqrt{r}} x\, dx \right] dr\, d\theta
$$

---

### **Cálculo da integral interior**

$$
\int_0^{\sqrt{r}} x\, dx = \left. \frac{x^2}{2} \right|_0^{\sqrt{r}} = \frac{r}{2}
$$

Então:

$$
I_x = \int_0^{\pi/2} \int_0^1 r^5 \cdot \frac{r}{2}\, dr\, d\theta = \int_0^{\pi/2} \int_0^1 \frac{r^6}{2}\, dr\, d\theta
$$

---

### **Integrais finais**

$$
\int_0^1 \frac{r^6}{2} dr = \frac{1}{2} \cdot \frac{1}{7} = \frac{1}{14}
\quad \text{e} \quad
\int_0^{\pi/2} d\theta = \frac{\pi}{2}
$$

Logo:

$$
I_x = \frac{\pi}{2} \cdot \frac{1}{14} = \boxed{\frac{\pi}{28}}
$$

---
## Problema 11.
Seja $f:\mathbb{R}^2\to\mathbb{R}$ uma função de classe $C^1$. Calcule $G'(x)$ onde $G:\mathbb{R}\to\mathbb{R} é uma função definida pela expressão
$$G(x)=\int_x^{x^3}f(tx,t^2+x^3)\,dt$$

**Solução**

Recordemos a regra de Leibniz para derivação sob o integral

![Derivação sob o integral](https://raw.githubusercontent.com/jarpepegit/Tutoring/main/Francisco/RegraLeibnizDerivIntegral.png)

Logo, 

$$\begin{split}\frac{d}{dx} G(x) &=\frac{d}{dx}\int_x^{x^3} f(tx,t^2+x^3)\,dt \\[2ex]
&=f(x^4,x^6+x^3)\frac{d}{dx}x^3-f(x^2,x^2+x^3)\frac{d}{dx}x+\int_x^{x^3}\frac{\partial}{\partial x}f(\underbrace{tx}_{u},\underbrace{t^2+x^3}_{v})\,dt\\[2ex]
&=3x^2f(x^4,x^6+x^3)-f(x^2,x^2+x^3)+\int_{x}^{x^3} (f_u u_x+f_v v_x)\,dt \\[2ex]
&=3x^2f(x^4,x^6+x^3)-f(x^2,x^2+x^3)+\int_{x}^{x^3} (t f_u(u,v) + 3x^2f_v(u,v) )\,dt .
\end{split}$$








> Written with [StackEdit](https://stackedit.io/).
