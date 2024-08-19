import tkinter as tk
from tkinter import messagebox
from PyDictionary import PyDictionary

# Initialize the PyDictionary object
dictionary = PyDictionary()

# Function to get the definition
def get_definition():
    word = entry.get()
    if word:
        definition = dictionary.meaning(word)
        if definition:
            result_text = "\n".join([f"{pos}: {', '.join(defs)}" for pos, defs in definition.items()])
        else:
            result_text = "No definition found."
    else:
        result_text = "Please enter a word."
    
    result_label.config(text=result_text)

# Create the main window
root = tk.Tk()
root.title("Dictionary App")

# Create and place widgets
tk.Label(root, text="Enter word:").pack(pady=5)
entry = tk.Entry(root, width=50)
entry.pack(pady=5)

tk.Button(root, text="Get Definition", command=get_definition).pack(pady=10)

result_label = tk.Label(root, text="", wraplength=400)
result_label.pack(pady=10)

# Run the application
root.mainloop()
