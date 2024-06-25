The marketing team recently conducted a media campaign on a product ABC and would like to know the effectiveness of that campaign (e,g., impact on sales) in the post intervention period. The goal of this study is to examine the causal impact of the campaign in a relatively short period and suggest strategies on media sepnd. As a result, positive causal impact of the campaign on sales was idnetified during the post intervention period.

Data : target: sales; covaraites: three types of media spend and holiday

pre-period: Jan 01, 2022-Aug 31, 2023

post-period: Sept 01, 2023-Dec 31,2023

The model used is Bayesian structure time series modeling (BSTS) with pybuc and pymc. Google has an R package called CausalImapct can estimate the causal effect of a designed intervention on a time series. I love it but the Python version is somewhat lack of flexibility (e.g., the underlying UnobservedComponents model from statsmodels package is not Bayesian). I recently discrovered a Python Bayesian Unobserved Components library (pybuc), which is an implenmentation of R's Bayesian structural time series package (bsts) can do the BSTS modeling for causal impact analysis. Alternatively, PyMC now has experimental support for linear, Gaussian state space time series models via the pymc_experimental.statespace module. Building BSTS models to conduct causal impact analysis with PyMC is more flexible but generally requires more effort compared to using other libraries like Pybuc.
