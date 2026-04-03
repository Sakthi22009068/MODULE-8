# # 🔢 Hackerrank:# 🏆 Student Topper Finder

This Python program helps determine the **top-performing student** based on the total marks across five subjects. It uses a dictionary to store each student’s marks and identifies the topper using simple calculations and built-in functions.

---

## 🎯 Aim

To maintain a dictionary of students with their marks in five subjects, calculate their **total marks**, store them in a new dictionary, and identify the **student with the highest total (topper)**.

---

## 🧠 Algorithm

1. **Start** the program.
2. Create a dictionary `student_marks`:
   - Keys → Student names.
   - Values → List of marks in five subjects.
3. Initialize an empty dictionary `total_marks`.
4. Loop through `student_marks`:
   - Calculate the total marks using `sum()`.
   - Store the result in `total_marks`.
5. Use `max()` on `total_marks` to find the student with the highest total.
6. Print:
   - The `total_marks` dictionary.
   - The **topper's name and score**.

---

## 💻 PROGRAM:

student_marks = {
    "Ravi": [85, 90, 88, 92, 87],
    
    "Arun": [78, 82, 80, 79, 81],
    
    "Meena": [91, 89, 94, 90, 93],
    
    "Kiran": [70, 75, 72, 68, 74]
}

total_marks = {}


for student, marks in student_marks.items():

    total_marks[student] = sum(marks)


topper = max(total_marks, key=total_marks.get)


print("Total Marks of Each Student:")

for student, total in total_marks.items():

    print(student, ":", total)

print("\nTopper:")

print(topper, "with total marks =", total_marks[topper])


## OUTPUT
Total Marks of Each Student:

Ravi : 442

Arun : 400

Meena : 457

Kiran : 359

Topper:

Meena with total marks = 457

## RESULT
The program successfully calculates the total marks of each student and identifies Meena as the topper with the highest score of 457 marks.
