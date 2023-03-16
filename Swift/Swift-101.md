# Swift Academy

### Var let and Static


- d
- d
- d
- Static variables will be inside the class and we can access them without instanciating,

```swift=

class Person{
    static let name="koushith";
    xxxxx
}

Person.name // koushith
```


### Types

- Type inference - swift will automatically detect the type if you dont specify the data type

```swift
var name ="koushith"

type(of: name ) // swift way of checking things.

```

Swift is the strongly typed language. you can define the types while declaring the variable.

```swift
var name:String ="koushith"  //annotation

```

Classes are used to create our own type.

you can either include the type or swift will annotate according to its types.

- when dealing with ui elements like buttons etc, swift is included with UIKit.

eg - 

```swift=

var button : UIButton = UIButton()
```


### Functions and parameters

- grouping a piece of reusable code.

```swift=

func add(){
    //code goes here
}


func add(a:Int, b:Int ) -> Int {
    return a+b
}

add(a:5, b:5)


//. -> Int -this is a signature which specifies the return type is int

```


### Classes and Structs

everything in the world can be modelled around objects. thats the concepts behing OOPS

##### You can model the object in two ways.
- Classes
- Struct

one difference is the notion of inheritance.

```swift=

class Vehicle{
    //code
}

class Car : Vehicle{
    //code
}

// this is the syntax for extending the class. aka inheritanc.

```

in swift ```init``` is the initilizer- like constructor.

```swift=
class Car{
  
    let make : String
    let color : String

  init(make: String, color: String){
    self.color=color
    self.make=make
  }
}

var bmw = Car(make: "BMW", color: "red")

print(bmw.color) //red
```

#### Struct 

- struct is exacly similar to class with minor difference.

Class is a reference type
Struct is a value type


reference type --- it will be pointing to same variable and any changes will modify the reference value aswell.

value type- i.e in ```struct``` it will create a copy and original value is isolated from copy.

```swift=
class Car{
  let make : String
  
  let color : String

  init(make: String, color: String){
    self.color=color
    self.make=make
  }
}

var bmw = Car(make: "BMW", color: "red")
var car2 = bmw    // whenever mbw changes car 2 changes. coz of reference type changes.

```
