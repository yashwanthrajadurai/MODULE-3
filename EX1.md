
# Ex.No:1
# Ex.Name: Write a c++ program to find simple & compound interest by using Hierarchical Inheritance (read the data In the order of p, n & r)
## Date:21/08/25

## Aim:
To wite a c++ program to find simple & compound interest by using Hierarchical Inheritance (read the data In the order of p, n & r)

## Algorithm:
1. Start the program.
2. Create a base class to store principal, time, and rate with input function.
3. Derive SimpleInterest class to calculate (p * n * r) / 100.
4. Derive CompoundInterest class to calculate p * (pow((1 + r/100), n) - 1).
5. In main(), create objects of derived classes.
6. Call input function once from base class.
7. Calculate and display SI and CI.
8. End the program.

## Program:
```cpp
#include <iostream>  
#include<cmath>
using namespace std;  
  
int main()
{
    float p,n,r,k;
    cin>>p>>n>>r;
    cout<<"Simple Interest Amount is :="<<p*n*r/100<<endl;
    k=p*pow((1+r/100),n)-p;
    cout<<"Compound Interest Amount is :="<<k;
}
```


## Output:
<img width="1124" height="382" alt="Screenshot 2025-09-13 192617" src="https://github.com/user-attachments/assets/51b302b8-ee34-46b7-bffd-86d49e2d447d" />


## Result:
The program successfully executed for simple & compound interest by using Hierarchical Inheritance.
