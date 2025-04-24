# 19CS301-Module5

Exp.No:5(a)	Constructors- Parameterized Constructor
### AIM
To write a Python code to create a Class for a Person with the parameterised constructor which will take the name and userid of the person as parameters print the userid  of the person,
### ALGORITHM

Step 1:	 Begin the program.

Step 2:	 Define the person class.

Step 3:	 The class person has an __init__ method, which is the constructor. It accepts two parameters: name and userid. 

Step 4:	Inside the __init__ method: Assign the name to self.name. Assign the userid to self.userid.

Step 5:	 Print the self.userid.

Step 6:	 Prompt the user to enter the name (string) and id.

Step 7:	 Create an instance s1 of the person class by passing the entered name and userid to the constructor.

Step 8:	 Terminate the program.
### PROGRAM
```
class person:
    def __init__(self,name,userid):
        self.name=name
        self.userid=userid
        print(self.userid)
name=input()
userid=input()
s1=person(name,userid)
```
### OUTPUT
 ![image](https://github.com/user-attachments/assets/95ebab44-d7da-435c-b994-e752ebeabd44)

### RESULT
Thus the python program for parameterised constructor which will take the name and userid of the person as parameters print the userid  of the person, was implemented and executed successfully.

Exp.No:5(b)	Destructor

### AIM
To create  a  Python Class Student with a destructor.
### ALGORITHM
Step 1:	 Begin the program.

Step 2:	 Define the student class:

Step 3:	 Inside the class student, define the __init__ method (constructor) and the __del__ method (destructor).

Step 4:	 Create an object s2 of the student class. When the object s2 is created, the __init__ method is called, and its print statements are executed.

Step 5:	 Use the del statement to delete the object s2. This triggers the __del__ method (destructor), and the respective print statements are executed.

Step 6:	  Terminate the program.

### PROGRAM
```
class student:
    def __init__(self):
        print("Inside Constructor")
        print("Object initialized")
        print("Hello, my name is Emma")
    def __del__(self):
        print("Inside destructor")
        print("Object destroyed")
s2=student()
del s2
```
### OUTPUT
 ![image](https://github.com/user-attachments/assets/bff64e83-c99e-4102-ab1d-ec15d0c3fae4)

### RESULT
Thus the python program for Class Student with a destructor, was implemented and executed successfully.

Exp.No:5(c)	Multiple Inheritance

### AIM
To Write a Python program to get the name, attendance and Id of a student and check they are eligible for Next Module using multiple inheritance, attendance >80 eligible student else Not Eligible student
### ALGORITHM
Step 1:	 Begin the program.

Step 2:	Define the Student class.

Step 3:	Inside the Student class, define the __init__ method (constructor). The __init__ method accepts two parameters: name and student_id. 

Step 4:	Inside the __init__ method: Assign the value of name to self.name, student_id to self.student_id.

Step 5:	Define the get_student_info method inside the Student class: Return a string formatted with self.name and self.student_id.

Step 6:	Define the Attendance class, which inherits from the Student class.

Step 7:	Inside the Attendance class, define the __init__ method (constructor).

Step 8:	The __init__ method accepts three parameters: name, student_id, and attendance.

Step 9:	Inside the __init__ method: Call the parent class constructor (super().__init__(name, student_id)) to initialize name and student_id. Assign the value of attendance to 
          self.attendance.

Step 10:	Define the check_eligibility method inside the Attendance class:

Step 11:	If self.attendance is greater than 80, return a formatted string indicating the student is eligible for the module exam. Otherwise, return a formatted string indicating the 
          student is not eligible for the module exam.

Step 12:	Prompt the user to enter the name (as a string), student_id (as an integer), attendance (as an integer).

Step 13:	Create an instance student of the Attendance class, passing the entered name, student_id, and attendance to the constructor.

Step 14:	Call the check_eligibility method on the student object and print the result.
### PROGRAM
```
class Student:
    def __init__(self, name, student_id):
        self.name = name
        self.student_id = student_id
    def get_student_info(self):
        return f"Name: {self.name}, ID: {self.student_id}"
class Attendance(Student):
    def __init__(self, name, student_id, attendance):
        super().__init__(name, student_id)  
        self.attendance = attendance
    def check_eligibility(self):
        if self.attendance > 80:
            return f"{self.name}\n{self.student_id}\nEligible for Module Exam"
        else:
            return f"{self.name}\n{self.student_id}\nNot Eligible for Module Exam"
name = input()
student_id = int(input())
attendance = int(input())
student = Attendance(name, student_id, attendance)
print(student.check_eligibility())
```
### OUTPUT
![image](https://github.com/user-attachments/assets/f4959ede-568d-4162-ab31-373c5d060226)
 
### RESULT
Thus the python program to get the name, attendance and Id of a student and check they are eligible for Next Module using multiple inheritance,was implemented and executed successfully.



Exp.No:5(d)	Multi-level Inheritance

### AIM
To write a Python program to Get the name, age and id of a person and display using Multilevel inheritance.
### ALGORITHM

Step 1:	  Begin the program.


Step 2:	 Define the Person class.

Step 3:	 Inside the Person class, define the __init__ method (constructor), with  two parameters: name and age.

Step 4:	 Inside the __init__ method, assign name to self.name., assign age to self.age.

Step 5:	 Define the PersonDetails class that inherits from the Person class.

Step 6:	 Inside the PersonDetails class, define the __init__ method (constructor). with three parameters: name, age, and person_id. 

Step 7:	 Inside the __init__ method, call the __init__ method of the Person class using super() to initialize name and age, assign person_id to self.person_id.

Step 8:	 Define the DisplayDetails class that inherits from the PersonDetails class.

Step 9:	 Inside the DisplayDetails class, define the __init__ method (constructor),with three parameters: name, age, and person_id.

Step 10:	Inside the __init__ method, call the __init__ method of the PersonDetails class using super() to initialize name, age, and person_id.

Step 11:	Inside the DisplayDetails class, define the show_details method.

Step 12:	Inside the show_details method, return a formatted string with self.name, self.age, and self.person_id.

Step 13:	Prompt the user to enter name (string),age (integer),person_id (integer).

Step 14:	Create an instance person of the DisplayDetails class, passing name, age, and person_id to the constructor.

Step 15:	Call the show_details method on the person object and print the result.

Step 16:	Terminate the program.

### PROGRAM
```
class Person:
    def __init__(self, name, age):
        self.name = name
        self.age = age

class PersonDetails(Person):
    def __init__(self, name, age, person_id):
        super().__init__(name, age)  # Call the parent class constructor
        self.person_id = person_id

class DisplayDetails(PersonDetails):
    def __init__(self, name, age, person_id):
        super().__init__(name, age, person_id)

    def show_details(self):
        return f"{self.name} {self.age} {self.person_id}"

name = input()
age = int(input())
person_id = int(input())

person = DisplayDetails(name, age, person_id)

print(person.show_details())
```
### OUTPUT
![image](https://github.com/user-attachments/assets/e87e458f-8ee8-4d8d-b2f7-a8f80354f44c)

 
### RESULT
Thus the python program to Get the name, age and id of a person and display using Multilevel inheritance. , was implemented and executed successfully.


Exp.No:5(e)	HIERARCHICAL INHERITANCE

### AIM
To write a Python program to Get the employee  and doctor details & display it using Hierarchical inheritance.create a parent (base) class name Details and two child (derived) classes named Employee and Doctor
### ALGORITHM

Step 1:	  Begin the program.

Step 2:	 Create a class Details with an __init__ method to initialize three attributes: id, name, and gender.

Step a:	Define a method display_details() to print the values of id, name, and gender.

Step 3:	 Create a class Employee that inherits from the Details class.

Step a:	Add two additional attributes: company and department.

Step b:	Override the display_details() method to print the employee-specific attributes (company and department) along with the inherited details.

Step 4:	 Create a class Doctor that also inherits from the Details class.

Step a:	Add two additional attributes: hospital and department.

Step b:	Override the display_details() method to print the doctor-specific attributes (hospital and department) along with the inherited details.

Step 5:	 Accept input for employee and doctor details.

Step 6:	Create objects of Employee and Doctor using the input.

Step 7:	Call the display_details() method for both objects to print the details.Step 8:	

### PROGRAM
# Parent class Details
class Details:
    def __init__(self, id, name, gender):
        self.id = id
        self.name = name
        self.gender = gender

    def display_details(self):
        print(f"Id:  {self.id}")
        print(f"Name:  {self.name}")
        print(f"Gender:  {self.gender}")

# Child class Employee
class Employee(Details):
    def __init__(self, id, name, gender, company, department):
        # Call parent class constructor
        super().__init__(id, name, gender)
        self.company = company
        self.department = department

    def display_details(self):
        print("Employee Object")
        super().display_details()
        print(f"Company:  {self.company}")
        print(f"Department:  {self.department}")

# Child class Doctor
class Doctor(Details):
    def __init__(self, id, name, gender, hospital, department):
        # Call parent class constructor
        super().__init__(id, name, gender)
        self.hospital = hospital
        self.department = department

    def display_details(self):
        print("Doctor Object")
        super().display_details()
        print(f"Hospital:  {self.hospital}")
        print(f"Department:  {self.department}")

# Main function to get input and display details
def main():
    # Create Employee object and display details
    employee_id = int(input())
    employee_name = input()
    employee_gender = input()
    employee_company = input()
    employee_department = input()

    employee = Employee(employee_id, employee_name, employee_gender, employee_company, employee_department)
    employee.display_details()
    print("")
    # Create Doctor object and display details
    doctor_id = int(input())
    doctor_name = input()
    doctor_gender = input()
    doctor_hospital = input()
    doctor_department = input()

    doctor = Doctor(doctor_id, doctor_name, doctor_gender, doctor_hospital, doctor_department)
    doctor.display_details()

# Run the main function
main()

### OUTPUT
 ![image](https://github.com/user-attachments/assets/49f2eb5f-b9a6-4e0e-8b36-cae4cbe497e1)

### RESULT
Thus the python program for Hierarchical Inheritance to get the employee details was implemented and executed successfully.






