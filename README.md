# Lambda-Calculus
My final year mathematics double project had the title: 'A World of Functions: Python Coding the Lambda Calculus'. This was a solo project, overseen by a super visor and worked on soley by myself. The full report is upload in this repository as 'λ_Calculus Project.pdf'. If henceforth I reference chapters and sections, I am referencing those within the report. A brief outline of the chapters:
					Chapter 1: 'Lambda Calculus'. An introduction to the syntax and its properties.
					Chapter 2: 'Booleans and the Integers'. We build the boolean and integer systems out of lambda functions.
					Chapter 3: 'SKI Calculus'. We introduce combinators and S, K and I.
					Chapter 4: 'SKI Combinatorics in Python - An Alternative Strategy'. We find the integers and booleans out of only 						SKI functions, in Python.

### What is Lambda Calculus
Lambda calculus is just a functional notation at heart, however it is an ideal language in which to express mathematical systems made up purely of functions. Lambda functions are explained in great detail in Chapter 1: 'Lambda Calculus'. It turns out, lambda functions are universal, that is to say that we can express any mathematical object in terms of them (see Chapter 2, especially section 2.3).

### A note on SKI functions
SKI functions, describe the combinators S, K and I. For more, detailed information on what a combinator is, its properties and definitions for S, K and I, see Chapter 3: 'SKI Calculus'. It turns out that, just as lambda functions are universal, it can be proven that the three simple combinators S, K and I, make up a universal language.


### Aims of the Project and General Method
The main aim of the project was quite an open one: to explore and motivate this idea that lambda functions, and in fact S, K and I alone, are universal. 

To achieve this, we first went through step by step, giving detailed explanation and commentary of the significance, how to build the boolean and integer systems purely out of functions which take functions as input  (using lambda notation). We did this in Python. This was by no means my original work. 

Next, we set out to find, in Python, the same functions that make up the integer and boolean systems, but purely in SKI form (a composition of S, K, I). To do this, we first find every possible compostion of n functions, using two different and entirely original techniques explained in the report section 4.2. Then, now with access to every possible composition of S, K and I, we built a function which can physically perform the actions of these combinators, and so reduce any SKI expression to its normal form (see report Chapter 3). This function was vital to us, primarily because some combinator expressions will recombine forever (or for a long time) and cause a stack overflow. Using strings, parsing and physical reduction, we are able to control reduction and flag and remove these "volatile" combinations. 

We generate all distinct SKI functions of size less than n (in our case n=9, there are ~250,000 distinct functions) and effectively use trial and error to find the functions which behave exactly how we looking for (and so ARE the functions we are looking for in SKI form).


## Files

#### 'λ_Calculus Project.pdf'
The final project report.

#### 'Integers.ipynb'
Building the booleans and integers in lambda calculus in Python. The majority is not originally my work.

#### 'SK-calculus.ipynb'
Functional combinatorics and SKI Calculus. Two original methods for finding all function compositions of size <n; the creation of SKIsimplify, our physical SKI reducer; input testing the generated function bank for boolean and integer functions in SKI form.

#### 'Dyck Paths.ipynb'
Code which generates all the Dyck paths of length N and translates them into their corresponding functional compostion. The bijection between Dyck Paths and function compositions is explained in section 4.2.3.

#### 'Input testing.ipynb'
Input testing proved useful at the very final stages of the work in 'SK-calculus.ipynb'. This file is just a bit of fun: a toy version of the strategy employed to find our SKI integers and booleans.

