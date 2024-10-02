// Benson Chen
// Homework 2 Part 2
// 10/01/24

#include <iostream>
using namespace std;

int main()
{   
    float score; //Variable to contain the score the user inputs
    float highest_score = 0; //Contains the highest scoring number
    float lowest_score = 10; //Contains the lowest scoring number
    float sum = 0; //Contains the sum of all the user inputs
    float final_score; //Contains the final score after all the calculations

    //For loop - set integer i = 1, iterates through this loop 6 times, each time increasing i by 1.
    for(int i = 1; i <= 6; i++)
    {   
        //Asks for user input - using i to keep track of which judge gave what score
        cout << "Enter judge score " << i << " (0.0 - 10.0): "; 
        cin >> score;

        /*If the score the user inputs is greater than 0 (highest_score's value)
        then that input will be saved as the highest score for now*/
        if(score > highest_score)
            highest_score = score; //If there is a higher score than the current one, it will replace the current highest score

        /*If the score the user inputs is less than 10 (lowest_score's value
        then tha tinput will be saved as the lowest score for now)*/
        if(score < lowest_score)
            lowest_score = score; //If there is a lower score than the current one, it will replace the current lowest score
        
        sum += score; //Adds each score the user inputs into a single value
    }

    //Takes the total sum of all the scores and subtracts the highest and lowest scores before dividing the entire thing by 4
    final_score = (sum - lowest_score - highest_score)/4;
    //Prints the final score
    cout << "The final score for this hackathon project is: " << final_score;

    return 0;
}
/*
Enter judge score 1 (0.0 - 10.0): 4.3
Enter judge score 2 (0.0 - 10.0): 7.9
Enter judge score 3 (0.0 - 10.0): 1.5
Enter judge score 4 (0.0 - 10.0): 6.6
Enter judge score 5 (0.0 - 10.0): 10
Enter judge score 6 (0.0 - 10.0): 8.3
The final score for this hackathon project is: 6.775
*/