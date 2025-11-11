# MEAN-VARIANCE-AND-CROSSCORRELATION
# Simulation of Mean and Variance Using Scilab

## Aim
To write a program for **mean**, **variance**, and **cross-correlation** in Scilab and verify the output.
 
---

## Equipment Needed
- Computer with i3 Processor  
- Scilab Software

---

## Algorithm
1. **Define the Function:** Specify the function you want to simulate. For example, `f(x) = sin(x)` or any other function.  
2. **Generate Sample Points:** Decide on the range and the number of sample points. Generate these sample points within the desired range.  
3. **Evaluate the Function:** Compute the function values at each of these sample points.  
4. **Compute Mean, Variance, and Cross-Correlation:** Use Scilab's functions to calculate the mean and variance of the computed function values.  
5. **Display Results:** Output the computed mean, variance, and cross-correlation.

---

## Procedure
1. Refer to the algorithm and write code for the experiment.  
2. Open **Scilab** on your system.  
3. Type your code in a new editor.  
4. Save the file.  
5. Execute the code.  
6. If any errors occur, correct the code and execute again.  
7. Verify the generated results.

---

## Program

```scilab
// Clear workspace and console
clear;
clc;
clear;

// Mean Value function X=f(x)
function z = f(x)
    z = 3*(1-x)^3; // Marginal Probability Density Function
endfunction

a = 0;
b = 1;
EX = intg(a, b, f); // Mean value of X

// Function Y=c(y)
function z = c(y)
    z = 3*(1-y)^3; // Marginal Probability Density Function
endfunction

EY = intg(a, b, c); // Mean value of Y

disp(EX, "i) Mean of X =");
disp(EY, "Mean of Y =");

// Variance
function z = g(x)
    z = 3*(1-x)^3 * x^2; // X^2 * PDF
endfunction

EX2 = intg(a, b, g); // E[X^2]

function z = h(y)
    z = 3*(1-y)^3 * y^2; // Y^2 * PDF
endfunction

EY2 = intg(a, b, h); // E[Y^2]

vX2 = EX2 - (EX)^2; // Variance of X
vY2 = EY2 - (EY)^2; // Variance of Y

disp(vX2, "ii) Variance of X");
disp(vY2, "Variance of Y");

// Cross-Correlation
x = input("Type in the reference sequence = ");
y = input("Type in the second sequence = ");
n1 = max(size(y)) - 1;
n2 = max(size(x)) - 1;
r = corr(x, y, n1);
plot2d3('gnn', r);
```

--- 

## Output

### Mean Values
- Mean of X = 0.3011687
- Mean of Y = 0.25

### Variance Values
- Variance of X = 0.0092974 
- Variance of Y = 0.0375000

### Cross-Correlation Input Example
- Reference sequence: `[1, 2, 3, 4, 5, 6, 7, 8]`  
- Second sequence: `[2, 1, 3, 5, 6, 3, 5, 9]`

---

<img width="610" height="420" alt="image" src="https://github.com/user-attachments/assets/92d08a66-c3d4-496a-8d39-1fc97f83530f" />

---

## MANUAL CALCULATION:

<img width="560" height="780" alt="image" src="https://github.com/user-attachments/assets/aa459ff0-d4ab-42e9-9a47-9143f50fae8d "/>

<img width="560" height="660" alt="image" src="https://github.com/user-attachments/assets/65ef0b65-fe6b-4eab-9e2b-3a075f7f11e9 "/>


---

## RESULT:
