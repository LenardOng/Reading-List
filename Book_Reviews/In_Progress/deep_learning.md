## Deep Learning
### Introduction to my experience with this book



### What's different
+ A book that is fully focused on deep learning and ensures new readers to machine learning can keep up with the content
+ Fast way to become up to date with deep learning research
+ More detailed statistical view into machine learning

### What else is good
+ Extended detail beyond the necessary
+ Representing the learning of an NN as a lower dimension manifold in higher dimensional space

### What can be improved
+ 

## Brief personal summary of the book and things that I've learned from the book:

+ Chapter 1 - Introduction - Structure of basic deep learning models and motivations

### Part 1 - Applied Math and Machine Learning Basics

+ Chapter 2  - Linear Alegebra - required for deep learning. For deep learning this is around an A level standard and not too difficult.

+ Chapter 3 - Probability and Information Theory - Introduction to basic probability and statistical concepts which spans from A level standards to more complex concepts. 
    + Basic probability concepts include the multinoulli distribution, the Gaussian distribution, Dirac Delta distribution, Gaussian Mixtures and Bayes' rule. 
    + Basic information theory include Shannon information, KL divergence / Cross-entropy, (a commonly used cost for multinoulli distributions).
    + Basic introduction to graphical models - The book misses a focus on the independence assumptions in directed models and considers 'random' to be a sufficient replacement.
    
+ Chapter 4 - Numerical Computation - Low level programming considerations when designing deep learning algorithms as well as the basics of optimisation
    + Underflow and overflow numberical issues
    + Numerical gradient descent using Jacobian and Hessian
    + Surprising amount of detail into constrained optimisation
    
+ Chapter 5 - Machine Learning Basics 
    + Performance, Task, Experience definition of machine learning
    + Bayes error as the best possible correct prediction rate (usually measured with reference to an expert)
    + Detailed comparison of the bias variance problem.
        + Definition of a biased estimator using examples
    + Maximum likelihood and its relation to the Gaussian distribution
    + Dual of an SVM returns alpha, the support vectors themselves
    + k-means clustering as producing a k dimensional one hot vectors
    + Manifolds - Idea of concentrated probability distributions in real life data such as images
        + The idea that most data has discernible pattern in a higher dimension 
    

### Part 2 - Deep Networks: Modern Practices
    
+ Chapter 6 - Deep Feedforward Networks
    + Acyclic graphs, multiple possible functions due to the feedforward style and width of network
    + Cost function and it's probabilistic interpretation
    + Log(sigmoid) results a scaled softplus function
    + Probabilistic models and multi-modal mixture models 
    + Doesn't mention subgradients that allow ReLU to be sub-differentiable
    + Absolute activation function for object recognition - Good gradients everywhere, symmetric response to illumination
    + Maxout activation funtction - Generalise ReLU by grouping activations
    + Linear layers reduce the number of parameters in a neural network from np to (n+p)q
    + Proper introduction with many citations into the universal approximation theorem
    + Deep introduction into how backpropagation and gradient descent works - Though it is better to try implementing this in NumPy or similar for better understanding (with Guidance i.e. from a CourseRA course)
    + Discussion on improvements to the backpropagation algorithm in current neural networks
    
+ Chapter 7 - Regularisation for Deep Learning
    + Regularisation as a method of increasing generalisation due to the functional differences between the neural network model and the true generating process
    + L2 regularisation shrinking weight vectors in the direction that reduces the non-aligned eigenvectors
    + Explicit constraints on neural network outputs through clipping rather than having a very large Lagrangian multiplier in the cost function.
    + Norm on each layer weights is possible - Mimicks having separate Lagrange multipliers for each column
    + Data augmentation techniques
    + Label Smoothing - data scaling, use (0+eps)/(k-1) and 1-eps instead of 0 and 1 for softer boundaries
    + The multiple interpretations of dropout
    + Adversarial examples and a discussion on the implications
    
+ Chapter 8 - Optimization for Training Deep Models
    + Indirect optimisation of a performance defined in a indirect cost
    + ML seeks to minimise the empirical generalisation error - known as risk - through the use of a surrogate loss function. This is useful as the underlying data distribution is unknown (hence not as optimisation task)
    + Non-linear improvement in gradient estimate with a larger mini-batch size (sqrt n)
    + Shuffling a large dataset once and then storing it. Draw random batches from there
    + Ill-conditioning of the Hessian leading to large gradients not changing the cost
    + Model identifiability problem - Number of local minima increases with a smaller training set
    + Saddle points result in bad convergence for second order optimisation algorithms
    + Initialising the output biases to match the distribution of the data
    + Methods to speed up gradient descent - Conjugate gradients
    + Impact of batch normalisation on the learning dynamics
    
+ Chapter 9 - Convolutional Networks
    + Basics of convolution
    + Lots of detail into the implications of stride and pooling on calculating the gradients
    + Differences between similar convolutional operators
    + Biological motivations for the CNN
    
+ Chapter 10 - Sequence models: Recurrent and Recursive Nets
    + Unrolling the RNN to understand the time-dependent information flow
    + Backpropagation through time to calculate gradients many time-steps backwards
    + RNN as a complete graph that can model complex state transfers
    + Variable state lengths - important for variable length sequences
    + Additional parameters to predict length of sequence, forget rate, etc.
    + Bi-directional RNN, auto-encoder RNN using a context intermediate state
    + Easier to optimise shallow architectures for RNNs - Skip connections can help propagate gradients
    + Echo networks - Training the output and not the recurrance nature of the network. Can set up quadratic cost to result in quadratic convergence. State transfer should be stable (eigenvalues close to one), but non-linearity reduces the state transfer significantly.
    + Leaky units to propagate state linearly in time
    + Easier to design a model that is easier to optimise than to find a more powerful one
    + Random step in any direction when gradient explodes to inf escapes 'cliff' zone
    + Explicity memory for neural networks in a neural turing machine architecture
    
+ Chapter 11 - Practical Methodology
    + Lots of content is similar to Andrew Ng's CourseRA MOOC detailing the practical implementations of a machine learning solution
    + Logarithmic scale on the amount of data needed to improve the algorithm
    + Random search for hyperparameters rather than grid search
    + Bayesian regression model to help decide the location of exploration
    + Fit a tiny dataset first and check for a low training error before fitting large datasets
    + Calculation of gradient through the use of complex numbers
    + Checking the activations in a neural network
    + Case study on the street view numbers dataset
    
+ Chapter 12 - Applications
    + Discussion on GPU implementation, distributed training using asynchronous stochastic gradient descent
    + Cascaded classifiers in order to reduce everyday computational load on 'easy' classifications - similar to a decision tree approach to separate neural network components
    + Truncating numerical precision at inference time
    + Global contrast normalisation for pre-processing images for NN input - maps the contrast differences onto a sphere - highlights the edges, removes impact of shadows
    + NNs are best for regressing the output from the directions of the multivariable vectors rather than locations - Normalisation of the image
    + Dataset augmentation to improve classification invariances
    + NLP - word embeddings for better relational performance
    + Split representations of frequent and infrequent words by using the NN to predict probabilities of using the other
    + Importance sampling - using negative samples to aid in training and calculation of gradients (only done w.r.t. the total of the positive and negative samples)
    + Using a relational database to learn more structure from the data - train by generating false negatives by random shuffling

### Part 3 - Deep Learning Research

+ Chapter 13 - Linear Factor Models
    + Statistical (generalisation) and computational challenges (intractable higher dimensional data)
    + Intractable inference/normalisation constants
    + Slowness principle by appending a cost proportional to the differences in time - penalises rapid changes and is differentiable
    + Imposing a prior to yield closed form solutions
    + Expectation maximisation as a general solution for probability models
    + Linear factor models with chosen priors allow for generative modelling

+ Chapter 14 - Autoencoders
    + Reconstruction error leads to useful properties of the functional mapping to be learned
    + Re-circulation training by comparing activation patterns between encoder and decoder
    + Regularising the encoder to learn more useful represetations
    + Manifold tangent planes - NNs learn a function that behaves correctly on the lower dimension manifold
    + Semantic hashing for information retrieval

+ Chapter 15 - Representation Learning
    + Pre-training more useful to NLP tasks than image tasks possibly due to images lying in a rich vector space where distances provide a low quality similarity metric
    + Pre-training reduces the variance of the possible converged networks 
    + Unsupervised pre-training to allow the learning algorithm to find the underlying causes that generate the observations
    + One-shot and zero-shot learning by trying to generalise across tasks and having unique representations in the latent space for every test input
    + Alternate losses (such as GAN loss) to encourage the learning of important salient features
    + Distributed representations - Increasing the output configurations by separating the features resulting in a large similarity space
    + Neural networks learn distributed representations that allow generalisation when the target function does not have the smoothness property. nd parameters result in n^d regions in input space
    + Large amount of possible regularisers to encourage the learned latent space to have good properties    
    
+ Chapter 16 - Structured Probabilistic Models for Deep Learning
    + Structured models to reduce the number of parameters needed to represent a joint distribution
    + Directed vs undirected models depending on the conditioning of the distributions
    + Nodes must not share any children in order to be considered d-separated when the child is observed
    + Deep learning approach to probabilistic models - Inflate model capabilities until it is barely trainable, use minimum information required, approximate objective function (which needs to have gradients) and approximately train a satisfactory model
    + Restricted Boltzmann machine - energy-based model (linear in parameters) with hidden units and a special structure that allows efficient block Gibbs sampling
    
    
+ Chapter 17 - Monte Carlo Methods
    + Markov chain - Update matrix (stochastic matrix) has a largest eigenvalue corresponding to 1, all other components decay to zero with enough steps. Eventually converges to an equilibrium distribution
    + Successive samples are correlated - need to burn in a few samples before re-drawing another sample
    + Ancestral sampling in graphs does not need any burn-in time (directed and acyclic) and only requires a single pass

+ Chapter 18 - Confronting the Partition Function
    + Contrastive divergence to reduce the cost of MCMC sampling by initialise the MCMC chain with a distribution close to the one being simulated
    + Stochastic maximum likelihood initialise multiple MCMC using samples drawn from a previous timestep of the MCMC state
    + Pseudolikelihood using the cancellation of the partition function when considering conditional probabilities

+ Chapter 19 - Approximate Inference
    + Recast as optimisation problem using the KL divergence

+ Chapter 20 - Confronting the Partition Function

### Things I need to revisit

    + Linear factor models
    + Approximate inference

