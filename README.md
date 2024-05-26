# Car Parking System

This is a simple console-based Car Parking System implemented in C++. The system allows users to keep track of cars, bikes, and rickshaws entering a parking lot, display the current count of each vehicle type, and reset the count.

## Features

- **Add Car**: Increment the count of cars in the parking lot.
- **Add Bike**: Increment the count of bikes in the parking lot.
- **Add Rickshaw**: Increment the count of rickshaws in the parking lot.
- **Show Record**: Display the current count of cars, bikes, and rickshaws.
- **Delete Record**: Reset the counts of all vehicle types to zero.
- **Exit**: Exit the program.

## Code

```cpp
#include <bits/stdc++.h>
using namespace std;

int main() {
    cout << "\t*******************************************" << endl;
    cout << "\t\t C A R     P A R K I N G" << endl;
    int car = 0, bike = 0, rikshaw = 0;
    int enter;

    while (true) {
        cout << "Press 1 to Enter Car" << endl;
        cout << "Press 2 to Enter Bike" << endl;
        cout << "Press 3 to Enter Rikshaw" << endl;
        cout << "Press 4 to Show the Record" << endl;
        cout << "Press 5 to Delete the Record" << endl;
        cout << "Press 6 to Exit" << endl;
        cout << "Enter Your choice: ";
        cin >> enter;

        if (enter == 1) {
            car++;
            system("cls");
            cout << "Car is Added" << endl;
        } else if (enter == 2) {
            bike++;
            system("cls");
            cout << "Bike is Added" << endl;
        } else if (enter == 3) {
            rikshaw++;
            system("cls");
            cout << "Rikshaw is Added" << endl;
        } else if (enter == 4) {
            cout << "Car " << car << endl;
            cout << "Bike " << bike << endl;
            cout << "Rikshaw " << rikshaw << endl;
        } else if (enter == 5) {
            car = 0;
            bike = 0;
            rikshaw = 0;
            system("cls");
            cout << "All Record is Deleted....!!" << endl;
        } else if (enter == 6) {
            exit(0);
        } else {
            cout << "Invalid Input" << endl;
        }
    }

    return 0;
}
