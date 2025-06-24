# Ficha 9

## Problema 1.
Determine o comprimento $L$ do caminho $C$ parametrizado por $g:[0,1]\to\mathbb{R}^3$, com $g(t)=\left(t,\frac{1}{\sqrt{2}}t^2,\frac{1}{3}t^3\right)$.

**Solução.**

Para calcular o comprimento de um caminho, usamos a seguinte fórmula

$$L=\int_C ds,$$

onde $ds$ é o diferencial do comprimento de arco. Já agora, deixo-te um vídeo do professor russo de quem te falei, acerca de integrais de linha

<div align="center">
  <a href="https://www.youtube.com/watch?v=cV4VaaPdUtQ" target="_blank">
    <img src="https://img.youtube.com/vi/cV4VaaPdUtQ/hqdefault.jpg" alt="Integral over curves" width="520" />
  </a>
</div>

Voltando ao cálculo do comprimento do caminho dado. Temos a seguinte fórmula
$$L=\int_0^1 \sqrt{(x'(t))^2+(y'(t))^2+(z'(t))^2}\,dt=\int_0^1 \sqrt{1+2t^2+t^4}\,dt=\int_0^1(1+t^2)\,dt=\frac{4}{3}.$$

---
## Problema 4.
Para cada um dos casos seguintes calcule o trabalho realizado pelo campo vetorial ao longo do caminho indicado:
> b) Campo $f:\mathbb{R}^3\to\mathbb{R}^3$ definido por $f(x,y,z)=(x,z,z-y)$ e caminho definido por $g(t)=(t^2,\cos t,\sin t)$ com $t\in[0,\pi]$.

**Solução**

Por definição (ver pág. 87 dos apontamentos), o trabalho realizado pelo campo de forças contínuo $\vec{F}$ para deslocar uma partícula ao longo da curva $C$ é dado pelo integral curvilíneo de $\vec{F}$ ao longo de $C$,
$$\boxed{W=\int_C \vec{F}\cdot d\vec{r}}$$
O $\vec{r}$ representa a posição da partícula -- no nosso caso, $\vec{r}(t)=\vec{g}(t)$--. Logo, utilizando a informação proporcionada no enunciado, temos que
$$\begin{split}W=\int_C \vec{F}\cdot d\vec{r} &=\int_{0}^\pi \vec{F}(\vec{g}(t))\cdot\vec{g}'(t)\,dt \\[2ex]
&=\int_{0}^\pi (x(t),z(t),z(t)-y(t))\cdot(x'(t),y'(t),z'(t))\,dt \\[2ex]
&= \int_{0}^\pi (t^2,\sin t,\sin t-\cos t)\cdot(2t,-\sin t,\cos t)\,dt \\[2ex]
&= \int_{0}^\pi (2t^3 - \sin^2 t + \sin t\cos t - \cos^2t) \,dt\\[2ex]
&= \int_0^\pi (2t^3-1+\sin t\cos t)\,dt = \left(\frac{2t^4}{4} - t + \frac{\sin^2t }{2}\right)\Bigg|_{t=0}^{t=\pi}\\[2ex]
&= \frac{\pi^4}{2}-\pi\,.
 \end{split}$$

---
## Problema 5.
Calcule o trabalho realizado pelo campo vetorial $f(x,y,z)=(x,z,2y)$ ao longo das seguintes curvas:
> b) A intersecção das superfícies $x^2+y^2=1$ e $z=x^2-y^2$ num sentido que parece o anti-horário quando visto desde o ponto $(0,0,100)$.

**Solução**

A intersecção das duas superfícies é 

![Intersecção de duas superfícies](https://raw.githubusercontent.com/jarpepegit/Tutoring/main/Francisco/ParabHiperCilindro.png)

Podemos facilmente parametrizar esta curva,
$$\mathcal{C}:\,\left\{\begin{split}
x &=\cos\theta \\[2ex]
y &=\sin\theta \\[2ex]
z &=\cos2\theta
\end{split}\right.\qquad\textsf{com}\qquad 0\le\theta\le 2\pi$$

Logo, o trabalho realizado pelo campo $f$ ao longo do caminho $\mathcal{C}$ é
$$\begin{split}W &=\int_{\mathcal{C}}\vec{f}\cdot d\vec{r} \\[2ex]
&=\int_0^{2\pi} (\cos\theta,\cos2\theta,2\sin\theta)\cdot(-\sin\theta,\cos\theta,-2\sin2\theta)\,d\theta \\[2ex]
&=\int_0^{2\pi}(-\cos\theta\sin\theta + \cos2\theta\cos\theta - 4\sin\theta\sin2\theta)\,d\theta
\end{split}$$


---

### 🧮 Passo 2: Integrar termo a termo

#### Primeiro termo:
$$
\int_0^{2\pi} -\cos\theta\sin\theta \, d\theta = 0 \quad (\text{função ímpar num intervalo simétrico})
$$

#### Segundo termo:
$$
\int_0^{2\pi} \cos2\theta\cos\theta \, d\theta
$$

Usamos a identidade:
$$
\cos2\theta\cos\theta = \frac{1}{2}(\cos\theta + \cos3\theta)
$$

Então:
$$
\int_0^{2\pi} \cos2\theta\cos\theta\, d\theta = \frac{1}{2} \int_0^{2\pi} \cos\theta\, d\theta + \frac{1}{2} \int_0^{2\pi} \cos3\theta\, d\theta = 0
$$

#### Terceiro termo:
$$
\int_0^{2\pi} -4\sin\theta\sin2\theta \, d\theta = -4 \int_0^{2\pi} \sin\theta\sin2\theta \, d\theta
$$

Usamos a identidade:
$$
\sin\theta\sin2\theta = \frac{1}{2}(\cos\theta-\cos3\theta)
$$

$$
\Rightarrow \int_0^{2\pi} \sin\theta\sin2\theta \, d\theta = \int_0^{2\pi} \frac{1}{2}(\cos\theta - \cos3\theta) \, d\theta = 0
$$

Portanto:
$$
-4 \cdot 0 = 0
$$

---

### ✅ Resultado final:

$$
\boxed{W=\int_{\mathcal{C}} \vec{f}\cdot d\vec{r} = 0}
$$

vamos a poner algo aqui y alguito más

> Written with [StackEdit](https://stackedit.io/).
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTE3NzM1ODc3NDRdfQ==
-->