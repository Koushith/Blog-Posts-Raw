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

in Struct car 2 is totally different from bmw.


### Loops and conditionals- pretty straight forward.


### Optionals and unwrapping

if something is not avaliable and dont want our program to break, use ``` ?``` to avoid it.

``` nil is null in swift ```

read more about unwrapping.

### Guard statements.

guard statement is very similar to if else.
helpful in validations -- check later.



### Enums

An enumeration defines a common type for a group of related values and enables you to work with those values in a type-safe way within your code.

helpful in typeSafty.

```swift=
enum States{
    case InProgress, Idle, Aborted
}

States.InProgress // how we access
```

- emums also inherits

accessing will be using . notation similar to objects.

```swift!
emum States: Int{
    case InProgress = 0,
    case Idle = 1
}
```

#### Shorthand

```swift!

enum States{
    case InProgress, Idle, Aborted
}

var current = States?  //current will be any one of the enum value. this is the shorthand to access.

current =.InProgress 
```




### Protocols

- this is very similar to ```interface``` in java or ts.

in Protocol you add the methods and properties to have.

check- deligate and datasource

```swift!


protocol CarProto {

  var color : String {get set}

  func drive() -> Bool
}

class Car{
  
}


class Bmw: Car , CarProto {

  var color : String

  init(color:String){
    self.color = color; 
  }

  func drive() -> Bool {
    // code
}
 
}
```

basically color string should be able to get and set aka update. its a rule defined un the protocol.

it defines a blueprint of methods or properties that a class, struct should have.

## Read about getters and setters.



### Strong vs weak - memory management.

- when it is safe to get rid of something from memory??

if there is no reference to any variable, and it is just initilized swift will get rid of it from memory. 

by default variables are ```strong```

```swift
  weak var colleague: "koushith"
 ```
 
 ### Closures -
 
 - kinda arrow fun- cjeck later



### String.

- we have string interpolation similar to js but with different syntax 

```swift!
var name ="koushith"
var last ="amin"

var final = "\(name) \(last)" //interpolation -> aka concatination
```
read about common methods



### Arrays and Dicts

- arrays are similar to arrays in js. can have multiple data types.

```swift!
var raw : [any] = ["koushith", 23, true]

//[string] -- it can be of any type.
```
##### Dictionaries

similar to array but hold key value pair.

```swift
var raw :[string:int] = ["roll":23, "place":571234]
```
