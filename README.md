# Python programming Portfolio

**Ossie Bannister**
**Bishop's Stortford College**
**Python for STEM**
**Year 12**

---

## About me

I am a year 12 student and I have been attempting python since September 2025.I study: Business, Geography and Design and Technology and I am currently predicted B,C,A but am aspiring to achieve A* (Design and Technology) A (Business) and B (Geography). I am currently planning on studying Business management at either Loughbourogh, Exeter or Nottingham for September of 2027.

---

## Course Overview

This portfolio documents my progress through a Python programming course designed for students preparing for STEM pathways at university. The course covers:

1) Python fundamentals (variables, input/output and data types)
2) Control structures (loop and conditionals)
3) Functions and modular code
4) Data structures (lists, dictionaries, tuples and sets)
5) Validation and error handling
6) File handling
7) Object-Orientated Programming (OOP)
8) Version control with Git and GitHub
9) Working with Jupyter Notebooks

---

## Portfolio Projects

|#| Project | Key Skills | Status |
|---|---|---|---|
|1| [Unit Converter](#) | Variables, functions and input/output | ✅ Complete |
|2| [Number Guessing Game](#) | Loops, conditionals and random | ✅ Complete |
|3| [To-Do List](#) | Lists, functions and data structures | ✅ Complete |
|4| [Student Grade Calculator](#) | Dictionaries, validation and error handling | ✅ Complete |
|5| [OOP Bank Account](#) | Classes and OOP principles | ✅ Complete |
|6| [Data Analysis Notebook](#) | Jupyter Notebook and data exploration | ✅ Complete |

---

## Skills I Have Developed

**Programming Concepts**
1) Wrting clean with well-commented Python code
2) Using function to organise and reuse code
3) Handling user input safely with validation

**Tools and Technologies**
1) Python 3 (Thonny IDE)
2) Jupyter Notebooks
3) Git version control
4) GitHub for code sharing and portfolio management
5) Markdown for documentation

## Contact

**GitHub:** OssieBannister
**Email:** 26bannio@bscmail.org

# Python projects 

## Unit Converter
```python
def km_to_miles(km):
    """Convert kilometres to miles."""
    miles = km * 0.621371
    return miles

def miles_to_km(miles):
    """Convert miles to kilometres."""
    km = miles / 0.621371
    return km

def c_to_f(c):
    """Convert Celsius to Fahrenheit."""
    return (c * 9/5) + 32

def f_to_c(f):
    """Convert Fahrenheit to Celsius."""
    return (f - 32) * 5/9


def show_menu():
    print("=== Unit Converter ===")
    print("1. Kilometres to Miles")
    print("2. Miles to Kilometres")
    print("3. Celsius to Fahrenheit")
    print("4. Fahrenheit to Celsius")
    print("5. Exit")


def main():
    while True:
        show_menu()
        choice = input("Enter your choice (1-5): ")

        if choice == "1":
            km = float(input("Enter kilometres: "))
            result = km_to_miles(km)
            print(f"{km} km = {result:.2f} miles\n")

        elif choice == "2":
            miles = float(input("Enter miles: "))
            result = miles_to_km(miles)
            print(f"{miles} miles = {result:.2f} km\n")

        elif choice == "3":
            c = float(input("Enter Celsius: "))
            result = c_to_f(c)
            print(f"{c}°C = {result:.2f}°F\n")

        elif choice == "4":
            f = float(input("Enter Fahrenheit: "))
            result = f_to_c(f)
            print(f"{f}°F = {result:.2f}°C\n")

        elif choice == "5":
            print("Goodbye!")
            break

        else:
            print("Invalid choice. Please enter 1–5.\n")


main()

```

### Number Quessing Game
```python
import random

def play_game():
    """Play one round of the guessing game."""
    secret = random.randint(1, 100)
    attempts = 0
    
    print("I'm thinking of a number between 1 and 100.")
    
    while True:
        guess = int(input("Your guess: "))
        attempts += 1
        
        if guess < secret:
            print("Too low! Try again.")
        elif guess > secret:
            print("Too high! Try again.")
        else:
            print(f"Correct! You got it in {attempts} attempts.")
            break

play_game()

```

### To-Do List Manager
```python
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


