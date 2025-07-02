---
title: Line Integrals
tags: 
draft: "false"
---
# Line Integrals of Vector Fields 
We can think of a line integral at first in the context of physics. Let us consider a [[Vector Field]] given by $\vec{F}$ and a displacement vector given by $\vec{r}$. When considering work we consider:
$$\text{Work=Force} \cdot \text{Displacement}=\vec{F}\cdot \Delta \vec{r}$$
This operation gives us the work, which tells us how much energy an operation needs to perform this operation. We consider $\Delta r$ to be a small nudge along our curve function over a region that is given by $\vec{r}$. 

In most cases we want to consider the total energy over the entire curve of $\vec{r}$ which we can consider by summing up the projections onto the curve for every point on the curve. 

We can call the trajectory that we are moving along, $c=c(x,y)$, and the force at that point given by  This requires integrating the dot product of the velocity function, $d\vec{r}$ vector function and the curve and the between $$w=\int_{c} \vec{F}\cdot d\vec{r}=\lim_{\Delta r_{i}\rightarrow 0} \sum_{i=1}^\infty\ \vec{F}\cdot \Delta \vec{r}_{i}$$Notice that this is equivalent to writing:
$$=\lim_{\Delta r_{i}\rightarrow 0} \sum_{i=1}^\infty\ \vec{F}\cdot \dfrac{\Delta \vec{r}_{i}}{\Delta t} \cdot \Delta t = \int_{t_{1}}^{t_{2}}\vec{F}\cdot\dfrac{d\vec{r}}{dt}dt$$
We can actually compute our expression with respect to time using our initial and end time as boundaries. Our vector field, $\vec{F}$ depends on $x,y$ before it depends on $t$, so we need to be able to express it in terms of each. 

Another way that we can think of our problem is thinking of the dot product of $\vec{F} = \langle M,N \rangle$ and $d\vec{r}=\langle dx,dy \rangle$. We can thus rewrite $\vec{F}\cdot d\vec{r}$:

$$\vec{F}\cdot d\vec{r}=Mdx+Ndy$$
$$\int_{c} \vec{F}\cdot d\vec{r}= \int_{c} Mdx+Ndy$$
Using our curve $c$, we only have 1 parameter that remains, and we can express our variables $x$ and $y$ in terms of this single parameter, which collapses this integral into a single variable integral, which can be easily computed. 

Another way that we can think of our line integral is through a geometric lens. We can consider $d\vec{r}$ to be a unit tangent vector, $\vec{T}$ that is scaled by some amount, $ds$, the arclength:
$$d\vec{r}=\langle dx,dy  \rangle = \vec{T}\cdot ds$$
Which would also give us:
$$\dfrac{d\vec{r}}{dt}= \left\langle \dfrac{dx}{dt}, \dfrac{dy}{dt} \right\rangle = \vec{T}\cdot \dfrac{ds}{dt}$$
We can rewrite our line integral formula as:
$$\int_{c}\vec{F}\cdot\vec{T}\cdot ds$$
In turn we get three equivalent ways to handle our line integral:
$$\int_{c} \vec{F}\cdot d\vec{r}= \int_{c} Mdx+Ndy=\int_{c}\vec{F}\cdot\vec{T}\cdot ds$$

---
#### Example 1.)
Let us consider the following vector field given by $\vec{F}$: $$\vec{F}=-y\hat{i}+x\hat{j}$$
Let us consider the curve, $c$, given by $x=t$ and $y=t^2$. 
$$\int_{c}\vec{F}\cdot d\vec{r}=\int_{0}^1\vec{F}\cdot \dfrac{d\vec{r}}{dt}dt= \int_{0}^1 \langle -y,x \rangle \cdot\langle 1,2t \rangle  dt$$
$$=\int_{0}^1(-y+2tx)dt=\int_{0}^1(-t^2+2t^2)dt=\int_{0}^1(t^2)dt=\dfrac{1}{3}$$
We can do this by the first method to obtain the following integral:
$$\int_{c} Mdx+Ndy=\int_{c} -y\cdot dx+x \cdot dy$$
We have two equations that relate $x$ and $y$, $x=t$ and $y=t^2$ so we can find their derivatives and substitute them in:$$\int_{c} (-t^2+2t^2)dt=\int_{0}^1 (t^2)dt=\dfrac{1}{3}$$
