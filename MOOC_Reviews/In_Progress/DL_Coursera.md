## Deep Learning Specialisation on Coursera

### Summary
+ Broken down into 5 sub-courses
    + Neural Networks and Deep Learning
    + Improving Deep Neural Networks: Hyperparameter Tuning, Regularisation and Optimisation
    + Structuring Machine Learning Projects
    + Convolutional Neural Networks
    + Sequence Models
    
+ Total of 16 weeks

+ Coding is now in Python 3 rather than Octave/Matlab and happens in a Jupyter Notebook rather than a separate program. Evaluation happens by analysing the notebook.


## Neural Networks and Deep Learning

+ Was a good re-introduction to neural networks again after doing the Machine Learning course
+ Coding tasks were easier in general due to the Jupyter Notebooks and code was provided where explanations may have not been clear

### Total of 4 weeks

+ Introduction to deep learning
    + Material very similar to Machine Learning Coursera MOOC
    
+ Neural Networks Basics
    + A little more basic than expected, assumes no knowledge of gradients or the chain rule
    + Coding felt a little too guided compared to ML Course
    
+ Shallow neural networks
    + Faster and clearer introduction to stacking layers in networks than ML Course
    + More time spent on vectorisation - How it works and its structure
    + Coding: Updated with newer and more trendy activation functions
    
+ Deep Neural Networks
    + Lots of focus on matrix dimension consistency (Usually handled by the deep learning library, but good for understanding)
    + Coding: Implementing a vectorised form of backpropagation with generalised functions for scalable code
    
## Improving Deep Neural Networks: Hyperparameter Tuning, Regularisation and Optimisation

### Total of 3 weeks

+ Practical Aspects of Deep Learning
    + Introduction to regularisation techniques in neural networks (weight decay and dropout), initialisation (zeros failing to break symmetry and using different initialising techniques), Gradient checking
    + Orthogonalisation as separating the fitting task and the regularisation task
    + Coding: Implementation of inverted dropout
    
+ Optimisation Algorithms
    + Intuition and implementation of gradient momentum, RMSprop and the adam method
    + Coding: Implementing momentum methods and the adam method
    
+ Hyperparameter tuning, Batch Normalisation, and Programming Frameworks
    + Creating a log search space for hyperparameter tuning
    + Batch normalisation for activations within a network with learnable parameters
    + Introduction to Tensorflow (Math ops are overloaded for tf variables!)
    + Good emphasis on functional programming
    + Coding: Using tensorflow for a basic classifier using a cross entropy loss
    
## Structuring Machine Learning Projects

+ Much more focused on the practical side of designing machine learning systems
+ Very useful in terms of getting pseudo-experience and tips on how to go about developing systems in a systematic way

### Total of 2 weeks
+ Part 1 - Machine Learning Strategy
    + Importance of a single number evaluation metric (Repeat from Machine Learning)
    + More detail into orthogonalising tuning parameters
            + Improving training set performance - Better optimisers, different architecture 
            + Improving validation set performance - Regularisation, dropout
            + Improving test set performance - Collection of more data (Validation should be representative of test conditions)
    + Can have other constraints (satisficing) in optimising parameters
+ Part 2 - Machine Learning Strategy
    + Error analysis on the mislabelled data in order to know where to focus efforts
    + Distribution mismatch when augmenting data with crawled vs collected images. Use small collected set as dev/test set!
    + Comparison between human error levels, training set errors, training-dev set errors and dev errors



## Convolutional Neural Networks

### Total of 4 weeks
+ Foundations of CNNs
    + Slight intuitions and basic introduction
+ Deep CNNs: Case Studies
    + Standard CNNs - AlexNet, LeNet-5, VGG16
    + Residual networks - Skip connection has potential to ignore layers by learning an identify function. Convolution layers must be padded for equal sizing
    + Inception modules - Motivation and structure
+ Object Detection
+ Special applications: Face recognition and neural style transfer

## Sequence Models

### Total of 3 weeks
+ Recurrent Neural Networks
+ Natural Language Processing and Word Embeddings
+ Sequence Models and Attention Mechanism