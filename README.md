# DSA-Jackpot-Project
Game based on python

# How to create a jackpot game in C++

So today when I was tweaking with random function in C++, I ended up to the idea of making a 3 figures jackpot game. Its as simple as it is sounding. All I did was, seeded and randomized 3 numbers (0,1,2) three times and stored them in three different variables and then I compared all the values separately to check whether I won or lost.

Here's the basic source code, for full code, you may download it here.
Archieve password: gautamknow.blogspot.com

#include <iostream.h> #include <stdlib.h> #include <stdio.h> #include <windows.h>

int r1,r2,r3,val=1000; // Random numbers and the initial money in your pocket declared char choice, name[31]; // Variable for choice y / n, array for your name declared void main() // Start of function main() {

cout << "Enter your name:\n"; gets( name );

profile: // Return place for goto profile statement cout << "----------Profile-----------" << endl; // Profile cout << "Name: " << name <<< endl; cout << "You have $" << val << " right now" << endl; cout << "---------------------------" << endl;

// Loop that will be executed as long as you have at least $100 and you choose yes when asked for re-try do {
cout << "Generating random numbers..." << endl; randomize(); r1 = random (5); cout << r1; r2 = random (5); cout << r2; r3 = random (5); cout << r3;

  if ( (r1==r2)&&(r2==r3) )                                                   // Statements for if you win
{ cout << "Congratulations! You won $500!" << endl; cout << "You now have $" << val+500 << endl; cout << "Try for more?(y/n)" cin >> choice; }

else                                                                                        // Statements for if you lose
{ cout << "Sorry! You lost $100!" << end; cout << "You now have $" << val-100 << endl; cout << "Try again?(y/n)" cin >> choice; } } while ( ( choice == 'y' || choice =='Y' ) && ( val >= 100 ) ); // End of do-while goto profile;

}
