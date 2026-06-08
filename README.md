# codealpha_task-student-grade-tracker

# 🎓 Student Grade Tracker

A simple Java-based console application developed to manage and analyze student grades efficiently.

---

# 📌 Project Overview

The **Student Grade Tracker** project allows users to:

* Add student names and marks
* Store records using ArrayList
* Calculate average marks
* Find highest and lowest marks
* Display complete student reports

This project demonstrates basic Java programming concepts including:

* Classes & Objects
* ArrayList
* Loops
* Scanner Class
* Conditional Statements

---

# 🚀 Features

✅ Add multiple student records
✅ Store data dynamically using ArrayList
✅ Calculate average marks
✅ Find highest marks
✅ Find lowest marks
✅ Display complete student report
✅ Beginner-friendly project

---

# 🛠 Technologies Used

* Java
* ArrayList
* Scanner Class
* OnlineGDB
* GitHub

---

# 📂 Project Structure

```text
StudentGradeTracker.java
README.md
```

---

# 💻 Complete Java Code

```java
import java.util.ArrayList;
import java.util.Scanner;

class Student {
    String name;
    int marks;

    Student(String name, int marks) {
        this.name = name;
        this.marks = marks;
    }
}

public class StudentGradeTracker {

    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);

        ArrayList<Student> students = new ArrayList<>();

        System.out.print("Enter number of students: ");
        int n = sc.nextInt();
        sc.nextLine();

        // Input student details
        for (int i = 0; i < n; i++) {

            System.out.println("\nStudent " + (i + 1));

            System.out.print("Enter name: ");
            String name = sc.nextLine();

            System.out.print("Enter marks: ");
            int marks = sc.nextInt();
            sc.nextLine();

            students.add(new Student(name, marks));
        }

        // Variables for calculations
        int total = 0;
        int highest = students.get(0).marks;
        int lowest = students.get(0).marks;

        // Process student data
        for (Student s : students) {

            total += s.marks;

            if (s.marks > highest) {
                highest = s.marks;
            }

            if (s.marks < lowest) {
                lowest = s.marks;
            }
        }

        double average = (double) total / n;

        // Display report
        System.out.println("\n===== STUDENT REPORT =====");

        for (Student s : students) {
            System.out.println("Name: " + s.name + " | Marks: " + s.marks);
        }

        System.out.println("\nAverage Marks: " + average);
        System.out.println("Highest Marks: " + highest);
        System.out.println("Lowest Marks: " + lowest);

        sc.close();
    }
}
```

---

# ▶️ How to Run

## Step 1: Compile the Program

```bash
javac StudentGradeTracker.java
```

## Step 2: Run the Program

```bash
java StudentGradeTracker
```

---

# 📸 Sample Input

```text
3
Ram
80
Sai
90
Rani
70
```

---

# 📸 Sample Output

```text
Enter number of students: 3

Student 1
Enter name: Ram
Enter marks: 80

Student 2
Enter name: Sai
Enter marks: 90

Student 3
Enter name: Rani
Enter marks: 70

===== STUDENT REPORT =====

Name: Ram | Marks: 80
Name: Sai | Marks: 90
Name: Rani | Marks: 70

Average Marks: 80.0
Highest Marks: 90
Lowest Marks: 70
```

---

# 📖 Concepts Learned

* Java Basics
* Classes and Objects
* ArrayList
* Loops
* Scanner Class
* Conditional Statements
* User Input Handling

---

# 🌟 Future Improvements

* Add GUI interface
* Add database storage
* Add grade calculation system
* Export reports automatically

---

# 👩‍💻 Author

**D. Amrutha**



# 🔗 GitHub

This project is uploaded to GitHub as part of internship and learning activities to improve Java programming skills.
