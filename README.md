
# Program to demonstrate OOPs concepts

# Base Class
class Student:

    def __init__(self, roll_no, name):
        self.__roll_no = roll_no
        self.__name = name

    # Encapsulation
    def display_details(self):
        print("Roll Number:", self.__roll_no)
        print("Name:", self.__name)

    # Polymorphism
    def show_result(self):
        print("Result: Not Declared")


# Inheritance
class Result(Student):

    def __init__(self, roll_no, name, marks):
        super().__init__(roll_no, name)
        self.marks = marks

    # Method Overriding
    def show_result(self):
        if self.marks >= 40:
            print("Result: Pass")
        else:
            print("Result: Fail")


# Main Program
s = Result(118, "Pranay", 85)

print("===== STUDENT DETAILS =====")

s.display_details()
print("Marks:", s.marks)
s.show_result()

print("\nOOP Concepts Demonstrated Successfully!")
