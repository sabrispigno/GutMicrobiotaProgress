Resume of our three days of discussions and to share with you my timeline for the next month.
We discussed about how to proceed on gut microbiota dynamics and explored two strategies.
The first one is about the investigation of the theoretical model (generalized Lotka-Volterra + Autotoxicity). Regarding this point we came out with two version of the model. 

Version 1 
The first version is the one which I showed the first day with the autotoxicity influencing the species growth rate and the autotoxicity increasing for the existence of the species.

$$
\frac{\dot{n}_i}{n_i} = g (1- {\rho} a_i ) - \sum_{j(\neq i)} C_{ij} n_j) 
$$

$$
\dot{a}_i = \beta n_i - \frac{1}\tau a_i.
$$

Version 2 
The second one, we discussed it the last day, includes also the positive effect on all the species of the no-self toxicity. To model this effect we added a positive term for the species that is the summatory of the no-self toxicity and we multiplied both the growth rate and this summatory to the term of autotoxicity (1-a). In this way, in presence of autotoxicity, we have both negative (by self) and positive (by no self) effects.


$$
\frac{\dot{n}_i}{n_i} = (g+\sum_{j(\neq i)} U_{ij} a_j ) (1- {\rho} a_i ) - {\delta_i} - \sum_{j(\neq i)} C_{ij} n_j
$$

$$
\dot{a}_i = \beta n_i - (\frac{1}\tau + \sum_{j(\neq i)} U_{ij} n_j ) a_i.
$$


The second regards modelling how the diet drives the gut microbiota and how we can make prediction on the gut microbiota changing the diet. We explored, again, two ways.
The first one is the development of a a model in a simplified system (i.e. C. elegans) which microbiota can be easily monitored. The idea was to study the species that are found in C. elegans and the metabolism of those species to parametrize for each species the growth rate on the diet. We discussed the possibility of build up a new experiment or to study already published data. This methodology can be good to understand really which exact species is driven by which diet, but we criticized the difficulty to scale up to a different system (i.e. human) where there are bigger communities.
The second one is to explore the human gut microbiota communities in terms of species abundance distribution and frequency abundance distribution. The idea is to review already published data about how gut species abundances are distributed in different diets and then compare it with the species abundance distributions found in the model simulations. With this methodology the aim is to predict how the diet drives the microbiota abundance distribution (if it does!), but not taxonomically naming the species.

My timeline activities
1. Simulates the model without the positive effect of no-self toxicity with a community of 500, 50, 10, 5 species. Deadline 11/12/24
2. Evaluates the AFD and SAD for the simplest model Deadline 11/12/24
3. Starting evaluating AFD and SAD for the data of the gut microbiota that I already got. Deadline 15/12/24
4. Simulates the model with the positive effect of no-self toxicity. Deadline 19/12/24
5. Evaluates the AFD and SAD for the model with the positive effect of no-self toxicity 19/12/24
6. Review experimental work that contains gut microbiota data driven by diet (it is not necessary that are in time but could be nice...) Deadline 12/01/24
