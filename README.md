# election-social-media-bias
Election data imputation and inference from social media plus poll data.

## imp-svd.ipynb
Contains the imputation process for incomplete data and for bias reduction using SVD.

### Data Imputation

This refers to replace missing data. There are two methods here: simple and multiple imputation. Simple imputation replaces missing data with the average of the column. Multiple imputation replaces data by drawing from a probability distribution obtained from historical data. A number of drawings is performed and for each set of drawings an analysis is done. These are then averaged to obtain a single result in the end.

### Bias Reduction

The assumption is that all measurements are coming from the same __true__ value and are biased due to sampling bias (over and under representation of certain sectors) and malicious actors (bots, fake news, fake accounts). Here SVD is used on the imputed data to get the best rank one approximation which would filter some of the biases. Finally, the difference between the observed (imputed) data and the rank one captures the bias in the observed data.

**Disclaimer**
This repo was made for personal use and has not being maintained for production.
