 EQUATIONS 
 $$

\dot{n}_i = n_i\Big[ 1 - \Big(\gamma \delta a_i + (1-\gamma)n_i\Big) - \sum_{j(\neq i)} C_{ij} n_j \Big]

$$

$$

\dot{a}_i = n_i - \delta a_i

$$
We draw $C_{ij}\sim \mathcal{N}(\mu,\sigma)$, i.e. not with weak interaction scaling. In the end there are (beside species richness $S$) four continuous parameters to study: $\mu,\sigma,\delta,\gamma$ 

SIMULATIONS -Fixing $\mu$ and $\sigma$ and changing $\gamma$ and $\delta$ 

 I parametrized the new model by using the old parameters; scaling the parameters in the new way (see. Notes Autotoxicity model by Emil). If $\beta=1$ and  $\delta$ = 0.001 (in the past version of the model, such as with the past parametrization), then,  $Cii$ = 1000. This means that in the new parametrization $\mu$ and $\sigma$ are not 0.5 and 0.3 but are divided by $Cii$ and that results in changing the phase regime from chaotic to fixed points.
$$ Cij = N \sim 0.005,0.003;\ \gamma=[0.8:0.99];\ \delta= [0.001:1 ] $$

SPECIES DYNAMICS WITH THE NEW PARAMETRIZATION
![a title](DeltaGamma/Allspecies_mylapoldparnewscale.png)
SPECIES ABUNDANCE DISTRIBUTIONS 

ABUNDANCE FLUCTUATION DISTRIBUTION


SIMULATIONS - Fixing $\gamma$ and $\delta$ and changing $\mu$ and $\sigma$ 
I fixed $\gamma$ =0.1 and $\delta$ = 0.1 and then I changed $\mu$ and $\sigma$ as the function of the angle $\phi$ 
I changed $\phi$ in the range [0.1-1.6]
![a title](PHI/changingphi.png)

|                   |                                            |
| ----------------- | ------------------------------------------ |
| Species Abundance | ![a title](PHI/AllspeciesPHI10species.png) |
|                   | Time                                       |
From the left top to the right bottom the values of phi decreases. Just 10 random species behavior is showed with colors while the other species are showed in grey in the bottom. Despite the numerical error, we can observe that the species fluctuates faster as the phi value increase.