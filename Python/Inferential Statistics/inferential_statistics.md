[Seeing Theory](https://seeing-theory.brown.edu/)

Summary -

First, you were introduced to two main counting principles through which you can calculate the probability for the outcomes that you are interested in. These counting principles are as follows:

- Permutations: A permutation is a way of arranging a selected group of objects in such a way that the order is of significance. For example, arranging some letters to form different words, arranging the top order batsmen of a team, or finding all the ways in which a group of friends can be seated in a cinema hall – all these methods use permutations. When there are 'n' objects to be arranged among 'r' spaces, the permutation value is given by the following formula:
                                                             
              nPr = n!/(n−r)!
                                                            
- Combinations: When you just have to choose some objects from a larger set and the order is of no significance, then the rule of counting that you use is called combination. For example, if you need to find the number of ways to choose three vowels from the given list of give, or choose four bowlers from the given roster of seven – all these methods use combinations. If you want to choose 'r' objects from a larger set of 'n' objects, then the number of ways in which you can do that is given by the following formula:

              nCr=n!/r!(n−r)!

Next, you learnt about some specific terms related to probability – events, sample space and experiments. You also learnt some basic rules of probability such as follows:
- Probability values always lie between 0 and 1.
- Probability values for all outcomes of an experiment always add up to 1.

Then, you learnt about specific types of events that can be encountered while computing probabilities of more than two events. They are as follows:
- Independent events: If you have two or more events and the occurrence of one event has no bearing whatsoever on the occurrence/s of the other event/s, then all the events are said to be independent of each other.
- Disjoint or mutually exclusive events: Now, two or more events are mutually exclusive when they do not occur at the same time, i.e., when one event occurs, the rest of the events do not occur.

You also learnt about the idea of complement A' for any event A and the probability rule for them, i.e., P(A) + P(A') =1.

Next, you were introduced to two main rules of probability that help you in finding the probabilities of two or more events. They are as follows:

- Addition rule: When you have the individual probabilities of two events A and B, denoted by P(A) and P(B), the addition rule states that the probability of the event that either A or B will occur is given as 
  P(A∪B) = P(A) + P(B) - P(A∩B),
         Where, P(A∪B) denotes the probability that either event A or B occurs. 
          P(A) denotes the probability that only event A occurs.
          P(B) denotes the probability that only event B occurs.
          P(A∩B) denotes the probability that both events A and B occur simultaneously.

- Multiplication rule: When an event A is not dependent on event B and vice versa, they are known as independent events. The multiplication rule allows us to compute the probabilities of both of them occurring simultaneously, which is given as:
  P(A and B) = P(A)* P(B)
Now, this rule can be extended to multiple independent events where all you need to do is multiply the respective probabilities of all the events to get the final probability of all them occurring simultaneously. For example, if you have four independent events A, B, C and D, then:
                                     P(A and B and C and D) = P(A)* P(B)* P(C)* P(D)
                                     
Finally, you also saw a comparison between the addition rule and the multiplication rule that would help you to decide which formula to use in a given scenario. If the question mentions an 'OR' to denote the relationship between the events, then you need to apply the addition rule. That is, either of the given events can occur at that time, P(Event A or Event B). Else, if an 'AND' is used to denote the relationship between the events, then the multiplication rule is used. Here, the events need to happen simultaneously and must be independent, P(Event A and Event B).

Expected Value
The expected value (EV) for X was calculated using the following formula:

    EV (X) = x_{1}*P(X=x_{1})+x_{2}*P(X=x_{2})+....................+x_{n}*P(X=x_{n})

Another way of writing this is as follows:

     EV(X) = sum{i=1}^{i=n}x{i}*P(X=x{i})

Discrete Probability Distribution - 

Binomial Distribution - It can be used to find the probability of any kind of event, if that event is a series of yes or no questions, with the probability of yes being the same for all questions. Formula -

     P(X=r)= nCr(p)r(1−p)n−r

Phrasing the conditions more formally, the binomial distribution can be used if, for an experiment:
- The total number of trials is fixed.
- Each trial is binary, i.e., it has only two possible outcomes: success or failure.
- The probability of success is the same for all the trials.

Continuous Probability Distribution - 

Continuous random variable is the probability of getting an exact value is very low, almost zero. Hence, when talking about the probability of continuous random variables, you can only talk in terms of intervals. For example, for a particular company, the probability of an employee’s commute time being exactly equal to 35 minutes was zero, but the probability of an employee having a commute time between 35 and 40 minutes was 0.2.

Hence, for continuous random variables, probability density functions (PDFs) and cumulative distribution functions (CDFs) are used instead of the bar chart type of distribution used for the probability of discrete random variables. These functions are preferred because they talk about probability in terms of intervals.

Then, major difference between a PDF and a CDF is that in a CDF, you can find the cumulative probability directly by checking the value at x. However, for a PDF, we need to find the area under the curve between the lowest value and x to find the cumulative probability. PDFs are still more commonly used, mainly because it is very easy to see patterns in them.

Normal distribution is symmetric, and its mean, median and mode lie at the centre.
Below is the 1-2-3 rule, which states that there is a:

- 68% probability of the variable lying within 1 standard deviation of the mean,
- 95% probability of the variable lying within 2 standard deviations of the mean, and
- 99.7% probability of the variable lying within 3 standard deviations of the mean.

Then, you learnt that to find the probability, you do not need to know the value of the mean or the standard deviation; just knowing the number of standard deviations away from the mean your random variable is suffices. That is given by:
         
       Z=(X−μ)/σ

This is called the Z score, or the standard normal variable.

the cumulative probability for Z =1.5 can be found using Excel by typing:

       = NORM.S.DIST(1.5, TRUE)

Also, we can find the probability without standardising. The syntax for that is:

       = NORM.DIST(x, mean, standard_dev, TRUE)

Central Limit Theorem

- Instead of finding the mean and standard deviation for the entire population, it is sometimes beneficial to find the mean and standard deviation for only a small representative sample. You may have to do this because of time and/or money constraints.
- For example, for an office of 30,000 employees, we wanted to find the average commute time. So, instead of asking all employees, we asked only 100 of them and collected the data. We found the mean to be 36.6 minutes and the standard deviation to be 10 minutes.
- However, it would not be fair to infer that the population mean is exactly equal to the sample mean. This is because the flaws of the sampling process must have led to some error. Hence, the sample mean’s value has to be reported with some margin of error.
- For example, the mean commute time for the office of 30,000 employees would be equal to 36.6 + 3 minutes, 36.6 + 1 minutes, or 36.6 + 10 minutes, i.e., 36.6  minutes + some margin of error.
- However, at this point in time, you do not exactly know how to find what this margin of error is.
- Then, we moved on to sampling distributions, some of the properties of which would help you find this margin of error.
- A sampling distribution, which is essentially the distribution of the sample means of a population, has some interesting properties, which are collectively called the central limit theorem. It states that no matter how the original population is distributed, the sampling distribution will follow these three properties:
  - Sampling distribution’s mean (mu_{\bar{X}}) = Population mean (\mu),
  - Sampling distribution’s standard deviation (Standard error) = \frac{\sigma}{\sqrt{n}}, where \sigma is the population’s standard deviation and n is the sample size
  - For n > 30, the sampling distribution becomes a normal distribution.
- We can use your knowledge of the CLT to infer the population mean from the sample mean.
- We estimated the mean commute time of 30,000 employees of an office by taking a sample of 100 employees, finding their mean commute time. Specifically, you were given a sample with a sample mean (X bar) = 36.6 minutes and a sample standard deviation S = 10 minutes.
- Then, learnt the following terminology related to the claim:
  - The probability associated with the claim is called the confidence level. (Here, it is 95.4%.)
  - The maximum error made in a sample mean is called the margin of error. (Here, it is 2 minutes.)
  - The final interval of values is called the confidence interval. [Here, it is the range (34.6, 38.6).]
- Let’s say you have a sample with a sample size n, mean \\bar{X} and standard deviation S. You learnt that a y% confidence interval (i.e., a confidence interval corresponding to a y% confidence level) for \\mu will be given by the range:

      Confidence interval = (\\bar{X}-\\frac{Z^{*}S}{\\sqrt{n}}, \\bar{X}+\\frac{Z^{*}S}{\\sqrt{n}}),

Where, Z* is the Z-score associated with a y% confidence level.
