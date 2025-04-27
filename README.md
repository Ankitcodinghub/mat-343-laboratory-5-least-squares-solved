# mat-343-laboratory-5-least-squares-solved
**TO GET THIS SOLUTION VISIT:** [MAT 343 Laboratory 5 Least Squares Solved](https://www.ankitcodinghub.com/product/mat-343-laboratory-5-least-squares-solved/)


---

📩 **If you need this solution or have special requests:** **Email:** ankitcoding@gmail.com  
📱 **WhatsApp:** +1 419 877 7882  
📄 **Get a quote instantly using this form:** [Ask Homework Questions](https://www.ankitcodinghub.com/services/ask-homework-questions/)

*We deliver fast, professional, and affordable academic help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;7151&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;5&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;5&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;5\/5 - (5 votes)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;MAT 343 Laboratory 5 Least Squares Solved&quot;,&quot;width&quot;:&quot;138&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

<div class="kksr-stars">

<div class="kksr-stars-inactive">
            <div class="kksr-star" data-star="1" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="2" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="3" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="4" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="5" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>

<div class="kksr-stars-active" style="width: 138px;">
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
</div>


<div class="kksr-legend" style="font-size: 19.2px;">
            5/5 - (5 votes)    </div>
    </div>
In this laboratory session we will learn how to

1. Factor a symmetric matrix using the Cholesky decomposition.

2. Solve Least Squares problems using MATLAB

3. Plot the data points together with the least squares approximation.

Introduction

Let S be a symmetric matrix. Since S is square (why?), it has an LU decomposition. In fact, the symmetry makes it possible to write S in the form S = LLT , where L is a lower-triangular matrix.

This is called the Cholesky decomposition of S, and it is dened only for symmetric matrices. Given a symmetric matrix, the Cholesky decomposition is always preferable in computations because it can be computed in half the time of the LU decomposition.

There is nothing special about writing the Cholesky decomposition in terms of a lower-triangular matrix.

We can just as well write S = UTU, where U = LT . In MATLAB, the command

U = chol(S)

returns the Cholesky decomposition of the symmetric matrix S in the upper-triangular matrix U.

Once the Cholesky decomposition S = UTU is found, solving a system of the form

Sc = z

proceeds in the same 2-step manner as solving Ax = b with the LU decomposition:

1. Solve UTw = z.

2. Solve Uc = w.

The normal equations for the least squares

Suppose we are given a collection of data points of the form f(xi; yigni

=1. The simplest potential statistical

relationship between x and y is that of a straight line; more precisely,

yi = c1 + c2xi (L5.1)

where c1 and c2 give the y-intercept and slope, respectively. Of course, the data points do not, in general,

lie on this line. The difference

yi 􀀀 (c1 + c2xi) = ϵi (L5.2)

is the \residual” or \noise”, that is, the amount by which c1+c2xi fails to coincide with yi. Our rst goal

is to estimate the unknowns c1 and c2 from the data. Although MATLAB provides an entire toolbox

for statistical analysis, we will use only a few simple commands to get started; the pedagogical purpose

is to make sure that you understand how the problem is set up mathematically. Equation (L5.2) can be

extended to any polynomial model. For example, if we suppose that

yi = c1 + c2xi + c3x2i

+ : : : + cpxp􀀀1

i + ϵi (L5.3)

then we have to estimate the p unknowns c1; c2; : : : ; cp so that ϵi is small for all i. Statisticians write

the estimation problem in the following form:

y = Xc + ϵ (L5.4)

c⃝

2011 Stefania Tracogna, SoMSS, ASU 1

MATLAB sessions: Laboratory 5

where y = (y1; y2; : : : ; yn)T is an n-vector of observations (i.e., the dependent variable), c = (c1; c2; : : : ; cp)T is

the p-vector of unknown parameters, X is the n p matrix

X =

2

6664

1 x1 x21

: : : xp􀀀1

1

1 x2 x22

: : : xp􀀀1

2

…

. . .

…

1 xn x2

n : : : xp􀀀1

n

3

7775

and ϵ = (ϵ1; ϵ2; : : : ; ϵn)T is the vector of residuals corresponding to the n observations.

It is straightforward to verify that the ith row of the matrix-vector product, plus the ith component of

ϵ, yields the right-hand side of (L5.3).

The least squares solution of (L5.4) is the solutionbc

of the Normal Equations:

XTXc = XT y (L5.5)

The vector bc

minimizes the quantity ∥ ϵ ∥=∥ y 􀀀 Xc ∥, that is, minimizes the difference between the

sum of squares of the differences between the \predicted” value of y from the \observed” value of y,

where the sum is taken over every point in the dataset.

Notice that XTX is a symmetric matrix.

The system (L5.5) can be solved as follows:

1. Dene z = XT y.

2. Dene S = XTX.

3. Solve Sc = z.

The last step must be performed using the Cholesky decomposition of S and solving the two triangular

systems.

MATLAB Notes

Transposition is denoted by prime (i.e. a single quotation mark): XT is denoted by X’.

The triangular systems obtained from the Cholesky decomposition must be solved using the MAT-

LAB \backslash” command. For example, to solve UTw = z, type w =U’nz.

Given the vector a = [a1; a2; : : : ; an]T , you can form the vector [a21

; a22

; : : : ; a2

n]T with the expression

a.^2 (component-wise exponentiation).

When building the matrix X you should use the special matrix ones.

Example 1: Least Squares t to a Data Set by a Linear Function.

Compute the coefficients of the best linear least-squares t to the following data.

x 2.4 3.6 3.6 4.1 4.7 5.3

y 33.8 34.7 35.5 36.0 37.5 38.1

Plot both the linear function and the data points on the same axis system.

Solution

We can solve the problem with the following MATLAB commands

x = [2.4;3.6;3.6;4.1;4.7;5.3]; % build vector of x -values

y = [33.8;34.7;35.5;36.0;37.5;38.1]; % build vector of y -values

X = [ones(size(x)),x]; % build the matrix X for linear model

z = X’*y; % right hand side of the Normal Equations

c⃝

2011 Stefania Tracogna, SoMSS, ASU 2

MATLAB sessions: Laboratory 5

S = X’*X; % Left hand side of the Normal Equations

U = chol(S); % Cholesky decomposition

w = U’\z; % solve the normal equations using the Cholesky decomposition

c = U\w

plot(x,y,’o’) % plot the data points

q = 2:0.1:6; % define a vector for plotting the linear fit

fit = c(1)+c(2)*q; % define the linear fit

hold on

plot(q,fit,’r’); % plot the linear fit together with the data points

Running the script le produces the output

c =

29.6821

1.5826

and the following gure.

2 2.5 3 3.5 4 4.5 5 5.5 6

32

33

34

35

36

37

38

39

40

EXERCISES

Instructions: For each of the following exercise, create an M-le to store the MATLAB commands.

Copy and paste the M-le into a text document. Include in the text document the pictures produced

by MATLAB. Resize and crop the pictures so that they do not take up too much space. If the question

requires written answers, include them in the text le in the appropriate location. Make sure you clearly

label and separate all the Exercises. Preview the document before printing and remove unnecessary page

breaks and blank spaces.

1. Consider a set of data points (1; y1); (2; y2); :::(100; y100) where the y’s are random numbers with a

normal distribution with mean 0 and variance 1 (note that this implies that the probability of the

y-values being less than zero is the same as the probability of being greater than zero).

(a) Based on the distribution of the points, what do you expect is the best straight-line model

that can be t to the data?

(b) To conrm numerically your answer to part (a), generate the data as follows:

x = [1:1:100]’; % note the prime

y = randn(size(x)); % a column vector of 100 standard normal values.

Plot the values as dots with the command plot(x,y,’.’). Follow Example 1 to nd the

best linear t using MATLAB. Answer the following questions:

c⃝

2011 Stefania Tracogna, SoMSS, ASU 3

MATLAB sessions: Laboratory 5

(i) What values do you obtain for the slope and y-intercept? Give the values in scientic

notation with ve digits of accuracy (use format short e).

Plot the linear t together with the points (use q = x;)

(ii) Do the values of the slope and y-intercept conrm your answer to part (a)? Explain.

2. Download the le co2.dat from the web page. This le contains two columns of numbers: the

year from 1959 to 2012 and the average annual carbon dioxide concentration in the atmosphere

(in parts per million), as measured at the Mauna Loa observatory in Hawaii. The data come from

the Earth Systems Research Laboratory (Global Monitoring Division) of the National Oceanic and

Atmospheric Administration (which is the government agency charged with developing weather and

climate forecast models; if you are interested in additional information and data set you can visit

http://www.esrl.noaa.gov/gmd/ccgg/trends ). The estimated standard error in the observations

is 0:12 ppm.

Save the le in the MATLAB working directory. Then load it with

dat = load(‘co2.dat’);

Note: if you do not save the le in your working directory, you need to include the whole path to

load it into MATLAB. For instance, if you saved your le in the C:ntmp directory you can load it

by entering load(‘C:ntempnco2.dat’).

This creates the 49 2 array dat whose rst column is the year and whose second column is the

CO2 concentration.

You may nd it convenient to create two separate data vectors, as follows:

year = dat(:,1);

conc= dat(:,2);

Plot the data with

plot(year,conc,’o’)

(a) Follow Example 1 to compute the best-t line for these data. What are the coefficients c1

and c2? Give the values with ve digits of accuracy. Plot the line in black ( use q = year;),

together with the original data. Use ‘linewidth’,2 and axis tight in your plot.

(b) Find the best-t quadratic polynomial to the CO2 data (make sure you change appropriately

the matrix X). What are the coefficients c1, c2 and c3? Give the values with ve digits of

accuracy. Plot the tted curve in red (use ‘linewidth’ ,2) together with the data points

and the linear t from part (a). Add a legend to the graph.

3. Among the important inputs in weather-forecasting models are data sets consisting of temperature

values at various parts of the atmosphere. These values are either measured directly with the use

of weather balloons or inferred from remote soundings taken by weather satellites. A typical set

of RAOB (weather balloon) data is given next. The temperature T in Kelvins may be considered

as a function of p, the atmospheric pressure measured in decibars. Pressure in the range from 1 to

3 decibars correspond to the top of the atmosphere, and those in the range from 9 to 10 decibars

correspond to the lower part of the atmosphere.

p 1 2 3 4 5 6 7 8 9 10

T 222 227 223 233 244 253 260 266 270 266

Enter the pressure values as a column vector p (use the colon : operator), and enter the temperature

values as a column vector T.

The goal of this problem is to nd the cubic polynomial y = c1 + c2x + c3x2 + c4x3 that gives the

best least square t to the data.

c⃝

2011 Stefania Tracogna, SoMSS, ASU 4

MATLAB sessions: Laboratory 5

(a) Follow Example 1 to nd the coefficients of the best cubic t (make sure you appropriately

modify the matrix X).

Plot the data together with the cubic t. Make sure you dene your vector q so that the

graph of the cubic is nice and smooth.

(b) Let X be the matrix you used in part (a). Here is an easier way to evaluate and plot the

cubic polynomial:

c = X\T

c = c([4:-1:1]);

q = 1:0.1:10;

z = polyval(c,q);

figure

plot(q,z,p,T,’o’);

How do the values of c compare to the ones you found in part (a)?

How does the plot compare to the one you found in part (a)?

Note that the system Xc = T is overdetermined. In this case, the \n” command nds the

least-squares solution to the system. In fact, for overdetermined systems, the \n” command is

equivalent to solving the Normal Equations using the Cholesky decomposition, just like you

did in the previous problems. Thus the vector c = XnT is the same one you found in part (a)

by solving the normal equations.

The command polyval(c,q) evaluates the polynomial with coefficients given by the vector c

in decreasing powers of q. Because the powers are decreasing we had to rearrange the entries

in c using the command c = c([4:-1:1]);. Type help polyval to learn more.

c⃝

2011 Stefania Tracogna, SoMSS, ASU 5
