# Employee-Management-System
This project is a simple console-based Employee Management System developed using Python. It allows users to add employee details, view employee records, and search employees by their ID. The system demonstrates basic programming concepts such as lists, dictionaries, functions, and loops.
# Employee Management System
# Author: Kalpana G R

employees = []

def add_employee():
    name = input("Enter Employee Name: ")
    emp_id = input("Enter Employee ID: ")
    salary = input("Enter Salary: ")

    employees.append({
        "name": name,
        "id": emp_id,
        "salary": salary
    })

    print("Employee Added Successfully")


def view_employees():

    if len(employees) == 0:
        print("No employees found")
        return

    for emp in employees:
        print("\nEmployee Name:", emp["name"])
        print("Employee ID:", emp["id"])
        print("Salary:", emp["salary"])


def search_employee():

    search_id = input("Enter Employee ID to search: ")

    for emp in employees:
        if emp["id"] == search_id:
            print("\nEmployee Found")
            print("Name:", emp["name"])
            print("Salary:", emp["salary"])
            return

    print("Employee not found")


while True:

    print("\nEMPLOYEE MANAGEMENT SYSTEM")
    print("1 Add Employee")
    print("2 View Employees")
    print("3 Search Employee")
    print("4 Exit")

    choice = input("Enter choice: ")

    if choice == "1":
        add_employee()

    elif choice == "2":
        view_employees()

    elif choice == "3":
        search_employee()

    elif choice == "4":
        break

    else:
        print("Invalid choice")
