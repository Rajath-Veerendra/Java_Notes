# Module 9 - Multidimensional Arrays

## Topics Covered
- [Definition](#define)
- [Create a Matrix](#matrix)
- [Printing the Matrix](#print_matrix)
- [Reading the Input](#read_input)
- [Examples](#example)

<a name="define"></a>
## Definition : 
### It is an array of arrays<br>
### It is useful, when you want to store data as a tabularform ( matrices or grids), like a table with rows and columns.

Eg:

    int[][] numb = { { 1,2,3,4 }, { 5,6,7,8 } };
    System.out.println ( numb[1][2] );  // Outputs 7
    System.out.println ( numb[0][3] );  // Outputs 4

### Loop through Multi-Dimensional

    for( int i=0; i< numb.length ; i++){

        for( int j=0; j < numb[j].length ; j++){

            System.out.println ( numb[i][j] );
    }
    }

    // numb.length = 2
    // numb[0].length = 4
    // numb[1].length = 4

<a name="matrix"></a>
### Create a Matrix
 
```plaintext
   __       __
0 |           |    int rows = 3;
1 |           |    int columns = 4; 
2 |__       __|    int[][] a = new int[rows][columns];
   0  1  2  3

```

<a name="print_matrix"></a>
### Printing the Matrix

```java

    // Iterarting over 2D Arrays (Matrix) and printing it.
    for( int i=0 ; i<arr.length ; i++ ){
        for( int j=0 ; j<arr.length ; j++ ){
            System.out.print( a[i][j] + " ");
        }
        System.out.println(""); 
    }

```

<a name="read_input"></a>
### Reading the Input

```java

    Scanner sc = new Scanner(System.in);

    int rows = sc.nextInt();
    int columns = sc.nextInt();

    int [][] matrix = new Int[rows][columns];

    for(int i=0; i< matrix.length; i++) // matrix.length returns number of rows
    {
        for(int j=0 ; j < matrix[i].length ; j++){
            matrix[i][j] = sc.nextInt();  
        }
    }


```

<a name="example"></a>
### Sum of two Matrices


```plaintext

    SAMPLE INPUT                            SAMPLE OUTPUT

    rows = 2
    columns = 2

   __       __           __      __        __      __
  | 1   2   3 |         | 10 20 30 |      | 11 22 33 |
  | 4   5   6 |   +     | 40 50 60 |   =  | 44 55 66 |
  |__       __|         |__      __|      |__      __|

```

