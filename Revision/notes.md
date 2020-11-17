# Rev 1

## Point 1. 
What the Illingworth paper does (mainly)  
- Fit two kind of models to flu trajectories. One that allows sweeps only (unlinked model), one that takes linkage into account.  
- The first model works very badly (no surprises here). In the second model, the inherent fitness effect of a mutation is not the biggest contribution to its fixation/loss. From this it is concluded that the background is more important that the inherent fitness effect of a mutation.  

Rev1 says about this work "By averaging over all amino-acid substitutions,
the authors show that the fates of mutations are not determined by the
value of the starting frequency."
I am not sure what he means by that. First, what we are saying is that the fate of mutation is **fully** determined by their frequency (as long as we have no other information than the trajectory).  
Then, I do not see that they show that anywhere in the Illingworth article. They only say in the discussion:  
`Further, interference makes the prediction of viral evolution more difficult. Identifying the most beneficial mutations at a given time does not necessarily identify those that will go on to fixation. A polymorphism that was growing in frequency might be killed off by the emergence of another, more beneficial mutation. A polymorphism that existed at low frequency, with no apparent benefit for the virus, might, through hitchhiking, reach fixation.`

As a general answer to point 1.  
- What we are doing can be considered as an elaboration of the above quoted sentence. After showing that linkage is important in flu evolution, they say that it should make prediction more difficult.  
What we do is **show** that prediction is indeed very difficult, and that it may even be harder than what one would expect if only linkage played a role. But obviously a big part of the "hardness" is due to linkage. 
We could add something along these lines in the introduction.

As an answer to point 1.1   
- We should make clear that we never assume that only the inherent fitness of a mutation contributes to its trajectory (and its fixation/loss). When selecting rising trajectories, we select mutations that have been subject to an effectively positive selection in the past.  
- Finally emphasize that if a mutation is rising in frequency, **all other things equal**, this suggests that it is under positive selection and that either the mutation itself or its background have a positive fitness effect. Thus, it should bias its odds of fixing in the population upwards. However, we are not saying that we expect rising mutations to fix 100% of the time. 

About point 1.2. I'm not sure what he means here.    
- We are not inferring a model, so "making use of the full trajectory" is not something we can do. What we can potentially do is take more detailed features of the trajectory into account, such as the sign of its derivative at a given point (this does not change our results). But looking at more aspects of a trajectory will simply reduce statistical power.  
- We not only look at fixation, but also the average trajectory.  
- Simulations show that one does not expect a neutral-like statistics for populations under selection, even without recombination.   
- Illingworth et. al. does not consider predicting trajectories at all. So there is nothing to compare to.  
We do however "compare" to methods that are based on epitope positions, and find that these methods may have worked because they were defined post-hoc. We also show that our observations are consistent with the fact that top LBI strains are good predictors of the future population. 

## Point 2. 
The aim of the paper is not at all to compare prediction methods. It is to challenge the hypothesis on which they are based. It's stated rather clearly in the introduction. Hence I'm not sure what to reply to this. 
Maybe he wants us to extend figure 3 or 4 to different prediction methods, computing the fitness of the mutation according to each of these methods every time? That's a lot of work because we will need to re-implement some of those, need access to HI titers data maybe, etc... But technically do-able and might be interesting. 


## Point 3. 

# Rev 2
 
## Point 1.
First, it's hard to believe that combining different methods that have no predictive power taken separately (*e.g.* LBI and some lists of epitopes in figure 3) would give something interesting. How would such a model be learned? Should we split the data in training and test (say before 2010 and after 2010)? That does not seem at all in the spirit of the paper...  
Seconds, we are also authors of a very recently published paper that does exactly that, although with a different take on what "predicting" means (*i.e.* closer to future population, not predicting fixation of an individual mutation). 

## Point 2. 
I have not re-read the text, but he's right they're clearly different. We should modify the writing in some places to reflect that. 
The only reason for this difference I can think of is that H1N1pdm is more recent, and hence probably sees a different immune response from the human population? (*i.e.* more people are not immune to it at all)? But we have only speculations to offer at this point I believe. 

## Point 3. 
Good point. The mutation business shows that predicting the evolution is a very hard task, and the implications is that it's hard to do vaccines that match perfectly. 
The last figure show that even though individual mutations are hard to predict, it's still possible to get a good estimate of what the future population will look like (good meaning better than a random pick). This does not contradict the apparent neutrality. 
This also frames the question of vaccines a bit differently: can we do better than taking the consensus strain?
We should add a few sentences in the discussion about this? 

## Point 4
Good point, and it also raises the question of how much trajectories influence themselves (kill the winner). 
Actually, we do believe that trajectories might be strongly influences by the current structure of the flu population (the selection advantage of a mutation drops once it's high in frequency), and potentially by the vaccine. 
The paper he cites is based on a simulation and concludes that vaccines could influence evolutionary trajectories. But it's a simulation, so we cannot draw direct conclusions. There is this other paper by the same first author in Viruses 2018, where the abstract suggests that we cannot really measure the effect of vaccines with the current data. 

## Point 5 (minor)
I'll try to change this and see what it looks like. It's better if figure 3B is a square though. 

