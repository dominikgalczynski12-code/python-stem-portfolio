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
**Output**

