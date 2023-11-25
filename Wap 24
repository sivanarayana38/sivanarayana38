from tkinter import *

def subtract_numbers():
    try:
        result = int(num1.get()) - int(num2.get())
        l3.config(text="Result: " + str(result))
    except ValueError:
        l3.config(text="Result: Error (Enter valid numbers)")

adding = Tk()
adding.title("Adding 2 no's")

l1 = Label(adding, text="Enter First Number")
num1 = Entry(adding)

l2 = Label(adding, text="Enter Second Number")
num2 = Entry(adding)

b = Button(adding, text="Add", command=subtract_numbers)
l3 = Label(adding, text="Result:")

l1.grid(row=0, column=0)
num1.grid(row=0, column=1)

l2.grid(row=1, column=0)
num2.grid(row=1, column=1)

b.grid(row=2, column=0)
l3.grid(row=2, column=1)

adding.mainloop()
