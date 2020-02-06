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
  
  

## Inheritance in interface
One interface can inherit another by use of the keyword **extends** . The synatx is the same as for inheriting classes. When a class implements an interface that inherits another
interface,it must provide implementations for all methods required by the interface inheritance chain. Following is an example : <br/>
<br/>
interface A{ <br/>
  void method1();<br/>
  void method2();<br/>
}<br/>
interface B extends A {<br/>
  void method3();<br/>
}<br/>
class MyClass implements B{ <br/>
   public void method1(){<br/>
    System.out.println("Implement method1");<br/>
}<br/>
public void method2(){<br/>
    System.out.println("Implement method2");<br/>
}<br/>
public void method3(){<br/>
    System.out.println("Implement method3");<br/>
 }<br/>
}<br/>

class IFExtend{<br/>
public static void main (String args[]){<br/>
   MyClass object = new MyClass();<br/>
    object.method1();<br/>
    object.method2();<br/>
    object.method3();<br/>
 }<br/>
}<br/>

