---
title: "Ficha I"
disciplina: "Cálculo II"
data: "2025-06-27"
temas:
  - Topologia
  - Limites
  - Continuidade
descricão: "Ficha dedicada à resolução de problemas de análise de funções de várias variáveis, nos temas mencionados."
---

# Ficha 1.

## Problema 1. 
Para cada um dos seguintes conjuntos determine o interior e o exterior, e a fronteira e diga, justificando, se é aberto, fechado, limitado ou compacto.

> b) $B=\{x\in\mathbb{R} \,:\, 0\le x\le 1 \,;\,  x\in\mathbb{Q}\}$

**Solução.**
Temos que $\operatorname{Int}(B) = \emptyset$. De facto, para qualquer $x \in B$ e para qualquer intervalo aberto $I$ que contenha $x$, podemos sempre encontrar um ponto $y \in I$ tal que $y \notin B$. Assim, nenhum desses intervalos está contido em $B$, i.e., $I \not\subset B$.
Pelo mesmo motivo, nenhum $x \in B$ pode pertencer ao conjunto exterior $\operatorname{Ext}(B)$, pois, para qualquer intervalo $I$ que contenha $x$, esse intervalo conterá simultaneamente pontos que pertencem a $B$ e pontos que não pertencem.
Desta forma, podemos concluir que o conjunto exterior é dado por $\operatorname{Ext}(B) = ]-\infty, 0[ \cup ]1, +\infty[$.
A fronteira de $B$, denotada por $\partial B$, é composta pelos pontos tais que, para qualquer intervalo que os contenha, esse intervalo contém pontos de $B$ e pontos fora de $B$. Assim, temos $\partial B = [0, 1]$. O **fecho** de $B$ é constituído pelos pontos de $B$ juntamente com os seus **pontos de acumulação**, ou seja, $\bar{B} = B \cup B'$.
Além disso, o conjunto $B$ **não é aberto**, pois não coincide com o seu interior: $B \ne \operatorname{Int}(B)$. Também **não é fechado**, uma vez que não coincide com o seu fecho: $B \ne \bar{B}$.
Por fim, $B$ **não é compacto**, pois, apesar de ser limitado, **não é fechado**, o que impede que satisfaça o critério de compacidade em $\mathbb{R}$.

---
## Problema 2.
Calcule ou mostre que não existem os seguintes limites:
> a) $\displaystyle\lim_{(x,y)\to(0,0)}\frac{x^2y}{x^2+y^2}$.

**Solução.**
Consideremos $y=0$ and let $x\to 0$. Then 
$$\lim_{(x,y)\to(0,0)}\frac{x^2y}{x^2+y^2}=\lim_{(x,0)\to(0,0)}\frac{0}{x^2}=0.$$
Por outra parte, consideremos agora $x=\sqrt{y}$ and let $y\to 0$. Then
$$\lim_{(x,y)\to(0,0)}\frac{x^2y}{x^2+y^2}=\lim_{(\sqrt{y},y)\to(0,0)}\frac{y^2}{y+y^2}=0.$$
Podemos explorar outros caminhos  -- a ideia, aqui, é encontrar trajetórias distintas que conduzam a limites diferentes. Se isso acontecer, então o limite **não existe**.

Por outro lado, se **não** conseguirmos encontrar tais caminhos, talvez o limite **exista** e seja igual a $0$.
Assim, mudemos de enfoque e tentemos demonstrar que esse é, de facto, o caso. Na definição de limite, temos é de mostrar que se
$$\lim_{(x,y)\to(0,0)}\frac{x^2y}{x^2+y^2}=0\,\iff\,\boxed{\begin{split}&\textsf{Dado }\varepsilon>0\,,\textsf{existe }\delta>0\,\textsf{tal que} \\[3ex] &\left\vert\dfrac{x^2y}{x^2+y^2}-0\right\vert<\varepsilon\,\,\textsf{desde que }\,0<\sqrt{x^2+y^2}<\delta\end{split}}$$
A ideia consiste em **majorar** a primeira desigualdade e, em algum momento oportuno, **utilizar a segunda desigualdade**, de modo a conseguirmos **exprimir $\delta$ em função de $\varepsilon$**. Vamos lá ver
$$\begin{array}{ccc}0\le x^2\le x^2+y^2 &\implies & 0\le\dfrac{x^2}{x^2+y^2}\le1\\[3ex]0\le\vert y\vert\le\sqrt{x^2+y^2} &\implies& 0\le \underbrace{\dfrac{x^2\vert y\vert}{x^2+y^2}}_{\left\vert\dfrac{x^2y}{x^2+y^2}\right\vert}\le\sqrt{x^2+y^2}\end{array}$$
Logo, colocamos as peças do jogo na sua posição:
> Dado $\varepsilon>0$, escolhemos $\delta=\varepsilon$, porque assim podemos garantir que
$$\textsf{se}\quad\sqrt{x^2+y^2}<\delta\quad\textsf{então}\quad\left\vert\dfrac{x^2y}{x^2+y^2}-0\right\vert<\varepsilon.$$
Logo, concluímos que $$\boxed{\lim_{(x,y)\to(0,0)}\frac{x^2y}{x^2+y^2}=0}$$

---
> g) $\displaystyle\lim_{(x,y)\to(0,0)}x\ln(xy)$.  (**Sugestão**: Considere a linha dada por $y=e^{-1 / x^2}$)

**Solução.**
Vejamos o que da o ChatGPT. Resposta validada por mim.

Vamos analisar o limite:

$$\lim_{(x, y) \to (0,0)} x \ln(xy)$$

Este é um limite bidimensional, e a sugestão é considerar uma trajetória particular para testar a existência (ou não) do limite. A estratégia é verificar se **o limite depende do caminho**, o que, se verdadeiro, implicará que o limite **não existe**.

---

### ✅ Etapa 1: Considerar a linha sugerida

A sugestão é considerar a curva:

$$y = e^{-1/x^2}$$

Note que:

- Quando $x \to 0$, temos $y = e^{-1/x^2} \to 0$.
    
- Logo, $(x, y) \to (0,0)$ ao longo desta curva.
    

Vamos substituir $y = e^{-1/x^2}$ na expressão original:

$$x \ln(xy) = x \ln(x \cdot e^{-1/x^2}) = x \ln\left( x \cdot e^{-1/x^2} \right)$$

Usando propriedades do logaritmo:

$$x \ln\left( x \cdot e^{-1/x^2} \right) = x \left( \ln(x) + \ln\left( e^{-1/x^2} \right) \right) = x \left( \ln(x) - \frac{1}{x^2} \right)$$

Distribuindo o $x$:

$$x \ln(x) - \frac{1}{x}$$

Agora, analisamos o limite de:

$$x \ln(x) - \frac{1}{x} \quad \text{quando } x \to 0^+$$

- $x \ln(x) \to 0$ (limite clássico)
    
- $\frac{1}{x} \to +\infty$
    

Logo:

$$x \ln(x) - \frac{1}{x} \to -\infty$$

---

### 🔴 Conclusão (Caminho 1):

Ao longo da curva $y = e^{-1/x^2}$, o limite da função é **menos infinito**.

---

### ✅ Etapa 2: Verificar outro caminho

Agora consideremos o caminho:

$$y = x$$

Então:

$$x \ln(xy) = x \ln(x \cdot x) = x \ln(x^2) = x \cdot 2 \ln(x) = 2x \ln(x)$$

E sabemos que:

$$\lim_{x \to 0^+} 2x \ln(x) = 0$$

---

### 🔴 Conclusão (Caminho 2):

Ao longo de $y = x$, o limite é **0**.

---

### ❌ Conclusão Final:

Como obtivemos **dois limites diferentes** ao longo de caminhos distintos, concluímos que:

$$\lim_{(x, y) \to (0,0)} x \ln(xy) \quad \textsf{\bf não existe}.$$




<!--stackedit_data:
eyJoaXN0b3J5IjpbMTc2MDk1MTAxMF19
-->