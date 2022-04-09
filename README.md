# Lab-4C: This program calculates a customer's change by subtracting the amount entered into the vending machine by the amount purchased, and then displays the change in a combination of quarters, dimes, nickels, and pennies.

#include <iostream>

using namespace std;

int main()
{
	char user_input;
	do
	{
		cout << "\nEnter amount into Vending Machine: $";
		double amountVending;
		cin >> amountVending;

		cout << "Enter amount of Purchase: $";
		double amountPurchase;
		cin >> amountPurchase;

		amountVending = amountVending * 100;
		amountPurchase = amountPurchase * 100;

		int cents = amountVending - amountPurchase;

		int quarters = cents / 25;
		cents = cents % 25;
		int dimes = cents / 10;
		cents = cents % 10;
		int nickels = cents / 5;
		cents = cents % 5;
		int pennies = cents;

		cout << endl;

		cout << "Customer's Change: " << endl;
		cout << "Quarters: " << quarters << endl;
		cout << "Dime: " << dimes << endl;
		cout << "Nickels: " << nickels << endl;
		cout << "Pennies: " << pennies << endl;

		cout << endl;

		cout << "Do you want to enter another value? (Y/N) ";
		cin >> user_input;

	} while (user_input != 'N');

	cout << endl;
	system("PAUSE");
	return 0;
}
