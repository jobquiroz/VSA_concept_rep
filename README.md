# VSA_concept_rep
Concept representation model using Vector Symbolic Architectures

## Introduction.
This repository includes all the files developed for the (under review) paper "Vector Symbolic Architectures for concept representation". 

Vector Symbolic Architectures are a family of methods that use high-dimensional vectors to represent objects: concepts, trees, sequences, etc. In this work we selected a binary VSA called *Binary Spatter Codes* proposed by Pentti Kanerva. Based on this VSA we designed a model for concept representation that creates "Semantic Pointers" based on a set of semantic features. 

We took the idea of semantic pointers from Eliasmith's model *Semantic Pointer Architecture*. Semantic pointers are vectors used to point to information within a memory system, therefore the term pointer. However, semantic pointers are also 'semantic', which means that the pointers themselves are similar to the information they reference. 

As stated before we create these semantic pointer based on a set of semantic features, which are words that try to define a concept based on its relations with other words. We used the semantic feature dataset from McRae et al. 

The following table correspond to the evaluation set used for the experiment:

![EvaluationTest](https://github.com/jobquiroz/VSA_concept_rep/blob/master/HumanSimilarity%20Benchmark.png)


**Description of files.**
All codes were implemented as Python Notebooks. This repository also includes the files from the McRae dataset which were slightly modified to acomodate our needs. 

The repository contains two folders: Code and Data. 
Within Code there are three notebooks: VSA-Experiments, EncodingDataset and HDComputing_basics.

- **HDComputing_basics** implements all the basic operations to be used with high-dimensional vectors, from generating new random vectors, to operating them. It also contains the description of the clean-up memory as well as its initialization.
- **EncodingDataset** contains all the functions to read the files from the McRae dataset and transform all the concepts and its relations into semantic pointers. 
- **VSA-Experiments** uses the functions from the previous notebooks for performing the experiments detailed within the paper.
- **Simple examples** shows the end-to-end process for creating a high-dimensional representation for a pair of concepts. It also shows some of the properties of these vectors. 

**Additional notes**
To successfully try our codes is also needed to download the nltk library, specifically those modules for Wordnet and wordnet_ic tools. 
Once everything is set up, running the entire 'VSA-Experiments' notebook should take around 10 minutes. The figures from the paper are automatically shown in this notebook.
