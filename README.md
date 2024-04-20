# Bank-mangment-system
print("Bank Management System Program")
import getpass

# Collecting user information
name = input("Enter your name: ")
cnic = input("Enter your ID card number in 0000000000000 format: ")
address = input("Enter your address: ")
age = input("Enter your age: ")
cellno = input("Enter your cell number: ")
username = input("Create your username: ")
password = input("Create your password: ")
amount = int(input("Deposit your amount: "))

# Login loop
for i in range(3):
    a = input("Enter your username: ")
    b = getpass.getpass(prompt="Enter your password: ")

    if a == username and b == password:
        print("You have logged in successfully!")
        print("1. Withdraw\n2. Balance Inquiry\n3. Fast Cash\n4. Check your balance")
        choice = int(input("Enter your choice: "))

        if choice == 1:
            withdrawal_amount = int(input("Select your amount: "))
            print("Your remaining balance is:", amount - withdrawal_amount)
            break
        else:
            print("Try again")
            break
    else:
        print("Invalid username or password. Please try again.")
