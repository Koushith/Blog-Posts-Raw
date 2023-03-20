# OOPS in Java

Quick analogy to understand OOPS.

lets say you want to create an application for a client with following requirements.

- able to store 5 numbers
- store 5 names
- marks of 5 students

you can do something lile

```java 

public class Main{
    psvm(string[] args){
        // store 5 roll numer
        int[] numbers = new int[5];
        
        //store 5 names
        string[] names = new String[5]
    }
}

```

now the new requirement pops up- you are creating individual ds for all info. can we combine all and create ``` {rollNo, name, marks} ``` DS?

Thats were Classes and OOP's comes in,

something like creating your own data type which contains certain info.

ex-  Student[] students = new Student[5]

class is a named groups of properties and functions. 


```

car example --

Class Car
    - engine
    - tyres
    - isGeat
    
Car Ferrari = new Car()

Ferrari 
    - petrol
    - 4
    - true
    
```

using this one Car template we created ferrari, template will be same, we can create n number of cars.

Ferrari is an instance of that class.

Class - logical construct
object - physical ---> occupies space in memory
 
 
 objects are stored in the heap memory
 reference variables are stored in a stack memory.
 
 - instance variables- variables that are inside instace of an object.

linking reference variable with instance variable.

```

let c1 = new Car("ferrari", "petrol", true)

c1-- reference variable stored in a stack
Car --- instance - obj stored in a heap mem

c1.name ---> accessing using dot notation.name is a instance variable

```

### new() Keyword

- in order to create an instance from class you need to initilize them.

when something is not initilized - by default it is ```null``` in java. ```undefined``` in JS.

- ```new xxx() ``` dynamically allocates memory at run time and returns a reference to it.





| stack.   |          | heap.            |
| -------- |          | ---------------  |
| Student  |          |     -------        |
                      |  | name :"jaja" ||
                      |  | roll :225    |


This is how it is stored in java. hence all class objects in java are allocated memory dynamically- i.e during runtime.

all the variable are allocated during compile time and
objects---> during run time. i.e while the program is running.

- new keyword does the dynamic memory allocation.


### Check for default values later. 


```java 

//pseudo code

class Student{
    name:"xxx",
    roll
    cgpa:2.5
}

Student student = new Student()

student.name = "koushith"

student.name // xxx --> koushith
student.roll // returns the defaukt value if no value present.in this case its null

```

#### Constructor

- assing a values like above example becomes repetative. 

constructor basically defines what happens when the object is created. aka used to initilize the value of objects.

constructor is a special funcytion that runs when it is instanciated.

```java 
package koushith;


public class Main {
    public static void main(String[] args) {

        Student koushith = new Student(15, "Koushith", 85.4f);
        Student rahul = new Student(18, "Rahul Rana", 90.3f);
        System.out.println(koushith.name);
        
    }
}

class Student {
    int rno;
    String name;
    float marks = 90;
    
    //constructor name should be same sa class name
    Student (int rno, String name, float marks) {
        this.rno = rno;
        this.name = name;
        this.marks = marks;
    }
}

// internally this will be replaced with reference variable

```

- constructor name should be same as class name.
- in js - if you rey to log the ref variable - it will print all properties with default value or with ```undefined``` . that's not the case in java

you can add the methods inside class


```java 

class Student {
    int rno;
    String name;
    float marks = 90;
    
    //constructor name should be same sa class name
    Student (int rno, String name, float marks) {
        this.rno = rno;
        this.name = name;
        this.marks = marks;
    }
    
    void greeting(){
        System.out.println("Hello" + this.name);

    }
}

// you can access it by

 Student rahul = new Student(18, "Rahul Rana", 90.3f);

rahul.greeting()

```

### You can also overload the constructor similar to functions. based on params passed it will determine.


### Why we dont need new keyword for primitives?

- primitives are not implimented as objects.

check passing referene vs value


### Final Keyword

- this makes sure that the content is not modifed. const
- const ---> final

```java 

final int a = 5 //you cant modify this. just like other languages you have to initilize this.
```

it works only for primitives. for reference type- naaah

### Garbage collection

- when obj is no longer referenced, or var is ideal, java does this to free up memory,

there is a method ```finalized``` this will run when the object is destroyed. read more.
