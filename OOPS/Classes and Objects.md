# Module 1 - Classes and Objects

## Topics Covered

- [Class](#Class)
- [Object](#Object)
- [Constructor](#chapter1)



<h1>OOPS :</h1><h3>Object Oriented Programming Style deals with Classes and Objects.</h3>

<a name="Class">
<h1>Class :</h1><h3>Blueprint for an Object </h3>
</a>

<a name="Object">
<h1>Object :</h1><h3>Entity with some state and some behaviour </h3>
</a>

### For Instance 

| Class             |               Object                   |
| ----------------- | -------------------------------------- |
| Factory           |                Car                     |
| ----------------- | -------------------------------------- |
| `Car1`            |    Properties   |   Functionalities    |
| `Car2`            | -------------------------------------- |
| `Car3`            |  `Model Name`   |        `Drive`       |
| `Car4`            |    `Color`      |     `Lock/Unlock`    |
| `Car5`            |    `Price`      |        `Music`       |


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

    void unloc

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

Java Constructor is special method called when an object is instantiated.
It has the same name as class itself and is invoked automatically at the time of Object construction.