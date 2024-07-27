# Module 6 - Strings

## Topics Covered
- [Definition](#definition)
- [String Class Methods](#string_class)
- [String Concatenation](#string_concatenate)
- [String Builder](#string_builder)
- [String vs Char](#string_char)
- [Palindrome](#palindrome)

<a name="definition"></a>
## Definition : 
### String is a data type used to represent text

String Pool resides in Heap memory

### String Pool

|  "abc"        |    
|  "Hello"      |   
|   "Ram"       | 

    String s1 = "abc";
    String s2 = "Hello";
    String s3 = "Ram";
    String s4 = "Ram";

    String s5 = new String ("abc");  `New Object is Created`

if( s1 == s5 ) returns false, bcoz it checks whether objects being referred are same<br>
if( s3 == s4 ) returns true, bcoz it checks whether objects being referred are same

if(s1.equals( s5 )) returns true, bcoz it checks whether Contents are Same and not objects

<a name="string_class"></a>
## String Class Methods : 

### 1. .charAt(x)
`.charAt(x) accessed the character at specified Index`

    String name = "Ishu";
    System.out.println(name.charAt(2)); // returns h 

### 2. .length()
`.length() returns the length of String`

    String name = "Ishu";
    System.out.println(name.length); // returns 4

### 3. .indexof() 
`index0f() returns the index of first occurence of specifies char or String`

    String sen = "Hello World";
    System.out.println(sen.indexof("World")); // returns 6

### 4. .equals() 
`equals() compare whether two strings contains same sequence of characters`

    String str1 = "abc";
    String str2 = new String("abc);
    System.out.println(str1.equals(str2));  //True
    System.out.println(str1 == str2);  //False

### 5. contains()
`returns boolean value, if String contains specified sequence of char values`

    String Str = "Hello" ;
    System.out.println(str.contains("ll"));
    System.out.println(str.contains("abc"));

### 6. toLowerCase(), toUpperCase()
`returns new String, original remains intact`

    String str1 = "rajath";
    String str2 = "YASH";

    System.out.println(Str1.toUpperCase()); //returns RAJATH
    System.out.println(Str2.toLowerCase()); //returns yash

### 7. substring() 
`returns substring of String`

    String str = "I Love Programming";
    System.out.println(str.substring(7));   // Programming
    System.out.println(str.substring(2,6)); // Love


<a name="string_concatenate"></a>
## String Concatenation : 

`Concatenated using +`

    String str1 = "Hello";
    String str2 = "World";
    System.out.println( str1 + str2) ;  //Hello World

### When we try to concatenate non-Primitive Datatypes, typecast to string

    String king = "Virat";
    String[] queen = {A,N,U,S,H,K,A};
    System.out.println( king + " "+ Arrays.toString(queen)); // Virat [A,N,U,S,H,K,A]

### Reverse of a String

    String inp = "ARM";
    String rev = "";

    for(int i = inp.length ; i > 0 ; i-- ){
    
    rev = rev + inp.charAt(i);

    }
    System.out.println(rev);

<a name="string_builder"></a>
## String Builder :

`Since strings are immutable, we use String Builder to modify old instances`

    StringBuilder inp = new StringBuilder(" Water Bottle ");

    inp.append( content );                                     // inp.append(" and Lunch Box");
    inp.insert(Starting index, content );                      // inp.insert( 13, "and Lunch Box" );
    inp.replace(Starting index, Ending index , content );      // inp.insert(0 , 6, "Juice" );
    inp.delete(Starting index, Ending index);                  // inp.delete(7,13);

    String str = inp.toString();

<a name="string_char"></a>
## String vs Char :

    String rock = "Water";
    Char[] arr = {'w','a','f','e','r'}

    Converting String to Array :
    char[] word = rock.toCharArray(); // {'w','a','t','e','r'}

    Converting Array to String :
    String rcb = new String(arr); //wafer

<a name="palindrome"></a>
## Palindrome String

    String rcb = sc.nextInt();  // TENET , Water
    StringBuilder sb = new StringBuilder(rcb);
    sb.reverse();

    String rcb2 = sb.toString();
    System.out.println(rcb2);   // TENET, retaW