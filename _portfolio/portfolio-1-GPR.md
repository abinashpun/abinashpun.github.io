
---
title: "Estimating Background with GPR"
excerpt: "Description on using Gaussian Process Regression to estimate background under the peak signal"
collection: portfolio
---

<!-- This is an item in your portfolio. It can be have images or nice text. If you name the file .md, it will be parsed as markdown. If you name the file .html, it will be parsed as HTML.  -->
-
<!-- under development -->

# Introduction
This project is about estimating the background in the data with Gaussian Process Regression (GPR) method.

## Gaussian Process Regression
Gaussian Process Regression (GPR) is a powerful statistical modeling technique used for regression analysis. It is a non-parametric Bayesian approach that can effectively capture complex patterns and relationships in data.

In GPR, the underlying assumption is that the data points are drawn from a Gaussian process, which is a collection of random variables where any finite subset follows a multivariate Gaussian distribution. This makes GPR a flexible and versatile method for modeling various types of data. The key idea behind GPR is to model the relationship between input variables (predictors) and output variables (response) as a continuous function. Unlike traditional regression methods that assume a fixed functional form, GPR provides a flexible framework that can adapt to the data by capturing both the mean and uncertainty in the predictions.

## Peak Signal and Background

The $J/\psi$ particle, also known as the $J/\psi$ meson, is a subatomic particle that belongs to the category of mesons with mass 3.14 GeV. Studying the properties and behavior of the $J/\psi$ particle provides valuable insights into the strong nuclear force and the interactions between quarks. It has contributed to our understanding of particle physics, the quark model, and the fundamental building blocks of matter.

The $J/\psi$ particle is unstable and quickly decays into lighter particles.  Its decay modes also include the production of muons and antimuons, a dimuon. We can investigate about the  $J/\psi$ particle by studying the 3.14 dimouns produced at any nuclear experiment. But in such experiments, along with the $J/\psi$ dimuons, many other dimuons from different physics (or non-physics) process can also be prodcued. Thus the underneath the $J/\psi$ peak of the dimuon mass spectrum, there are some background those need to be subtracted. The background might not have any particular shape and might depend on various kinematics. So,we use GPR method to extract such background underneath the peak.

# Analysis Steps
<p align="center">
<img src="{{ site.url }}{{ site.baseurl }}//portfolio_files/gpr_intro.png">
</p>

## Take two Side Bands from either sides of $J/\Psi$ peak 
## Fit GPR with Side Band Data
```python 
from sklearn.gaussian_process.kernels import RBF, ConstantKernel as C
sideband_kernel = C(50000.0, (1e-10, 1e15))*RBF(length_scale=5, length_scale_bounds=(1e-4, 1e15))
gaussian_process = GaussianProcessRegressor(kernel=sideband_kernel, alpha=Y_train_error**2, n_restarts_optimizer=5000)
gaussian_process.fit(np.atleast_2d(X_train).T, Y_train)

```
## Predict the background underneath the peak with GPR

# Sanity Check with MonteCarlo 

# Conclusion

# Reference