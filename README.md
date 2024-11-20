This is an ATM simulator that retains data even after exiting the program, you can use persistent storage like a file or a database.

How it works:
Persistence: The program saves the account balance in a JSON file (atm_data.json) every time you exit.
Data Retention: When you restart the program, it reads the balance from the file.
Menu: You can check your balance, deposit, withdraw, and exit.
Validation: Ensures only valid inputs and amounts are processed.

Functions:
load_data(): Reads the JSON file to get the saved balance. If the file doesn’t exist, it initializes the balance to 0.
save_data(data): Writes the current account data (e.g., balance) to the JSON file when exiting the program.

Main Menu:
Purpose: Provides options for the user to interact with the ATM.
Options:
Check Balance: Displays the current balance loaded from the file.
Deposit Money: Allows the user to add a positive amount to the balance.
Withdraw Money: Allows the user to withdraw an amount if it doesn’t exceed the available balance.
Exit: Saves the updated balance to the JSON file and exits the program.

