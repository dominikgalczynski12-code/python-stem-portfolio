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
def km_to_miles(km):
    """Convert kilometres to miles."""
    miles = km  * 0.621371
    return miles

def miles_to_km(miles):
    """Convert miles to kilometres."""
    km = miles / 0.621371
    return km

def celsius_to_fahrenheit(celsius):
    """Convert celsius to fahrenheit"""
    fahrenheit= celsius + 273
    return fahrenheit

def fahrenheit_to_celsius(fahrenheit):
    """Convert fahrenheit to celsius"""
    celsius= fahrenheit - 273
    return celsius


def show_menu():
    print("=== Unit Converter ===")
    print("1. Kilometres to Miles")
    print("2. Miles to Kilometres")
    print("3. Celsius to Fahrenheit")
    print("4. Fahrenheit to Celsius")

def main():
    show_menu()
    choice = input("Enter your choice (1-4): ")
    
    if choice == "1":
        km = float(input("Enter kilometres: "))
        result = km_to_miles(km)
        print(f"{km} km = {result:.2f} miles")

    if choice == "2":
        miles = float(input("Enter miles: "))
        result = miles_to_km(miles)
        print(f"{miles} miles = {result:.2f} km")


    if choice == "3":
        celsius = float(input("Enter Celsius: "))
        result = celsius_to_fahrenheit(celsius)
        print(f"{celsius} celsius = {result:.2f} fahrenheit")

    if choice == "4":
        fahrenheight = float(input("Enter Fahrenheit: "))
        result = fahrenheit_to_celsius (fahrenheit)
        print(f"{fahrenheit} fahrenheit = {result:.2f} celsius")


```Python


```
**Output**

