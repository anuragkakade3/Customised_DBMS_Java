# Overview of the Code

The provided code is a simple implementation of a Database Management System (DBMS) in Java. It allows users to perform various operations on a database that stores employee records. The DBMS supports basic SQL queries such as insertion, deletion, selection, aggregation, and counting.

**Employee Class**

The `Employee` class represents a single employee record and has four attributes:

*   `EID`: Employee ID
*   `Ename`: Employee Name
*   `EAddress`: Employee Address
*   `ESalary`: Employee Salary

The `Employee` class has a constructor that initializes these attributes and a method `DisplayInfo()` that prints the employee's information.

```java
public class Employee {
    public int EID;
    public String Ename;
    public String EAddress;
    public int ESalary;

    private static int Counter;

    static {
        Counter = 0;
    }

    public Employee(String B, String C, int D) {
        this.EID = ++Counter;
        this.Ename = B;
        this.EAddress = C;
        this.ESalary = D;
    }

    void DisplayInfo() {
        System.out.println(EID + "\t" + Ename + "\t" + EAddress + "\t" + ESalary);
    }
}
```

**MarvellousDBMS Class**

The `MarvellousDBMS` class represents the Database Management System and has the following attributes and methods:

*   `lobj`: A linked list to store employee records
*   `InsertIntoTable()`: Inserts a new employee record into the database
*   `SelectStar()`: Prints all employee records in the database
*   `SelectSpecific(int ID)`: Prints employee records with a specific ID
*   `SelectSpecific(String Name)`: Prints employee records with a specific name
*   `DeleteFrom(int ID)`: Deletes an employee record with a specific ID
*   `DeleteFrom(String Name)`: Deletes employee records with a specific name
*   `AggregateSum()`: Calculates the sum of all employee salaries
*   `AggregateMax()`: Finds the maximum employee salary
*   `AggregateMin()`: Finds the minimum employee salary
*   `AggregateAvg()`: Calculates the average employee salary
*   `AggregateCount()`: Counts the number of employee records

```java
public class MarvellousDBMS {
    public LinkedList<Employee> lobj;

    public MarvellousDBMS() {
        System.out.println("Marvellous DBMS started succesfully...");
        lobj = new LinkedList<Employee>();
    }

    protected void finalize() {
        System.out.println("Deallocating all resources of DBMS");
        lobj = null;
    }

    // Other methods...
}
```

**Program665 Class**

The `Program665` class represents the main program and has the following attributes and methods:

*   `main(String Arg[])`: The main method that starts the DBMS
*   `Scanner sobj`: A scanner object to read user input
*   `MarvellousDBMS mobj`: An instance of the `MarvellousDBMS` class
*   `while(true)`: A loop that continues until the user chooses to terminate the DBMS

```java
public class Program665 {
    public static void main(String Arg[]) {
        // Create a new instance of the DBMS
        MarvellousDBMS mobj = new MarvellousDBMS();

        // Create a scanner object to read user input
        Scanner sobj = new Scanner(System.in);

        // Loop until the user chooses to terminate the DBMS
        while (true) {
            // Display the menu
            System.out.println("----------------------------------------------------------");
            System.out.println("Please select your choice based on your requirement: ");
            System.out.println("----------------------------------------------------------");

            // Other code...
        }
    }
}
```

**Example Usage**

Here's an example of how to use the DBMS:

1.  Create a new instance of the DBMS: `MarvellousDBMS mobj = new MarvellousDBMS();`
2.  Insert a new employee record: `mobj.InsertIntoTable("John Doe", "123 Main St", 50000);`
3.  Print all employee records: `mobj.SelectStar();`
4.  Print employee records with a specific ID: `mobj.SelectSpecific(1);`
5.  Delete an employee record: `mobj.DeleteFrom(1);`
6.  Calculate the sum of all employee salaries: `mobj.AggregateSum();`

Note that this is a simplified example and does not cover all the features and edge cases of the DBMS.
