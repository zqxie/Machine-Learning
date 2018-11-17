## Chapter 1 The Fundamentals of Machine Learning
### What is Machine Learning?
 - A computer program is said to learn from experience E with respect to some task T and some performance measure P, if its performance on T, as measure by P, improves with experience E — Tom Mitchell, 1997

### Why Use Machine Learning?
- **Hard to write new rules forever.** A great example can be presented by building a spam filter. With Learning, we need to write a long list of complex rules and pretty hard to maintain. Besides, if spammers notice our rules, they can slightly change emails, which makes us hard to response.
- **No known algorithm problems.** How to distinguish speech? The best solution is to write an algorithm that learns by itself, given many example recordings for each word, rather than hard-decode them.
- **Help human learn.** ML can give us their best predictors, which can help us better understand the problem. 

### Machine Learning Purpose
 - Problems for which existing solution require a lot of hard-tuning or long lists of rules: one Machine Learning algorithm can often simplify code and perform better.
 - Complex problems for which there is no good solution at all using a traditional approach: the best Machine Learning techniques can find a solution.
 - Fluctuating environments: a machine Learning system can adapt to new data.
 - Getting insights about complex problems and large amounts of data.
 
### Types of Machine Learning Systems
 - Human supervision? (Supervised, unsupervised, semisupervised, reinforcement learning)
 - Learn incrementally on the fly? (Online versus batch learning)
 - Comparing new data points to known data points versus Detect patterns in training data and build a predictive model?

### Supervised / Unsupervised / semisupervised / reinforcement
  - Instance Label is one of the criterial factors, including classification and regression
    - Important supervised learning algorithms: k-Nearest Neighbors, Linear Regression, Logistic Regression, Support Vector Machines, Decision Trees and Random Forests, Neural network 
    - Important unsupervised learning algorithms: 
       - Clustering: k-Means, **_Hierarchical Cluster Analysis, Expectation maximization_**
       - Visualization and dimensionality reduction: Principal Component Analysis (PCA), Kernel PCA, **_Locally-Linear Embedding(LLE)_**, **_t-distributed Stochastic Neighbor Embedding (t-SNE)_**
       - Association rule learning: **_Apriori, Eclat_**
  - Semisupervised: 
    - lots of unlabeled data and a little labeled data. Google Photos, when upload family photos, it automatically recognized person face in difference group (clustering, unsupervised), then it asks you to label who they are; 
    - Combinations of unsupervised and supervised methods, deep belief networks (DBNs), based on unsupervised Boltzmann machines (RBMs), fine-tuned using supervised learning techniques
- Reinforcement
    - Learning System called agent, it can observe the environment, select and perform actions, get rewords in return. To get the most rewards over time, it must learn by itself what is the best strategy, which is called policy.
    - Robots, DeepMind’s AlphaGo

### Batch and Online Learning
 - Batch, system incapable of learning incrementally. It needs to train with the whole training sets, which is fairly time-consuming (which cannot adapt to rapidly changing data), computer resource-consuming (Even be impossible when data is too huge to put into the memory space, out-of-core learning)
 - Online, feed with data instances sequentially, individual or mini-batch. 

### Instance-Based Versus Model-Based Learning
 - Instance-Based emphasizes the similarity between known spam and new emails. Methods like k-Nearest Neighbors Regression
 - Model-Based makes prediction. Methods like Linear Regression
      
### Main Challenges of Machine Learning
#### Bad Data
 - Insufficient Quantity of Training Data. **Banko and Brill, Learning Curves for Confusion Set Disambiguation, 2001**, **Peter Norvig et al., The Unreasonable Effectiveness of Data, 2009**.
 - Non-representative Training Data, sampling sizes and sampling bias. **US presidential election in 1936, *Literary Digest***
 - Poor-Quality Data, full of errors, outliers, and noise. Most data scientists spend a significant part of time clearing up training data. **Discard outliers, missing features problem (ignore attribute? Ignore instances? fill in missing value? train with it and without it, then compare?)
 - Irrelevant Features. **Feature selection, find most useful features; Feature extraction, produce more useful ones like dimensionality reduction; Creating new features by gathering new data.**
 
#### Bad algorithms
 - Overfitting the Training Data, Learning too much on training data like noises so that generalizes worse on testing data. **Simplify model by selecting one with fewer parameters, gather more training data, reduce noise in training data** 
   - Regularization, force parameters to keep their small. **This Hyperparameter is a parameter of a learning algorithm, not of the model. It must be set prior to training and remains constant during training. Tuning Hyperparameters is an important part of building a Machine Learning system.**
 - Underfitting the Training Data

### Testing and Validating
 - Split data into two sets, 80% training, 20% testing. Using test set to evaluate generalization error.  
 - For the training set, split it, use validation set to fine-tune the Hyperparameters. Cross-validation emerges.

### No free Lunch Theorem
 - **David Wolpert, The lack of A Priori Distinctions Between Learning Algorithms, 1996**, if you make absolutely no assumption about the data, then there is no reason to prefer one model over any other, known as *No Free Lunch (NFL) theorem*.
 - Assumptions.  Take care of it.


**Finished 
2018.10.19 1.5hr**