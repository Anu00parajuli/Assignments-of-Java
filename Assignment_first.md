## Anonymous array in JAVA
An array in Java without any name is anonymous array. It is an array just for creating and using instantly.

We can create an array without name, such type of nameless arrays are called *anonymous array*.
The main **purpose** of anonymous array is just for instant use (just for one time usage) .
Anonymous array is passed as an argument of method.

Syntax :
new int[] { 1, 2, 3, 4};  //int type anonymous array

An example to illustrate the concept of anonymous array is given below :

class Test { <br/>
    public static void main(String[] args) <br/>
    { </br>
        sum(new int[]{ 1, 2, 3 });  //anonymous array
    } </br>
    public static void sum(int[] a) <br/>
    { <br/>
        int total = 0; <br/>
          for (int i : a) { <br/>
            total = total + i; <br/>
         System.out.println("The sum is:" + total); <br/>
    } <br/>
    
} 
