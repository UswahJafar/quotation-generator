# quotation-generator
a GUI based application that shows quotations every time click "new" button
<br>
import random

# List of sample quotes
quotes = [
    "The only limit to our realization of tomorrow is our doubts of today.",
    "Success is not in what you have, but who you are.",
    "Don't watch the clock; do what it does. Keep going.",
    "Believe you can and you're halfway there.",
    "Act as if what you do makes a difference. It does."
]

# Function to change the quote
def new_quote():
    quote = random.choice(quotes)
    quote_label.config(text=quote)

# Create main window
root = tk.Tk()
root.title("Quotation Generator")
root.geometry("400x200")

# Create label to display the quote
quote_label = tk.Label(root, text=random.choice(quotes), wraplength=380, justify="center", font=("Arial", 12))
quote_label.pack(pady=20)

# Create button to get new quote
new_button = tk.Button(root, text="New", command=new_quote)
new_button.pack()

# Run the GUI loop
root.mainloop()
