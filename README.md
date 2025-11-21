Book Rewards Calculator (Python & Tkinter)

This project is a desktop-based rewards points calculator built using Python’s tkinter library. The application allows users to enter the number of books purchased in a month and calculates the corresponding reward points through an interactive GUI.

Overview:
The application demonstrates how to create a simple GUI, handle user input, and implement conditional logic in Python. When launched, the interface displays an instruction label, an input field for the number of books, buttons to compute points or clear results, and an area where the points earned are displayed.

Features:

Graphical interface built with tkinter

Calculates reward points based on monthly book purchases

Input validation for non-numeric entries

Clear button to reset input and output fields

How the Program Works:

Input Handling:
The user enters the number of books purchased in a text field. The program checks whether the input is numeric. If the input is invalid, an error message is displayed.

Points Calculation:

0 or 1 books: 0 points

2 to 3 books: 5 points

4 to 5 books: 15 points

6 to 7 books: 30 points

8 or more books: 60 points

Button Functions:

Compute Points: Calculates and displays points based on the number of books entered

Clear Result: Clears the input field and resets the displayed result

Each function updates the result label immediately based on the user’s input and provides feedback if the input is invalid.

Requirements:

Python 3.x

tkinter (included with standard Python installations)

How to Run:
Run the program from a terminal or command prompt using:
python book_rewards_calculator.py
