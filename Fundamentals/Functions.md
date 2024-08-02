# Module 7 - Functions

## Topics Covered
- [Definition](#define)
- [Parameters and Arguments](#param_args)
- [Return Types](#return)
- [Method Overloading](#overloading)
- [Call Stack](#call_stack)
- [Scope of Variable](#scope)
- [Variable Arguments](#varargs)


<a name="define"></a>
## Definition : 
### Blocks of Code executed, only when they are called.

```java

    void hello(String name){

        System.out.println(" Hello ");

    }

    // void  - return type of function
    // hello - name of function
    // String name - Parameters( Multiple allowed, None allowed )
    // { .... }  - body of the function

    //----------***------------***-----------***---------------//
    

    class main{
        static void tea() {  ...  }
        static void coffee() {  ...  }
    }

    public static void main ( String[] args){

        tea();   // To call a function inside a function, both methods should be Same 
        coffee(); // ( here, in this case is static )

    }

    //----------***------------***-----------***---------------/

```
<a name="param_args"></a>
## Parameters and Arguments 

```java

public static void main(String[] args){

    int age = 23;
    intro (age); // Here intro function is called


}

void intro (int age){   // Here age paramater is passed as argument

System.out.println(" My age is : " + age);

}


```
<a name="return"></a>
## Return Types 
### return some values back to caller using return statement

``` java

int x = square(5); //25

int square (int num){ // here returntype is int
    returm num*num ;
}

// No return, hence void

void square(int num){

    System.out.println(num);
}

```

<a name="overloading"></a>
## Method Overloading
### Act of having multiple methods having same name but different parameters

```java

class Main{

    static int add(int a , int b ){
        System.out.println(" Inside first add ");
        return a + b ;
    }

    static String add( String a, String b){
        System.out.println(" Inside second add ");
        return a + b ;
    }

    public static void main( String [] args){
        System.out.println(add(5,4));
        System.out.println(add( "Hello ", "World "));
    }

}


```

Method signature works only on the name of the method & parameters of method,
But does not account for return types.

## Call Stack : 
### Call Stack is used by program to keep track of method calls 
`Call Stack is made up of Stack Frames` 

## Scope of Variable :
### Region of Program which is accessible

## Variable Arguments - varargs

Syntax: 

    return_type methodName( dataType... args){
        // body
    }

Variable Argument (varargs) is an argument of a method that can accept any number of values.

```java

class Main{
    public static void main(String[] args){
        float avg1 = getAvg(4,5,6);
        float avg2 = getAvg(2,8,9,4,5,1,7);

        System.out.println(avg1);
        System.out.println(avg2);
    }

    static float getAvg(float... varargs){
        float total = 0;
        for ( float num : varargs){
            total += num;
        }
        return total/varargs.length;  
    }

}

s
```


