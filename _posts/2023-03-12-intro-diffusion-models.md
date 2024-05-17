---
layout: post
title:  Understanding the 'Understanding Diffusion Models- A Unified Perspective' paper
date:   2023-03-12
description: Notes on the paper, and introduction to diffusion models
tags: diffusionModel, generativeModel
# categories: sample-posts
---
### Understanding Diffusion Models: A Unified Perspective



<!-- **Original Paper:** 
[![Read the OG paper](https://arxiv.org/abs/2208.11970) -->
  
<!-- **Authors:**
Calvin Luo -->

This is just me reading this paper and making some notes on the go. Let me know if someone wants to discuss the paper or find something intersting in my notes. Pardon my casual poor language skills throughout 😄

> I will try to go through some concepts in detail, while we also talk briefly through other relevant concepts. The text is purely my interpretation of the published work by Calvin Luo, and please dont use these notes to understand the paper. Rather think of this text as an exercise to check if you understood the concepts better than me or not 😉

- As I mentioned , these are just some notes. I'd suggest read the [Paper](https://arxiv.org/abs/2208.11970) first.

- I wont go in detail of many concepts but sure you can.

- Please let me know if you find any error in my understanding of concepts. Always feel great to be wrong 😭



## <font size="6" color="darkblue">Introduction </font>

The goal of generative model is to learn a true data distribution `p(x)` given some observed samples `x`. 
The learned model can:
- Generate new samples from approximate data
- Evaluate the likelihood of sampled data

There are various directions for generative models as mentioned in text. 
Generative Adversarial Networks (GANs) learn to model sampling in an adversarial manner.
> Adversarial means two sides which oppose each other. GANs have generator and discriminator networks both of which are trained in adversarial manner. One network tries to generate new data and the other attempts to predict if the output is fake or real data.

`Likelihood-based` generative models are another class where the model assign high likelihood to the observed data samples. These include - *Autoregressive models*, *Normalizing flows*, and *Variational Autoencoders (VAEs)*.
>An autoregressive (AR) model is a type of statistical model used for analyzing and predicting time series data. It determine the probabilistic correlation between elements in a sequence, and use the knowledge derived to guess the next element in an unknown sequence. For example, during training, an autoregressive model processes several English language sentences and identifies that the word “is” always follows the word “it” It then generates a new sequence that has “it is” together.

>Normalizing flows are like starting with a simple shape, such as a ball of clay, and transforming it into a complex shape by squeezing and stretching it multiple times. Each transformation is reversible, so we can always go back to the ball shape. This process helps us model and understand complex patterns in data by starting from something simple and making it more intricate step-by-step.

