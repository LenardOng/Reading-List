## Deep Learning
### Introduction to my experience with this book
+ This is an introductory book that is more accessible and provides a high level introduction to complex topics 


### What's different
+ A book that is fully focused on deep learning and ensures new readers to machine learning can keep up with the content
+ More detailed statistical view into machine learning

### What else is good
+ Extended detail beyond the necessary

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
    
+ Chapter 11 - Practical Methodology
+ Chapter 12 - Applications

### Part 3 - Deep Learning Research

+ Chapter 13 - Linear Factor Models
+ Chapter 14 - Autoencoders
+ Chapter 15 - Representation Learning
+ Chapter 16 - Structured Probabilistic Models for Deep Learning
+ Chapter 17 - Monte Carlo Methods
+ Chapter 18 - Confronting the Partition Function
+ Chapter 19 - Monte Carlo Methods
+ Chapter 20 - Confronting the Partition Function

### Things I need to revisit



