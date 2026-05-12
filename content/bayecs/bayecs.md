# Sherwood Webb 2020 in Stan

This is a Stan-based approach for calculating the posterior distributions of ECS from [Sherwood, Webb et al. 2020](https://doi.org/10.1029/2019RG000678) (hereafter SW20). The original code is slow, taking $\mathcal{O}\left(10\;\text{hrs}\right)$ to calculate a full posterior. The Stan implementation brings it down to $\mathcal{O}\left(10\;\text{secs}\right)$.

By refactoring the posterior calculation in Stan we hope to achieve two goals: 
1. increase the speed by two orders of magnitude taking advantage of Stan's Hamiltonian Monte Carlo (HMC) sampler
2. take advantage of Stan's expressive natural language syntax to make the Bayesian framework more user friendly.

### Difference from SW20
There is only one (intentional) difference from SW20's model. Our model does not account for the correlation between historical forcing ($F_{hist}$) and the forcing associatd with a doubling of CO$_2$  $(F_{2\times CO_2})$. I tried implementing this correlation and it resulted in very small differences in the posterior  of <0.05K at all percentiles (consistent with SW20), but sacrificed code simplicity and ease of reading. 

### Colab and Github:
This jupyterbook contains a Google colab version of the code. The colab version is not regularly updated,  and is primarily intended as a frictionless demo that does not require installing a new python environment. 

A Github repository for the code (which may be more up to date) can be found here [https://github.com/cdds-uiuc/bayecs](https://github.com/cdds-uiuc/bayecs)

### More Info 
Checkout the Readme for the overall statistical model and 
a few issues related to the numerical estimation of the posterior.

In order to understand the underlying Bayesian framework, readers
should familiarize themselves with [Sherwood, Webb, et al. 2020](https://doi.org/10.1029/2019RG000678), and
[Marvel and Webb 2025](https://doi.org/10.5194/esd-16-317-2025).

