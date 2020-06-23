---
name: Correlation Coefficients
use_math: true
heading1: Correlation Coefficients
motivation: Someday it will all make sense.
about: MATH
--- 

Correlation Coefficients

## Pearson Correlation Measures

The Pearson product-moment correlation coefficient is a measure of the strength 
of the <u>linear relationship</u> between two variables.


**If the relationship between the variables is not linear, then the correlation**
**coefficient does not adequately present the strength of the relationship between**
**the varibles..**

The symbol for Pearson's correlation is "ρ" when it is measured in the population and "r" when it is measured in a sample. 
Because we will be dealing almost exclusively with samples, we will use r to represent Pearson's correlation unless otherwise noted.

Pearson's r can range from -1 to 1. 
* An r of -1 indicates a perfect negative linear relationship between variables, 
* an r of 0 indicates no linear relationship between variables, 
* an r of 1 indicates a perfect positive linear relationship between variables. 


---

There are several formulas that can be used to compute Pearson's correlation. Some formulas make more conceptual sense whereas others are easier to actually compute. We are going to begin with a formula that makes more conceptual sense.

We are going to compute the correlation between the variables X and Y shown in Table 1. We begin by computing the mean for X and subtracting this mean from all values of X. The new variable is called "x." The variable "y" is computed similarly. The variables x and y are said to be deviation scores because each score is a deviation from the mean. Notice that the means of x and y are both 0. Next we create a new column by multiplying x and y.

Before proceeding with the calculations, let's consider why the sum of the xy column reveals the relationship between X and Y. If there were no relationship between X and Y, then positive values of x would be just as likely to be paired with negative values of y as with positive values. This would make negative values of xy as likely as positive values and the sum would be small. On the other hand, consider Table 1 in which high values of X are associated with high values of Y and low values of X are associated with low values of Y. You can see that positive values of x are associated with positive values of y and negative values of x are associated with negative values of y. In all cases, the product of x and y is positive, resulting in a high total for the xy column. Finally, if there were a negative relationship then positive values of x would be associated with negative values of y and negative values of x would be associated with positive values of y. This would lead to negative values for xy.

**$r = \frac{\sum{XY} - \frac{\sum{X}\sum{Y}}{N}}{\sqrt{(\sum{(X^2)} - \frac{(\sum{X})^2}{N})(\sum{(Y^2)-\frac{(\sum{Y})^2}{N}})}}$**


## The variance sum law

[Variance Sum Law and Practical Significance](https://apcentral.collegeboard.org/courses/ap-statistics/classroom-resources/why-variances-add-and-why-it-matters)

The Variance Sum Law is used to forecast a specific situations composed by several different components.

[Variance and Standard Deviations](https://www.mathsisfun.com/data/standard-deviation.html)


## Pearson Correlation Measures

The Pearson product-moment correlation coefficient is a measure of the strength  of the <u>linear relationship</u> between two variables.

## Spearmans Correlation

<u>Spearman rank correlation</u>: Spearman rank correlation is a non-parametric test that is used to measure the degree of association between two variables.  The Spearman rank correlation test does not carry any assumptions about the distribution of the data and is the appropriate correlation analysis when the variables are measured on a scale that is at least ordinal.

## Kendall Correlation

Kendall rank correlation: Kendall rank correlation is a non-parametric test that measures the strength of dependence between two variables.  