import java.util.*;
class Student {
    String name;
    int id;
    String contact;

    public Student(String name, int id, String contact) {
        this.name = name;
        this.id = id;
        this.contact = contact;
    }

    public String name() {
        return name;
    }

    public int id() {
        return id;
    }

    public String contact() {
        return contact;
    }

    public void name(String name) {
        this.name = name;
    }

    public void id(int id) {
        this.id = id;
    }

    public void contact(String contact) {
        this.contact = contact;
    }

    public void display() {
        System.out.println("Name: " + name);
        System.out.println("ID: " + id);
        System.out.println("Contact: " + contact);
    }
}
class Course {
    String name;
    int courseId;

    public Course(String name, int courseId) {
        this.name = name;
        this.courseId = courseId;
    }

    public String name() {
        return name;
    }

    public int id() {
        return courseId;
    }
}
class Faculty {
    String name;
    int facultyId;

    public Faculty(String name, int facultyId) {
        this.name = name;
        this.facultyId = facultyId;
    }

    public String name() {
        return name;
    }

    public int id() {
        return facultyId;
    }
}
public class CollegeManagement {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        Student[] students = new Student[100];
        Course[] courses = new Course[20];
        Faculty[] faculties = new Faculty[20];
        int studentCount = 0;
        int courseCount = 0;
        int facultyCount = 0;

        while (true) {
            System.out.println("***********************************");
            System.out.println("College Management System");
            System.out.println("***********************************");
            System.out.println("1. Add Student");
            System.out.println("2. Add Course");
            System.out.println("3. Add Faculty");
            System.out.println("4. Display Students");
            System.out.println("5. Display Courses");
            System.out.println("6. Display Faculties");
            System.out.println("7. Update Student Contact");
            System.out.println("8. Remove Student");
            System.out.println("9. Remove Course");
            System.out.println("10. Remove Faculty");
            System.out.println("11. Exit");
            System.out.print("Enter your choice: ");
            int choice = sc.nextInt();
            sc.nextLine();

            switch (choice) {
                case 1:
                    System.out.print("Enter student name: ");
                    String studentName = sc.nextLine();
                    System.out.print("Enter student ID: ");
                    int studentId = sc.nextInt();
                    sc.nextLine();
                    System.out.print("Enter student contact: ");
                    String studentContact = sc.nextLine();
                    students[studentCount] = new Student(studentName, studentId, studentContact);
                    studentCount++;
                    System.out.println("Student added successfully!");
                    break;
                case 2:
                    System.out.print("Enter course name: ");
                    String courseName = sc.nextLine();
                    System.out.print("Enter course ID: ");
                    int courseId = sc.nextInt();
                    sc.nextLine();
                    courses[courseCount] = new Course(courseName, courseId);
                    courseCount++;
                    System.out.println("Course added successfully!");
                    break;
                case 3:
                    System.out.print("Enter faculty name: ");
                    String facultyName = sc.nextLine();
                    System.out.print("Enter faculty ID: ");
                    int facultyId = sc.nextInt();
                    sc.nextLine();
                    faculties[facultyCount] = new Faculty(facultyName, facultyId);
                    facultyCount++;
                    System.out.println("Faculty added successfully!");
                    break;
                case 4:
                    System.out.println("***********************************");
                    System.out.println("List of Students:");
                    for (int i = 0; i < studentCount; i++) {
                        System.out.println("Student " + (i + 1) + ":");
                        students[i].display();
                        System.out.println();
                    }
                    break;
                case 5:
                    System.out.println("***********************************");
                    System.out.println("List of Courses:");
                    for (int i = 0; i < courseCount; i++) {
                        System.out.println("Course " + (i + 1) + ":");
                        System.out.println("Name: " + courses[i].name());
                        System.out.println("ID: " + courses[i].id());
                        System.out.println();
                    }
                    break;
                case 6:
                    System.out.println("***********************************");
                    System.out.println("List of Faculties:");
                    for (int i = 0; i < facultyCount; i++) {
                        System.out.println("Faculty " + (i + 1) + ":");
                        System.out.println("Name: " + faculties[i].name());
                        System.out.println("ID: " + faculties[i].id());
                        System.out.println();
                    }
                    break;
                case 7:
                    System.out.print("Enter student ID to update contact: ");
                    int updateId = sc.nextInt();
                    sc.nextLine();
                    System.out.print("Enter new contact: ");
                    String newContact = sc.nextLine();
                    boolean found = false;
                    for (int i = 0; i < studentCount; i++) {
                        if (students[i].id() == updateId) {
                            students[i].contact(newContact);
                            System.out.println("Contact updated successfully!");
                            found = true;
                            break;
                        }
                    }
                    if (!found) {
                        System.out.println("Student not found!");
                    }
                    break;
                case 8:
                    System.out.print("Enter student ID to remove: ");
                    int removeStudentId = sc.nextInt();
                    sc.nextLine();
                    found = false;
                    for (int i = 0; i < studentCount; i++) {
                        if (students[i].id() == removeStudentId) {
                            students[i] = students[studentCount - 1];
                            studentCount--;
                            System.out.println("Student removed successfully!");
                            found = true;
                            break;
                        }
                    }
                    if (!found) {
                        System.out.println("Student not found!");
                    }
                    break;
                case 9:
                    System.out.print("Enter course ID to remove: ");
                    int removeCourseId = sc.nextInt();
                    sc.nextLine();
                    found = false;
                    for (int i = 0; i < courseCount; i++) {
                        if (courses[i].id() == removeCourseId) {
                            courses[i] = courses[courseCount - 1];
                            courseCount--;
                            System.out.println("Course removed successfully!");
                            found = true;
                            break;
                        }
                    }
                    if (!found) {
                        System.out.println("Course not found!");
                    }
                    break;
                case 10:
                    System.out.print("Enter faculty ID to remove: ");
                    int removeFacultyId = sc.nextInt();
                    sc.nextLine();
                    found = false;
                    for (int i = 0; i < facultyCount; i++) {
                        if (faculties[i].id() == removeFacultyId) {
                            faculties[i] = faculties[facultyCount - 1];
                            facultyCount--;
                            System.out.println("Faculty removed successfully!");
                            found = true;
                            break;
                        }
                    }
                    if (!found) {
                        System.out.println("Faculty not found!");
                    }
                    break;
                case 11:
                    System.out.println("Exiting...");
                    sc.close();
                    System.exit(0);
                    break;
                default:
                    System.out.println("Invalid choice!");
            }
            System.out.println("***********************************");
        }
    }
}
