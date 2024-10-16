# Dictionary to store account details
accounts = {
    'ramu': {'pin': 123, 'balance': 1000},
    'gayatri': {'pin': 456, 'balance': 5000},
    'roja': {'pin': 789, 'balance': 1500}
}

# Function to check if login is successful
def login(name, pin):
    if name in accounts and accounts[name]['pin'] == pin:
        return True
    else:
        return False

# Function to deposit money
def deposit(name, amount):
    if amount > 0:
        accounts[name]['balance'] += amount
        print(f"deposited successfully\nyour current balance is: {accounts[name]['balance']}")
    else:
        print("Invalid deposit amount.")

# Function to withdraw money
def withdraw(name, amount):
    if amount > 0 and amount <= accounts[name]['balance']:
        accounts[name]['balance'] -= amount
        print(f"withdrawn successfully\nyour current balance is: {accounts[name]['balance']}")
    elif amount > accounts[name]['balance']:
        print("Insufficient balance.")
    else:
        print("Invalid withdrawal amount.")

# Function to check balance
def check_balance(name):
    print(f"Your current balance is: {accounts[name]['balance']}")

# Main ATM Interface
def atm():
    print("Welcome to the ATM!")
    
    name = input("Enter your account name: ")
    pin = int(input("Enter your pin: "))
    
    # Login check
    if login(name, pin):
        print("Login successful!")
        
        while True:
            print("\nChoose an option:")
            print("1. Deposit")
            print("2. Withdraw")
            print("3. Check Balance")
            print("4. Exit")
            
            choice = input("Enter your choice: ")
            
            if choice == '1':
                amount = float(input("Enter amount to deposit: "))
                deposit(name, amount)
                break
               
            
            elif choice == '2':
                amount = float(input("Enter amount to withdraw: "))
                withdraw(name, amount)
                break
               
                
            elif choice == '3':
                check_balance(name)
                break
               
                
            elif choice == '4':
                print("Thank you for using the ATM!")
                break
                
            else:
                print("Invalid choice. Please try again.")
                
    else:
        print("Invalid account name or pin.")
        atm()

# Run the ATM
atm()
