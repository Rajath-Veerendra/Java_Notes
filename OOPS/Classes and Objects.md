# Module 1 - Classes and Objects

## Topics Covered

- [Class](#Class)
- [Object](#Object)
- [Constructor](#Constructors)
- [Access Modifiers](#AccessModifiers)
- [Objects in Memory](#objectsinMemory)



<h1>OOPS :</h1><h3>Object Oriented Programming Style deals with Classes and Objects.</h3>

<a name="Class">
<h1>Class :</h1><h3>Blueprint for an Object </h3>
</a>

<a name="Object">
<h1>Object :</h1><h3>Entity with some state and some behaviour </h3>
</a>

### For Instance 

| Class     | Object   |
|-----------|----------|
| Blueprint | Car      |

| Car    |  Properties  |  Functionalities  |
|--------|--------------|-------------------|
| `Car1` | `Model Name` | `Drive`           |
|        | `Color`      | `Lock/Unlock`     |
|        | `Price`      | `Music`           |



Now considering Factory and Car as an example,

>Blueprint(Class) is the planning of how cars are manufactured, and factory is the place where we create cars(Objects).

```java

/* ------------ Blueprint ------------ */
class Car{
    String model = "Hatchback";
    String color = "Black";
    int price = 1000000;
    boolean isLocked = false;

    void drive(){
        System.out.println("Zoom Zoom Zoom");
    }

    void lock(){
        isLocked = true;
        System.out.println("Car is locked");
    }

    void unlock(){
        isLocked = false;
        System.out.println("Car is now unlocked");
    }

    void music(){
        System.out.println("I'm in the shape of you 🎶🎶🎶");
    }

    int getPrice(){
        return price;
    }

    void setprice(int priceValue){
        price = priceValue;
    }


/* ------------ Factory ------------ */
class Main(){

    public static void main(String[] args){
        Car c1 = new Car();
        Car c2 = new Car();

        System.out.println(C1.color); //Black
        System.out.println(C1.model); //Hatchback
        System.out.println(C1.price); //100000

        C2.color = "Gray";
        System.out.println(C2.color); //Gray


        C1.lock();
        C2.unlock();

        C2.setprice(5000);
        System.out.println(C2.getPrice());
    }
}

}

```

<a name="Constructors">
<h1>Constructors</h1>
</a>

Java Constructor is special method called when an object is initialized.
It has the same name as class itself and is invoked automatically at the time of Object construction.

There are 3 Types of Constructors:
   - Default Constructor :
   - Parameterized Constructor :
   - Copy Constructor :  


### Default Constructor
A constructor that has no parameters is known as default the constructor. A default constructor is invisible.

### Parameterized Constructor 
A constructor that has parameters is known as parameterized constructor.

### Copy Constructor
There is no such inbuilt copy constructor available like in other programming languages, instead we can create our own copy constructor by passing the object of the same class to the other instance(object) of the class.

 ```java

/* ------------ Constructor Blueprint ------------ */
class Car{

    String model = "Hatchback";
    String color = "Black";

    car(){  //--------Default Constructor
    String model = "Hatchback";
    String color = "Black";
    }

    Car(String Model_Name, String Which_Color){ //--------Parameterized Constructor

        model = Model_Name;
        color = Which_Color;
    }

    car(Car CC){  //--------Copy Constructor
    String model = CC.model;
    String color = CC.color;
    }
    

/* ------------ Constructor Factory ------------ */
class Main(){

    public static void main(String[] args){
        

    // Create Constructor Object

   
    Car c2 = new Car();              //----- Default
    Car c1 = new Car("SUV","Red");   //----- Parameterized
    Car c3 = new Car(C1);            //----- Copy

    System.out.println(C1.model); //Hatchback
    System.out.printlm(c1.Color); //Black

    System.out.println(C1.model); //SUV
    System.out.printlm(c1.Color); //Red

    System.out.println(C3.model); //SUV
    System.out.printlm(c3.Color); //Red

    }
}

}

```

<a name="objectsinMemory">
<h1>Objects in Memory</h1><h3>How Objects are stored in memory?</h3>
</a>

Primitive datatypes are stored in stack memory.
Non-Primitive datatypes are stored in heap memory, but address to this non-primitive datatypes are stored in stack memory.
 
### For instance

```java

class main(){
    int x=10; //x and y is stored in stack memory 
    int y=20;

    
    System.out.println(x+" "+y); // 10 20
    swap(x,y);
    System.out.println(x+" "+y); // 10 20

    /* Here, the values are not swapped because, once the values have been passed through swap function,
     inside the swap fuction the values are swapped, but the x and y in main function are not swapped */

    Pair p1 = new Pair();
    p1.x = 10; //Object p1 is created in heap memory.
    p1.y = 20; //also values are stored there itself.

    System.out.println(p1.x+" "+p1.y); // 10 20
    swap(p1.x,p1.y);
    System.out.println(p1.x+" "+p1.y); // 20 10

    /* Here, the values are swapped because, once the values have been passed through swap function, 
    swapped values are not of swap function, values are of Object itself*/


}

private static void swap(int x, int y){
    int temp = x;
    x = y;
    y = temp;
}

class Pair(){
  int x ;
  int y ;

}


```



<a name="AccessModifiers">
<h1>Access Modifiers</h1><h3>Keywords used to control the Visibility</h3>
</a>


| Access Modifier | Description                                         |
|-----------------|-----------------------------------------------------|
| public          | `Code is accessible across all classes`             |
| private         | `Code is accessible only within the class.`         |
| default         | `Code is accessible across all classes within the`  |
|                 | `same package, but not outside of it.`              |
| protected       |                                                     |
