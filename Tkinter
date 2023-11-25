from tkinter import *

def calculate_cgpa():
    total_credits = 0
    total_points = 0

    for sem, entry in semester_entries.items():
        marks = entry.get()
        credit = int(credit_entries[sem].get())
        
        try:
            marks = float(marks)
            total_credits += credit
            total_points += marks * credit
        except ValueError:
            result_label.config(text="Result: Enter valid marks for all semesters")
            return

    cgpa = total_points / total_credits
    grade = assign_grade(cgpa)
    result_label.config(text=f"CGPA: {cgpa:.2f}\nResult: {grade}")

def assign_grade(cgpa):
    if cgpa == 10:
        return 'O'
    elif cgpa >= 9:
        return 'A+'
    elif cgpa >= 8:
        return 'A'
    elif cgpa >= 7:
        return 'B'
    elif cgpa >= 6:
        return 'C'
    elif cgpa >= 5:
        return 'D'
    elif cgpa >= 4:
        return 'P'
    else:
        return 'F'

# GUI setup
root = Tk()
root.title("Overall Grade Calculator")

semester_labels = ["Semester 1", "Semester 2", "Semester 3", "Semester 4", "Semester 5", "Semester 6"]

semester_entries = {}
credit_entries = {}

for i, sem_label in enumerate(semester_labels):
    Label(root, text=sem_label).grid(row=i, column=0, padx=10, pady=5)
    semester_entries[sem_label] = Entry(root)
    semester_entries[sem_label].grid(row=i, column=1, padx=10, pady=5)

    Label(root, text="Credit Hours").grid(row=i, column=2, padx=10, pady=5)
    credit_entries[sem_label] = Entry(root)
    credit_entries[sem_label].grid(row=i, column=3, padx=10, pady=5)

calculate_button = Button(root, text="Calculate", command=calculate_cgpa)
calculate_button.grid(row=len(semester_labels), column=0, columnspan=4, pady=10)

result_label = Label(root, text="Result:")
result_label.grid(row=len(semester_labels) + 1, column=0, columnspan=4, pady=5)

root.mainloop()
