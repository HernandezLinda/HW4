# HW4
// Name: Linda Hernandez
// Date: 11/6/2018
// Class: COP2000 T 6:30
// Assignment: Homework Assignment 4 Race Results Program
// This program allows one to enter three race time and the racer's first name.
// It will determine the lowest, the highest, and the average.
#include <iostream>
#include <string>
using namespace std;

void welcome();
void getRaceTimes(string &, double &);
void findWinner (string &,  double &);
void raceAverage(double &);

int main()
{
   const int NUMBER_OF_RACERS = 3;
   string racer_one, racer_two, racer_three
   double time_one, time_two, time_three;
   
   string racer_names = string[NUMBER_OF_RACERS];
   
   double racer_times = double[NUMBER_OF_RACERS];

   welcome();
   getRaceTimes(racer_one, time_one);
   cout << endl;
   getRaceTimes(racer_two, time_two);
   cout << endl;
   getRaceTimes(racer_three, time_three);
   cout << endl;
   findWinner (racer_one, racer_two, racer_three, times_one, time_two, time_three);
   double result = raceAverage(time_one, time_two, time_three);
   cout << "The overall average of the race " << result << "." << endl;
   
   return 0;
   
}

void raceAverage(double race_times)
{
    
    average = (time_one + time_two + time_three)/3; << endl;
    cout << average;
    return average;
}
void findWinner (string racer_one, string racer_two, string racer_three, double times_one, double times_two, double times_three)
{
    if((time_one < time_two) && (time_one < time_three))
    {
        cout << "Congratulations " << racer_one << " you are the winner!" << endl;
    }
    else if((time_two < time_one) && (time_two < time_three))
    {
        cout << "Congratulations " << racer_two << " you are the winner!" << endl;
    }
    else if((time_three < time_one) && (time_three < time_two))
    {
        cout << "Congratulations " << racer_three << " you are the winner!" << endl;
    }
    else if((time_two < time_one) && (time_two == time_three))
    {
        cout << "Congratulations " << racer_two << " and " << racer_three << " you are the winners" << endl;
    }
    else if((time_three < time_two) && (time_three == time_one))
    {
        cout << "Congratulations " << racer_one << " and " << racer_three << " you are the winners" << endl;
    }
    else if((time_two < time_three) && (time_two == time_one))
    {
        cout << "Congratulations " << racer_one << " and " << racer_two << " you are the winners" << endl;
    }
    else
    {
        cout << "We have a 3 way tie! There is no winner for this race." << endl;
    }
    return;
}
void getRaceTimes(string &racer_names, double &racer_times)
{
    cout << "Please enter racer's name:" << endl;
    cin >> racer_names;
    cout << "Please enter racer's time:" << endl;
    cin >> racer_times;
    while(racer_time <= 0)
    {
     cout << "Your input time is invaild. Please enter a valid time." << endl;
     cin >> racer_times;
    }
    return;
}
void welcome()
{
    cout << "************************************************" << endl;
    cout << "Welcome to Race Results Program." << endl;
    cout << "You are asked to Enter Three Racer’s Names" << endl;
    cout << "and their respective Race Times." << endl;
    cout << "Please enter a real number for Race Time." << endl;
    cout << "The Race Time must be > 0." << endl;
    cout << "Program Developed by : Linda Hernandez" << endl;
    cout << "************************************************" << endl;
    return;
}
