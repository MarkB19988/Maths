# Maths

### 1. How to calculate the Greatest Common Divisor and Least Common Multiple

The Greatest Common Divisor is the largest possible number that will divide into 2 given numbers. the first step towards finding the GCD of the 2 numbers is to first find out all the divisors for both numbers. Then you compare the two lists of divisors and look for the largest one that they share. 

The Least Common Multiple is the smallest number that is a multiple of 2 given numbers. To find out the LCM you can use a similar process to finding the GCD. firstly you make a list of X ammount of muliples for each number, e.g. Multiples of 7 are 7, 14, 21, 28, 35 and the multiples of 3 are 3, 6, 9, 12, 15, 18, 21. Now you just look for the first number that appears in both lists. In this case, the LCM of 3 and 7 is 21.

### 2. Expectation Of An Event Occurring From a Discrete, Random Variable

Random selection is only possible from a finite ammount. So what have to do is always select from a finite ammount but do the task repeatedly. Below is the formula you can use, you can input any random variable into the formula:

![formula](https://i.imgur.com/SIZuZA6.jpg)

As an example, The probability of a random integer being divisible by 5 is 1/5. To work this out we have to first break down the decimal system. In the decimal system there are ten possible digits that a number can end with in the units collum, that is 1,2,3,4,5,6,7,8,9,0. We also know that 5 can divide into any number that ends with a 5 or a 0. Now that we have this information we simply count how many numbers are in each list to get out probability. In this case we are left with a 2/10 which can be simplified down to 1/5.

### 3. Algorithm to Calculate Arithmetic and Geometric Progressions

The following code snippet is an algorithm we created for calculating Arithmetic and Geometric progressions. The language used is C++


#include 'iostream'

#include 'cstdlib'

using namespace std;

int main () {

int input;

cout<< "type a number: \n";

cin >> input; 

int loop = 0;


do{

int geometric = input * input;

int arithmetic = input + input;

int arithmetic2 = arithmetic + input;

int geometric2 = geometric * input;

int arithmetic3 = arithmetic2 + input;

int geometric3 = geometric2 * input;

loop++;

  cout<<"geometric value:";
  cout<<geometric;
  cout<<"\n";
  cout<<"arithmetic value:";
  cout<<arithmetic;
  cout<<"\n";
  cout<<"geometric value:";
  cout<<geometric2;
  cout<<"\n";
  cout<<"arithmetic value:";
  cout<<arithmetic2;
  cout<<"\n";
  cout<<"geometric value:";
  cout<<geometric3;
  cout<<"\n";
  cout<<"arithmetic value:";
  cout<<arithmetic3;
  cout<<"\n";
  
} while( loop < 0 );
return (0);

}

### 4. Deduce the conditional probability of different events occurring within independent trials

For my example of independant trials, I will be using dice rolling as there are varying probabilities for each result when rolling 2 or more dice, however for this theory experiment I will be rolling 2 dice.

##### What is the probability of rolling a total of 7 when rolling two dice?

To work this out we first need to determine how many possible outcomes there are when you throw 2 dice, these outcomes can include different rolls with the same total, (e.g. 5 and 1 or 3 and 3 are classed as different results even though the total is 6 in both rolls). To do this you simply multiply the number of outcomes for each individual variable, in this case, each die has 6 sides so 6x6 is 36

Now you must determine how many of these possible outcomes will result in the predicted total, which in this case is 7. with 2 dice the possible combinations that result in 7 are as follows. 6 and 1, 5 and 2, 4 and 3, 3 and 4, 2 and 5, 1 and 6. Because there are 6 different combinations that result in a total of 7, the chance of rolling a 7 is 6/36, which can be simplified down to 1/6.

