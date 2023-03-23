# OOPS -2 , Singleton, static and much more

- previously after instanciating the class and try to log the reference variable, it use to print the package name along with some random string. if we want to print the exact object use ```@override```


## Packages -

- packaages are like containers for classes. we can have same multiple classes with same class name. 
- it is just like a folder.'

importing packages -> name should follow as it is defined in the file system amd oder matters.



```java 


// you can call the methods defined inside other classed




package com.koushith.packages; //this is flolder -> com->koushith->packages

import static com.koushith.packages.Message.message;

public class Greet {
    public static void main(String[] args) {
        message("Koushith");
    }
}

// -----------------------------------------

package com.koushith.packages;

public class Message {
    public static void main(String[] args) {

    }

    public  static  void message(String name){
        System.out.println("Hello , good morning" + name);
    }
}


```

- it is avaliabe only if it is declared as public


### Static

- use statc -> when certain values are not related to that object.
- we can use it without instanciating the class.

- we use ClassNAme to access this. 
- it is not dependent on objcet so we can use it before instanciating.


### Why main method should be declared as class?

- in order to run the class, object has to be instanciated. but for static methods, we dont have to instanciate.

if main is the first thing to run without, it makes perfect sense to run.

- static methods can access only static data. so to every function/most we are adding static keyword before.

```java 

public class Message {
    public static void main(String[] args) {
        message("don");
    }

    // if you remove static keyword, we cant access it.
    
     static void message(String name) {
        System.out.println("Hello , good morning" + name);
    }
}
```


- you cant call ```this``` inside static methiods
