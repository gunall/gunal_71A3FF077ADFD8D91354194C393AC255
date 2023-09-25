class BankAccount:
  def __init__(self,account_number,account_holder_name,initial_balance=0.0):
   self.__account_number=account_number
   self.__account_holder_name=account_holder_name
   self.__account_balance=initial_balance
  def deposit(self,amount):
    if amount>0:
      self.__account_balance+=amount
      print("Deposited Rs{} New Balance       is:Rs{}".format(amount,self.__account_balance))
    else:
      print("Invalid Deposit Amount!Please Enter a Positive Amount")
  def withdraw(self,amount):
    if amount>0 and amount<=self.__account_balance:
      self.__account_balance-=amount
      print("Withdraw Rs{}. New Balance{}".format(amount,self.__account_balance))
    else:
      print("You have insufficient Balance!")
  def display_balance(self):
    print("Account Balance for {} is Acconunt Number:{} Account Balance is: Rs{}".format(self.__account_holder_name,self.__account_number,self.__account_balance))
account=BankAccount(account_number='1234567',account_holder_name='V.Balasubramanian',initial_balance=5000.0)
account.display_balance()
account.deposit(500.0)
account.withdraw(250.0)
account.display_balance()