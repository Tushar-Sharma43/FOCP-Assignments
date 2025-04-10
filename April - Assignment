// FOCP Assignment - Student Management System
#include <iostream>
#include <vector>
#include <string>
using namespace std;

class Student {
private:
    string name;
    int roll_number;
    float cgpa;
    vector<string> enrolled_courses;

public:
    // Default Constructor
    Student() {
        name = "Unknown";
        roll_number = 0;
        cgpa = 0.0;
    }

    // Parameterized Constructor
    Student(string n, int r) {
        name = n;
        roll_number = r;
        cgpa = 0.0;
    }

    // Copy Constructor
    Student(const Student& other) {
        name = other.name;
        roll_number = other.roll_number;
        cgpa = other.cgpa;
        enrolled_courses = other.enrolled_courses;
    }

    // Destructor
    ~Student() {
        cout << "Destructor called for: " << name << endl;
    }

    // Getter for Roll Number
    int getRollNo() const {
        return roll_number;
    }

    // Add Course
    void addCourse(string course) {
        enrolled_courses.push_back(course);
    }

    // Update CGPA
    void updateCgpa(float newCgpa) {
        if (newCgpa >= 0 && newCgpa <= 10) {
            cgpa = newCgpa;
        } else {
            cout << "Invalid input for CGPA" << endl;
        }
    }

    // Display Info
    void displayInfo() const {
        cout << "Student name: " << name << endl;
        cout << "Roll number: " << roll_number << endl;
        cout << "CGPA: " << cgpa << endl;
        cout << "Enrolled courses: ";
        if (enrolled_courses.empty()) {
            cout << "None";
        } else {
            for (int i = 0; i < enrolled_courses.size(); i++) {
                cout << enrolled_courses[i];
                if (i != enrolled_courses.size() - 1) {
                    cout << ", ";
                }
            }
        }
        cout << endl;
    }
};

// Student Management System Class
class StudentManagementSystem {
private:
    vector<Student> students;

public:
    void addStudent(const Student& s) {
        students.push_back(s);
    }

    void searchByRoll(int rollToFind) {
        bool found = false;
        for (int i = 0; i < students.size(); i++) {
            if (students[i].getRollNo() == rollToFind) {
                cout << "\nStudent found:\n";
                students[i].displayInfo();
                found = true;
                break;
            }
        }
        if (!found) {
            cout << "\nStudent with roll number " << rollToFind << " not found.\n";
        }
    }

    void displayAllStudents() {
        for (const auto& s : students) {
            s.displayInfo();
            cout << "--------------------------\n";
        }
    }
};

int main() {
    StudentManagementSystem sms;

    // Sample students
    Student s1("Alice", 101);
    s1.addCourse("Math");
    s1.addCourse("English");
    s1.updateCgpa(9.2);

    Student s2("Bob", 102);
    s2.addCourse("Physics");
    s2.updateCgpa(8.5);

    // Adding students to the system
    sms.addStudent(s1);
    sms.addStudent(s2);

    // Search a student by roll number
    int roll;
    cout << "\nEnter roll number to search: ";
    cin >> roll;
    sms.searchByRoll(roll);

    // Display all students (optional)
    cout << "\nAll Students:\n";
    sms.displayAllStudents();

    return 0;
}
