# Modern Statistics with Python
This repository contains my learned reference to applying modern statistical methods through python. It contains the following modules: <br>
**ms_ch1 = Descriptive Statistics and Analyzing variability** <br>
**ms_ch2 = Probability Models and Distributions [Theory-oriented]<br>**

Beyond that, my self made notes on further understanding of advanced statistical methods is given below behttps://docs.google.com/document/d/1dtnvNcdeTeGxM9bdSZMH4E_l80Mw17SI4r8WyPhrHjw/edit?usp=sharing

## Part-1:Statistical Methods
### hey


**NOTES FROM ADVANCED STATISTICAL ANALYSIS BY OPTMZE (ayush.devmail@gmail.com)**

**PART-I: STATISTICAL METHODS**

**(I) Introduction to Statistics**

- The idea behind statistical analysis is to analyze the data recorded from a data-generating process (Nature) and then utilize the same to gain more knowledge and make predictions on the basis of data generated(DATA). To accomplish the same we build models; NO MODEL IS FULLY CORRECT, the aim is to find which one is more accurate than the others

- Always remember it is the model that produces the data and not the other way around. For example: A coin toss is assumed to have 50% chance for head or tail, but if you toss the coin 10 times and only get 4 heads, then it does not mean the model has changed. This data is not what produces the model, the model is what has produced this data.

- Analysis needs data, data can be collected via different means like experiments, surveys and these do affect the result interpretation. Research can be divided into:

1) **Confirmatory Research:** You ask the question like “Does X affect Y” beforehand and collect data accordingly (**primary data**)
1) **Exploratory Research**: We have data beforehand which we analyze and then pose the question on the basis of available data (**secondary data**)


- Primary data conclusions are more reliable but time-consuming and costly. Secondary data may be less reliable but are more readily available (less expensive)

- **Models:**

A model explains how Nature works and makes predictions about it. The model we make for nature is that the data comes from a probability model **p(y).** If DATA\* is similar to DATA, then it’s a good model

1) **Deterministic Model** Y = f(x) : Outcome Y is decided entirely by x, for an x we have only a single outcome Y (perfect predictability). It doesn’t account for variability in the real world.

1) **Probabilistic Model** Y ~ f(x) : Also known as Stochastic Model. Not exactly a correct model but is more realistic than the deterministic model.



`             `In the real world if you want to travel 200 km at 50 kmph it will not take exactly 4 hours most 

`             `Times. Thus a deterministic model is not suitable or correct here.

`            `But that doesn’t mean that deterministic model is not useful, it is useful in sciences where it may 

`            `not give an exact value but gives a very good estimate(eg: the weight a bridge can support) . It 

`            `isn’t as useful in social sciences(what’s going to happen tomorrow?), biology/medical sciences.



- Probabilistic models assign likelihoods to the outcomes, while a deterministic model gives the

outcome with 100% certainty. What exactly does it mean?

Eg: If somebody has cancer and has the choices:

(a) Treatment-A: 95% survival chance

(b) Treatment-B: 80% survival chance

It means that in all hypothetical world, in 95% of them you would survive with treatment A and 

similarly goes for treatment B. The difference is that there is not a 100% certainty, at the end the

choice is to be made and both outcomes are possible no matter what treatment is chosen.

- **Parameters:**

Both models have parameters that govern their performance. Always remember that:

(i) Model gives DATA

(ii) A model has unknown parameters

(iii) DATA reduces uncertainty about the unknown parameters. Remember “reduces” not “eliminates”.

For example in y = round{(1+p)x}; p :  a parameter. 

`            `Θ is the notation used for a generic parameter, there may be more than 1 parameter in 

`             `Θ (a parameter vector)

`            `With statistical analysis the goal is to estimate the parameters that makes the curve ( data 

`            `reduces uncertainty of unknown parameter)

- **Purely Probabilistic Statistical Model**

`                                                                  `**Y ~ p(y)**

A pdf (**probability distribution function**) assigns likelihoods to the different values of Y.

If p(y1) is large then more values of Y are near y1 and the opposite for small values. In the above example y = 3.1 has a higher probability so more values can be seen near that mark.

Probabilistic models only allow you to make what-if predictions in aggregate

- A model with both probabilistic and deterministic components = “Regression Model” (how distribution of Y changes for different x values):

`                                                               `**Y | X = x ~ p(y|x,Θ)**

“ given X=x, Y is produced by a pdf that depends on x and unknown parameters”

Note: | is read as “given that”

For example we see that the one with both components is dependent on the value of x, here x = 20 and x = 40.



<table><tr><th colspan="2" valign="top"><b>PROBABILISTIC DISTRIBUTION</b></th><th colspan="3" valign="top"><b>BOTH COMPONENTS</b></th></tr>
<tr><td valign="top">y</td><td valign="top">p(y)</td><td valign="top">y</td><td valign="top">p(y|x=20)</td><td valign="top">p(y|x=40)</td></tr>
<tr><td rowspan="3" valign="top">Red</td><td rowspan="3" valign="top">0\.50</td><td rowspan="3" valign="top">Red</td><td rowspan="3" valign="top">0\.20</td><td rowspan="3" valign="top">0\.50</td></tr>
<tr></tr>
<tr></tr>
<tr><td valign="top">Gray</td><td valign="top">0\.20</td><td valign="top">Gray</td><td valign="top">0\.40</td><td valign="top">0\.20</td></tr>
<tr><td valign="top">Green</td><td valign="top">0\.30</td><td valign="top">Green</td><td valign="top">0\.40</td><td valign="top">0\.30</td></tr>
<tr><td valign="top">Total</td><td valign="top">1\.00</td><td valign="top">Total</td><td valign="top">1\.00</td><td valign="top">1\.00</td></tr>
</table>














NOTE: The model with both probabilistic and deterministic is mother of all models, the two components are  just a specific case.

- **Statistical Inference**

Say we have a bent coin, what is the probability like? We have to assume an unknown parameter ‘m’ so using the bernouilli’s distribution we have the following

Tails: 1 - m

Heads: m

This can be generalized to more parameters via a parameter vector  Θ = (m1,m2,m3). The parameters m1,m2,m3 are unknown parameters whose uncertainty can be reduced by statistical inference on the DATA records collected.

- **A model is considered to be good if:**
**
`             `(i) Model set of  all possible outcomes matches nature’s set of possible outcomes

`             `Eg: For a coin, the outcomes = {H,T} so our bernoulli’s distribution is good as it has two  

`             `possible outcomes too

(ii) Frequency of occurrence and successive combo of outcomes matches that with nature

`  `(0,0,1,0,1,1)

`             `Eg of a bad model is say: if odd = heads, else even = tails. This means randomly generating the

`             `data would produce ..H,T,H,T.. But this does not include the possibility of something like ..H H ..

`             `Hence the domains don’t match!

`            `**YOU DON’T NEED TO KNOW A MODEL’S PARAMETERS VALUE TO KNOW IT’S A GOOD** 

`            `**MODEL**

- **What do we do with a model?** 

Well we run simulations to produce DATA\*, we can use to this compare optimal trading strategies, coin tosses , predicting election results etc.

- **CLASSES OF MEASUREMENT:**

Broadly we have:

1. Nominal = labels/non-numeric; eg: color, job title etc
1. Ordinal = intermediate between nominal and continuous; intrinsic order; eg: no of siblings 
1. Continuous = numeric/values lie in a continuous range; eg: wait-time = 0 to 60 minutes













`        `**Nominal, Ordinal =** Discrete Data, things like coin flips = {0,1}, discrete number of values

`        `**Ratio, Interval =** Continuous Data ; might have values like 8.3,8.4 etc.












- Analysis always discrete at some level, but we still need models that produce continuous data for example: usually avg computed are nearly continuous (central limit theorem). Continuous data can be made discrete by rounding them off. Continuous models are simpler, give better results than complex models even when they are wrong.

- **WHEN TO USE A CONTINUOUS MODEL OVER A DISCRETE MODEL?**

Context matters! More the discrete data fills the continuum in between the better the continuous model is.

**UGLY RULE OF THUMB**:” if the set of discrete outcomes is 10+, continuous may be adequate.”


**(II) Random Variables and Their Probability Distributions**

A random variable is a variable which represents the outcome of a trial, an experiment or event. It is different each time the trial is repeated.

**Types of Discrete Probability Distributions:**




















- If an RV is discrete use a discrete pdf for your model, meaning all potential values can be listed.

- Another distribution that was missed out above is the Bernoulli Distribution, which deals with probability of success/failure from a Bernoulli trial (an experiment with only two outcomes). It is basically n=1 for a Binomial distribution. Also Binomial distribution is with replacement.













- For multiple outcomes (more than 2 ) we have a “Multinomial Discrete Distribution”:










- **Continuous Probability Distributions**

**        












**          



**           To model the continuous value between discrete values we have the area under the function.

`              `When working with continuous probability distributions we make statements like “the probability 

`              `Between the range 85.5 - 86.5 is 0.0013”.

`              `For example:






















`             `Here +/- delta/2 = 0.005 -> delta = 0.001

`             `**Note:** There is zero probability that a continuous R.V Y equals to a specific value, as to get a 

`                        `specific value we need to make delta decreases the probability also decrease and goes

`                         `to zero








- **Probability of an outcome using the population definition:**

`             `If a person is randomly sampled from 1000 people, where 4 whose weights are between 79.5 and 

`             `80.5 then probability using the above = 0.004. This is true but not useful as the universe is not 

`             `defined by these 1000 people.







- **Note:** The Normal distribution / bellcurve, which in practice is never correct as there is always a skewness in DATA. But it is often a convenient and simple approximation to give answers that are good enough














This is a normal distribution with parameters u = 74.0 and sd = 18.7, though it’s apparent it’s not a good fit as it predicts the likeliness of someone who weighs 40 kg less than center is the same as 40 kg more. In view of physiology this doesn’t make sense where we expect someone with that less weight would probably be dead, but more than 40kg ones are possible more, thus it is a right skew distribution (expectation that weight distribution is larger on the right side)














The constant is there so the area under the pdf is 1.0. The area under g(y) gives 2\*pi\*sigma so we multiply 1/constant to cancel it out to 1. g(y) is called the kernel of the function.



- Statistics is about approximations, but always ask how good the approximation is as you can approximate an apple to the moon but it wouldn’t be a very good approximation. The relative scale matters when we approximate.

- **Note on derivatives and integrals:**

A derivative graphically is the slope of the tangent to a point on the curve. Now we know that a slope is basically = y2 - y1/ x2 - x1. But with a derivative it’s simply f’(x0) for a function f(x) at point x = x0. How is it that we needed 2 parameters for the normal slope formula, but here we are using only one point as the parameter to find the slope? The answer lies in approximations and limits! The derivative at a point is basically:





We can see that we are bringing x1 closer to x2 and thus y2 also gets close to y1

**Application: Obtaining sample mean using calculus of least squares**

Say a data set = [3.2,5.6,1.0,1.5], what value of x is closest to all these values?

We use least squares criterion: x is close if sum of squared deviation is small, so we want minimum of  


This is called the least squares estimate, we basically find the minima of this functions to find minimum x which would also be incidentally the mean.











- **Cumulative Distribution Functions**

The cdf is function P(y) which gives probability that say for example person’s weight is less than or equal to y. The cdf unlike the pdf always gives probability.\













RELATION BETWEEN P(y) AND p(y) FOR A CONTINUOUS p(y) IS:

`  `Derivative of cdf is equal to the pdf

` `In general:





HOW? : Well the area under the pdf p(y) b/w  say 70 and 80 is the probability of y to be in between that range. The cdf probability for upto 80 -  cdf probability upto 70 is the same as the probability for it to be between 70-80.

Example: A triangular distribution with say: p(y) = 0.0002y for 0<=y<=100 and 0 otherwise

`                `What proportion of grades will be between 70 and 90?







Note: In case of infinite case we basically replace the infinity by a large a number and see if the function converges to a value, for example here  below it converges to zero 





- How the graphs look: The bar type graphs show that they are discrete distributions
















**(III) Probability Calculation and Simulation**

- Real systems are complex: for example a call center operation, many more factors affect the waiting time. Method of simulation (DATA\*) is used to analyze complex systems.

- Analytic calculation is still the gold standard for precise answers but simulation gives us a good approximation. Example of analytic calculation:











- Two common methods of analyzing data:

**(i) Bootstrapping**

**(ii) Markov Chain Monte Carlo**

- **Method of Simulation:**







Flip the coins 1000 times (NSIM),  to count how many times it turns up heads; A = {heads} and divide the number of heads by 1000. The estimates can be made better by choosing a larger NSIM.

- **Generating Random Numbers:**

A lot of random number functions for named distributions are available in libraries. But if you don’t find one for a distribution you can use the **“inverse cdf method”**

**The inverse of a cumulative distribution function is called a quantile function.**

(remember an inverse is: y = f(x) and x = f-1(y) )

In this method we use uniform distribution to make all values between 0 and 1 equally likely. The pdf of the uniform distribution is p(y) = 1 for 0 < y < 1 here. It is referred to as the mother of all distributions, as all distributions whether discrete or continuous can be constructed from the U(0,1) pdf.

To find the inverse cdf: set p = P(y) and solve for y = P-1(p) ; here P-1(p) is the inverse cdf function or the quantile function, so we have:


For example:

p(y) = 0.002y for 0<=y<=100 then:

Now to find inverse of P(y):

We can generate a sample now using this as:


For example for a randomly generated u\* = 0.731 we would have y\* = (10000\*0.731)^½ = 85.5

Since it’s a uniform distribution , the u\* = 0.731 ensures that the value produced would be so that 73.1% are less than 85.5. Thus the method gives you data appears in correct frequencies

**For the discrete case:**

You would have to recode U\* values as the discrete values so the probabilities are right, for example:






**(IV) Identifying Distributions**

- The question arises as to what distribution to use? Well obviously the one which produces DATA\* similar to DATA. But this is not a trivial task and remember there are usually no right answers. A pdf p(y) is unknown as it consists of unknown parameters, but recall that data reduces uncertainty about the unknown parameters, thus you can identify models that are reasonable and which aren’t.

- Even before collecting data, we may have an idea about what model might be appropriate (discrete/continuous, range of values, symmetry/asymmetry,knowledge of historical data). We can list down possible distributions.

- Many cases, it is not important for distribution p(y) to be a named form like uniform etc. If we don’t assume such a form it’s called **nonparametric models.** Remember all models are wrong but some are useful (George Box)

- **Identifying Distribution from Theory Alone:**

Example: if you need to count insects caught in traps and say 50% of your traps produce no insects, and the remainder produces a range from 1 to 500, with many over 100. 

Sample space S = {0,1,2,....}, sample space is similar to the Poisson model. But poisson model is not good because percentage of zeroes in your DATA\* will be too small if lambda is large.


- **Generic Distribution:** It is flexible with no constraints. Basically you don’t have to specify the form, you can just say that the distribution is Y ~ p(y). But we can’t always use them as identifying a distribution gives a more complete story and we can make better predictions and apply specific optimal statistical procedures.For example in physics, the motion of particles is better modeled in terms of normal distributions. On the flipside, sometimes better answers are found without identifying the form.

- **Using Data, estimating distributions via the histogram:**

Data reduces the uncertainty about the unknown parameters,again don’t think the data will answer which distribution produced the data. Many plausible candidates for a p(y) and you won’t be able to tell which one is right and which ones are wrong. For example if we have the following data:

y1 = 0.3, y2 = 2.3, y3 = 1.0, y4 = 0.1, y5 = 3.9, y6 = 0.8












`                         `**Possible distributions                                                      Impossible distribution**

`        `The impossible ones are impossible as you have near zero probability for them. It is clear that 

`        `you can use the data to rule out many distributions but can’t be used to rule in any of them. ( though 

`        `theoretically it is possible that those data could have been produced by those models/ explainable by

`        `chance alone, but likelihood is so small we discount these cases)

`        `Several ways to estimate distributions, one way is using a histogram ; it can’t tell any named 

`        `distribution but helps identifying generic properties: symmetry, skewness and bimodality. For 

`        `example of the above. The below equation states that the rectangular approximation to the 

`        `distribution is given:










**         Here p(yi) is probability within the +/- delta/2 of yi (the midpoint of the interval). Delta is

`         `basically the interval width. So for our example:

`         `~p(y) = estimated pdf p(y);

`           `p(yi) = estimated probability

`         `so here for example between 0.0 and 0.5 we have 2 values so 2/6 and then you divide by interval 

`         `length = 2/6/0.5 = 0.667












- You want two things: **more data records** and **narrower intervals** , but for narrower intervals if   your   sample size is too small then way to little in between them and some may have the incorrect estimate of 0.0 probability. **Interval size depends on the sample size**, larger sample size means more narrower intervals

- **How many intervals should we pick?** 

Ugly rule of thumb:  **If n is your sample size, pick n^½ intervals**


- If we had 1000 call times, the resulting graph may look something like this
















`                                       `**A                                                                                        B**

- **Now we note two things here: Figure A has a wait time in the negative too which is not correct,  that’s why we don't accept software defaults blindly,** we have to make adjustments so the software presents the data accurately, tell software to take 0 as a lower endpoint. **The second thing is that in the y axis we have a percentage and not an estimated pdf, the area under them won’t be equal to 1. T**o make the estimated pdf we have to divide by interval width, but this won’t change the shape and location. The histograms suggest the shape and location even if values on y axis (which is basically the estimated probabilities) are not on the pdf scale (they just differ by a constant of proportionality 1/delta)

- A histogram is a non parametric tool, it estimates generic p(y) without making any assumption about the form of distribution. If the named distribution and the histogram have very similar appearance you can be more confident in using that.

- **How large is large enough?** 

Ugly rule of thumb: **if sample size n>=30 then histogram is an adequate estimate of p(y)**

Larger n = Better accuracy

- What to look for:

Range of observed values, approximate center of the distribution, indication of symmetry/asymmetry or bimodality(two peaks), to assess if normal distribution is good enough we look for rough symmetry and somewhat of a bell shape, the sample size

NOTE: You can never conclude data is normally distributed or is not normally distributed, both these sentences are meaningless. As data can never be normally distributed or any continuous distribution because they are discrete value even if measured to a lot of decimals.

The question whether it’s normal or any distribution is a question about the process that produces the data and not the data set.

- Look at this plot below:





















`      `**Quantiles: Theoretical and Data-based Estimates**

- Histograms are a good tool for looking at data; should use it whenever you analyze data. But they are not good for looking at tail behavior.  For example in the above distribution it may look like that the normal distribution might be a good approximation, but it’s not and we are unable to see that in the histogram.

- Tail behavior is often the most important aspect of the distribution; Nassim Nicholas Taleb calls them black swans, as they have the largest impact on the financial markets and society.

- To look at tail behavior we should use **q-q plots (quantile-quantile plot.**

**> Quantile:*** If P(y\_p) = p, then y\_p is the p quantile of the distribution of p(y). Basically if portion p out of the data produced by p(y) is less than or equal to y\_p then y\_p is called the pth quantile of the distribution. Note P(y) refers to cdf while p(y) is the probability density function

**> Percentile:** If (100\*p)% of data produced by p(y) is less than or equal to y\_p, then y\_p is called   the pth quantile of the distribution. For example if your score of 250 was given 80th percentile then y\_0.8 = 100

- The 50th percentile is called the median Similarly we have quartiles, quintiles and deciles. Any continuous distribution, the p quantile is basically:

- Now for example in our triangular distribution: p(y) = 0.0002y, the cdf is p = P(y) = 0.0001y^(2)

The inverse cdf gives us: y\_p = (10,000p)^(½). The median is basically:

- But in discrete cases there is often no y so that P(y) = p. For example in a Poisson distribution with lambda = 0.5, what is the 0.75 quantile? You can find P(0) = 0.6065 and P(1) = 0.9098, but no value for which P(y) = 0.75. This can occur when estimating quantiles using data. Another example is:


Data: y1=0.3,y2=2.3,y3=1.0,y4=0.1,y5=3.9,y6=0.8

What is the median > for any number between 0.8 and 1 half of the values are lower and half are more. So what value do we choose? Your software decides how it handles these cases. For the median you take the average: (0.8 + 1)/2 = 0.9 as estimated median (though is not the best estimate).

Another ambiguity is how we see the smallest data value, for example here is y4 = 0.1 basically 1/6th quantile? The largest data y = 3.9 is 6/6 of the quantile? There’s no way that 3.9 is the largest in the data set.

- **How to deal with the ambiguities?**

One way is defining order statistics using y(i). For the above example we have:

y(1) = 0.1    y(3) = 0.8   y(5) = 2.3

y(2) = 0.3    y(4) = 1.0   y(6) = 3.9

A common assignment of quantile estimates is then: 






`      `**NOTE ON ORDER STATISTICS**

`     `order statistics = characteristics values sorted from smallest to largest.

`     `[2385,2400,2285,2765,2410,2360,2750,2200,2500,2550] = [X\_1,X\_2 ... X\_n] here n = 10

`     `You first sort the sample, then:

`     `1) X\_i = ith order statistic

`     `2) X\_i.5 = (Xi + X(i+1)) / 2 = mean

`     `3) X\_1 = sample minimum

`     `4) X\_n = sample maximum

`     `5) X\_n - X1 = sample range

`     `6) M\_e = Xm where m = (n+1)/2 middle value in ordered sample or median ; if n = 10 then:

`     `m = (10 + 1) / 2 = 5.5 so:

`     `M\_e = X\_5.5 = (X5 + X6) / 2

`     `A median tells us the about the center of dispersion of sample values

`     `7) Q1 = X\_q1 , Q3 = X\_q3 = sample quartiles where:

`     `q1 = (n+1)/4

`     `q3 = 3(n+1)/4

`     `Where Q1 = lower quartile and Q3 = upper quartile. They divide the sample such that:

`       `(i) 1/4th values is smaller than Q1

`       `(ii) 1/2 are between Q1 and Q3

`       `(iii) 1/4 are greater than Q3

`     `For example: q1 = 11/4 for n = 10 -> 2.75


Similarly we did for X\_5.5, another way to find the value is: 

Some definitions:

Sample median, quartiles -> sample quantiles

pth sample quantile -> number that exceeds exactly 100p% of sample values For example: median is the 0.5 sample quantile


Remember that i-0.5/n is an estimate, so it is obviously wrong in the sense that is not equal to the true value. The -0.5 helps us make sure that ambiguities like the largest value becoming the 1 quantile etc does not occur.




**NOTE ON QUANTILE PLOTS**

It is a plot of the sample quantiles xp against p, where 0 < p < 1 where:


It helps us obtain a graphical estimate of the quantiles in the distribution. If the data values falls along a roughly straight line at 45 degree angle, then data is normally distributed

General QQ plot A method to compare two probability distributions by plotting their quantiles, a point (x,y) is ; quantile of one distribution plotted against the same quantile of the other














The Normal QQ plot is thus basically:

Data values are ordered and cumulative distribution values are calculated as (i-0.5)/n for the ith ordered value out of n total values (basically proportion of data below a certain value)

Basically here we have the cumulative distribution, data set as a standard normal distribution with mean = 0 and sd = 1




- **Comparing distributions using the quantile-quantile plot**
**
`           `The                       is a non parametric estimate, it does not assume anything about the

`             `distribution. You can assume a form of a distribution, for example if you think it’s a normal

`             `Distribution, you estimate the parameter u and sigma as             then you can estimate the p 

`             `quantile                      The q-q plot is basically 



`             `If assumed distribution is the true distribution then we get a straight line, if different then we get a 

`             `curvature. For example:

Example-A: Normality of stock market returns = We can see that the values do not fall near the straight line. The extremes are further out in the tails. In finance the return distributions have heavier tails than a  normal distribution. So it’s not good here.

Example-B: Call centers; using our y1=0.3,y2=2.3,y3=1.0,y4=0.1,y5=3.9,y6=0.8; The question is could these data values have a normal distribution? We make estimates of u and sigma, usually your software does that for you. You can create a table in Excel with inverse CDF. There is not enough data points to make a firm determination; it’s bad that our lower quantiles are negative as calls can’t be negative. We consider the graph and “subject matter” to say normal plot isn’t good here.

























`                               `**EXAMPLE-A                                                                      EXAMPLE-B**



**RULE OF THUMB:** If sample size n>=30 then the quantiles are good enough estimates. Thus the q-q plots can be trusted. A larger n provides better accuracy

`    `**HOW TO INTERPRET Q-Q PLOTS:**

** 
















- Perfection does not exist in the real world, your data can never perfectly reflect the process that produced the data. Always an inherent variability in data. No two samples are the same , even coming from the same process. Randomness has an effect on any statistical analysis. It is good to try many simulations therefore.

- A core thing in statistics you’ll see is that you can’t really prove something, you can only show that it is not (disprove). So you cannot ever prove normality for any distribution form using data, but you can disprove it. 

- Generally with larger samples, randomness is less.

**(V) Conditional Distributions and Independence**

- **Conditional distribution**              : probability distribution of y given a particular x.

- You can use conditional distributions to make predictions: **Use what you know (X=x) to predict what you don’t know (Y).** Empirical research involves the concept of conditional distributions a lot; **about  “effect”.** Papers like: 

“Effect of Ambiguity on Business Decisions” = Are business decisions generally better with less 

`                                                                          `ambiguity?

“Effect of Nicotine Patches on Smoking Cessation” = Do people generally quit more when using a 

`                                                                                     `patch?

- It talks about how two variables relate to each other; we used generally as these aren’t deterministic relationships. 

- Distribution of successes and failures (binary Y) in business decision when ambiguity is low

p(y|X=Low), but a potentially different distribution of successes and failures when ambiguity is high p(y|X=High)

potentially-different: We use this term, as if the distributions don’t differ at all, then the X variable has no effect on Y.

Statement: X has an effect on Y = typical research hypothesis; the effect itself is an example of the unknown parameter. The effect parameter has many forms: difference between means, correlation coefficient, odds ratio, hazard ratio, regression coefficient. It depends on the type of distribution p(y|x).

- X (**explanatory variable**,**predictor variable**, **exogenous variable**, **descriptor variable** ) explains some variation in Y (**response variable**, **endogenous variable**, **target variable**)

- **Note:** X explains Y not that X causes Y; if there is a causal connection, then pick X to be the variable that causes Y; to say there is a connection requires more carefully controlled experiments. We can change Y if you can control X. Y should be something important.

- **Conditional Discrete Distributions:**



`                                                                                `Model produces data, model has unknown

`                                                                                `parameters.
**


`                                                                                `The pi numbers are unknown parameters, but

`                                                                                `we can say that they are continuous functions 

`                                                                                `Of x. Meaning it does not differ much for 20

`                                                                                `year old vs 20.1 year old.










`                                                                                                       `**X = 20,40,60**

**A popular advanced model is the multinomial logistic regression model varies continuously**

- **To understand concept of distributions varying continuously as x changes**






**NOTE: NATURE FAVORS CONTINUITY OVER DISCONTINUITY**

It’s pretty unusual for distributions to change discontinuously. For example after age 40 everyone must   have a green car, that’d make the probability for X=40 near 1. Distributions are not from data, as say for a case like X = 20.00000… years old, how many people are at that age precisely? None. So probabilities cannot refer to counts out of a total.

Models are producers of data; understand this and not make silly claims about populations or misinterpretations of data. The continuity assumption comes from processes in Nature. It is quite logical to assume that people who are 20.000000.. years old do not differ much from those who are 20.0000032 years old.



- **Estimating Conditional Discrete Distributions**

`             `We use the binning methods: identify ranges of values where there are sufficient number of 

`             `observations. So if you gathering data about 20 year olds you’ll have to settle for an estimate

`             `of people who are between 20 and 21 years old as no one is precisely 20 years old. You make a

`             `Frequency table like this:

`                                                                        `Note these are just estimates so you need put a 

`                                                                                      `hat on them to show they are not same as true

`                                                                                      `values:
**

**

**
`                                                                        `For example if counts were 3,0, and 1. The result 

`                                                                                      `estimates are:

**                                                                       
**
`            `But this makes our estimates less precise. To make it more precise you have to assign a bigger

`              `group of say 16-25 years old. A trade off here exists (resulting probabilities more precise but data 

`              `does not  cater to 20 year old now. So a good rule of thumb is:

`             `**FOR FREQUENCY TABLES, HAVE AT LEAST 5 IN EACH CATEGORY TO OBTAIN** 

`             `**RELIABLE ESTIMATES OF THE TRUE PERCENTAGES**

- **Estimate Conditional Continuous Distributions:**
**
`           `We saw for continuous distribution, we chose a histogram for estimates, same thing here. The 

`             `only change is that conditional distributions refer to subsets of potential data defined by X = x. 

`             `The problem is that you may not have enough n >=30 for good histogram estimate. So the

`             `grouping needs to be sensible. Thus we can estimate                            much better if A is a range

`             `of values rather than a specific value x or p(y|x).

`             `You can divide by mean and median, but they might not be pleasing numbers. If not then it’s 

`             `Common sense to use numbers which are more pleasing even if not exactly accurate. For 

`             `Example instead of 13,212.33 just use 15k. Again this does depend on your audience. 

`             `Example of a split of A1 =  {x; x<=60} and A2 = {x;x>=80} we have:




















`           `**Interesting to see how there is more variability in the greater than 80k range due**

`           `**to the fact that more income means more freedom of choice.**

- **Independence:**

We know that most research involves the effect of an X variable on a Y variable. We are questioning nature here, not data. We use the data to learn about nature (data reduces uncertainty about unknown parameters). At a fundamental level there may not exist any relation between X and Y.

Independence is a property of nature not data. Your data can steer you wrong; infact almost always it will show some evidence of relation between X and Y even if there isn’t any. The question is can you explain that by chance alone?


- For example you have: 10 coin tosses: T H T T T H H H T H

`             `Is the next flip dependent on the previous flip? 

`             `P(Head|Previous Tail) = 3/5

`             `P(Head|Previous Head) = 2/4 

`             `Can we say that if you toss a coin and get tails, then the next outcome is more likely to be heads?

`             `The data may suggest this; but remember that numbers from data are not the same as the model 

`             `parameters. These are just estimates and for such  a small sample size, they’re bad.

- YOU CANNOT PROVE INDEPENDENCE USING DATA;

With data you can say:

1\.Variables **appear independent**/**close to independent**/ **independence is reasonable**; if the estimated distributions                        and                      are **reasonably similar** for different choices of A1 and A2.

**[Reasonably similar = within chance variation = practically insignificant]**

2\.Variables appear dependent if estimated are distributions are grossly different (statistically significant/ can’t be explained by chance alone)

- **What does within chance mean?**

It is easy to establish that differences are obviously outside realm of chance; you have formal probability calculations for the same. Chance is basically:

Say you flip a coin 100 times, you expect heads 50% of the times but you get 509 heads. The difference between the both falls under chance. You can say that get 100 heads is outside of chance

- Example of Independence of Consecutive Market Returns

**(VI) Marginal Distributions, Joint Distribution, Independence and Bayes’ Theorem**









































































**Chebychev Theorem:** Relates the standard deviation to probability of deviation from the mean, if the sd sigma exists then:



Probability that a rv will deviate from it’s expected value by more than 3 sd is less than 1/9

This implies the following:

**pth quantile of distribution F(x) is the smallest value of x , k such that F(x) >= p. (k = F-1(p)).**

For example:** 































** 




































