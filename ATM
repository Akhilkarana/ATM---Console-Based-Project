bank = {
    101: ["Akhil", "0906", 10000, [9, 6, 2000]],
    102: ["Praveen", None, 20000, [3, 11, 2002]],
    103: ["Sivaji", "9876", 0, [11, 1, 1999]]
}

def withdraw():
    print("Withdraw")
    accno = int(input("Enter your account number: "))
    if accno not in bank:
        print("Invalid Account number")
        return
    print(f"Welcome {bank[accno][0]}")
    pin = input("Enter your Pin: ")
    if pin != bank[accno][1]:
        print("Invalid Pin")
        return
    amt = int(input("Enter amount to withdraw: "))
    if amt > bank[accno][2]:
        print("Insufficient Balance")
    else:
        bank[accno][2] -= amt
        print("Withdraw Successful")

def deposit():
    print("Deposit")
    accno = int(input("Enter your account number: "))
    if accno not in bank:
        print("Invalid Account number")
        return
    print(f"Welcome {bank[accno][0]}")
    pin = input("Enter your Pin: ")
    if pin != bank[accno][1]:
        print("Invalid Pin")
        return
    amt = int(input("Enter amount to deposit: "))
    bank[accno][2] += amt
    print("Deposit Successful")

def pin_generation():
    print("Pin Generation")
    accno = int(input("Enter your account number: "))
    if accno not in bank:
        print("Invalid Account number")
        return
    print(f"Welcome {bank[accno][0]}")
    if bank[accno][1] is not None:
        print("Pin already generated")
        return
    print("Verify Date of Birth: ")
    date = int(input("Enter Birth Date: "))
    month = int(input("Enter Birth Month: "))
    year = int(input("Enter Birth Year: "))
    if [date, month, year] == bank[accno][3]:
        pin = input("Enter your new Pin: ")
        cpin = input("Confirm your Pin: ")
        if pin != cpin:
            print("Pins do not match, try again")
        else:
            bank[accno][1] = pin
            print("Pin Generated Successfully!")
    else:
        print("Incorrect Date of Birth Details")

def mini_statement():
    print("Mini Statement")
    accno = int(input("Enter your account number: "))
    if accno not in bank:
        print("Invalid Account number")
        return
    print(f"Welcome {bank[accno][0]}")
    pin = input("Enter Your Pin: ")
    if pin != bank[accno][1]:
        print("Invalid Pin")
        return
    print(f"Balance: {bank[accno][2]}")

def main():
    while True:
        print("\nChoose the required option: ")
        print("1. Withdraw")
        print("2. Deposit")
        print("3. Pin Generation")
        print("4. Mini statement")
        print("5. Exit")
        choice = int(input())
        
        if choice == 1:
            withdraw()
        elif choice == 2:
            deposit()
        elif choice == 3:
            pin_generation()
        elif choice == 4:
            mini_statement()
        elif choice == 5:
            print("Thank you, visit again!")
            break
        else:
            print("Invalid choice, please try again.")

if __name__ == "__main__":
    main()
