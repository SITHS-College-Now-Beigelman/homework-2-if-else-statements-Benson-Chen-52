// Benson Chen
// Homework 2 Part 1
// 10/01/24

#include <iostream>
using namespace std;

int main()
{   
    //Defines the variables of month and day
    int month;
    int day;

    //Asks for the user's input for month and day
    cout << "\nInput the month and day as a number separated by a space: ";
    cin >> month >> day;

    //First if statement - If user inputs any dates within the range of dates specified here then it will print that date doesn't exist
    if(month==2 && day>=30 || month==4 && day>=31 || month==6 && day>=31 || month==9 && day>=31 || month==11 && day>=31)
        cout << "That date doesn't exist!";
    //Uses and/or operators to select the range of dates for Spring
    else if(month>=3 && day>=21 && day<=31 && month<=5 || month>=4 && month<=6 && day>=1 && day<=20)
        cout << "It is now Spring!";
    //Uses and/or operators to select the range of dates for Summer
    else if(month>=6 && month<=8 && day>=21 && day<=31 || month>=7 && month<=9 && day>=1 && day<=22)
        cout << "It is now Summer!";
    //Uses and/or operators to select the range of dates for Autumn
    else if(month>=9 && month <=11 && day>=23 && day<=31 || month>=10 && month<=12 && day>=1 && day<=21)
        cout << "It is now Autumn!";
    //Uses and/or operators to select the range of dates for Winter
    else if (month==12 && day>=22 && day<=31 || month>=1 && month <=3 && day>=1 && day<=20 || month>=1 && month<=2 && day>=21 && day<=31)
        cout << "It is now Winter!";
    /*Any other date that is somehow not in the range or within the specified dates
     in the first if statement will have the program print it doesn't exist.*/
    else
        cout << "That date doesn't exist!";

    return 0;
}
/*
Input the month and day as a number separated by a space: 5 6
It is now Spring!
*/