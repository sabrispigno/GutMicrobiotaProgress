Modelling how the diet drives the gut microbiota and how we can make prediction on the gut microbiota changing the diet. 

1. The first one is the development of a a model in a simplified system (i.e. C. elegans) which microbiota can be easily monitored. The idea was to study the species that are found in C. elegans and the metabolism of those species to parametrize for each species the growth rate on the diet. We discussed the possibility of build up a new experiment or to study already published data. This methodology can be good to understand really which exact species is driven by which diet, but we criticized the difficulty to scale up to a different system (i.e. human) where there are bigger communities.

2. The second one is to explore the human gut microbiota communities in terms of species abundance distribution and frequency abundance distribution. The idea is to review already published data about how gut species abundances are distributed in different diets and then compare it with the species abundance distributions found in the model simulations. With this methodology the aim is to predict how the diet drives the microbiota abundance distribution (if it does!), but not taxonomically naming the species.

##

#### Does the diet variate the gut microbiota?
#### Hypothesis:

##### 1. The diet variates the abundance distribution of the gut microbiota

Questions:

-  More polysaccharides mean more dilution so less diversity?

-  An animal-based diet means more specialized microbiota so less diversity?

- Different diets correspond to different shapes in gut microbiota abundance distributions?

- Different diets correspond to the same shape in gut microbiota abundance distribution but to the different slope?

IT DOES NOT VARIATE THE ABUNDANCE DISTRIBUTION SEE "Data approaches.md"



##### 2. The diet variates the taxonomy of the gut microbiota and not the abundances

As metagenomic data are nonnegative data carrying relative, rather than absolute, information-- we treat them with Compositional data analysis-- a statistical approach designed specifically to handle data where the components are proportions that sum to a costant (usually 1)

# Center Log-Ratio (CLR) Transformation

Given a composition $\mathbf{x} = (x_1, x_2, \ldots, x_s)$ such that:

$$
\sum_{i=1}^{s} x_i = 1 \quad \text{and} \quad x_i > 0 \quad \forall i,
$$

the **Center Log-Ratio (CLR)** transformation is defined as:

$$
c_i = \log\left( \frac{x_i}{g(\mathbf{x})} \right)
$$

where the geometric mean $g(\mathbf{x})$ is:

$$
g(\mathbf{x}) = \left( \prod_{i=1}^{s} x_i \right)^{1/s}
$$

The transformed components $c_i$ satisfy:

$$
\sum_{i=1}^{s} c_i = 0
$$

This transformation maps compositional data from the simplex to a real Euclidean space, enabling standard statistical techniques to be applied more appropriately.

> ⚠️ Note: CLR cannot be applied directly when any $x_i = 0$ due to the logarithm and geometric mean being undefined in that case. Actually this trasformation works just if i substitute the zeros with a pseudocount.



###### MADs
Select the species that occur in all (almost? the samples (per diet or total) compute the MAD Mean Abundance Distribution) and the AFD Abundance Fluctuation Distribution... or Alternative Fur Deutschland) from Grilli 2020 we expect
that MAD is Lognormal, AFD is Gamma.

![a title](MADs.png) 

Fig. 7 the Mean Abundance Distribution (MAD) in three type of diets. For each diet, the mean of across samples were computed and then the histogram of each mean were plotted. Each point represents the probability of the species to exist with the current abundance 

** The species in the abundance class 1e-1 are variates more between the diets than the species in the higher abundance class or in the lower abundance class (?)**


###### Abundance Fluctuation Distribution (AFD)

1. **Normalized abundance** of species *i* in sample *s*:
   
   It is defined as the relative abundance of species *i* in sample *s*, divided by the **mean abundance** of that species across all samples:

   $$
   \tilde{x}_{i,s} = \frac{x_{i,s}}{\langle x_i \rangle}
   $$

2. **Log-transform** the normalized abundance:

   $$
   \log_{10}(\tilde{x}_{i,s}) = \log_{10}\left( \tilde{x}_{i,s} \right)
   $$

3. **Plot** the log-transformed normalized abundance values in **linear X-axis and log-scaled Y-axis** (i.e., linear space for X, log-scale for frequency/density).

   This shows the distribution of $\log_{10}(\tilde{x}_{i,s})$ as an approximation of the species' Abundance Fluctuation Distribution (AFD), and allows visual comparison with a theoretical Gamma distribution.

![a title](AFDsRelMean.png) 

Fig. 8B The Abundance Fluctuation Distribution AFD of less current species


###### SPECIES ABUNDANCE VARIANCE ACROSS THE DIETS
Select species that are present in most of the samples (independently of the diet).
Compare the species abundance variance within a diet, across different diets.

![a title](OVG_plot.png) 

Fig. 9  Species abundance variances of the omnivore diet vs vegetarian diet



![a title](OV_plot.png) 

Fig. 10  Species abundance variances of the omnivore diet vs vegan diet

![a title](VVG_plot.png) 

Fig. 11  Species abundance variances of the omnivore diet vs vegan diet

##### 3. The health condition variates the abundance distribution of the gut microbiota
No progress

