# Ex.No:5
# Ex.Name:Write a C++ program to pass the string "Shiva" to the parameterized constructor of a base class through a derived class constructor. 
## Date:21/8/25
## Aim:
Write a C++ program to pass the string "Shiva" to the parameterized constructor of a base class through a derived class constructor. 


## Algorithm:
Start the program.

Create a base class with:

A parameterized constructor that accepts a string value.

A statement to store or display the received string.

Create a derived class inheriting from the base class.

In the derived class constructor:

Call the base class parameterized constructor and pass the string "Shiva".

In main():

Create an object of the derived class (which triggers the constructor chain).

End the program.

## Program:
```
#include <iostream>
#include <string>
using namespace std;

// Base class
class Base {
public:
    Base(string name) {
        cout << "The name passed to the base class is " << name << endl;
    }
};

// Derived class
class Derived : public Base {
public:
    Derived(string name) : Base(name) {   // passing parameter to base class constructor
        cout << "The name " << name << " is passed through the derived class constructor" << endl;
    }
};

// Main function
int main() {
    // Create derived class object with name "Shiva"
    Derived obj("Shiva");
    return 0;
}
```



## Output:

<img width="1030" height="361" alt="image" src="https://github.com/user-attachments/assets/3afd6378-b35c-491b-972f-1464c9493dca" />




## Result:
Hence the program is executed sucessfully.

