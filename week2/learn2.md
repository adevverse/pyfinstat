# Week 2
# Module Introduction
>  1. Outcomes and Random Variable
>  2. Frequency and Distribution
>  3. Models of Stock

<!-- In the trading strategy explained in Module 1, 
random variables - MA50 and MA10 - help us make better predictions and decisions. 
Such concepts are applied into different contexts in our daily lives. Let us see some examples ...  -->

<!-- Proxy Means Test
  Wall meterial 
  Ceiling meterial
  Assets at home
 -->
 
<!--  Insufficient / Non-existings credit history -->

##  1. Outcomes and Random Variable
> What are outcomes of Random variables
> Dice game
> > Sum of faces
> > Rolling dice in python
<code>
# X = The sum of faces 
# Random Variable -> Discrete -> Continuous 2,3,4,5,6,7,8,9,10,11,12
# 1.5% -> -4.558% -> -8.8756% -> 13.48 % 
</code>

##  2. Frequency and Distribution
> Discuss frequency, relative frequency and distribution
#Frequency 
#Rolling dice in python - 50 Time
freq = pd.DataFrame(result)[0].value_counts() #count values
sort_freq = freq.sort_index() #Sort Index List of different outcomes
sort_freq #freqency
#Frequency
#X = The sum of faces 
#Random Variable -> Discrete -> Continuous 2,3,4,5,6,7,8,9,10,11,12
#1.5% -> -4.558% -> -8.8756% -> 13.48 % 
#Relative frequency = Frequency / No. of trials
trial = 2000
result = [die.sample(2, replace = True).sum().loc[0] for i in range (trial)]
freq = pd.DataFrame(result)[0].value_counts() #count values
sort_freq = freq.sort_index() #Sort Index List of different outcomes
relative_freq = sort_freq/sort_freq.sum()
relative_freq.plot(kind='bar',color='blue')
#infinite number of trials?
#Limit:Distribution of sum of face X
#Distribution table
#X             2     ............................................. 12 
#Probability  P(X=2)                                            P(X=12)
#X                             6           7             8
#Probabil                  5x(1/6)**2     6x(1/6)**2   5x(1/6)**2
X_distri = pd.DataFrame(index=[2,3,4,5,6,7,8,9,10,11,12])
X_distri['Prob']= [1,2,3,4,5,6,5,4,3,2,1] 
X_distri['Prob']= X_distri['Prob']/36

#Nice progress! From the first part of the video, 
#we understand that if we mimic the roll dice game for infinite number of times, 
#the frequencies of the outcomes are the probability  represented by Distribution Table. 
#We do not know the shape of outcome immediately, 
#but you can imagine it is very close to a normal distribution. 

## Mean and Variance of a distribution
>> Mean (or Expectation) = Expectation i pi xi 
>> Variance = Expectation (xi-Mean)**2 pi



##  3. Models of Stock
> How to compute probability of yearly return and Value at Risk


 
