# Basics of Java
**Need to learn Java**
1. Most technologies (~90%) are java based technologies
    - E-Com Technologies (Amazon, FlipKart)
    - Payment Gateways
    - Mobile Application Development
---
More info about Java
- Java is both compiled and interpreted.
- Java is platform independent language.
- Java is architecturally neutral(can run on any architecture).
- After compilation of java we get *.class* file.
- JDK contains a crucial tool known as the compiler. It first changes the source code in a .java file into a special code called bytecode, by creating a .class file. After that, the Java Virtual Machine (JVM) interprets this bytecode and generates the output. The process of converting a .java file to a .class file is known as compilation

What is platform independent?
If we compile the program in windows and we get .exe file as output , And if this .exe file is executed in linux then it will not work.

---
**Installation and setup of Java Development Kit(JDK)**

JDK-17 is more stable than JDK-21 thereofore we will install JDK-17. To install JDK-17 for Windows OS follow the below steps:
1. Visit [Oracle Website](https://www.oracle.com/java/technologies/downloads/#java17).
2. Under JDK 17 tab select Windows tab.
3. Click the link for x64 Installer.
4. Open downloaded file, read the instructions carefully and install java.
4. To verify installation:
    - open command prompt and write:
    ```
    > cd C:\Program Files\Java\jdk-17\bin
    > javac.exe
    ```
    If you see many instructions, it means it is successfully installed.
5. To make javac (java compiler) as environment variable:
    - Search env in windows search bar and open *Edit the system environment variable*.
    - Click *Environment Variables*.
    - Click *New* and enter *PATH* in the variable name and enter *C:\Program Files\Java\jdk-17\bin;* in variable name.
    - Click ok till the window closes.
---
# First Program
- File name and class name should be same.
- Class name should start from a capital letter.
- Java is a case sensitive language.
```java
public class Hello_world
{
    public static void main(String[] args)
    {
        System.out.println("Hello World!");
    }
}
```
---
To compile and run java file.

1. First you have to save your code with .java extension. Open terminal and change the directory to your folder and type
    ```
    javac filename.java
    ```
2. This will compile your code and to execute the file type
    ```
    java filename
    ```
---
### String

```java
public class College
{
    public static void main(String[] args)
    {
        String st = "Symbiosis Institute of Technology, Nagpur";
        System.out.println("My college name is " + st + ". "); // println ends with a new line.
        System.out.print(st + " is located in Nagpur."); // + is a concatenation operator.
    }
}
```
---
### Two variable swap without using third variable.
```java
class Swap
{
    public static void main(String[] args)
    {
        int a = 10, b = 20;
        System.out.println("Value of a before swapping: " + a);
        System.out.println("Value of b before swapping: " + b);
        a = a + b;
        b = a - b;
        a = a - b;
        System.out.println("Value of a after swapping: " + a);
        System.out.println("Value of b after swapping: " + b);
    }
}
```
---
- **Note:** Keywords are words which have special meaning in a programming language. In java all keywords are in lowercase.
- A comment is a sequence of non-executable characters. There are three types of comments in Java:-
    1. End-of-line comment : It starts with // and the content following // till the end of that line is a comment. It is also called as the single-line comment.
    2. Traditional comment : It starts with /* and ends with \*/, the content between /* and */ is the comment. It is also called as multi-line comment.
    3. Java Doc comment : It starts with /** and ends with \*/, the content between /** and */ contains the java documentation information.
- All other input elements other than comments and whitespace are called as tokens. The tokens are further classified as:
    1. Identifiers - Names used to refer or identify are called Identifiers. For example, names of variables, methods and classes are all called Identifiers.
    2. Keywords - one of the 50 reserved words in Java language like *public, new, for, if,* etc. are called Keywords. These have a special meaning when used as part of the program.
    3. Literals - these are the fixed values assigned in a source code. They can be of primitive, String or a null type.
    4. Operators - in Java language we have 38 different operators like *-, <, <=, =, >, >=,* etc.
    5. Separators - in Java language we have 12 Separators:- *( ) { } [ ] ; , . ... @ ::*
---
**Installation of Eclipse IDE**
1. Visit [here](https://www.eclipse.org/downloads/download.php?file=/oomph/epp/2023-12/R/eclipse-inst-jre-win64.exe), and download the IDE.
2. After installation open the downloaded `eclipse-inst-jre-win64.exe` file and select *Eclipse IDE for Java Developers*
3. Locate JAVA 17+VM , and from drop down select *JRE 17.0.10* and click install (This may take time because it downloads dependencies from the internet)
4. After installation you can *Launch*
5. Select a directory as workspace and Launch
6. Goto File -> New -> Java Project , give project nae and create
7. Remove the file from src (it creates error)
8. right click and create class, here you can start.
---
# Data Types in Java
- It is used to specify the type of data.
- Two types of datatype: Primitive Datatype and Non-Primitive Datatype(or Derived Datatype).

## Primitive Datatype
- Primitive Datatype is divided into 8 families.
### Integral Datatype
1. **byte**
    - Size: 1 Byte(8 bits).
    - Range: -128 to 127.
    - Stores: Whole Numbers.
    - Example:
        ```java
        class ExampleByte
        {
            public static void main(String[] args)
            {
                byte b = 13;
                System.out.println("b = " + b);
            }
        }
        ```
2. **short**
    - Size: 2 Bytes(16 bits).
    - Range: -32,768 to 32,767.
    - Stores: Whole Numbers.
    - Example:
        ```java
        class ShortExample
        {
            public static void main(String[] ergs)
            {
                short s = 32767;
                System.out.println("s = "+s);
            }
        }
        ```
3. **int**
    - Size: 4 Bytes(32 bits).
    - Range: -2,147,483,648 to 2,147,483,647.
    - Stores: Whole Numbers.
    - To store the whole numbers in Java the default data type is "int".
    - Example:
        ```java
        class IntExample
        {
            public static void main(String[] args)
            {
                int i = 85207410;
                System.out.println("i = " + i);
            }
        }
        ```
4. **long**
    - Size: 8 Bytes(64 bits).
    - Range: -9,223,372,036,854,775,808 to 9,223,372,036,854,775,807.
    - Stores: Whole Numbers.
    - Example:
        ```java
        class LongExample
        {
            public  static void main(String[] args)
            {
                long lg = 74108520963L; // "74108520963" is called as literal value or a constant.
                System.out.println("lg = " + lg);
            }
        }
        ```
### Floating-Point Datatype
5. **float**
    - Size: 4 Bytes(32 bits).
    - Range: Sufficient for storing 6 to 7 decimal digits.
    - Stores: Fractional Numbers.
    - Example:
        ```java
        class FloatExample
        {
            public static void main(String[] args)
            {
                float pi = 3.14f;
                System.out.println(" pi = " + pi);
            }
        }
        ```
6. **double**
    - Size: 8 Bytes(64 bits).
    - Range: Sufficient for storing 15 decimal digits.
    - Stores: Fractional Numbers.
    - To store the fractional numbers in Java the default data type is "double".
    - Example:
        ```java
        class DoubleExample
        {
            public static void main(String[] args)
            {
                double d = 8520.7410;
                System.out.println("d = " + d);
            }
        }
        ```
### Character Datatype
7. **char**
    - Size: 2 Bytes(16 bits).
    - Stores: A single character/letter or ASCII values.
    - Supports Unicode.
    - Example:
        ```java
        class CharExample
        {
            public static void main(String[] args)
            {
                char ch = 'A';
                System.out.println("ch = " + ch);
            }
        }
        ```
### Boolean Datatype
7. **boolean**
    - Size: 1 Bit.
    - Stores: True or False values.
    - Cannot type-cast boolean type datatype.
    - Example:
        ```java
        class BooleanExample
        {
            public static void main(String[] args)
            {
                boolean b =true;
                System.out.println("b = " + b);
                boolean b1 = !b;
                System.out.println("b1 = " + b1);
            }
        }
        ```
## Derived Datatype or Non-Primitive Datatype
- These are the data types which are created by combining other primitive data types.
- Examples of derived data types include String, Array and Class in Java.
### String Datatype
- A String variable contains a collection of characters surrounded by double quotes.
- Stored in memory as the array of char, starting index from 0.
#### String Methods
- str.length( )
    - Returns an integer value.
    - Returns the length of the given string.
- str.indexOf('single_character_argument')
    - Returns an integer value.
    - Searches for the argument character/string in the given string.
    - Returns the first occurrence of argument in the specified string. If there is no such element it returns -1.
- str.lastIndexOf('single_character_argument')
    - Returns an integer value.
    - Same as above but returns the last occurrence of the argument character/string in the given string is returned.
- str.charAt(num)
    - Returns a character value.
    - Returns a single character present at the specified index num.
- Example:
    ```Java
    class StringExample
    {
        public static void main(String[] args)
        {
            String city = "Nagpur.";
            System.out.println("City = " + city);
            int len = city.length();
            System.out.println("Length of city is = " + len);
            int index = city.indexOf('g');
            System.out.println("Index of g is = " + index);
            int index1 = city.lastIndexOf('a');
            System.out.println("Last Index of a is = " + index);
            char ch = city.charAt(5);
            System.out.println("Character at index 5 is = " + ch);
        }
    }
    ```
    ---
- Q. Write a program in Java to calculate the number of times a specified character appears in the given string.
    - Solution:
        ```java
        class q
        {
            public static void main(String[] args)
            {
                String str = "Abc abc xyz a", str1 = str.toLowerCase();
                int len = str.length(), count = 0;
                for(int i = 0; i < len; i++)
                {
                    if (str1.charAt(i) == 'a') count++;
                }
                System.out.println("Number of times 'a' appears in the string is : " + count);
            }
        }
        ```
- Q. Write a program in Java to print a Fibonacci series using for loop.
    - Solution:
        ```java
        public class Fibonacci
        {
            public static void main(String[] args)
            {
                int val1 = 0, val2 = 1;
                for(int index = 0; index < 10; index++)
                {
                    System.out.print(val1 + " ");
                    int temp = val1;
                    val1 = val2;
                    val2 = val2 + temp;
                }
            }
        }
        ```
- Q. Write a program in Java to print an left right-angled triangle of astrict.
    - Solution:
        ```java
        public class LeftRightAngledTriangle
        {
            public static void main(String[] args)
            {
                for(int row = 0; row < 3; row++)
                {
                    for(int cloumn = 0; cloumn <= row; cloumn++) System.out.print("* ");
                    System.out.println();
                }
            }
        }
        ```
- Q. Write a program in Java to print an left right-angled triangle of numbers where in each row the number starts from "1".
    - Solution:
        ```java
        public class LeftRightAngledTriangleNumber
        {
            public static void main(String[] args)
            {
                for(int row = 1; row <= 3; row++)
                {
                    for(int cloumn = 0; cloumn <= row; cloumn++) System.out.print(row + " ");
                    System.out.println();
                }
            }
        }
        ```

# Abstraction
- Abstraction refers to hiding the implementation details of a code and exposing only the necessary information to the user. It provides the ability to simplify complex systems by ignoring irrelevant details and reducing complexity. Java provides many in-built abstractions and few tools to create our own.
- Abstraction in Java can be achieved using the following tools it provides :
    1. Abstract classes
    2. Interfaces

## Abstract Class
- An abstract class is a class that cannot be instantiated on its own and is meant to be subclassed. It provides a common base for subclasses to inherit method and field definitions, but allows for subclasses to provide their own implementations.
- Rules:-
    1. We declare a method as abstract if the method is incomplete.
    2. If any method declared inside the class is abstract then the the whole class should be declared as abstract.
    3. If abstract classes are there you need to inherit the abstract class.
    4. We have to override every method of abstract class to sub class.
    5. We cannot instance of an abstract classes.
    6. We can create reference of an abstract class.
- Abstract class :-
    ```java
    public abstract class Shape {
	        public abstract void area();
            public abstract void showArea();
        }
    ```
- Sub class :-
    ```java
    public class Circle extends Shape{
        private double radius, total_area;
        private float pi = 3.13f;
        public void area() {
            total_area = pi * radius * radius;
        }
        public void showArea() {
            System.out.println("Area of Circle = " + total_area);
        }
    }
    ```

    ```java
    public class Rectangle extends Shape{
        private double length, breadth, total_area;
        public void area() {
            total_area = length * breadth;
        }
        public void showArea() {
            System.out.println("Area of rectangle = " + total_area);
        }
    }
    ```
- Reference variable :-
    ```java
    public class AreaCalculation {
        public static void main(String[] args) {
            Shape s; // Reference of a abstract class
            s = new Circle();
            s.area();
            s.showArea();
            s = new Rectangle();
            s.area();
            s.showArea();
            // This method is known as dynamic method dispatch.
        }
    }
    ```
# Final Keyword
- We can use final keyword with class, method and variable.
- If you declare any variable as final then the Java compiler as constant.
    - Example :-
        ```java
        public class FinalKeyword {
            public static void main(String[] args) {
                final int n = 5;
                System.out.println(n); // 5
                n = 7; // The final local variable n cannot be assigned. It must be blank and not using a compound assignment
                System.out.println(n);
            }
        }
        ```
- When you declare a method as final, you cannot override it.
- When you decare a method as final, you cannot inherit that class.
---
Q. Create a project of classroom as main containing two object of projectors, hundred object of bench, two hundred object of chair, 180 object of students. This project is called as tight coupling.

---
# Array
- An array is a data structure that stores a fixed-size sequence of elements of the same data type.
- Example:-
    ```java
    public class Array {
        public static void main(String[] args) {
            int arr[] = new int[5];
            double arr2[] = new double[5];
            String str[] = new String[5];
            System.out.println("Integer type array: ");
            for(int i = 0; i < arr.length; i++) {
                System.out.print(arr[i] + " ");
            }
            System.out.println();
            System.out.println("Double type array: ");
            for(int i = 0; i < arr2.length; i++) {
                System.out.print(arr2[i] + " ");
            }
            System.out.println();
            System.out.println("String type array: ");
            for(int i = 0; i < str.length; i++) {
                System.out.print(str[i] + " ");
            }
    }
    ```
- Q. Write a program in java to find the greatest and second greatest element in the array.
    ```java
    public class Q_Array {
        public static void main(String[] args) {
            int arr[] = {52, 76, 63, 84, 21}, max = 0, second_max = 0;
            for(int i = 0; i < arr.length; i++) if(arr[i] > max) max = arr[i];
            System.out.println("Greatest element in the array: " + max);
            for(int i = 0; i < arr.length; i++) if(arr[i] > second_max && arr[i] < max) second_max = arr[i];
            System.out.println("Second Greatest element in the array: " + second_max);
        }
    }
    ```
# Exception Handling in Java
- An error typically refers to a mistake, fault, or deviation from accuracy or correctness.
- Exceptions are runtime errors. They occur when the code encounters an unexpected condition during its execution.
- Two types, 
    - Checked Exceptions
    - Unchecked Exceptions
- There is a special class in java to handle exceptions in java.
## Checked Excpetion
- Checked exceptions are the exceptions that have exception definition in the compiler.
- Arithmetic Exception:
    ```java
    public class ExceptionExample {
        public static void main(String[] args) {
            try {
                int a = 10, b = 0;
                int c = a / b;
                System.out.println("c = " + c);
            }
            catch(ArithmeticException e) {
                System.out.println("Exception " + e);
            }
            System.out.println("The End..");
        }

    }
    ```
- Array Exception:
    ```java
    public class ArrayExceptionExample {
        public static void main(String[] args) {
            try {
                int arr[] = new int[5];
                for(int i = 0; i <= arr.length; i++) System.out.println(arr[i]);
            }
            catch(ArrayIndexOutOfBoundsException e) {
                System.out.println("Exception " + e);
            }
            System.out.println("The End..");
        }
    }
    ```
- Null Pointer Exception:
    ```java
    public class NullPointerExceptionExample {
        public static void main(String[] args) {
            try {
                String str = null;
                int len = str.length();
                System.out.println("Length = " + len);
            }
            catch(Exception e) { // no need to write the whole exception line
                System.out.println("Exception " + e);
            }
            System.out.println("The End..");
        }
    }
    ```
- Number format Exception:
    ```java
    public class NumberFormatExceptionExample {
        public static void main(String[] args) {
            try {
                String age = "Eighteen";
                int newage = Integer.parseInt(age);
                if(newage >= 18) System.out.println("Eligible for Voting..");
                else System.out.println("Not Eligible for Voting..");
            }
            catch(Exception e) {
                System.out.println("Exception " + e);
            }
            System.out.println("The End..");
        }
    }
    ```
- Multiple Catch Block:
    ```java
    public class MultipleExcpetion {
        public static void main(String[] args) {
            try {
                String age = "Eighteen";
                int newage = Integer.parseInt(age);
                if(newage >= 18) System.out.println("Eligible for Voting..");
                else System.out.println("Not Eligible for Voting..");
            }
            catch(ArithmeticException e) {
                System.out.println("Exception " + e);
            }
            catch(NullPointerException e) {
                System.out.println("Exception " + e);
            }
            catch(Exception e) {
                System.out.println("Exception " + e);
            }
            System.out.println("The End..");
        }
    }
    ```
## Unchecked Exceptions / User-Defined Exceptions
- These are the exceptions defined by the user.
- Example:
    ```java
    public class MyException extends Exception{
        public MyException(String msg) {
            super(msg);
        }
    }
    ```
    ```java
    public class FindFactorial {
        public static void findFact(int num) throws MyException {
            if(num < 0) {
                throw new MyException("can not calculate the factorial of negative number");
            } else {
                int fact = 1;
                for(int i = 1; i < num; i++) {
                    fact = fact * i;
                }
                System.out.println("Factorial = " + fact);
            }
        }
    }
    ```
    ```java
    public class CalcFact {
        public static void main(String[] args) {
            try {
                FindFactorial.findFact(-5);
            } catch(Exception e) {
                System.out.println("Exception = " + e);
            }
        }
    }
    ```
# Wrapper Classes in Java
- A Wrapper class in Java is a class whose object wraps or contains primitive data types. When we create an object to a wrapper class, it contains a field and in this field, we can store primitive data types. In other words, we can wrap a primitive value into a wrapper class object.
- They convert primitive data types into objects. Objects are needed if we wish to modify the arguments passed into a method (because primitive types are passed by value).
- The classes in java.util package handles only objects and hence wrapper classes help in this case also.
- An object is needed to support synchronization in multithreading.
- Collections allowed only object data.
- Wrapper classes in Java are Byte, Integer, Short, Long, Float, Double, Character, Boolean.
- Example:
    ```java
    public class WrapperExample1 {
        public static void main(String[] args) {
            int a = 10;
            // converting the value from int to object
            // Integer obja = new Integer(a); -> Old School
            // Auto Boxing
            Integer obja = a;
            // converting the value from object to int
            // Auto Un-Boxing
            int a1 = obja;
            System.out.println(a1);
        }
    }
    ```
# Multi-Threading in Java
- A program under execution is called a process.
- Multithreading in Java is a process of executing multiple threads simultaneously.
- A thread is a lightweight sub-process, the smallest unit of processing. Multiprocessing and multithreading, both are used to achieve multitasking.
- However,we use multithreading than multiprocessing because threads use a shared memory area. They don't allocate separate memory area so saves memory, and context-switching between the threads takes less time than process.
- Java Multithreading is mostly used in games.
- Threads can be implemented by two ways:
    - By implementing runnable interface (best way)
    - By extending thread class
- Example:
    ```java
    public class ThreadExample1 {
        public static void main(String[] args) {
            Thread t = Thread.currentThread();
            System.out.println(t); // -> Thread[name, priority, group]
        }
    }
    ```
- Example:
    ```java
    public class MyThread {
        public static void main(String[] args) {
            ChildThread t1 = new ChildThread("Child Thread");
            for(int i = 0; i < 5; i++) {
                System.out.println("Main Thread: " + i);
                try {
                    Thread.sleep(1000);
                }
                catch (Exception e) {
                    System.err.println("Exception: " + e);
                }
            }
        }
    }
    ```
- Example:
    ```java
    public class ChildThread implements Runnable {
        private Thread t;
        public ChildThread(String name) {
            t = new Thread(this, name);
            t.start();
        }
        @Override
        public void run() {
            for(int i = 0; i < 5; i++) {
                System.out.println("Child Thread: " + i);
                try {
                    Thread.sleep(1000);
                }
                catch(Exception e) {
                    System.out.println("Exception: " + e);
                }
            }
        }
    }
    ```
# Database
- Oracle is the leader of databases in the market, because of it's security and low table algorithm.
- Download [MySQL Installer](https://dev.mysql.com/downloads/installer/).
- Select your operating system and select the second available link on the website.
- Run the installer. Make sure you have internet access, select custom->select server and workbench till you reach the end of the folder, select the files and click on the green arrow->click execute->click next/finish->click next/finish/execute till you reach the end and your system opens a program.
- Close the program and search for MySQL Command Line Client in start menu and run it.
- Type `show databases;`, it displays databases in the system.
- Type `create database database_name` to create a database.
- Type `use database_name` to change the database.
- Type `show tables;` to see the tables.
- Type 
    ```
    create table table_name
        -> (
        -> int_data_var int,
        -> text_data_var text,
        -> text_data_var text
        -> );
    ```
    to create a table with required columns.
- Type `desc table_name;` to see the table.
- Type `select * from table_name;` to fetch/show data from the table.
- Type `insert into table_name values (100, 'AAA', 'CSE');` to insert  data into the table, type `select * from table_name;` to fetch data from the table.
---
- AWT Example:-
    ```java
    import java.awt.*;
    public class AWTExample1 extends Frame{
        AWTExample1() {
            Button b1 = new Button("Click Me!!");
            Button b2 = new Button("Click Me!!");
            Button b3 = new Button("Click Me!!");
            b1.setBounds(50,100,80,30);
            add(b1);
            b2.setBounds(50,200,80,30);
            add(b2);
            b3.setBounds(150,100,80,30);
            add(b3);
            setSize(300,300);
            setTitle("This is our basic AWT example");
            setLayout(null);
            setVisible(true);
        }
        public static void main(String[] args) {
            AWTExample1 f = new AWTExample1();
        }
    }
    ```
- Swing Example:-
    ```java
    import javax.swing.JButton;
    import javax.swing.JFrame;
    import javax.swing.JLabel;
    import javax.swing.JTextField;

    public class SwingExample {
        JTextField txt_rollno,txt_name,txt_branch;
        JButton btn_save;
        JLabel lbl_name,lbl_rollno,lbl_branch;
        public SwingExample() {
            JFrame f = new JFrame();
            lbl_rollno = new JLabel("Roll no.: ");
            lbl_rollno.setBounds(50,50,100,50);
            txt_rollno = new JTextField();
            txt_rollno.setBounds(120,70,100,20);
            
            f.add(lbl_rollno);
            f.add(txt_rollno);
            
            lbl_name = new JLabel("Name: ");
            lbl_name.setBounds(50,80,100,50);
            txt_name = new JTextField();
            txt_name.setBounds(120,100,100,20);
            
            f.add(lbl_name);
            f.add(txt_name);
            
            btn_save = new JButton("Save");
            btn_save.setBounds(120,130,80,20);
            f.add(btn_save);
            
            f.setSize(300,300);
            f.setLayout(null);
            f.setVisible(true);
        }
        public static void main(String[] args) {
            new SwingExample();
        }
    }
    ```
---
## Java Database Connectivity (JDBC)
- You may need to download [drivers](https://dev.mysql.com/downloads/connector/j/) for MySQL database connectivity.
- Example:
    ```java
    import java.sql.Connection;
    import java.sql.DriverManager;
    import java.sql.PreparedStatement;
    public class DatabaseConnectivity {
        public static void main(String[] args) {
            try {
                Class.forName("com.mysql.jdbc.Driver");
                System.out.println("Drivers Registered...");
                Connection conn = DriverManager.getConnection("jdbc:mysql://localhost:3306/studentdb"/*database name*/,"root"/*user name*/,"root"/*password*/);
                System.out.println("Connecction Established...");
                String sql = "insert into tbl_student values(200,'ZZZ','CSE')";
                PreparedStatement statement = conn.prepareStatement(sql);
                statement.execute();
            } catch(Exception e) {
                System.out.println("Exception = "+e);
            }
        }
    }
    ```