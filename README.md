Counting the sum of numbers in a string
In this article we will learn how to write a C++ program to count the sum of numbers in a string. To count the sum of numbers first we have to find the numbers among all the characters present in the string. For this process we will be using a for loop that will iterate each character from the string and when we will reach the end of the string then we will terminate the loop. We will  count the sum of numbers found, in this loop only and then we can print the result.

Capitalize The First and Last Letter in java
Here we need to count the sum of the number present in the string in the string we can have alphabets as well as some digits so we need to find the sum of the digits

Using ASCII values
Using inbuild function
First we can iterate through the string and check if the character is in range of ‘0’ to ‘9’ if that is the case we will add it to the sum and then print the result.

Using inbuild function we can do the same that is iterate throughout the string and check if the character is a digit or not using isdigit() function.

Algorithm:
Initialize the variables.
Accept the input.
Initialize a for loop.
Iterate each character of the string through the loop.
If the character iterated is a numeric value then,  add that value.
Terminate loop at the end of string.
Print result.
C++ programming code to count the sun of numbers in a string
Run
#include<iostream>
using namespace std;

int findSum(string str)
{
int sum = 0;
for (char ch : str)
{
if (isdigit(ch))
{
sum += ch - '0';
}
}
return sum;
}
int main()
{
string str="Pr22e44pinsta";
cout << "Sum :" << findSum(str) << endl;
}
Output
Sum :12
Method 2
Run
#include <iostream> 
using namespace std;
int main()
{
    //Initializing variables.
    char str[100]="4PREP2INSTA6";
    int i,sum = 0;
    
    //Iterating each character through for loop.
    for (i= 0; str[i] != '\0'; i++)
    {
        if ((str[i] >= '0') && (str[i] <= '9'))  //Checking for numeric characters.
        {
            sum += (str[i] - '0'); //Adding numeric characters.
        }
    }
    //Printing result.
    cout<<"Sum of all digits:"<< sum;
    return 0; 
}
Output
Sum of all digits:12
