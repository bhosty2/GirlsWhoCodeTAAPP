# GirlsWhoCodeTAAPP
/*
Brittany Hosty
Girls Who Code TA application
Rock Paper Scissors game
*/

#include <iostream>
#include <ctime> 
#include <cstdlib>
using namespace std;

int main()
{
	int repeat_game = 1;
	do
	{
		int choice = 0;
		cout << "This is a program to play Rock Paper Scissors against a computer opponent" << endl;
		cout << "Please enter '1' for Rock, '2' for Paper, and '3' for Scissors: ";
		cin >> choice;
		cout << endl;


		srand(time(NULL));
		int random_integer = (rand() % 3) + 1;

		cout << "Rock" << endl;
		cout << "Paper" << endl;
		cout << "Scissors" << endl;
		cout << "Shoot" << endl;

		if (random_integer == 1)
		{
			if (random_integer < choice)
				cout << "The Computer chose 'Rock'. You win!" << endl;
			else if (random_integer = choice)
				cout << "The Computer chose 'Rock'. It's a tie!" << endl;
		}
		else if (random_integer == 2)
		{
			if (random_integer < choice)
				cout << "The Computer chose 'Paper'. You win!" << endl;
			else if (random_integer == choice)
				cout << "The Computer chose 'Paper'. It's a tie!" << endl;
			else
				cout << "The Computer chose 'Paper'. You lose!" << endl;
		}
		else
		{
			if (random_integer > choice)
				cout << "The Computer chose 'Scissors'. You lose!" << endl;
			else
				cout << "The Computer chose 'Scissors'. It's a tie!" << endl;
		}
		cout << "Do you want to play again?" << endl;
		cout << "Enter 1 to play again. Press any other key to exit" << endl;
		cin >> repeat_game;
		system("CLS\");
	} while (repeat_game == 1);
	return 0;
}
