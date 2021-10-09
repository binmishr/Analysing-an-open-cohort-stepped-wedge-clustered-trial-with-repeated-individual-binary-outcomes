# Analysing-an-open-cohort-stepped-wedge-clustered-trial-with-repeated-individual-binary-outcomes

The details of the codeset and plots are included in the attached Adobe Acrobat reader (.pdf) file in this repository. 
You need to download the same to view the contents. There are referrals to other contents in BLUE colour also to follow.

A Brief Introduction
=====================

I am currently wrestling with how to analyze data from a stepped-wedge designed cluster randomized trial. A few factors make this analysis particularly interesting. First, we want to allow for the possibility that between-period site-level correlation will decrease (or decay) over time. Second, there is possibly additional clustering at the patient level since individual outcomes will be measured repeatedly over time. And third, given that these outcomes are binary, there are no obvious software tools that can handle generalized linear models with this particular variance structure we want to model. (If I have missed something obvious with respect to modeling options, please let me know.)

I introduced the project that is motivating all of this, the HAS-QOL study, when I provided simulations of the data generating process we are assuming for this analysis. And before that, I described (here and here) Bayesian models that can be used to analyze data with more complicated variance patterns, though all of those examples were based on continuous outcomes. Here, I am extending and combining those ideas to present an approach to estimating treatment effects in the context of HAS-QOL.

This post walks through the data generation process and describes a Bayesian model that addresses the challenges posed by the open cohort stepped-wedge study design.
