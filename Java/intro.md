### Java 1

- in java we write every program iniside a class. java file itself is a class. 

MyProg.java - this file is a class. class is a named group of properties and methods

- file name should be same as class name.

naming convension- if a variable starts with uppercase- it is a class.

- pubilc. ---> this class can be accessed from anywhere.


in java we should have main function- that's where your program starts.

if you comiple a java code we will get xxx.class -> this is nothing but the byte code.

if you share this code- any one will be able to run .class file.

```

public class Main{
    public static void main(String[] args){
        System.out.println(args);
        System.out.println("Hello");

    }
} 

```

main is the reserved keyword. all the function execution starts from here.

- static -> to run a class without creating any object. aka to run without creating a object of a class.
- void is a return type. here in main- we dont want any return type.
- string[] args. ---> if you pass any arguements it will be stored in the array.

you can seperate your src and compliled file. use -d flag while compiling.


package- it is a folder where your java file lies.

System is a class which has few methods in it.


Taking the user input- 
- we have a scanner class which helps to take user input.
- input can be from anywhere- file, cmd etc
- we have to instanciate the scanner and specify where do we want to take the input.


### Primitive

- any type which we cant break further. it is defined and we know the type.

String is not a primitive- we can break further into char

"koushith" ---> k  ->o -> u


```
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {

        Scanner input = new Scanner(System.in);
        System.out.println(input.nextLine());
    }
}

```

 - scanner is the class that is required to take the input
 - input is the object we are creating to take the input
 - new is the keyword we use to take the input
 
 
 ```
 import java.util.Scanner;

public class Main {
    public static void main(String[] args) {

        Scanner input = new Scanner(System.in);


        int num = input.nextInt();
                int num2 = input.nextInt();
                        int sum = num+num2;
                                System.out.println("sum" + sum);
    }
}
```

create one input scanner object and use that.


### Type conversion

- conversion of one data type to another data type that happens automatically. (if some conditions are met)

when?
- when two types are compactable- float and int, float and double

- destination type shoud be greater than source type.

### Type Casting

-  we are converting from one type to another. aka explicit conversion.

### Loops

 - when you dont know how many times the loop should run, use while loop
 - when you know how many times - use for
