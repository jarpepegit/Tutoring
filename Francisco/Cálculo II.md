## Problema 2b)

O nosso erro foi representar incorretamente a região. De facto, a região $\mathcal{D}$ nas perspectivas cartesiana e polar é dada por

$$\boxed{\begin{array}{c}\underline{\textsf{cartesiana}} \\[3ex] x\le y\le \sqrt{2-x^2} \\[2ex] 0\le x\le 1\end{array}}\qquad \boxed{\begin{array}{c}\underline{\textsf{polar}} \\[3ex] \dfrac{\pi}{4}\le \theta\le \dfrac{\pi}{2} \\[2ex] 0\le x\le \sqrt{2}\end{array}}$$

<iframe src="https://www.geogebra.org/classic/nkx6ysuv?embed" width="800" height="600" allowfullscreen style="border: 1px solid #e4e4e4;border-radius: 4px;" frameborder="0"></iframe>
Desta forma, segue-se que

$$\underbrace{\displaystyle\int_0^1\left(\displaystyle\int_x^{\sqrt{2-x^2}}\dfrac{1}{1+x^2+y^2}dy\right)dx}_{\textsf{cartesianas}} = \underbrace{\displaystyle\int_{\frac{\pi}{4}}^{\frac{\pi}{2}}\left(\displaystyle\int_0^{\sqrt{2}}\dfrac{1}{1+r^2}\,\,{\color{red}r}\,\, dr\right)d\theta}_{\textsf{polares}}=\frac{\pi\ln 3}{8}.$$

---

## Problema 3

a) Já tínhamos determinado as imagens dos vértices do triângulo $T$. Estes são, do vértice $A=(0,0)$, a imagem é $A'=(0,0)$, do vértice $B=(1,0)$, a imagem é $B'=(2,1)$, do vértice $C=(0,2)$, a imagem é $C'=(2,-2)$. Para ter uma ideia cabal da região $S$, imagem via a transformação $x=2u+v$, $y=u^2 -v$, só precisamos saber como se transformam os segmentos que conformam a fronteira do triângulo $T$. Assim, por exemplo, o segmento $AB$ ($0\le u\le 1$, $v=0$) do triângulo $T$, tem como imagem os pontos $x=2u$, $y=u^2$. Portanto, $y=\frac{1}{4}x^2$. Procedemos similarmente com os outros segmentos fronteira do triângulo $T$. Temos assim que

![[Untitled-2025-06-09-2225.png]]

b) Antes de avançar com a solução desta parte, recordemos que o  valor absoluto do Jacobiano da transformação associada é 	 $$ \boxed{\vert J(u,v)\vert=\left\vert\operatorname{det}\begin{pmatrix}x_u & x_v \\ y_u & y_v\end{pmatrix}\right\vert = \vert x_uy_v-x_vy_u\vert = \vert -2-2u\vert = 2(1+u)}$$
Ora bem, comecemos
$$\begin{split}\displaystyle\int\int_S\dfrac{1}{\sqrt{x+y+1}}\,dxdy &= \displaystyle\int\int_T\dfrac{1}{\sqrt{2u+v+u^2-v+1}}{\color{red}\vert J(u,v)\vert}\,dudv \\[2ex] &= \displaystyle\int\int_T\dfrac{1}{\sqrt{2u+u^2+1}}{\color{red}2(1+u)}\,dudv\\[2ex] &= \displaystyle\int\int_T\dfrac{1}{\sqrt{(u+1)^2}}{\color{red}2(1+u)}\,dudv\\[2ex] &=2\displaystyle\int\int_T\dfrac{1}{(u+1)}{\color{red}(1+u)}\,dudv \end{split} $$
Como $0\le u\le 1$, segue-se que $u+1>0$ . Logo, podemos concluir, usando a geometria do problema, que
$$\displaystyle\int\int_S\dfrac{1}{\sqrt{x+y+1}}\,dxdy \,\,=\,\, 2\displaystyle\int\int_T 1\,dudv \,\,=\,\, 2\operatorname{Area}(T) \,\,=\,\, 2$$

A **pior estratégia** teria sido calcular o integral do lado direito acima, usando os correspondente limites de integração
$$2\displaystyle\int\int_T\dfrac{1}{(u+1)}{\color{red}(1+u)}\,du\,dv
\,\,=\,\,2\displaystyle\int_0^1\int_0^{2(1-u)} 1 \,dv\,du \,.$$

