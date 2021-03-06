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

### 5. Identify Simple Shapes Using Co-Ordinate Geometry

When you are developing software, you will often find that you will be creating shapes using co-ordinate geometry most of the time. Co-ordinate geometry is the rules by which different shapes can be created and identified. for example, an equallateral triangle must have 3 sides of the same length and 3 equal angles. By following these rules, you will always end up with an equallateral triangle.

Every shape has their own unique properties, these properties are shown in the following tabel. Some share properties while others have properties that are completely unique.

![Table](https://i.imgur.com/65etQxD.png)

There are also various formulae that can be used to identify shapes using co-ordinates. For example, because any square will always have 4 sides of the same length and 4 right angles. You can desplay the co-ordinates of the vertices of the square like this - (3,3) (3,-3 (-3,3) (-3,-3), this is because each vertex is a direct opposite of on another because all lengths and angles are the same.

Some of the formulae are shown as follows:

![formulae](https://i.imgur.com/Zd9ubFD.png)

### 6. Determine shape parameters using appropriate vector methods

A vector is a quantity that has two independent properties, these are magnitude and direction. The term also includes the mathematical or geometrical representation.

To scale shapes and identify shape parameters I have created a formula that you can use to scale a shape using vector methods
```
<html>
<body>

<canvas id="myCanvas" width="300" height="150" style="border:1px solid #d3d3d3;"></canvas>

<br>
<button onclick="move(1)">LEFT</button>
<button onclick="move(2)">UP</button>
<button onclick="move(3)">DOWN</button>
<button onclick="move(4)">RIGHT</button>
<br>
<button onclick="move(5)">DIAGONAL RIGHT DOWN</button>
<button onclick="move(6)">DIAGONAL RIGHT UP</button>
<br>
<button onclick="move(7)">DIAGONAL LEFT DOWN</button>
<button onclick="move(8)">DIAGONAL LEFT UP</button>
<br>
<button onclick="shape()">SHAPE?</button>


<script>
var c = document.getElementById("myCanvas");
var ctx = c.getContext("2d");
ctx.beginPath();

var curX=parseInt(prompt("Please enter the initial X"));;
var curY=parseInt(prompt("Please enter the initial Y"));;

function move(dir){
var mag = parseInt(prompt("Please enter the magnitude"));

if(dir==1){
  //left
  ctx.moveTo(curX, curY);
  curX = curX-mag;
  ctx.lineTo(curX, curY);  
  alert("Vector Direction: Left / Vector Magnitude: "+mag);
}else if(dir==2){
  //up
  ctx.moveTo(curX, curY);
  curY = curY-mag;
  ctx.lineTo(curX, curY);  
  alert("Vector Direction: Up / Vector Magnitude: "+mag);
}else if(dir==3){
  //down
  ctx.moveTo(curX, curY);
  curY = curY+mag;
  ctx.lineTo(curX, curY);  
  alert("Vector Direction: Down / Vector Magnitude: "+mag);
}else if(dir==4){
  //right
  ctx.moveTo(curX, curY);
  curX = curX+mag;
  ctx.lineTo(curX, curY);  
  alert("Vector Direction: Right / Vector Magnitude: "+mag);
}else if(dir==5){
  //diagonal right down
  ctx.moveTo(curX, curY);
  curX = curX+mag/2;
  curY = curY+mag/2;
  ctx.lineTo(curX, curY);  
  alert("Vector Direction: Diagonal Right Down / Vector Magnitude: "+mag);
}else if(dir==6){
  //diagonal right up
  ctx.moveTo(curX, curY);
  curX = curX+mag/2;
  curY = curY-mag/2;
  ctx.lineTo(curX, curY);  
  alert("Vector Direction: Diagonal Right Up / Vector Magnitude: "+mag);
}else if(dir==7){
  //diagonal left down
  ctx.moveTo(curX, curY);
  curX = curX-mag/2;
  curY = curY+mag/2;
  ctx.lineTo(curX, curY);  
  alert("Vector Direction: Diagonal Left Down / Vector Magnitude: "+mag);
}else if(dir==8){
  //diagonal left up
  ctx.moveTo(curX, curY);
  curX = curX-mag/2;
  curY = curY-mag/2;
  ctx.lineTo(curX, curY);  
  alert("Vector Direction: Diagonal Left Up / Vector Magnitude: "+mag);
}

ctx.stroke();

}

function shape(){
  var shape = prompt("Is this a shape Y/N?");

  if(shape=='Y'){
      prompt("What shape?");
  }else {
      alert("Keep drawing!");
  }
}

</script>

</body>
</html>
```
### 7. Determine the rate of change within an algebraic function

Average rate of change is the average rate that one value is changing with respect to another thing (e.g. another value) changing. While the idea sounds complex we are already familiar with a number of average rate change calculations. For example the term 'miles per hour' is a rate of change calculation. It is calculated by dividing the distance travelled in miles by the time it takes to travel them in hours.

Generally speaking, the average rate of change function is a process that determines the ammount that one value changes by dividing it by the ammount of change in another value. The following formula uses function notation to show the average rate of change for function f from a to x.

![Imgur](https://i.imgur.com/ZsFXPjx.jpg)

Here are some examples of rate of change calculations
```
F(x) = x²
	Rate of change from 1 to 3
	(3² - 1²) / (3-1) = (9-1) / (3-1) = 8/2 = 4

This answer converted into binary is 0100
  
	
    F(x) = 2x+3
    	Rate of change from 10 to 100
	(2*100+3) - (2*10+3) / (100 - 10) = 180/90 = 2

This answer converted into hexadecimals is 2

  ```





### 8. Use integral calculus to solve practical problems involving area

Intergral calculas is used to calculate whats inside a curve, if the shape is normal or common then you don't have to use integral calculus. However if the shape is more complex, then you can use the given a and b points on a graph to work out the area of a to b.

Here are some example formulae for integral calculus:

![calculus](https://i.imgur.com/4sY1T77.png)

The Integral symbol ∫ ,represents intergration, this means the finding of an integral. The opposite of this is derivation. The a and b signs are placed on each side of the ∫ symbol since we want to calculate from a to b. The symbol dx represents the differential of the variable x, indicates that the variable of integration is x. Finding the area to the x axis from the curve means we have to find the integral of a function with respect to x.

A 'higher derirative' is a way of essentially making a complex funtion simpler .Where a simple function is also called a liniaer function as it is portrayed as a line on a graph, but when the function is more complex it becomes curved, a higher derirative is a way of converting a curved line into a straight line. X is infinite, meaning that the whole infinite (x) can be divided into segments and by using each part a sum may be reached.

By multiplying the function by the derivative of the function, we can calculate the area by creating an infinite area of rectangles to find the area. Because we already know the formula for the area of a rectangle, it makes it simple to calculate.

![Graph](https://i.imgur.com/NnqLOp3.png)

![Rec](https://i.imgur.com/IGeVbPZ.png)








