# 🎓 Hackerrank:Python Program to Find Students with the Second Lowest Grade

This program reads student names and their corresponding grades, identifies the **second lowest grade**, and prints the names of all students who have that grade in **alphabetical order**.

---

## 🎯 Aim

To write a Python program to:
- Read a list of students and their grades.
- Identify the second lowest grade.
- Print the names of students who have that grade, sorted alphabetically.

---

## 🧠 Algorithm

1. **Read** an integer `n` representing the number of students.
2. **Read** each student’s name and grade, and store them as a sublist inside a list.
3. **Extract** all the grades and sort them.
4. **Identify** the second lowest grade from the sorted grade list.
5. **Collect** names of all students whose grade matches the second lowest grade.
6. **Sort** the names alphabetically.
7. **Print** each name on a new line.

---

## 💻  Program

n = int(input("Enter number of students: "))

students = []

for _ in range(n):

    name = input("Enter student name: ")
    
    grade = float(input("Enter grade: "))
    
    students.append([name, grade])

grades = sorted(set([student[1] for student in students]))

second_lowest = grades[1]


second_lowest_students = [student[0] for student in students if student[1] == second_lowest]


second_lowest_students.sort()


print("\nStudents with second lowest grade:")

for name in second_lowest_students:

    print(name)
    


## Output
Enter number of students: 5

Enter student name: Harry

Enter grade: 37.21

Enter student name: Berry

Enter grade: 37.21

Enter student name: Tina

Enter grade: 37.2

Enter student name: Akriti

Enter grade: 41

Enter student name: Harsh

Enter grade: 39

Students with second lowest grade:

Berry

Harry

## Result
The program successfully identifies the second lowest grade and prints all students who have that grade in alphabetical order, ensuring correct handling of duplicate grades and sorting.
