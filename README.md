# neural-decoding
Use multiple computational models to decode neural signals inside mouse visual cortex system. Also an exploration into AllenSDK.

## Introduction & Problem Description
This project aims to **decode the stimulus identity from neural activity in the visual system of mice**. To be concrete, here is the problem I am going the attack: by analyzing the behaviors of a group of neurons inside the visual system of a mouse's brain, can we tell, to the maximum probability, what type of stimuli presentation pattern is exerted onto its vision system.

All the data in this project comes from AllenSDK. This is an interface to download data from [Allen Brain Observatory](https://allensdk.readthedocs.io/en/latest/brain_observatory.html), a `database of the visually-evoked functional responses of neurons in mouse visual cortex based on 2-photon fluorescence imaging'. This dataset is well-organized, informative and still convenient to use thanks to a well-designed AllenSDK library, so it is perfectly suitable for a start-up project like this.

I will to try different models on this decoding task, including probability & statistics models that I learned in an [online computational neuroscience course](https://www.coursera.org/learn/computational-neuroscience), and machine learning (ML) / deep learning (DL) models that I have already knew before.

It is my first project in computational neuroscience (CNS). My expectation is that I can build a deeper understanding through this project in the following aspects:
1. the structure and characteristics of the visual system in mice
1. the best practice to interact with AllenSDK
1. the basic workflow and methodology in CNS research
1. common models of neural decoding
1. common approaches to presenting experiment result in this field, e.g. plotting tuning curve, illustrating intermediate features, presenting plausible accuracy metrics, etc.

## Project Pre-Design
I think this project will basically include the following steps:

1. (In Progress) Download the AllenSDK complete dataset to local storage to enhance the data access efficiency
2. (In Progress) Preprocess the dataset: select experiment sessions, split training set/testing set
3. Design, implement and multiple decoding models
    1. Do feature engineering: extract features from neural behaviours (recodings from electrophysiological experiments)
        - Different cortical areas, different cortical depth
        - Different filters
        - Other data-preprocess techniques
    2. Apply different classifiers to this decoding task
        - Bayes' Model
        - ML Model
        - (Other models TBD)
    3. Set up metrics to judge the performance the classifier
        - Accuracy and loss
        - (Other metrics TBD)
    4. Explain the results by observing dataset in depth
        - plot tuning curve
        - observe response properties across areas and layers
        - look at the dynamics of population in state space
4. Select the 'best' model, write documentations, present the result, polish and publish the code

## Credit & Reference
- AllenSDK: https://github.com/AllenInstitute/AllenSDK