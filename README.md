# PYTHON-batch1
the project submission repository
# Teacher Schedule Management System

print("===== HOD LOGIN =====")

username = input("Enter HOD Username: ")
password = input("Enter Password: ")

if username == "hod" and password == "1234":

    print("\nLogin Successful!")

    teacher = input("Enter Teacher Name: ")
    department = input("Enter Department: ")
    class_name = input("Enter Class: ")

    days = ["Monday", "Tuesday", "Wednesday", "Thursday", "Friday"]

    schedule = {}

    for day in days:
        print("\n---", day, "---")

        subject1 = input("Enter Subject 1: ")
        subject2 = input("Enter Subject 2: ")
        subject3 = input("Enter Subject 3: ")

        schedule[day] = [subject1, subject2, subject3]

    # Display timetable
    print("\n==============================")
    print("       TEACHER SCHEDULE")
    print("==============================")
    print("Teacher    :", teacher)
    print("Department :", department)
    print("Class      :", class_name)
    print("------------------------------")

    for day in days:
        print(day, ":", ", ".join(schedule[day]))

else:
    print("\nInvalid HOD Username or Password!")
