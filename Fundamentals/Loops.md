# Module 4 - Loops

## Topics Covered

- [For Loops](#for)
- [For Each Loop](#for_each)
- [While Loops](#while)
- [Do While Loops](#do_while)
- [Break and Continue](#break_continue)

<a name="for"></a>
## For Loops : 
### For loop is used to execute a block of code certain number of times (and times is known)

`Syntax :  for(initialization ; condition ; update){`
`             body                                  `
`             }                                     `

```java

int n = 10;
for( int i = 0 ; i < n; i++){ // also you can write( int i = 0, n = 10 ; i < n; i++){
    System.out.print (i);
}


```

<a name="for_each"></a>
## For Each Loop : 
### For each loop is used to run block of code of times the array size

`Syntax :  for(type variableName : arrayName){      `
`             body                                  `
`             }                                     `

```java

int arr = {5,4,3,2,1};
for (int num : arr){
    System.out.println(num);
}

String cars = {"Volvo", "BMW" ,"Benz" , "Ford" ,"Tata" ,"Mahindra" , "Hyundai" ,"Maruti"};
for (String i : cars){
     System.out.println(i);
}

```

<a name="while"></a>
## While Loops : 
### While Loops are used when number of iterations are not known

`Syntax :  while(condition){                        `
`             body                                  `
`             }                                     `

```java

int i = 1;
while(i<10){
    statement to be executed
    i++ ;
}
```
<a name="#do_while"></a>
## Do While Loops : 
### Body inside do while is executed atleast once in worst case and they are Exit Controlled Loops

`Syntax :  do{                                      `
`             //Code  to be executed                `
`             }                                     `
`             while(condition);                     `

```java

int i = 1;
do{
    System.out.print( " "+i);
    i++;
}while(i<10);

```
<a name="#break_continue"></a>
 
 ## BREAK : 
 `Break statement is used to exit out of loop`

  ## Continue : 
 `Continue statement is used to skip the iteration`

```java

public static void main (String[] args){
    while(true){
        int num = int (Math.random()* 10 + 1);
        if (num==5)
            break;     // break jumps out of the loop
        if (num % 4 == 0)
            continue;
        System.out.println(num + " ");
    }

}

```






