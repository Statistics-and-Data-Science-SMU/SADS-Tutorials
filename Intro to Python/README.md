# Introduction to Python Programming

Below: a great python tutorial! 
https://www.kaggle.com/code/kanncaa1/data-sciencetutorial-for-beginners

# Installation

# Getting Started

Here are the instructions on how to get Python set up:

    Download Python: Visit the official Python website to download the latest version. Make sure to select the version for your operating system.
    Install an IDE: While you can use Python's built-in IDLE, I recommend installing an IDE like VSCode or PyCharm for a better coding experience.
    Verify Installation: Open a terminal or command prompt and type python --version to confirm Python is installed correctly.

Python Files vs. Jupyter Notebooks

    What is a Python script? A Python script is a text file with a .py extension that contains Python code. You can execute these files to run your code.
    What is a Jupyter Notebook? Jupyter Notebooks are interactive web-based documents that allow you to write and execute Python code in blocks. They are excellent for data analysis and visualization. You can install Jupyter with the command pip install jupyter.

Data Handling
Basic Data Structures

Lists: A list is a collection of items.


    fruits = ["apple", "banana", "cherry"]

Dictionaries: A dictionary holds key-value pairs.

    student = {"name": "Alice", "age": 25, "courses": ["Math", "Science"]}

Tuples: A tuple is an immutable collection of items.


    coordinates = (10.0, 20.0)

Data Cleaning

Remove Duplicates:

    To remove duplicates from a list, convert it to a set and back to a list:

    python

    numbers = [1, 2, 2, 3, 4, 4]
    unique_numbers = list(set(numbers))
    print(unique_numbers)  # Output: [1, 2, 3, 4]

Handling Missing Data:

Filter out None values from a list:

    data = [1, None, 3, None, 5]
    cleaned_data = [x for x in data if x is not None]
    print(cleaned_data)  # Output: [1, 3, 5]

Data Analysis with Functions
Basic Operations

Arithmetic Operations: Perform calculations directly.


    a = 10
    b = 5
    print(a + b)  # Output: 15
    
Logical Operations: Use conditions to control flow.


    if a > b:
        print("a is greater than b")

Using Functions

Defining Functions:

Create a function to compute the square of a number.


    def square(x):
        return x * x

    print(square(4))  # Output: 16

Task: Basic Data Manipulation

Calculate Total of a List:

Write a function to sum a list of numbers.


    def total(numbers):
        return sum(numbers)

    print(total([1, 2, 3, 4]))  # Output: 10

Data Visualization (using Matplotlib)
Creating Simple Plots

Install Matplotlib:
        Use the command pip install matplotlib to install the library.

Basic Plot:
        Create a simple line plot.


    import matplotlib.pyplot as plt

    x = [1, 2, 3, 4, 5]
    y = [2, 3, 5, 7, 11]
    plt.plot(x, y)
    plt.title("Simple Line Plot")
    plt.xlabel("X-axis")
    plt.ylabel("Y-axis")
    plt.show()

