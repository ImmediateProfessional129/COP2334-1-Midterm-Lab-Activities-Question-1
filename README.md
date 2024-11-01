# COP2334-1-Midterm-Lab-Activities-Question-1
This is a repository for the Midterm Lab Activity Question 1 Answer

// This program is designed to determine the current hour and type of day to calculate the total amount for the toll price.

// Include the necessary libraries
#include <iostream>
using namespace std;
// Declare the main function
#include <iostream>
using namespace std;

double CalcToll(int hour, bool Morning, bool Weekend) { // Declare the function with the parameters
  if (Weekend) { // If the day is a weekend
    if (hour < 7) { // If the hour is before 7.
      return 6.05;
    }
    else if (hour >= 7 && 20) { // If the hour is between 7 and 8.
      return 7.15;
    }
    else { // If the hour is after 8.
      return 6.10;
    }
  }
  else { // If the day is not a weekend
    if (hour < 7) { // If the hour is before 7.
      return 6.15;
    }
    else if (hour >= 7 && 10) { // If the hour is between 7 and 10.
      return 7.95; 
    }
    else if (hour >= 7 && 15) { // If the hour is between 7 and 15.
      return 6.90;
    }
    else if (hour >= 7 && 20) { // If the hour is between 7 and 20.
      return 8.95;
    }
    else { // If the hour is after 20.
      return 6.40;
    }
  }
}

int main() { // Declare the main function
  int hour; // Declare the variable for the hour
  bool Morning;
  bool Weekend; // Declare the variables for the morning and weekend
  cout << "What is the current hour in your area?: ";
  cin >> hour; // Get the current hour
  cout << "Is it morning? (Y for yes, N for no): ";
  cin >> Morning; // Get the morning
  cout << "Is it a weekend? (1 for yes, 0 for no): ";
  cin >> Weekend; // Get the weekend
  cout << "Your toll is: $" << CalcToll(hour, Morning, Weekend) << endl; // Print the toll price
  return 0;
}
