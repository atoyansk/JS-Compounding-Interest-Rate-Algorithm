# JS-Compounding-Interest-Rate-Algorithm
Variable Savings Compounding Interest Rate Algorithm

##Scenario

Suppose you want to deposit a fixed monthly amount into an investment fund for a set period of time.
In addition to the amount resulting from this monthly deposit, the investment fund still has a fixed interest rate on this investment.
To know a base value for redemption the amount resulting from deposits and monthly interest, the following algorithm can be used.

##Code

This algorithm was coded in JavaScript, and it considers fake values in order to becomes easier the understanding.

```javascript
var invValue = 100;
var t = 72;
var i = 0.01;
var p = 1;

for(j=1; j<=t; j++){
   finalValue = (invValue += 100) * Math.pow((1 + i),p++);
};
console.log(finalValue);
```
In this hypothetical case, the monthly amount invested is 100 (var invValue), the period is 72 months (var t), and the rate of return is 1% per month (var i).
The calculation is based on the following formula: **A = V * (1 + i)^t**

An update to a function would be
```javascript
function compInterest (invValue,t,i){
	var p = 1;
	for(j=1; j<=t; j++){
   	compInterest = (invValue += 100) * Math.pow((1 + i),p++);
	};
   return compInterest.toFixed(2);
}
```
To call de function: 
```javascript
compInterest(100,72,0.01);
```
And the result:
```javascript
"14943.82"
```
