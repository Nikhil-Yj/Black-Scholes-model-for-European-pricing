# Black-Scholes-model-for-European-pricing
References:

1.	F. Black, M. Scholes "The pricing of options and corporate liabilities", J. Polit. Econ., 81, pp. 637-654, (1973).
2.	P. Wilmott, S. Howison, J. Dewynne "Option Pricing: Mathematical Models and Computation",
Oxford Financial Press, Oxford (1993).

Black-Scholes model
Under certain assumptions, the value (or price)   of a European call option on a stock, whose price at time   is  , is given by the Black-Scholes model (1973)

whose analytical solution is given by


  is the standard normal cumulative distribution function   is the volatility of the stock
r is the risk-free interest rate T is the maturity/expiry date K is the strike price


Transformation to a constant coefficient initial value problem (IVP):
Using the transformation
 
the original Black-Scholes model can be transformed to the following IVP:


Localization: Imposing artificial boundary conditions
In order to implement implicit finite difference methods to approximate the solution u, the above problem needs to be localized on a bounded domain  , that is,
where, in the spatial direction, the artificial boundary conditions 0 and   are imposed on the left boundary   and right boundary  , respectively.
Implement the following finite difference method


Consider the following parameter values






and a uniform partition

 

of the rectangle  .

Find	, such that
 
 





