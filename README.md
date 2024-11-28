# Statistical Research Skills: Assignment 1

This assignment was for MATH11188 Statistical Research Skills, academic year 2023–2024. 
The course was organised and lectured by Dr. Torben Sell, Lecturer in Machine Learning, School of Mathematics, The University of Edinburgh (torben.sell@ed.ac.uk).
The assignment's problem statement and marking scheme are in `Assignment 1.pdf` and `Assignment 1_marking_scheme.pdf` respectively. The task was to write a report on the following article: 
> Sloughter, J. M., Gneiting, T., and Raftery, A. E. (2010). 'Probabilistic wind speed forecasting using ensembles and Bayesian model averaging', *Journal of the American Statistical Association*, 105(489), pp. 25–35.

My submitted report is in `TengWeiYeo_S2566430_A1_SRS.pdf`. 

Sloughter et al. (2010) proposed a Bayesian Model Averaging (BMA) procedure to generate probabilistic forecasts of discretised wind speed data.
One of their suggested approaches --- the *Standard Method* --- does not account for the discretisation of the wind speed data when doing parameter estimation through maximum likelihood estimation (using the ECME algorithm). 
They try another approach --- the *Fully Discretised Method* --- which does consider the discretisation.
They find that both approaches generate very similar results. 
To check this claim, I used simulated data to identify whether the *Standard Method* and the *Fully Discretised Method* give different results, in terms of (i) the BMA probability density functions, (ii) the maximum log likelihoods, and (iii) the 77.8% symmetric prediction interval.
The code is in `SRS_A1_S2566430.R`.
The results of my simulation do not reject their claims.

Please email me (Teng Wei Yeo, student number S2566430) at yeotengwei@gmail.com for any questions.

# Erratum
My submitted report, `TengWeiYeo_S2566430_A1_SRS.pdf`, falsely states that INLA is inappropriate for wind speeds because wind speed data is not normally distributed. 
This is incorrect because INLA can be used to fit Latent Gaussian Models, which is a type of GAM, meaning that INLA can model response variables from an exponential family distribution.