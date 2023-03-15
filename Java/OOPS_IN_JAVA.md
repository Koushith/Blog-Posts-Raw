
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
                      |  | roll :225    ||






This is how it is stored in java. hence all class objects in java are allocated memory dynamically- i.e during runtime.

all the variable are allocated during compile time and
objects---> during run time. i.e while the program is running.



















