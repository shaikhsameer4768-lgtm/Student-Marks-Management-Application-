# Student-Marks-Management-Application-
. IntroductionMaintaining student marks in a paper register is slow and error-prone. Totals and percentages must be calculated by hand, finding one student means scanning many pages, and identifying the class topper takes extra effort. A single lost or damaged register can also destroy the entire record.

# Student Marks Management Application
PPS Mini Project – B.Tech AIML, Alard University
Built with HTML, CSS and JavaScript. Uses lists, tuples, dictionaries and file processing.
Features: add, delete, search and sort records; auto total, percentage, grade and result.

code:-
       SUBJECTS = ("Maths", "Physics", "Chemistry", "English", "Computer")  # tuple
students = []                                                           # list
 
def grade(p):
    if p >= 90: return "A+"
    if p >= 80: return "A"
    if p >= 70: return "B"
    if p >= 60: return "C"
    if p >= 40: return "D"
    return "F"
 
def add_student(roll, name, marks):
    student = {"roll": roll, "name": name, "marks": marks}            # dictionary
    student["total"] = sum(marks)
    student["percent"] = student["total"] / 5
    student["grade"] = grade(student["percent"])
    student["result"] = "Pass" if min(marks) >= 40 else "Fail"
    students.append(student)
 
def save(filename="marks.txt"):
    with open(filename, "w") as f:                                     # file
        for s in students:
            f.write(f"{s['roll']},{s['name']}," + ",".join(map(str, s['marks'])) + "\n")


git init
git add .
git commit -m "PPS mini project report"
git branch -M main
git remote add origin https://github.com/<your-username>/student-marks-management.git
git push -u origin main

website link https://share.google/i9ItDIYAW5syiWUln
Thank you for visiting a site.