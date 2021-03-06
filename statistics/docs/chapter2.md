---
title: Descriptive Statistics and General Probability
layout: default
---

# II. Descriptive Statistics and General Probability

[Home]({{ site.baseurl }}{% link index.md %}) <br/>
[Section Home]({{ site.baseurl }}{% link statistics/index.md %})

## Statistical Methods
__Descriptive statistics__
: describe key features of a data set.
	
__Inferential statistics__
: draw conclusions about the population based on sample data.

	Where a population refers to an ideal or theoretical group
	that would be too costly to adequately measure.
	
__Statistic__
: a descriptive measure computed from the data of a sample.

__Parameter__
: a descriptive measure computed form the data of a population.

|Measurement | Population Parameter | Sample Statistic |
| :---: | :---: | :---: |
|mean | $$\mu$$ | $$\bar{x}$$ |
|proportion | p | $$\hat{p}$$ |
|variance | $$\sigma^{2}$$ | $$s^2$$ |
|correlation coefficient | $$\rho$$ | r |
{: rules="groups"}

## Sampling Methods and Techniques
__Random Sample__
: a sample of *n* measurements selected from <br/>
a population is random if every different sample of size <br/>
*n* has an equal probability of being selected.

__Simple Random Sampling__
: each individual within a sample is chosen at <br/>
random and each member of the population has an equal probability <br/>
of being included in the sample.

__Systematic Sampling__
: selection of elements from an ordered sampling frame. <br/>
The selection starts by taking an element at random followed by <br/> 
every $$k^{th}$$ element, where:<br/>
$$ K = (\frac{N}{n})$$

__Stratified Sampling__
: There may often be factors that divide of partition the <br/> 
population into subpopulations (i.e. groups/strata), and we may reasonably <br/>
expect the measurement of interest to vary among them. The strata must therefore <br/>
be disjoint in order to reduce sampling variability.

## Measurents of Central Tendency
	
__mean__
: the average of *n* values of data. <br/>
$$\bar{x} = \frac{1}{n}\left (\sum_{i=1}^n{x_i}\right ) = \frac{x_1+x_2+\cdots +x_n}{n}$$

__median__
: the central value of an ordered dataset, more robust than the mean to outliers.

__mode__
: the most frequent data entry in a set. Can have no more, unimodal or bimodal.

## Measures of Spread / Variation

__MAD__
: median absolute deviation
$$ MAD = median_i( | X_i - median_j(x_j) | ) $$

__SSE__
: sum of squared errors
$$ \sum_{i=1}^n{x_i}(x_i - \bar{x}^2)$$

__Standard deviation__
: $$ s = \sqrt{\frac{\sum_{i=1}^N (x_i - \bar{x})^2}{N-1} } $$

__Variance__ 
: $$ s^2 $$

__Coefficient of Variation__
: $$ CV = \frac{s}{\bar{x}}*100% $$

__Range__
: Gives the minimum value and maximum value for a dataset to show the boundaries.

__IQR__
: Interquartile Range, the third quartile minus the first quartile 
$$ IQR = (Q_3 - Q_1) $$.

__Outliers__
: any datapoint that lies more that ( 1.5 * IQR ) lower or higher than the first or third quartiles

## Basic Probability Concepts

Probability of event A, __P(A)__, describes the uncertainty that event A occurs, and is given by values that range from 0 to 1, inclusive.

$$ P(A) = \frac{n_a}{n_s} = \frac{\text{# Of Ways Event A Can Occur}}{\text{# Of Ways An Experiment May Proceed}} $$

Relative frequency concept of probability

$$ P(A) = \lim_{x \to \infty}\frac{n_a}{n} \approx \frac{n_a}{n} = \frac{\text{# Of Times Event A Occured}}{\text{# Of Times An Experiment Was Run}} $$

*Alternatively, subjective probabilities are based on personal opinion*


## Sample Space and Events

__Sample space__
: a sample space for an experiment is a set *S* that contains all possible outcomes. Each experimental outcome corresponds exactly once to an element of *S*, ccalled a __sample point__.

__Event__
: Any subset, *A*, of a sample space is an event. The empty set $$ \emptyset $$ is the impossible event and the subset of *S* is the certain event.


$$ P(A\cup B) = \text{ The union of A with B. Outcomes favorable to A OR B.} $$

$$ P(A\cap B) = \text{ The intersection of A with B. Outcomes favorable to A AND B.} $$

__Mutually Exclusive Events__
: two events are mutually exclusive if, and only if, the intersection of the two events is the empty set.

: this tells us that if two events are mutually exclusive, the occurence of one precludes the other event.

$$ P(A\cap B) = \emptyset $$

$$ P(A\cup B) = P(A) + P(B) $$

## Conditional Probability

The probability of A given the occurence of B. 

$$ P(A \mid B )= \frac{P(A \cap B)}{P(B)}  , P(B) \neq 0 $$

## Independence

It is possible that the occurence of event B has no effect on the occurence of event A. (i.e. the conditional probability $$ P(A \mid B ) = P(A) $$ ). 
This is true if, and only if, 

$$ P(A\cap B) = P(A) \times P(B) $$

*Note: independence is a distinct concept from mutual exclusivity.*


## Joint and Marginal Probability

__Joint probability__
: $$ P(A \cap B ) = P(A \mid B) \times P(B) $$

__Marginal probability__
: $$ P(A) = \sum_B P(A \cap B) = [ \, \sum_B P(A \mid B) \times P(B) ] \, $$

__Bayes' Theorem__
: The posterior probability, or the probability of event *A* given event *B*, is equal to the joint probability of *B* AND *A* divided by the marginal probability of event *A*.

$$ P(A \mid B) = \frac{P(B \mid A) \times P(A)}{[ \, \sum_B P(A \mid B) \times P(B) ]}$$


## Terminology in diagnostic tests

__Specificity__
: The probability of a negative test result among patients without the disease.

$$ specificity = \frac{\text{true negatives}}{\text{(true negatives + false positives)}} $$

$$ specificity = \frac{\text{TN}}{\text{(TN + FP)}} $$

__Sensitivity__
: The probability of a positive test result among patients with the disease.

$$ sensitivity = \frac{\text{true positives}}{\text{(true positives + false negatives)}} $$

$$ sensitivity = \frac{\text{TP}}{\text{(TP + FN)}} $$

__Prevalence__
: The ratio of disease occurences to the total samples or population.

$$ prevalance = \frac{\text{Diseased}}{\text{(Diseased + Healthy)}} $$

$$ prevalance = \frac{\text{D}}{\text{(D + H)}} $$

__Accuracy__
: The ratio of true test results to the total samples or population.

$$ accuracy = \frac{\text{(true positives + true negatives)}}{\text{(Diseased + Healthy)}} $$

$$ accuracy = \frac{\text{(TP + TN)}}{\text{(D + H)}} $$

__Positive Predictive Value__
: (PPD) The ratio of true positives to all positive test results.

$$ PPD = \frac{\text{true positives}}{\text{(true positives + false positives)}} $$

$$ PPD = \frac{\text{TP}}{\text{(TP + FP)}} $$

__Negative Predictive Value__
: (NPD) The ratio of true negatives to all negative test results.

$$ NPD = \frac{\text{true negatives}}{\text{(true negatives + false negatives)}} $$

$$ NPD = \frac{\text{TN}}{\text{(TN + FN)}} $$

|Test Result | Disease (D) | Healthy (H) |
| :---: | :---: | :---: |
|Diseased (+) | TP | FP |
|Healthy (-) | FN | TN |
{: rules="groups"}




