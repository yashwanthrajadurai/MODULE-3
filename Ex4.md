# Ex.No:4
# Ex.Name: To develop a c++ program for Electricity Bill calculation using multilevel inheritance (use service no ,name, previous reading, current reading, unit consumption & amount as data members)( units<=100 per unit Rs.2.50 ,units>100 and unit<=300 rs=3.50,unit 301 to 500  rs.5.50 per unit,units above 500 rs 7.50 per unit)
## Date:21/8/25
## Aim:
To develop a c++ program for Electricity Bill calculation using multilevel inheritance (use service no ,name, previous reading, current reading, unit consumption & amount as data members)( units<=100 per unit Rs.2.50 ,units>100 and unit<=300 rs=3.50,unit 301 to 500  rs.5.50 per unit,units above 500 rs 7.50 per unit)


## Algorithm:
Start the program.

Create the first base class with:

Data members: service number, name.

A method to read these details.

Create the second class derived from the first class with:

Data members: previous reading, current reading, unit consumption.

A method to read meter readings.

A method to calculate unit consumption as:

units
=
current
−
previous
units=current−previous

Create the third class derived from the second class with:

Data member: amount.

A method to calculate bill amount using the conditions:

If units ≤ 100 → rate = 2.50

If units > 100 and ≤ 300 → rate = 3.50

If units > 300 and ≤ 500 → rate = 5.50

If units > 500 → rate = 7.50

Compute:

amount
=
units
×
rate
amount=units×rate

A method to display all details and bill amount.

In main():

Create an object of the last derived class.

Call methods to read customer details and meter readings.

Call method to calculate units and bill amount.

Call method to display the bill.

End the program.

## Program:
```
#include <iostream>
using namespace std;

// Base class: stores service number and name
class Service {
protected:
    int service_no;
    string name;
public:
    void getServiceDetails() {
        cin >> service_no >> name;
    }
};

// Derived class 1: stores previous and current reading, calculates units consumed
class Meter : public Service {
protected:
    int previous_reading, current_reading;
    int units_consumed;
public:
    void getMeterReadings() {
        cin >> previous_reading >> current_reading;
        units_consumed = previous_reading - current_reading;
    }
};

// Derived class 2: calculates the amount based on units consumed and displays all details
class Bill : public Meter {
    double amount;
public:
    void calculateAmount() {
        if (units_consumed <= 100)
            amount = units_consumed * 2.50;
        else if (units_consumed > 100 && units_consumed <= 300)
            amount = 100 * 2.50 + (units_consumed - 100) * 3.50;
        else if (units_consumed > 301 && units_consumed <= 500)
            amount = 100 * 2.50 + 200 * 3.50 + (units_consumed - 300) * 5.50;
        else
            amount = 100 * 2.50 + 200 * 3.50 + 200 * 5.50 + (units_consumed - 500) * 7.50;
    }

    void displayBill() {
        cout << "service number:" << service_no << endl;
        cout << "service name:" << name << endl;
        cout << "unit consumption:" << units_consumed << endl;
        cout << "amount:" << amount << endl;
    }
};

int main() {
    Bill customer;
    customer.getServiceDetails();
    customer.getMeterReadings();
    customer.calculateAmount();
    customer.displayBill();
    return 0;
}
```



## Output:

<img width="1037" height="668" alt="image" src="https://github.com/user-attachments/assets/fb5de67d-6378-4044-aec5-39cde56d94db" />


## Result:
Hence the program is executed successfully.

