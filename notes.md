# Results
- What should I put in the first figure? I think of it as a general illustration figure. Number of seqs / year seems useful to "show" the data. Trajectories at a given position as well (but I only need one pos., not 2). Maybe I should also show the tree since we'll use it in the rest and I want the next figures to be results. How to organize panel then? (also, how do I extract a nice tree picture from augur? screenshot? ). 
If I show a tree built with 18 years of influenza, how do I color it? I could go with LBI, it would illustrate the fact that it's larger at the base of big clades, and we'll use this observation later.  

## Short term predictions
- Should we add same results with f0 = 0.5 (in SM)? I would be surprised if the conclusions did not go the same way... 

## Pfix v frequency (long term predictions)
- For Pfix v frequency plots, I should explain how error bars are computed in the SM (I don't remember but it's not completely trivial). 
- Pfix v frequency plots that should go to the SM : 
	+ Using binary positions only (i.e. never 3 aa at the same time) - for HA and NA 
	+  Mutation appears once or more in the tree (gives some signal, mutations that appear more than once are more likely to fix)
	+ Conditionning on a strictly positive derivative when reaching target frequency 
	+ With larger timebins? (doesn't make a difference)
- What are the references for the epitopes positions? --> get them from author names or ask Richard... 
- How did I define the number of times a mutation appears in the tree? 
How many mutations define a clade? (*i.e.* appear only once at a given date)

## Model
Badly written. Some of it should be in Methods or SM. The conclusion is also not super clear. What I want to say is that even though clonal interference combined with linkage may push the curve towards the diagonal, it doesn't suffice to explain the observations in any simple way. It might be possible to build a model that explains what we see, but it probably won't be a trivial one and it might have to include population structure and pop size variation. 

## Why do predictions work
- The timescale I use for the LBI (tau) is the one for which the top-LBI strain is as close as possible to the consensus sequence (*i.e.* it's the result of an optimization). What I saw by playing with tau is that any other value than this one tends to make the LBI a *worse* predictor of the future population. However, I have *not* tested that in a systematic way. Moreover, the fact that we find the LBI and the consensus to fare so similarly in the figure I show in the main text is mostly due to this choice of tau (which btw is equal to 3 years). 
What I should probably do is choose the tau that gives the best prediction for the LBI. If this is the same that the one that gets you  closer to the consensus, it shows something! 
- Should figure 10 of SM (ie predicting the future using multiple sequences based on local maximas of the LBI) be in the main text? 
It shows different important things. First, on a long enough timescale, the overall consensus is better than the more sophisticated method. But on a shorter time scale, using multiple sequences that are somehow representative of the population is better than the consensus *and* than the naive method of taking the whole population (which would be saying all fitnesses are equal in John's model). So there are methods which allow a good prediction on an intermediate timescale. 
What I do not know is if this would be expected in a neutrally evolving population or if it's some sign of selection (or pop. structure? spatial/temporal?). 

# Refs to find
- Epitope sites
- I mention Wright-Fisher model
- iqtree
- augur / auspice (esp. the latter) since I'll most likely show a tree
- LBI

For EMD, John refers to ML papers on images and words. 
``
Rubner Y, Tomasi C, Guibas LJ (1998) *A metric for distributions with applications to image databases.*
``
and 
``Kusner MJ, Sun Y, Kolkin NI, Weinberger KQ (2015) *From word embeddings to document distances.*
``

For apparent neutrality:
https://www.pnas.org/content/96/17/9716
and 10.1186/1745-6150-1-34 

For fitness models that people use
- Trevor style model https://www.biorxiv.org/content/biorxiv/early/2019/09/30/780627.full.pdf (and John's manuscript)
- LBI
- Epitope + non epitope from Laessig & Luksza


# To do in SM
- Derivation that the consensus is the best single sequence and even multisequence prediction for neutral evolution (on the long term of course)
- Probably, detailed description of the ffpopsim model
- How I calibrate the integration time of the LBI. Quickly: \tau optimized so that the strain with the max. LBI is as close to the consensus sequence as possible. I find an optimal integration time of 3 years with this. If I change this, I get further away from the consensus and the prediction from the LBI becomes worse. 
- How error bars are computed in the Pfix v frequency plots. Basically, how does one estimate error bars for the estimate of the parameter of a Bernoulli distribution ($p$ and $1-p$). 
	

