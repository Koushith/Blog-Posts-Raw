### OOPS - Raw and unedited

# OOPS

## Primitive Data types 
    -who's value is known - string, int etc
## Non primitive- objects
    - helps in grouping all related data

Eg- lets say you are developing a chess game- 

A coin might have certain properties like -color, position and isCaptured. if we are using a primitive we might need 3 differnt variable to store single coin.

with the help of objects we can store in one variable.

 ``` let coin ={color:"black", isCaptured:false, position:"xxx"}```
 
 we have 4 differnt pieces, insted of creating 4 differnt objects we can create a boilder plate and create coins out of it. aka ```Class``` and ```instance of class```
 
 
 Struct in c is similar to arrays. struct had some limitations- read latter.
 
 ### Objects
 - Objects are the instance of class. using class we can create multiple objcts

### Class
- class is like a template or blueprint to create more objects.




ex-    knight

class knight
 - color
 - move()
 - position

we are not assigning the value here- rather we can create an instance of class and assign the values over there.

if we assign the values here, it will start from the defaut assigned position which we dont want.

we can define move inside calss- coz it has the fixed movement behaviour.

### OOPS helps us in writing more complex programsby groupig related data and functions togather. 


The main princples of OOPS are
 - Encapusaltion
 - Abstraction
 - inheritance
 - Polymorpism

#### Encapsulation

- basically defining the methods within the class. i.e setters, getters etc. 
- the data is hidden from other code outside the class. 
- data access is only from provided methods.
- it helps to protect the data that is bein modified or accessed outside
- encapsulation is achieved through the use of access modifiers such as 
    - public.
    - private. 
    - protected. 

These access modifiers determine which parts of the program can access the data and functions of an object.

 
#### Abstraction

- hiding out all implimentation details nd showing only necessary things.

you dont need to know the implimentaion details. just use the methods provided and use it. 

another analogy would be, driving a car, it has .move, .break(), .getFuel() methods. just use it. you dont need to know the implimentstions.

we are doing this with interface

#### Inheritance

- derive one class from another class.
- parent class is known as super class and children which is inheriting is known as subclass

#### Polymorphism

- this is closely related to inheritance.
- poly... methods that can take many form.

###### There are two types of poly
    - Dynamic
    - Static



##### Dynamic

- dynamic polymorpism occurs during the runtime of the program. this descriples when the signature is defined in both subclass and super class
- The methods share same name but have diffrent implimemtations.
- the subclass implimentations of methods overrides superclass implimentations.

This works because the form of the method is decided based on where is the form hirarchy called.


###### Static

- this occurs during the compile time.
- when multiple methods can have same name but different parameters.
    - differnet number of parameters
    - differnt types of paramerted

this is called method overloading. 

based on the params match, the method will be executed.
