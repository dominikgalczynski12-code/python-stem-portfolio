# Python-Stem-Portfolio
#Python Programming Portfolio - Bishop's Stortford College STEM course

**Dominik Galczynski**
**Bishop's Stortford College**
**Python for STEM**
**Year 12**

---
## About Me
I am currently a student at Bishop Stortford College who is currently studying A level Maths, Chemistry and Economics. I chose these because I enjoy doing quantitve subjects that can challenge me and subjects that have relevance in day to day life.

## Course Overview

This portfolio documents my progress through a Python programming course designed for students preparing for STEM pathways at University:
- Python fundamentals (variables, input/output, data types)
- Control structures (loops and conditionals)
- Functions and modular code
- Data structured (lists, dictionaries, tuples, sets)
- Validation and error handling
- File handling
- Object-oriented programming (OOP)
- Version control with GIT and GITHUB
- Working with Jupyter Notebooks

---

## Portfolio Projects
1. [Unit Converter](#unit-converter) ! Variables, functions, input/output | ✅ Complete 


    1. [Unit Converter](#unit-converter) | 
    

    "| 2 | [Number Guessing Game](#) | Loops, conditionals, random | ✅ Complete |\n",

    "| 3 | [To-Do List](#) | Lists, functions, data structures | ✅ Complete |\n",

    "| 4 | [Student Grade Calculator](#) | Dictionaries, validation, error handling | ✅ Complete \n",
    
    "| 5 | [OOP Bank Account](#) | Classes, OOP principles | ✅ Complete |\n",

    "| 6 | [Data Analysis Notebook](#) | Jupyter Notebooks, data exploration | ✅ Complete |\n",

# Projects

## Unit Converter
**Description**

A program that converts between common units. At minimum:

Kilometres ↔ Miles

Celsius ↔ Fahrenheit

Kilograms ↔ Pounds
    

 


```Python
 def km_to_miles(km): 
   """Convert kilometres to miles.""" 
   miles = km * 0.621371 
   return miles 
 
 
def miles_to_km(miles): 
   """Convert miles to kilometres.""" 
   km = miles / 0.621371 
   return km 
 
 
def celsius_to_fahrenheit(celsius): 
   """Convert Celsius to Fahrenheit.""" 
   fahrenheit = (celsius * 9 / 5) + 32 
   return fahrenheit 
 
 
def fahrenheit_to_celsius(fahrenheit): 
   """Convert Fahrenheit to Celsius.""" 
   celsius = (fahrenheit - 32) * 5 / 9 
   return celsius 
 
 
def kg_to_pounds(kg): 
   """Convert kilograms to pounds.""" 
   pounds = kg * 2.20462 
   return pounds 
 
 
def pounds_to_kg(pounds): 
   """Convert pounds to kilograms.""" 
   kg = pounds / 2.20462 
   return kg 
 
 
def litres_to_pints(litres): 
   """Convert litres to pints.""" 
   pints = litres * 1.75975 
   return pints 
 
 
def pints_to_litres(pints): 
   """Convert pints to litres.""" 
   litres = pints / 1.75975 
   return litres 
 
 
def show_menu(): 
   print("=== Unit Converter ===") 
   print("1. Kilometres to Miles") 
   print("2. Miles to Kilometres") 
   print("3. Celsius to Fahrenheit") 
   print("4. Fahrenheit to Celsius") 
   print("5. Kilograms to Pounds") 
   print("6. Pounds to Kilograms") 
   print("7. Litres to Pints") 
   print("8. Pints to Litres") 
 
 
def get_number(message): 
   """Ask the user for a number and stop the program crashing if they type letters.""" 
   try: 
       number = float(input(message)) 
       return number 
   except ValueError: 
       print("Please enter a valid number.") 
       return None 
 
 
def main(): 
   show_menu() 
 
   choice = input("Enter your choice (1-8): ") 
 
   if choice == "1": 
       km = get_number("Enter kilometres: ") 
       if km is not None: 
           result = km_to_miles(km) 
           print(f"{km} km = {result:.2f} miles") 
 
   elif choice == "2": 
       miles = get_number("Enter miles: ") 
       if miles is not None: 
           result = miles_to_km(miles) 
           print(f"{miles} miles = {result:.2f} km") 
 
   elif choice == "3": 
       celsius = get_number("Enter Celsius: ") 
       if celsius is not None: 
           result = celsius_to_fahrenheit(celsius) 
           print(f"{celsius}°C = {result:.2f}°F") 
 
   elif choice == "4": 
       fahrenheit = get_number("Enter Fahrenheit: ") 
       if fahrenheit is not None: 
           result = fahrenheit_to_celsius(fahrenheit) 
           print(f"{fahrenheit}°F = {result:.2f}°C") 
 
   elif choice == "5": 
       kg = get_number("Enter kilograms: ") 
       if kg is not None: 
           result = kg_to_pounds(kg) 
           print(f"{kg} kg = {result:.2f} pounds") 
 
   elif choice == "6": 
       pounds = get_number("Enter pounds: ") 
       if pounds is not None: 
           result = pounds_to_kg(pounds) 
           print(f"{pounds} pounds = {result:.2f} kg") 
 
   elif choice == "7": 
       litres = get_number("Enter litres: ") 
       if litres is not None: 
           result = litres_to_pints(litres) 
           print(f"{litres} litres = {result:.2f} pints") 
 
   elif choice == "8": 
       pints = get_number("Enter pints: ") 
       if pints is not None: 
           result = pints_to_litres(pints) 
           print(f"{pints} pints = {result:.2f} litres") 
 
   else: 
       print("Invalid choice. Please enter a number from 1 to 8.") 
 
 
main() 

```
##  Number Guessing Game
**Description**

The computer picks a random number. The player guesses until they get it right. The program tells them if their guess is too high or too low. It counts the number of guesses.






```Python
import random 
 
 
def get_number(message): 
   """Ask the user for a number and stop the program crashing if they type letters.""" 
   try: 
       number = int(input(message)) 
       return number 
   except ValueError: 
       print("Please enter a valid whole number.") 
       return None 
 
 
def choose_difficulty(): 
   """Let the user choose the difficulty level.""" 
   print("=== Choose Difficulty ===") 
   print("1. Easy: 1 to 50") 
   print("2. Medium: 1 to 100") 
   print("3. Hard: 1 to 500") 
 
   choice = input("Enter your choice (1-3): ") 
 
   if choice == "1": 
       return 50 
   elif choice == "2": 
       return 100 
   elif choice == "3": 
       return 500 
   else: 
       print("Invalid choice. Medium difficulty selected.") 
       return 100 
 
 
def play_game(): 
   """Play one round of the guessing game.""" 
   max_number = choose_difficulty() 
   secret = random.randint(1, max_number) 
   attempts = 0 
 
   print(f"\nI'm thinking of a number between 1 and {max_number}.") 
 
   while True: 
       guess = get_number("Your guess: ") 
 
       if guess is None: 
           continue 
 
       attempts += 1 
 
       if guess < secret: 
           print("Too low! Try again.") 
       elif guess > secret: 
           print("Too high! Try again.") 
       else: 
           print(f"Correct! You got it in {attempts} attempts.") 
           return attempts 
 
 
def main(): 
   best_score = None 
 
   print("=== Number Guessing Game ===") 
 
   while True: 
       attempts = play_game() 
 
       if best_score is None or attempts < best_score: 
           best_score = attempts 
           print("New best score!") 
 
       print(f"Best score so far: {best_score} attempts") 
 
       play_again = input("\nDo you want to play again? (yes/no): ") 
 
       if play_again.lower() != "yes": 
           print("Thanks for playing!") 
           break 
 
 
main()



```
 
## To-Do List Manager
**Description**

    

 



```Python
def show_tasks(tasks): 
   """Display all tasks with their numbers.""" 
   if len(tasks) == 0: 
       print("No tasks yet!") 
       return 
    
   print("\n=== Your Tasks ===") 
   for i, task in enumerate(tasks, start=1): 
       print(f"{i}. {task}") 
   print() 
 
def add_task(tasks): 
   """Add a new task to the list.""" 
   new_task = input("Enter task: ") 
   tasks.append(new_task) 
   print(f"Added: '{new_task}'") 
 
def remove_task(tasks): 
   """Remove a task by number.""" 
   show_tasks(tasks) 
   number = int(input("Enter task number to remove: ")) 
   if 1 <= number <= len(tasks): 
       removed = tasks.pop(number - 1) 
       print(f"Removed: '{removed}'") 
   else: 
       print("Invalid number.") 
 
def main(): 
   tasks = [] 
    
   while True: 
       print("=== To-Do List ===") 
       print("1. View tasks") 
       print("2. Add task") 
       print("3. Remove task") 
       print("4. Quit") 
        
       choice = input("Choose: ") 
        
       if choice == "1": 
           show_tasks(tasks) 
       elif choice == "2": 
           add_task(tasks) 
       elif choice == "3": 
           remove_task(tasks) 
       elif choice == "4": 
           print("Goodbye!") 
           break 
 
main() 


```
## Student Grade Calculator
**Description**

    

 



```Python
def get_grade(average): 
   """Return a letter grade based on average percentage.""" 
   if average >= 70: 
       return "A" 
   elif average >= 60: 
       return "B" 
   elif average >= 50: 
       return "C" 
   elif average >= 40: 
       return "D" 
   else: 
       return "U" 
 
 
def get_valid_score(subject): 
   """Ask for a score and keep asking until a valid number is entered.""" 
   while True: 
       try: 
           score = float(input(f"Enter score for {subject} (0-100): ")) 
 
           if 0 <= score <= 100: 
               return score 
           else: 
               print("Score must be between 0 and 100.") 
 
       except ValueError: 
           print("Please enter a number.") 
 
 
def calculate_student_results(): 
   """Collect scores for one student and return their results.""" 
   name = input("\nStudent name: ") 
 
   subjects = ["Maths", "English", "Science"] 
   scores = {} 
 
   for subject in subjects: 
       scores[subject] = get_valid_score(subject) 
 
   average = sum(scores.values()) / len(scores) 
   grade = get_grade(average) 
 
   student = { 
       "name": name, 
       "scores": scores, 
       "average": average, 
       "grade": grade 
   } 
 
   return student 
 
 
def display_student_results(student): 
   """Display results for one student.""" 
   print(f"\n=== Results for {student['name']} ===") 
 
   for subject, score in student["scores"].items(): 
       print(f"{subject}: {score:.1f}") 
 
   print(f"Average: {student['average']:.1f}%") 
   print(f"Grade: {student['grade']}") 
 
 
def display_summary(students): 
   """Display all students ranked by average.""" 
   print("\n=== Class Summary ===") 
 
   students.sort(key=lambda student: student["average"], reverse=True) 
 
   print("Rank | Name | Average | Grade") 
   print("------------------------------") 
 
   rank = 1 
 
   for student in students: 
       print(f"{rank} | {student['name']} | {student['average']:.1f}% | {student['grade']}") 
       rank += 1 
 
 
def main(): 
   students = [] 
 
   print("=== Student Grade Calculator ===") 
 
   while True: 
       student = calculate_student_results() 
       students.append(student) 
 
       display_student_results(student) 
 
       another = input("\nDo you want to enter another student? (yes/no): ") 
 
       if another.lower() != "yes": 
           break 
 
   display_summary(students) 
 
 
main()

```
## OOP Bank Account
**Description**

    

 



```Python










class BankAccount: 
   """A simple bank account class.""" 
 
   def __init__(self, owner, initial_balance=0): 
       """Set up the account with an owner name and starting balance.""" 
       self.owner = owner 
       self.balance = initial_balance 
       self.transactions = [] 
 
       if initial_balance > 0: 
           self.transactions.append(f"Opening balance: £{initial_balance:.2f}") 
 
   def deposit(self, amount): 
       """Add money to the account.""" 
       if amount > 0: 
           self.balance += amount 
           self.transactions.append(f"Deposit: +£{amount:.2f}") 
           print(f"Deposited £{amount:.2f}. New balance: £{self.balance:.2f}") 
       else: 
           print("Deposit amount must be positive.") 
 
   def withdraw(self, amount): 
       """Remove money from the account if funds are available.""" 
       if amount <= 0: 
           print("Withdrawal amount must be positive.") 
       elif amount > self.balance: 
           print(f"Insufficient funds. Balance is only £{self.balance:.2f}") 
       else: 
           self.balance -= amount 
           self.transactions.append(f"Withdrawal: -£{amount:.2f}") 
           print(f"Withdrew £{amount:.2f}. New balance: £{self.balance:.2f}") 
 
   def show_balance(self): 
       """Display the current balance.""" 
       print(f"\nAccount holder: {self.owner}") 
       print(f"Current balance: £{self.balance:.2f}") 
 
   def show_history(self): 
       """Display all transactions.""" 
       print(f"\n=== Transaction History for {self.owner} ===") 
 
       if len(self.transactions) == 0: 
           print("No transactions yet.") 
       else: 
           for transaction in self.transactions: 
               print(transaction) 
 
       print(f"Current balance: £{self.balance:.2f}") 
 
 
class SavingsAccount(BankAccount): 
   """A savings account that adds interest.""" 
 
   def __init__(self, owner, initial_balance=0, interest_rate=2): 
       """Set up the savings account.""" 
       super().__init__(owner, initial_balance) 
       self.interest_rate = interest_rate 
 
   def apply_interest(self): 
       """Increase the balance by the interest rate percentage.""" 
       interest = self.balance * (self.interest_rate / 100) 
       self.balance += interest 
 
       self.transactions.append(f"Interest added: +£{interest:.2f}") 
       print(f"Interest added: £{interest:.2f}") 
       print(f"New balance: £{self.balance:.2f}") 
 
 
def get_money(message): 
   """Ask for a money amount and stop the program crashing.""" 
   while True: 
       try: 
           amount = float(input(message)) 
           return amount 
       except ValueError: 
           print("Please enter a valid number.") 
 
 
def show_menu(): 
   """Display the menu.""" 
   print("\n=== Bank Menu ===") 
   print("1. Deposit") 
   print("2. Withdraw") 
   print("3. Check balance") 
   print("4. View history") 
   print("5. Apply interest") 
   print("6. Exit") 
 
 
def main(): 
   print("=== OOP Bank Account ===") 
 
   name = input("Enter account holder name: ") 
   opening = get_money("Enter opening balance: £") 
   interest_rate = get_money("Enter interest rate percentage: ") 
 
   account = SavingsAccount(name, opening, interest_rate) 
 
   while True: 
       show_menu() 
 
       choice = input("Choose an option (1-6): ") 
 
       if choice == "1": 
           amount = get_money("Amount to deposit: £") 
           account.deposit(amount) 
 
       elif choice == "2": 
           amount = get_money("Amount to withdraw: £") 
           account.withdraw(amount) 
 
       elif choice == "3": 
           account.show_balance() 
 
       elif choice == "4": 
           account.show_history() 
 
       elif choice == "5": 
           account.apply_interest() 
 
       elif choice == "6": 
           print("Thank you for banking with us.") 
           break 
 
       else: 
           print("Invalid choice. Please enter a number from 1 to 6.") 
 
 
main() 

```
 

 



