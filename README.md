## Sparse Wasserstein barycenter

In this small project I present a simulation of the free support barycenter problem:

$$
\underset{Y:=(y_1,\ldots,y_N)\in(\mathbb{R}^d)^N}{\arg\min} \ \frac{1}{L}\sum_{\ell=1}^L W_2^2\left(\mu_n^\ell,\frac{1}{L}\sum_{i=1}^N \delta_{y_i}\right)
$$

where each $\mu_n^\ell,\: \ell = 1,\ldots,L$ are population measures of the respective target measures $\mu^1,\ldots,\mu^L$. This problem is a subclass of the sparse Wasserstein barycenter problem[^1].

The algorithm we use is the fixed point procedure proposed by Cuturi and Doucet[^2]. An implementation of the latter is given in the [POT library](https://pythonot.github.io/auto_examples/barycenters/plot_free_support_barycenter.html).

The example I give has four target Gaussian measures and shows the evolution of their fixed support barycenter when the size $n$ of each empirical measure increases.

[^1]: L Portales, E Pauwels, E Cazelles. *Sample complexity of optimal transport barycenters with discrete support*. 2025.
[^2]: M Cuturi, A Doucet. *Fast computation of Wasserstein barycenters*. 2014.
