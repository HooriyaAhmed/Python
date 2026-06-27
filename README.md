#Data Abstraction
#Data ko hide karke sirf method se access karwana
class BankAccount:
    def __init__(self, balance):
        self.__balance = balance   # hidden data

    def deposit(self, amount):
        self.__balance += amount

    def get_balance(self):
        return self.__balance
    

acc = BankAccount(1000)

acc.deposit(500)

print(acc.get_balance())  # 1500



"""Kya hidden hai?
__balance direct access nahi ho sakta
Sirf methods se access hota hai

👉 Ye Data Abstraction hai"""





#2. Process Abstraction (real code example)

#Process/logic ko hide karke simple function dena

class WashingMachine:
    def start_wash(self):
        self.__fill_water()
        self.__add_detergent()
        self.__wash_clothes()
        print("Washing completed")

    def __fill_water(self):
        print("Filling water")

    def __add_detergent(self):
        print("Adding detergent")

    def __wash_clothes(self):
        print("Washing clothes")
        
        
        
        
        
wm = WashingMachine()
wm.start_wash()


"""Kya hidden hai?

User sirf:

wm.start_wash()

Andar kya ho raha hai:

water fill
detergent add
washing process

👉 Ye Process Abstraction hai"""


"""💡 Super simple yaad rakhna:
Data Abstraction = data hide (variables)
Process Abstraction = steps hide (logic/functions)"""


#“andar ke steps (process) hide kar dena, aur user ko sirf ek simple function dena Yani user ko yeh nahi pata hota ke kaam kaise ho raha hai, bas result mil jata hai.
""""Process abstraction means user ko sirf function use karna hota hai, andar ka process hidden hota hai"""
