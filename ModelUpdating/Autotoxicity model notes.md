
**Generalizing GLV to autotoxicity model** 
Our starting point is the GLV
$$
\dot{n}_i = n_i( r_i - C_{ii} n_i - \sum_{j(\neq i)} C_{ij} n_j ) 
$$
This is a phenomenological and not a mechanistic model! The intra-specific suppression term, for instance, is meant to roughly capture the net effect of a variety of processes: conspecifics competition over resources, space, the effect of pathogens -- and autotoxicity. We should therefore think of the autotoxicity model as "unpacking" some of the biological processes hidden in the phenomenological self-suppression term, rather than adding new mechanisms *on top* of what's already represented by the GLV. This gives the generalization 
$$
\dot{n}_i = n_i( r - C_{ii} h(n_i,a_i) - \sum_{j(\neq i)} C_{ij} n_j ) ,
$$
with $a_i$ the autotoxin concentration. We want to preserve, in a sense, the interpretation of $C_{ii}$ as the net strength of self-suppression effects. $h(n,a)$ should partition these effects into a fraction $\gamma$ due to autotoxicity and the remaining fraction $1-\gamma$  due to the other implicit causes. If we assume that individuals die due to autotoxicity at a rate proportional to the autotoxin concentration, then $h(n,a)$ is linear in both arguments. To have a notion of partitioning between $a$ and $n$, we must find what amount of $n$ constitutes an "equivalent" amount of $a$.

To this end, consider the autotoxicity dynamics. Production occurs at a per capita rate $\beta$ and degradation/dilution at a rate $\delta$:
$$
\dot{a}_i = \beta n_i - \delta a_i.
$$
The formal solution is
$$
a_i(t) = \frac{\beta}{\delta} \int_{-\infty}^t K_\delta(t-s) n_i(s)\, ds 
$$
where $K_\delta$ is an exponentially decaying memory kernel 
$$
K_\delta(s) = \delta e^{-\delta|s|}\quad \implies\quad \int_{-\infty}^0 K_\delta(s)\, ds = 1  
$$
We can therefore write
$$
a_i(t) = \frac{\beta}{\delta}\hat{n}_i(t) 
$$
where $\hat{n}_i$ is a historical weighted average of the abundance.  The ratio $\beta/\delta$ is therefore the "conversion ratio" between suppression from autotoxicity and implicit density-dependent effects. The "unpacking" due to autotoxicity can be interpreted as
$$
C_{ii}n_i \to C_{ii}[ \gamma \hat{n}_i + (1-\gamma)n_i].
$$
Writing out the abundance dynamics in full,
$$
\dot{n}_i = n_i\Big[ r - C_{ii} \Big(\gamma \frac{\delta}{\beta}a_i + (1-\gamma)n_i\Big) - \sum_{j(\neq i)} C_{ij} n_j \Big] 
$$
There are *three ways* that the autotoxicity model can exactly reduce to the GLV in this representation: 
- $\gamma \to 0$ (trivially)
- $\delta \to \infty$ (so that $\hat{n}_i \to n_i$)
- $\delta \to 0$ (but this is meaningless because autotoxicities explode)

For any values of $\gamma,\delta,\beta$, the fixed points are identical to those of the original GLV, although the stability properties can differ; the Jacobian of the autotoxicity model depends separately on these three parameters (compare Onofrio's notes).

**Comparison to previous parametrization:**
Before we had written the model as
$$
\dot{n}_i / n_i = g ( 1 - \rho a_i ) - \sum_{j} B_{ij} n_j  
$$
with the diagonal elements sometimes $B_{ii}=1$ other times $B_{ii}=0$, causing some confusion. Comparing the versions we have
$$r=g, \quad
C_{ii} \gamma \delta/\beta = g \rho,\quad C_{ii}(1-\gamma) = B_{ii}$$

**Nondimensionalization**
To simplify the study of the model, we make use of the fact that the arbitrary choice of units to measure time, abundance, and autotoxicity concentration allow us to reduce the number of relevant parameters by three. A detailed analysis proceeds by substituting $n = N\tilde{n}$, $a = A\tilde{a}$, $t= T\tilde{t}$ in the dynamics, where the tilde-variable is nondimensional and the capital letter is the units of measurement to be decided. This leads one to conclude that the natural choice is $T = 1/r$, $N= r/C_{ii}$, $A=\beta/C_{ii}$. Note that this only works if $C_{ii}$ does not depend on $i$, but this we assume. We similarly nondimensionalise the other parameters: $\beta = \tilde{\beta}A/TN$, $\delta = \tilde{\delta}/T$, $C_{ij} = \tilde{C}_{ij}TN$. In practise, this procedure is equivalent to simply putting $r=1,\beta=1,C_{ii}=1$ and dropping all the tildes. Thus, the simplified model is
$$
\dot{n}_i = n_i\Big[ 1 - \Big(\gamma \delta a_i + (1-\gamma)n_i\Big) - \sum_{j(\neq i)} C_{ij} n_j \Big] 
$$
$$
\dot{a}_i = n_i - \delta a_i
$$
We draw $C_{ij}\sim \mathcal{N}(\mu,\sigma)$, i.e. not with weak interaction scaling. In the end there are (beside species richness $S$) four continuous parameters to study: $\mu,\sigma,\delta,\gamma$

**Agenda**
To understand how the $(\mu,\sigma)$ phase diagram of the GLV (not assuming weak scaling) is extended in the $\delta,\gamma$ directions.
1. First look at dynamics versus $\delta,\gamma$ for few pairs $(\mu,\sigma)$ lying in the different phases in the GLV case
2. Assuming we then find a fixed $\delta$ for which $\gamma$ can change stability, do numerical bifurcation diagram in $\gamma$ to determine type. (Perhaps complement with Jacobian spectrum plots)
3. For the GLV, an arc in $(\mu,\sigma)$-space with not-too-large radius $\mu_0$ and focal point $(1,0)$ will cross all the boundaries of non-diverging phases perpendicularly. With $\phi$ the angle of such an arc, look at the dynamics in the $(\phi,\gamma)$-plane for some fixed $\delta,$ or in $(\phi,\delta)$-plane for $\gamma=1$.

We move forward after getting a sense of the range of the dynamics from these studies.