This is repository of code used in the commissioned NIHR multi-cancer test HTA call. 
The use of multi-cancer detection (MCD) tests for the diagnosis of cancer in primary care in individuals with abdominal symptoms. Nicholson/Middleton. 

1. Primary outcome sample size justification.
 Relates to this text in the app
   "To achieve 90% power and a two-sided 5% significance level, with equal allocation, 8,050 participants will be randomised to each arm.
   Accounting for an estimated 5% attrition due to withdrawal or sample failure, a total sample size of 16,906 is estimated. We have assumed:
   a cancer prevalence of 4% (322 cancers per arm), MCT cancer sensitivity of 73%, and limited the potential reduction of diagnostic interval
   by up to a half to those longer than 42 days. The rate ratio is estimated to be 0.78 (95% CI, 0.66-0.91)." 

Files used: 

The 8,050 numbers and confidence interval above are dervied from a simulation in whih diagnostic intervals between the two randomised groups are compared using 
an exact Poisson test in the file S2_power_calculation_RateRatio. 

As we have said we will use a GLM with random effect for GP practice, we checked that we had the same power using this approach. 
In the file S2_power_calculation_MixedEffects we check that changing from an exact test to a GLM with quasi-Poisson errors does not lower the power.  

We also checked the power using a Cox model with time-dependent covariates and Heaviside function (S2_power_calculation_TimeDepCoxModel), 
a log-rank test (S2_power_calculation_LogRankTest) and an accelerated failure time model (S2_power_calculation_ParametricRegression). 

2. Secondary outcomes. Eg. cancer conversion rate, proportion of incurable cancers, routes to diagnosis, and cancer specific mortality, can be found in S2_power_calculations_SecondaryOutcomes

Other files on this repo include stage shift and mortality comparison were not used in the final application. 
