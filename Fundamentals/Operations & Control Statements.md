# Module 3 - Operations & Control Statements

## Topics Covered

- [Arithmetic Operators](#arithmetic)
- [Relational Operators](#relational)
- [Assignment Operators](#assignment)
- [Logical Operators](#logical)
- [Branching - if else](#if_else)
- [Ternary Operator](#ternary)
- [Branching - switch](#switch)

<a name="arithmetic"></a>
## Arithmetic Operators : 
### ( + , - , * , / , % , ++ , --)

<a name="relational"></a>
## Relational Operators : 
### ( == , > , < , >= , <= , != )

<a name="assignment"></a>
## Assignment Operators : 
- ( x = 3)
- ( x += 3)  `x = x+3` 
- ( x -= 3)  `x = x-3`
- ( x /= 3)  `x = x/3`
- ( x *= 3)  `x = x*3`
- ( x %= 3)  `x = x%3`

<a name="Logical"></a>
## Logical Operators : [ & / && , | / || , !] 
- && → `Logical Short Circuit AND` → checks second statement only if first one is true
- || → `Logical Short Circuit OR` → checks second statement only if first one is false 
- !  → `NOT ` → returns the reverse of boolean value

<a name="if_else"></a>
## if else : 
### if statement is used to test a boolean condition, 

```java

if(condition){
    body;
}else if{
    body;
}else{
    body;
}

```
### eg : To check even or odd

```java

import java.util.Scanner;

public class Main {
  public static void main(String[] args){

    System.out.println("Enter an Integer :");
    Scanner input = new Scanner(System.in);

    if(input.hasNextInt()){
        int x = input.nextInt();
        System.out.print(" "+x);

        if(x%2 == 0){
            System.out.println("Entered Integer is Even Number");
        }else{
            System.out.println("Entered Integer is Odd Number");
        }

    }else{
        System.out.println("Not an Integer !");
    }


  }

}

```

<a name="ternary"></a>
## Ternary Operator : (short hand if else)
### Ternary/Condition Operator lets you write one line of Code 

`Syntax :  variable = (condition) ? expression_True : expression_false ;`

```java

public static void main(String args) {

    int age = 10;
    String result = (age >= 18) ? "Yes, you can vote!" : "No, you can't vote!";
    System.out.println(result); // prints -> No, you can't vote!

}

```


<a name="switch"></a>
## Switch Case : 
### Switch Case is used to tranfer control to a particular block of Code

```java

switch(weather){
    case "Rainy" :
        System.out.println("Take Umbrella");
        break;
    case "Sunny" :
        System.out.println("Carry sunglasses");
        break;
    case "Chill" :
        System.out.println("Carry Jacket");
        System.out.println("also Carry Muffler");
        break;
    default :
        System.out.println("Carry Jacket");
}

```
### Lets write the above code using "Enhanced Switch Case" method

```java

// In Enhanced Switch Case, no need of using break statements.

switch(weather){
    case "Rainy" -> System.out.println("Take Umbrella");  // Single Code Lines

    case "Sunny" -> System.out.println("Carry sunglasses");

    case "Chill" -> {
                System.out.println("Carry Jacket");        // Multiple Code Lines
                System.out.println("also Carry Muffler");
    }
    default -> System.out.println("Carry Jacket");
}

```



