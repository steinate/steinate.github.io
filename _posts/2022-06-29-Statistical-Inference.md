---
layout: post
title: Statistical Inference
date: 2023-07-12 00:00:00 +0800
category: tutorial
thumbnail: /style/image/thumbnail.png
icon: book
---


* content
{:toc}
# Statistical Inference

## Bayesian Hypothesis Testing  

Each of the possible scenarios corresponds to a hypothesis.  When there are M hypotheses, we denote the set of possible hypotheses using $H=\{H_0, H_1, ..., H_{M-1}\}$.

The observed collection of data is represented as a random vector $y$, which may be discrete- or continuous-valued . 

In a Bayesian hypothesis testing problem, the complete model therefore consists of the a **priori probabilities**:

$$p_H(H_m), m=0, 1, ..., M-1$$

together with a characterization of the observed data under each hypothesis, which takes the form of the **conditional probability distributions**

$p_{y|H}(·|H_m), m =0,1,...,M-1$

a complete characterization of our knowledge of the correct hypothesis based on our observations is the set of a **posteriori probabilities** 

$p_{H|y}(H_m|y), m=0,1,...,M-1$

Bayes’ Rule:  

$p_{H|y}(H_m|y)=\frac{p_{y|H_m}p_H(H_m)}{\sum_{m'}p_{y|H_{m'}}(y|H_{m'})p_H(H_{m'})}$

### Bayesian Hypothesis Testing

Specializing to the binary case, our model consists of two components. One is the set of **prior probabilities** :

$P_0=p_H(H_0)$

$P_1=P_H(H_1)=1-P_0$

The second is the observation model, corresponding to the likelihood functions:

$H_0: p_{y|H}(y|H_0)$

$H_1: p_{y|H}(y|H_1)$

### Optimum Decision Rules: The Likelihood Ratio Test  

The solution to a hypothesis test is specified in terms of a **decision rule**. 

use an objective function taking the form of an expected **cost function**:

$\hat{C}(H_j, H_i)=C_{ij}$

**Bayes risk:**

$\phi(f)=E[\hat{C}(H, f(y))]$

The **optimum decision rule** takes the form:

$\hat{H}(·)=argmin(\phi(f))$

- Theorem 1. Given a priori probabilities $P_0, P_1$, data $y$, observation models $p_{y|H}(·|H_0)$, and valid costs $C_{00}, C_{01}, C_{10}, C_{11}$, the optimum Bayes’ decision rule takes the form:  

  $L(y)=\frac{p_{y|H}(y|H_1)}{p_{y|H}(y|H_0)}>_{H_1}<_{H_0}\frac{P_0(C_{10}-C_{00})}{P_1(C_{01}-C_{11})}=\eta$

### Maximum A Posteriori and Maximum Likelihood Decision Rules

- The minimum probability-of-error decision rule takes the form  :

  $\hat{H}(y)=argmax P_{H|y}(H|y). H\in \{ H_0, H_1\}$

  When the hypotheses are equally likely, the minimum probability oferror decision rule takes the form: 

  $\hat{H}(y)=argmax P_{y|H}(y|H). H\in \{ H_0, H_1\}$

  

  

  