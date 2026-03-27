# Polymorphism

Polymorphism is another name for function overloading. As we discussed in class, a program can have several functions with the same name. However, each function must have different types or different numbers of formal parameters. For this part of the lab assignment, you need to figure out which function gets called and the order of the functions that gets called manually. The following program has **nine functions** that take different number and different types of parameters and calculate the sum of the numbers passed into the functions.

```c++
#include <iostream>
#include <cstdlib>

using namespace std;

// First sum
int sum(int x, int y);

// Second sum
double sum(double x, double y);

// Third sum
double sum(int x, double y);

// Fourth sum
int sum(int x, int y, int z);

// Fifth sum
double sum(double x, double y, double z);

// Sixth sum
int sum(int a, int b, int c, int d);

// Seventh sum
double sum(double a, double b, double c, double d);

// Eighth sum
double sum(int a, double b, int c, double d, int e, double f);

// Ninth sum
double sum(double a, double b, double c, double d, double e, double f);

int main()
{
	int n1 = 2;
	int n2 = 4;
	int n3 = 6;

	double m1 = 1.5;
	double m2 = 123.45;
	double m3 = 0.56;

	cout << sum(n1, n2) << endl;
	cout << sum(n1, m1) << endl;
	cout << sum(n1, n2, n3, 10) << endl;
	cout << sum(n1, m1, n2, m2, n3, m3) << endl;
	cout << sum(5.5, 6.5, 10.0, 17.0, 4.2, 11.5) << endl;

	return (EXIT_SUCCESS);
}

// First sum
int sum(int x, int y)
{
	return (x + y);
}

// Second sum
double sum(double x, double y)
{
	return (x + y);
}

// Third sum
double sum(int x, double y)
{
	return (x + y);
}

// Fourth sum
int sum(int x, int y, int z)
{
	return (sum(x, y) + z);
}

// Fifth sum
double sum(double x, double y, double z)
{
	return (x + sum(y, z));
}

// Sixth sum
int sum(int a, int b, int c, int d)
{
	return (sum(a, b) + sum(c, d));
}

// Seventh sum
double sum(double a, double b, double c, double d)
{
	return (sum(a, b) + sum(c, d));
}

// Eighth sum
double sum(int a, double b, int c, double d, int e, double f)
{
	return (sum(a, c, e) + sum(b, d, f));
}

// Ninth sum
double sum(double a, double b, double c, double d, double e, double f)
{
	return (sum(a, c, b, d) + sum(e, f));
}
```

## Questions (10 pts each)

*Please answer with the commented names above each function (ex, first sum)*

1. For the **first** **cout** statement, which **sum** is called?

>Answer:

2. For the **second** **cout** statement, which **sum** is called?

>Answer:

3. For the **third** **cout** statement, which functions are called? In this case, **give the order that the functions are called as well.**

>Answer:

4. For the **fourth** **cout** statement, which functions are called? In this case, **give the order that the functions are called as well.**

>Answer:

5. For the **fifth** **cout** statement, which functions are called? **In this case, give the order that the functions are called as well.**

>Answer:

# Parameter Passing

Read and understand find_min.cc. Compile and run with **many different sets** of integer values. For example, enter list of numbers with the minimum value at middle, at the end etc.

For the following questions, you will need to make changes, save, and recompile the program as needed.

1. **Explain** what happens if you **remove** the **&** sign from the **findMin** function **declaration** (prototype) and the **function heading.** **Do not forget to PUT THE & back before moving on.***

>Answer:

2. Similarly, **explain** what happens if you remove the **&** sign from the **getNum** function **declaration** (prototype) and the function heading. **Don’t forget to put the & back before moving on the next question.**

>Answer:

3. Explain what happens if the change the order of the **actual arguments** in the **function call**

```c++
findMin(minimum, number);
```

to

```c++
findMin(number, minimum)
```

>Answer:

4. Explain what happens if you **remove the call** to the function **getNum(number)** ; Coment (//) this statement out and run the program to find out the outcome. **Remove the // before moving on to the next question (4 sub 2)**

a. **Before** the while loop

>Answer:

b. **Inside** the while loop

>Answer:

5. Identify and write the names of **value and/or reference** parameters in the following functions. Write the word *none* if not applicable.

|                      | getNum | findMin |
| -------------------- | ------ | ------- |
| value parameters     |        |         |
| reference parameters |        |         |
