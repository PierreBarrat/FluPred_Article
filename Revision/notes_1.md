**Rev1 2.**: 
>  The authors examined the predictive power of one predictive method, the LBI. However, they did not do a systematic comparison of the different methods that they cite (Morris et al, 2018), which differ in prediction targets and methods. Therefore, the general conclusions about predictability, eg. on page 8, in line 47, and on page 9, line 48 are too sweeping and should be made precisely for those methods looked at in detail.

I'm not sure what line numbers he's using. But I think the lines he doesn't like are in the second and fifth paragraph of Discussion. These are:  
1. > (ii) previous methods to predict influenza evolution work primarily because they pick strains that represent the future well, not because they predict future dynamics.

and   

2. > The low power to predict frequency dynamics or fixation naturally triggers the question why the above methods have been found to work. Picking representatives of the future and predicting frequency dynamics are distinct objectives and success at the former (as compared to random picks) is not necessarily inconsistent with a lack of predictable dynamics.

We might need to tone down 1. We're not rigorously testing every previous method for its ability to predict dynamics, and I don't think we want to start doing that. We're only doing it seriously for the LBI. I am not sure that what I'm doing with John's models is enough to back the statement up.  
For 2., we can change the formulation. For instance *the qualitative difference between the dynamics of trajectories in A/H3N2 influenza and what is expected from models of adapting populations triggers the question why the above methods have been found to work*. We're challenging hypotheses the methods are based on, not their results. And then we're giving a reason why some hypotheses can be wrong, and the method still works.  
More generally, we should be careful when saying that trajectories are unpredictable. It's more that 
- according to theory, we should see a difference between Pfix and f. 
- many quantities thought of as being related to fitness do not predict Pfix, even though according to theory they should.

As an answer, I would go for something like *We agree with rev1 that we made an overstatement when saying that previous methods cannot predict trajectory dynamics. we modified the main text to tone down these claims. At the same time, we added a figure in the SM showing that the fitness scores on which many methods are based on (LBI / HI titer / epitope mutations / Mut. load) are not predictive of fixation, except in the case of mutational load. What we are claiming is not that these methods do not work, especially since their goal is often not to predict fixation of individual mutations but to pick a representative of the future population, but rather to challenge the hypotheses they are based on, namely the fact that A/H3N2 trajectories behave differently from  what is expected.  *  


**Rev2.1**: 
> The authors focus on one feature at a time (frequency, epitope status, LBI …). It is interesting to see that each of these is not very predictive of future frequency / prob of fixation. However, I think the obvious next step is to see whether a combination of many features could do a better job of predicting. I am not sure why the authors don’t try to fit a model that takes into account all information they have about sites (say, type of AA change, location in the gene, current frequency etc) and see if a ML model is able to make predictions. 

The only combination of features we'll be able to show is `HI titers + mut. load` and `LBI + mut. load`. That's not really combining the features we've shown initially in fig. 3. The way I would answer is  
- The aim of the paper is not to find the best possible predictor of frequency trajectories. Our aim is rather to explore the behavior of frequency trajectories in influenza, and to see whether simple quantities that are thought to be related to fitness can be informative of their future dynamics. The strategy of fitting models is a different one and is implemented in another paper (cite John's work). 
- We agree with Rev2 that this approach might be surprising for readers. For this reason, we've decided to investigate the power of individual fitness models (LBI / HI titers / mut. load / epitope muts.) to predict trajectory dynamics, as well as some of their combinations (LBI + HI / LBI + mut. load). Combinations do not seem to give any improvement as to predicting dynamics. 

