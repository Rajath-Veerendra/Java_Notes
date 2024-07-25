# Module 5 - Arrays

## Topics Covered
- [Array Basics](#basics)
- [Input Output](#i_o)
- [Linear Search](#linear)


<a name="basics"></a>
## Definition : 
### Data Structures that stores data of the same type in a sequential manner.

```java

int [] marks = new int[10]; 
float [] marks = new float [5];
marks[0] = 10;
marks[1] = 20;

// OR

int[] marks = {1,2,3,4,5,6,7,8,9,10};
System.out.println(marks[0]);

```
<a name="i_o"></a>
### INPUT OUTPUT ARRAYS

```java
Scanner sc = new Scanner(System.in);

int[] arr = new int[5];

// INPUT LOOP
for(int i =0; i<arr.length ; i++){
    arr[i] = sc.nextInt();
}

// OUTPUT LOOP
for(int i = 0; i<arr.length ; i++){
    System.out.println(arr[i]);
}
```
<a name="linear"></a>
### Linear Search Algorithm

```java

int n = input.nextInt();
int[] arr = new int[n];

for(int i = 0 ; i < arr.length ; i++){
    arr[i] = input.nextInt();
}

int key = input.nextInt();
int ans = -1;

for(i=0;i<n;i++){

    if(arr[i] == key){
        ans = i;
        break;
    }

}

```

### Linear Search Algorithm using For Each Loop

```java

int n = input.nextInt();
int[] arr = new int[n];

for(int i = 0 ; i < arr.length ; i++){
    arr[i] = input.nextInt();
}

int key = input.nextInt();
int ans = -1;

// Perform linear search using for-each loop
    int i = 0;
        for (int num : arr) {
            if (num == key) {
                index = i; // Update the index where key is found
                break;
            }
            i++;
        }

```
