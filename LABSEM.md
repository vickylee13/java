1..


import java.util.Scanner;
class BMIcalculator {
    private double weight;
    private double height;
    private double bmi;
    private String grade;

    public BMIcalculator(double weight, double height) {
        this.weight = weight;
        this.height = height;
        this.bmi = calculateBMI();
        this.grade = calculateGrade();
    }

    private double calculateBMI() {
        return weight / (height * height);
    }

    private String calculateGrade() {
        if (bmi < 18.5) {
            return "U";
        } else if (bmi >= 18.5 && bmi < 25) {
            return "N";
        } else if (bmi >= 25 && bmi < 30) {
            return "H";
        } else {
            return "O";
        }
    }

    public void displayBMI() {
        System.out.print(grade);
    }

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        double weight = scanner.nextDouble();
        double height = scanner.nextDouble();
        BMIcalculator bmiCalculator = new BMIcalculator(weight, height);
        bmiCalculator.displayBMI();
    }
}




2.

import java.util.Scanner;

class Overloading {
    private String name;
    private String day;
    private int temp;

    // Default constructor
    public Overloading() {
        this.name = "Argentina";
        this.day = "Yesterday";
        this.temp = 29;
    }

    // Parameterized constructor 1
    public Overloading(String name, int temp) {
        this.name = name;
        this.day = "Today";
        this.temp = temp;
    }

    // Parameterized constructor 2
    public Overloading(String name, String day, int temp) {
        this.name = name;
        this.day = day;
        this.temp = temp;
    }

    public void display() {
        System.out.println(name + " " + day + " Temperature: " + temp + "\u00B0");
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        // Default constructor call
        Overloading defaultObj = new Overloading();
        defaultObj.display();

        // First parameterized constructor
        String name1 = scanner.next();
        int temp1 = scanner.nextInt();
        Overloading paramObj1 = new Overloading(name1, temp1);
        paramObj1.display();

        // Second parameterized constructor
        String name2 = scanner.next();
        String day2 = scanner.next();
        int temp2 = scanner.nextInt();
        Overloading paramObj2 = new Overloading(name2, day2, temp2);
        paramObj2.display();

        scanner.close();
    }




3.

import java.util.*;

class PasswordValidation {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String password = sc.nextLine();

        if (password.matches("^(?=.*[a-z])(?=.*[A-Z])(?=.*\\d)(?=.*[@#$%^&+=]).{8,}$"))
            System.out.println("Valid password");
        else
            System.out.println("Invalid password");
    }
}

4.


import java.util.Scanner;

class Person {
    String name, gender;
    int age;

    Person(String name, int age, String gender) {
        this.name = name;
        this.age = age;
        this.gender = gender;
    }
}

class Student extends Person {
    int studentId;
    String course, major;
    int year;

    Student(String name, int age, String gender, int studentId, String course, String major, int year) {
        super(name, age, gender);
        this.studentId = studentId;
        this.course = course;
        this.major = major;
        this.year = year;
    }

    void display() {
        System.out.println("Name: " + name);
        System.out.println("Age: " + age);
        System.out.println("Gender: " + gender);
        System.out.println("Student ID: " + studentId);
        System.out.println("Course Enrollment: " + course);
        System.out.println("Major: " + major);
        System.out.println("Year of Study: " + year);
    }
}

public class InheritanceExample {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        String name = sc.nextLine();
        int age = sc.nextInt();
        sc.nextLine();

        String gender = sc.nextLine();
        int studentId = sc.nextInt();
        sc.nextLine();

        String course = sc.nextLine();

        String major = sc.nextLine();

        int year = sc.nextInt();

        Student student = new Student(name, age, gender, studentId, course, major, year);
        student.display();
    }
}


5.



import java.util.Scanner;

class Gift {
    protected int amount;

    public Gift(int amount) {
        this.amount = amount;
    }

    public int getAmount() {
        return amount;
    }
}

class Mobile extends Gift {
    public Mobile(int amount) {
        super(amount);
    }
}

class Laptop extends Gift {
    public Laptop(int amount) {
        super(amount);
    }
}

class Bike extends Gift {
    public Bike(int amount) {
        super(amount);
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int mobileLaptopAmount = scanner.nextInt();
        int bikeAmount = scanner.nextInt();

        Mobile mobile = new Mobile(mobileLaptopAmount);
        Laptop laptop = new Laptop(mobileLaptopAmount);
        Bike bike = new Bike(bikeAmount);

        int TotalGiftAmount = mobile.getAmount() + laptop.getAmount() + bike.getAmount();
        System.out.println("Total amount of gifts: " + TotalGiftAmount);
    }
}


6..

 import java.io.*;
import java.util.*;
import java.lang.Math;
abstract class maths {
    abstract public void rectanglePerimeter();
    abstract public void squarePerimeter();
    abstract public void trianglePerimeter();
    abstract public void trapezoidPerimeter();
    abstract public void circlePerimeter();
}
class perimeter extends maths {
    public int length;
    public int breadth;
    public int side;
    public int t1;
    public int t2;
    public int t3;
    public int tr1;
    public int tr2;
    public int tr3;
    public int tr4;
    public int radius;
    public int [] peri= new int[5];
    public void rectanglePerimeter() {
        this.peri[0] = 2*(length+breadth);
        System.out.println(this.peri[0]);
    }
    public void squarePerimeter() {
        this.peri[1] = 4*side;
        System.out.println(this.peri[1]);
    }
    public void trianglePerimeter() {
        this.peri[2] = t1+t2+t3;
        System.out.println(this.peri[2]);
    }
    public void trapezoidPerimeter() {
        this.peri[3] = tr1+tr2+tr3+tr4;
        System.out.println(this.peri[3]);
    }
    public void circlePerimeter() {
        this.peri[4] = (int) Math.PI*2*radius;
        System.out.println(this.peri[4]);
    }
    public void calculateSum() {
    int sum = 0,i;
    for(i=0;i<5;i++) {
        sum += this.peri[i];
    }
    System.out.println(sum);
    }
    public void sortPerimeter() {
        Arrays.sort(this.peri);
        for(int i=0;i<5;i++) {
            System.out.print(this.peri[i]+" ");
        }
    }
}
class Main {
    public static void main(String [] args) {
        perimeter p = new perimeter();
        Scanner sc = new Scanner(System.in);
        p.length = sc.nextInt();
        p.breadth = sc.nextInt();
        p.rectanglePerimeter();
        p.side = sc.nextInt();
        p.squarePerimeter();
        p.t1 = sc.nextInt();
        p.t2 = sc.nextInt();
        p.t3 = sc.nextInt();
        p.trianglePerimeter();
        p.tr1 = sc.nextInt();
        p.tr2 = sc.nextInt();
        p.tr3 = sc.nextInt();
        p.tr4 = sc.nextInt();
        p.trapezoidPerimeter();
        p.radius = sc.nextInt();
        p.circlePerimeter();
        p.calculateSum();
        p.sortPerimeter();
    }
} 


7..


import java.util.NoSuchElementException;
import java.util.Scanner;

class InvalidInputException extends Exception {
    public InvalidInputException(String message) {
        super(message);
    }
}

class main {
    public static void validate(String regNo, String mobileNo) throws InvalidInputException {
        if (!regNo.matches("\\d{2}[A-Z]{3}\\d{4}")) {
            throw new InvalidInputException("Register Number does not contain exactly 9 characters");
        }
        if (mobileNo.length() != 10) {
            throw new InvalidInputException("Mobile Number does not contain exactly 10 characters");
        }
        if (!mobileNo.matches("\\d{10}")) {
            throw new InvalidInputException("Mobile Number cannot contain any character other than a digit");
        }
        if (!regNo.matches("[0-9A-Z]+")) {
            throw new InvalidInputException("Registration Number cannot contain any character other than digits and alphabets in format specified");
        }
    }

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        String regNo = scanner.nextLine();
        String mobileNo = scanner.nextLine();

       try {
            validate(regNo, mobileNo);
            System.out.println("Valid");
        } catch (Exception e) {
            System.out.println("Invalid");
            System.out.println(e.getMessage());
        }
    }
}



8.


import java.util.ArrayList;
import java.util.List;
import java.util.ListIterator;
import java.util.Scanner;

public class IncreasingSequence {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        int N = scanner.nextInt();
        List<Integer> list = new ArrayList<>();

        for (int i = 0; i < N; i++) {
            int num = scanner.nextInt();
            if (list.isEmpty() || num > list.get(list.size() - 1)) {
                list.add(num);
            }
        }

        System.out.println(list);
    }
}



9.



import java.util.HashSet;
import java.util.Scanner;
import java.util.Set;

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        // Input string
        String input = scanner.nextLine();

        // Split the input string into words
        String[] words = input.split(" ");

        // Use HashSet to store unique words
        Set<String> uniqueWords = new HashSet<>();

        // Add words to the HashSet
        for (String word : words) {
            uniqueWords.add(word.toLowerCase()); // Convert to lowercase to count words case-insensitively
        }

        // Output the count of unique words
        System.out.println(uniqueWords.size());

        scanner.close();
    }
}



10.

import java.util.Scanner;

class Counter {
    int count = 0;

    synchronized void increment() {
        count++;
    }
}

 class ThreadSafeCounter {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int T = scanner.nextInt();
        int N = scanner.nextInt();

        Counter counter = new Counter();

        Thread[] threads = new Thread[T];

        for (int i = 0; i < T; i++) {
            threads[i] = new Thread(() -> {
                for (int j = 0; j < N; j++) {
                    counter.increment();
                }
            });
            threads[i].start();
        }

        for (int i = 0; i < T; i++) {
            try {
                threads[i].join();
            } catch (InterruptedException e) {
                e.printStackTrace();
            }
        }

        System.out.println("Final counter value: " + counter.count);
    }
}


11.

import java.sql.*;
import java.util.*;

class EmployeeDetails {
    public static void main(String[] args) {
        // Database connection details
        String url = "jdbc:mysql://localhost/ri_db";
        String user = "test";
        String password = "test123";

        // Scanner for user input
        Scanner scanner = new Scanner(System.in);

        try {
            System.out.print("Enter Employee ID: ");
            int empId = scanner.nextInt(); // Read employee ID
            scanner.nextLine(); // Consume newline

            System.out.print("Enter Department: ");
            String department = scanner.nextLine(); // Read department

            // Establish connection to the database
            Connection connection = DriverManager.getConnection(url, user, password);

            // SQL query to retrieve employee details
            String query = "SELECT * FROM COMPANY WHERE empid = ? AND department = ?";
            PreparedStatement preparedStatement = connection.prepareStatement(query);

            // Set values for the query parameters
            preparedStatement.setInt(1, empId);
            preparedStatement.setString(2, department);

            // Execute the query
            ResultSet resultSet = preparedStatement.executeQuery();

            // Process the result
            if (resultSet.next()) {
                int id = resultSet.getInt("empid");
                String empname = resultSet.getString("empname");
                String dep = resultSet.getString("department");
                String addr = resultSet.getString("address");
                double sal = resultSet.getDouble("salary");

                System.out.println("Employee ID: " + id);
                System.out.println("Employee Name: " + empname);
                System.out.println("Department: " + dep);
                System.out.println("Address: " + addr);
                System.out.printf("Salary: %.2f",sal);
            } else {
                System.out.println("No employees found with the given criteria.");
            }

            // Close resources
            resultSet.close();
            preparedStatement.close();
            connection.close();
        } catch (Exception e) {
            e.printStackTrace(); // Print exception details
        }
    }
}


12.


NO ANSWER SERVLETS 



13.

import java.awt.*;
import java.awt.event.ActionEvent;
import javax.swing.*;
public class StudentForm extends JFrame {
    public StudentForm() {
        setTitle("Student Form");
        setSize(300, 250);
        setLayout(new FlowLayout(FlowLayout.LEFT, 10, 10));

        JTextField nameField = new JTextField(20);
        JTextField regnoField = new JTextField(20);
        JTextField cgpaField = new JTextField(20);
        JCheckBox maleCheckbox = new JCheckBox("Male");
        JCheckBox femaleCheckbox = new JCheckBox("Female");

        maleCheckbox.addActionListener(e -> femaleCheckbox.setSelected(!maleCheckbox.isSelected()));
        femaleCheckbox.addActionListener(e -> maleCheckbox.setSelected(!femaleCheckbox.isSelected()));

        JButton submitButton = new JButton("Submit");
        submitButton.addActionListener((ActionEvent e) -> JOptionPane.showMessageDialog(null, "Welcome!"));

        add(new JLabel("Name:")); add(nameField);
        add(new JLabel("Regno:")); add(regnoField);
        add(new JLabel("CGPA:")); add(cgpaField);
        add(new JLabel("Gender:")); add(maleCheckbox); add(femaleCheckbox);
        add(submitButton);
    }
    public static void main(String[] args) {
        SwingUtilities.invokeLater(() -> new StudentForm().setVisible(true));
    }
}


13 ANS 2

import javax.swing.*;
import java.awt.*;
import java.awt.event.ActionEvent;
import java.awt.event.ActionListener;

public class StudentForm extends JFrame {
    public StudentForm() {
        setTitle("Student Form");
        setSize(300, 300);
        setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
        setLayout(new GridLayout(5, 2));

        JLabel nameLabel = new JLabel("Name:");
        JTextField nameField = new JTextField();
        JLabel regnoLabel = new JLabel("Regno:");
        JTextField regnoField = new JTextField();
        JLabel cgpaLabel = new JLabel("CGPA:");
        JTextField cgpaField = new JTextField();

        JCheckBox maleCheckbox = new JCheckBox("Male");
        JCheckBox femaleCheckbox = new JCheckBox("Female");

        JButton submitButton = new JButton("Submit");

        submitButton.addActionListener(new ActionListener() {
            @Override
            public void actionPerformed(ActionEvent e) {
                JOptionPane.showMessageDialog(null, "Welcome");
            }
        });

        add(nameLabel);
        add(nameField);
        add(regnoLabel);
        add(regnoField);
        add(cgpaLabel);
        add(cgpaField);
        add(maleCheckbox);
        add(femaleCheckbox);
        add(submitButton);

        setVisible(true);
    }

    public static void main(String[] args) {
        new StudentForm();
    }
}