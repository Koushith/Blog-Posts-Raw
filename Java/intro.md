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






### string- this is pretty weird compared to other languages.


a="koushith"
b="koushith"

a==b // true --- it is pointing to same object


### Functions

- functions in java- we call it as methods

return type-> the value of the returned variable.
if you dont want to return anything- write void. 

```java 
   static int sum2(){
        return  xxx;
    }
```

passing params- pass in the order of decelaration.

``` java 
sum(int a, int b){   ----params

}


sum(20,30) --- args

```


in Java there is no pass by reference. 

```java 


psvm(s a){
    name ="koushith";
    greet(name);
   s.o.pln(name) 

    greet(naam){
       naam="amin"
        xxxxxxxxxx 
    }
}

koushith
amin

```


here name is a reference variable and value is stored somewhere in the heap

- here the value is passed inside fn call. not the reference.

name and naam is same. and naam is the copy of reference variable.

### Scoping


- values that are initilized inside the block will remain inside the block.

```
{
some code declared here- it is not accessable outside
}

```

but if you try to access something which is already initilized in the same methods will be accessable

goes well for the for loops aswell.

in js that is not the case.

```java
 public static void main(String[] args) {
        int a=20;
        String name ="koushith";
        greet(name);
        System.out.println(name);
        System.out.println(a);
        for (int i=0; i<20; i++){
        System.out.println(a);
        }
    }
```
### Loop scope
it will print 20- but if you try to initilize inside for loop. it wont allow. in js we can- 

### Shadowing


when we use a same variable name in differnt scopes, and try to log it it shadows the high level scope var value.

```javas 
package koushith;

import java.util.Scanner;

public class sum {

    static int a=30;
    public static void main(String[] args) {
        System.out.println(a);
        int a=20;
        String name ="koushith";
        greet(name);
        System.out.println(name);
        System.out.println(a);
        for (int i=0; i<20; i++){

        System.out.println(a);
        }
    }

}
```

- value of a will be shaodwed to 20 inside main function.
- it all depends n scope, where you have defined the cariable.

class variable should be in static.
scope will begin when the value is initilized.


### Variable args

- when you dont know the length of the params use this. 
```
static void leng(string ...v){
code goes here.
}
```


### Function overloading

- when you have a function of same name, but different parameters, it is known as overloading.
- it checks at compile time. based on the arguements passed to it.

there is no concept of overloading in js.

```java 
package koushith;

public class OverLoading {
    public static void main(String[] args) {


        func("hello");
        func(20);
    }

    static void func(int a){
System.out.println(a);
    }

    static void func(String a){
        System.out.println(a);
    }


}
```

Note - parametser should be different. or else it will throw an error

