
# Ex.No:2
# Ex.Name: Write a program to implement protected member with integer values?
## Date:21/08/25

## Aim:
To write a program to implement protected member with integer values

## Algorithm:
1. Start the program.
2. Define a base class with a protected integer variable.
3. Provide a public function in the base class to assign value to the protected variable.
4. Define a derived class inheriting from the base class.
5. In the derived class, create a function to display the protected variable.
6. In main(), create an object of the derived class.
7. Call the base class function to set the value.
8. Call the derived class function to display the value.
9. End the program.

## Program:
```cpp
#include <iostream>
using namespace std;

class Base 
{
protected:
    int num;  

public:
    void setNum(int n)
    {
        num = n;
    }
};

class Derived : public Base
{
public:
    void displayNum()
    {
        cout << "The value of num is: " << num << endl;
    }
};

int main()
{
    Derived obj;
    int input;

    cin >> input;

    obj.setNum(input);

    obj.displayNum();

    return 0;
}
```


## Output:
<img width="952" height="293" alt="Screenshot 2025-09-13 193136" src="https://github.com/user-attachments/assets/c163881d-c3a6-4f43-9bef-3ed7a338d28a" />


## Result:
The program successfully executed to implement protected member with integer values.
