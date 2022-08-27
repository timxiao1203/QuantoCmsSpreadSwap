# Quanto CMS Spread Swap


A quanto CMS spread swap is an exotic interest rate swap. The swap consists of two legs: One leg is a fixed rate leg. The other leg pays a fixed rate during a portion of the tenor and a variable rate during the remaining part. The variable rate is based on a spread between GBP and EURO 10 year CMS rates. Depending on the deal, the floating rate payments may last up to 20 years.

All payments are made in the EURO currency. The floating rate payments are specified by

•	T0 		- the start date of the floating rate payments,
•	Ti		- annual reset dates,
•	S_B 		- 10 year GBP CMS rate based on a semiannual reset swap starting on Ti,
•	S_E 		- 10 year EURO CMS rate based on an annual reset swap starting on Ti,
•	mB		- the leverage ratio for  ,
•	nE		- the leverage ratio for  
•	c		- the cap on the payments,
•	f		- the floor on the payments, f < c,
•	Pi 		- the payoff set at time Ti and 	paid at time Ti+1:

The value of the floating rate payment that sets at Ti,  ,  is given by its expectation under the Ti+1-forward measure times today's price of a Ti+1-maturity zero coupon bond:

Under the T-forward probability measure, each swap rate is assumed to have the following distribution:

The mean value, S0, is based on the CMS rate forward value adjusted both for convexity and for the delay of payment to Ti+1:
		 
where

SF	- is the Ti-forward 10Y CMS rate,
ac	- is the convexity adjustment,
at	- is the timing delay adjustment

Additionally, a quanto adjustment is made to the GBP CMS rate. The adjustment, aq, is calculated as
 
where

X	- is the forward exchange rate (GBP worth of one EURO),
Sigma_X 	- is the volatility of the forward exchange rate,
Sigma_B 	- is the volatility of the GBP 10Y CMS  rate,
Rho 	- is the correlation between the forward exchange rate and GBP 10Y CMS  rate.

Quanto CMS spread swap is an exotic derivatives. Many exotic derivatives have barrier and callable features (see https://finpricing.com/lib/EqBarrier.html)

Reference:

https://osf.io/umeq3/download

		 

