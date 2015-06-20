---
layout: post
category: research
tags: michael-jordan, log-linear, mean-field-variational
title: Some Updates on Log-linear Models and Mean Field Variational Bayes
---

### On the accuracy of self-normalized log-linear models

<div class='message'>
The paper [1] deals with fast calculation of normalizer in log-linear models. The authors is based on the recently proposed technique known as <code>self-normalization</code>, which introduces a <code>regularization term</code> to penalize log normalizer for deviating from zero. The authors also prove <code>general bounds</code> on the estimated <code>variances</code> of normalizers, and the <code>loss of accuracy </code> due to self-normalization.
</div>

**Log-linear models** have the following forms:

$$p_\eta(y | x) = e^{\eta^T T(y,x)} - A(\eta,x)$$

with

$$A(\eta, x) = \log\Sigma_{y\in\mathcal{Y}} e^{\eta^T T(y,x)}$$

**Self-normalization**: the log-linear model $$p_\eta$$ is *self-normalized w.r.t* $$\mathcal{S} \in \mathcal{X}$$ if $$\forall x\in \mathcal{S}, A(x,\eta)=0$$.

### Linear Response Methods for Accurate Covariance Estimates from Mean Field Variational Bayes

<div class='message'>
The paper [2] focuses on the Mean field variational Bayes (<code>MFVB</code>). The main issue with MFBV is that it <em>underestimates the uncertainty of the model variables</em>, and provides <em>no information about variable covariance</em>. The authors generalize <code>linear response models</code> from statistical physics to deliver <code>accurate uncertainty estimates</code> for model variables.
</div>

### References:

1. Jacob Andreas, Maxim Rabinovich, Dan Klein, Michael I. Jordan, *On the accuracy of self-normalized log-linear models*, [link](http://arxiv.org/pdf/1506.04147.pdf)

1. Ryan Giordano, Tamada Broderick, Michael Jordan, *Linear Response Methods for Accurate Covariance Estimates from Mean Field Variational Bayes* [link](http://arxiv.org/pdf/1506.04088.pdf)
