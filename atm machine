class ATM:
    def __init__(self, pin, balance=0):
        self.pin = pin
        self.balance = balance
        self.transactions = []

    def check_pin(self, entered_pin):
        return self.pin == entered_pin

    def balance_inquiry(self):
        print(f"Your current balance is: ${self.balance}")

    def cash_withdrawal(self, amount):
        if amount > self.balance:
            print("Insufficient funds.")
        else:
            self.balance -= amount
            self.transactions.append(f"Withdrawn: ${amount}")
            print(f"${amount} withdrawn successfully. Current balance: ${self.balance}")

    def cash_deposit(self, amount):
        self.balance += amount
        self.transactions.append(f"Deposited: ${amount}")
        print(f"${amount} deposited successfully. Current balance: ${self.balance}")

    def change_pin(self, old_pin, new_pin):
        if self.check_pin(old_pin):
            self.pin = new_pin
            print("PIN changed successfully.")
        else:
            print("Incorrect old PIN. PIN change failed.")

    def transaction_history(self):
        if not self.transactions:
            print("No transactions found.")
        else:
            print("Transaction history:")
            for transaction in self.transactions:
                print(transaction)

def main():
    # Initialize the ATM with a default PIN and balance
    atm = ATM(pin="1234", balance=500)

    # Basic user interaction loop
    while True:
        print("\nATM Menu:")
        print("1. Balance Inquiry")
        print("2. Cash Withdrawal")
        print("3. Cash Deposit")
        print("4. Change PIN")
        print("5. Transaction History")
        print("6. Exit")

        choice = input("Enter your choice: ")

        if choice == '1':
            atm.balance_inquiry()
        elif choice == '2':
            amount = float(input("Enter amount to withdraw: "))
            atm.cash_withdrawal(amount)
        elif choice == '3':
            amount = float(input("Enter amount to deposit: "))
            atm.cash_deposit(amount)
        elif choice == '4':
            old_pin = input("Enter old PIN: ")
            new_pin = input("Enter new PIN: ")
            atm.change_pin(old_pin, new_pin)
        elif choice == '5':
            atm.transaction_history()
        elif choice == '6':
            print("Exiting the ATM. Thank you!")
            break
        else:
            print("Invalid choice. Please try again.")

if __name__ == "__main__":
    main()