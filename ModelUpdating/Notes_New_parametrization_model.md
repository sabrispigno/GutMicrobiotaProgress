 EQUATIONS 
 
$$
\dot{n}_i = n_i\Big[ 1 - \Big(\gamma \delta a_i + (1-\gamma)n_i\Big) - \sum_{j(\neq i)} C_{ij} n_j \Big]+ \lambda

$$

$$
\dot{a}_i = n_i - \delta a_i
$$

We draw $C_{ij}\sim \mathcal{N}(\mu,\sigma)$, i.e. not with weak interaction scaling. In the end there are (beside species richness $S$) four continuous parameters to study: $\mu,\sigma,\delta,\gamma$ 

SIMULATIONS -Fixing $\mu$ and $\sigma$ and changing $\gamma$ and $\delta$ 

$$ Cij = N \sim 0.4,0.2;\ \gamma=[0-1];\ \delta= [0.001-2];\ \lambda= 1e-10\ S=500 $$
*Memo for me: it is the folder called "DatChParNew"*

SPECIES DYNAMICS 
![a title](DeltaGamma/10speciesCH.png)

Now the plot of the same simulation but in Linear scale
![a title](DeltaGamma/10speciesCHLinear.png)

AUTOTOXIN DYNAMICS
![a title](DeltaGamma/10autotoxCH.png)

Now the plot of the same simulation but in Linear scale
![a title](DeltaGamma/10autotoxCHLinear.png)

#### Fixed Point Regime 
I have parametrised the new model by using the old parameters, scaling the parameters in the new way (see. Notes Autotoxicity model by Emil). If $\beta=1$ and  $\delta$ = 0.001 (in the past version of the model, as in the past parametrisation), then,  $Cii$ = 100. This means that in the new parametrisation $\mu$ and $\sigma$ are not 0.5 and 0.3 but are divided by $Cii$ resulting in a change of the phase regime from chaotic to fixed points.
$$ Cij = N \sim 0.005,0.003;\ \gamma=[0.8-1];\ \delta= [0.001-2];\ \lambda= 0 $$
*Memo for me: it is the folder called "DatFpParNew"*

SPECIES DYNAMICS
![a title](DeltaGamma/10speciesFP.png)

Now the plot of the same simulation but in Linear scale
![a title](DeltaGamma/10speciesFPLinear.png)

AUTOTOXIN DYNAMICS
![a title](DeltaGamma/10autotoxFP.png)

Now the plot of the same simulation but in Linear scale
![a title](DeltaGamma/10autotoxFPLinear.png)

#### Changing PHI
SIMULATIONS - Fixing $\gamma$ and $\delta$ and changing $\mu$ and $\sigma$ 
I fixed $\gamma$ =0.1 and $\delta$ = 0.1 and then I changed $\mu$ and $\sigma$ as the function of the angle $\phi$ 
I changed $\phi$ from 0.1 to 1.6 radians.
![a title](PHI/changingphi.png)

$$ Cij = N \sim \mu(\phi),\sigma(\phi)\ ;\ \phi = [0.1-1.6]; \gamma=0.5;\ \delta= 0.1;\ \lambda= 1e-10\  $$

*Memo for me: it is the folder called "Dat_Phi3" Simulations with LSODA method*

SPECIES DYNAMICS 
![a title](PhiGamma/10speciesPhiGammaLSODA.png)
From the top left to the bottom right, phi values decrease. The behaviour of only 10 random species is shown in colour, while the other species are shown in grey. Despite the numerical error, we can see that the species fluctuate faster as the phi value increases.

Now the plot of the same simulation but in Linear scale

![a title](PhiGamma/10speciesPhiGammaLinear.png)

AUTOTOXIN DYNAMICS 
![a title](PhiGamma/10autotoxPhiGammaLSODA.png)

Now in linear scale

![a title](PhiGamma/10autotoxPhiGammaLSODALinear.png)

Now I made the same simulation but plotting the species by changing phi in the same graph.

![a title](PhiGamma/10speciesPhiAdiabatic.png)

#### Changing Sigma Gammma
SIMULATIONS - Fix $\mu$ and $\delta$ and change $\gamma$ and  $\sigma$. 

We now consider the space $\mu$ and $\sigma$ as in  Ecological communities with Lotka-Volterra dynamics; DOI: https://doi.org/10.1103/PhysRevE.95.042414. In our case mu and sigma are $\hat{\mu} = S \mu$ and $\hat{\sigma} = \sqrt{S} \sigma $
In this case it will change to the Unique Fixed Points regime where the values of $\mu$ and $\sigma$ are smaller (0.005 and 0.001). The point is to change $\sigma$, to see if we get into the multiple attractor phase.

$$ 
Cij = N \sim (\mu ,\sigma) ;\  \mu=0.001;\ \sigma=[0.002-0.013];\ \gamma=[0.01-0.99];\ \delta= 0.01;\ \lambda= 1e-10\  
$$

*Memo for me: it is the folder called "Dat_SigmaGammaRK45" 

SPECIES DYNAMICS
![a title](SigmaGamma/10speciesSigmaGammaRK45.png)

Now I plot the same simulation but in Linear scale
![a title](SigmaGamma/10AspeciesSigmaGammaRK45Linear.png)

AUTOTOXIN DYNAMICS
![a title](SigmaGamma/10autotoxSigmaGammaRK45.png)

Now I plot the same simulation but in Linear scale
![a title](SigmaGamma/10autotoxSigmaGammaRK45Linear.png)



1. Change the model by using instead of $\gamma$ a parameter called $\theta$ that represents the sensibility to the Toxicity. 
$$
\dot{n}_i = n_i\Big[ 1 - \Big(\Theta a_i + (1-\frac{\Theta}{\delta})n_i\Big) - \sum_{j(\neq i)} C_{ij} n_j \Big] 
$$
$$
\dot{a}_i = n_i - \delta a_i
$$ 
In the end there are (beside species richness $S$) four continuous parameters to study: $\mu,\sigma,\delta,\Theta$ where $\Theta$ is now defined as $\theta = \gamma \delta$. Note that in this new parametrization is always $\Theta<\delta$ to avoid negative values of $n_i$

2. Fix $\mu$ and $\sigma$ and change $\theta$ where $\theta$ is the sensibility to the toxicity

*For the moment I am keeping $\gamma$*

3. Bifurcation analysis

I tried a bifurcation analysis changing the parameter $\gamma$  from 0.8 to 0.978
#### Plotting the mean of all the species
![a title](Bifurcation/BifurcationGammaMEAN.png)

#### Plotting the most abundant species

![a title](Bifurcation/BifurcationGammaM1.png)
#### Plotting the second most abundant species
![a title](Bifurcation/BifurcationGammaMAX2.png)

#### Plotting the third most abundant species
![a title](Bifurcation/BifurcationGammaMAX3.png)