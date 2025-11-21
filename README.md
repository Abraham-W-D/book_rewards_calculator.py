# book_rewards_calculator.py
import tkinter as tk

#window setup
root = tk.Tk()
root.title("Serendipity Points Calculator")
root.geometry("400x300")
root.resizable(0, 0)
root.configure(bg="light grey")

#functions
def calculate_points():
    user_input = entry_books.get().strip()

    if user_input.isdigit():
        books = int(user_input)

        if books == 0:
            result_label.config(text="You earned 0 points this month!")

        elif books == 1:
            result_label.config(text="You earned 0 points this month!")

        elif 2 <= books <= 3:
            result_label.config(text="You earned 5 points this month!")

        elif 4 <= books <= 5:
            result_label.config(text="You earned 15 points this month!")

        elif 6 <= books <= 7:
            result_label.config(text="You earned 30 points this month!")

        elif books >= 8:
            result_label.config(text="You earned 60 points this month!")

    else:
        result_label.config(text="Invalid input, please try again.")

#clear button
def clear_result():
    entry_books.delete(0, tk.END)
    result_label.config(text="")


#widgets
instruction_label = tk.Label(root, text="Enter the number of books purchased this month:", bg="light grey", fg="black", font=("Arial", 11))
instruction_label.pack(side=tk.TOP)

entry_books = tk.Entry(root, width=10, font=("Arial", 12), justify="center", bg="white", fg="black", relief="flat", bd=1)
entry_books.pack(side=tk.TOP)

compute_button = tk.Button(root, text="Compute Points", command=calculate_points, font=("Arial", 10, "bold"), bg="light grey", fg="black", relief="flat", bd=0, highlightthickness=0, activebackground="light grey")
compute_button.pack(side=tk.TOP)

clear_button = tk.Button(root, text="Clear Result", command=clear_result, font=("Arial", 10, "bold"), bg="light grey", fg="black", relief="flat", bd=0, highlightthickness=0, activebackground="light grey")
clear_button.pack(side=tk.TOP)

result_label = tk.Label(root, text="", bg="light grey", fg="black", font=("Arial", 12, "bold"))
result_label.pack(side=tk.TOP)

root.mainloop()
