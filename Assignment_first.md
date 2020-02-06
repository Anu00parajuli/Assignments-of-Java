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
## Nested Interfaces
An interface can be declared a member of a class or another interface. Such an interface is called a ""member interface"" or ""nested interface"".A nested interface can be declared as
public, private or protected. This differs from a top-level interface, which must either be declared as public or use the default access level, as previously described. When a nested 
interface is used outside of its enclosing scope, it must be qualified by the name of the class or interface of which it is a member. Thus, outside of the class or interface in which a
nested interface is declared, its name must be fully qualified.<br/>
Here is an example that demonstrates a nested interface : <br/>
class A { <br/>
   public interface NestedIF{ <br/>
boolean isNotNegative(int x); <br/>
}<br/>
}<br/>
class B implements A.NestedIF{
 public boolean isNotNegative(int x){ <br/>
   return x < 0 ? false : true; <br/>
} <br/>
}<br/>
class NestedIFDemo { <br/>
  public static void main (String args[]) { <br/>
     A.NestedIF nif = new B(); <br/>
     if(nif.isNotNegative(10))<br/>
        System.out.println("10 is not negative");<br/>
     if(nif.isNotNegative(-12))<br/>
        System.out.println("this wont be displayed");<br/>
 }<br/>
}<br/>


## How to create your own exception class ?
Java provides us facility to create our own exceptions which are basically derived classes of Exception. For example MyException in below code extends the Exception class.

We pass the string to the constructor of the super class- Exception which is obtained using “getMessage()” function on the object created.<br/>

// A Class that represents use-defined expception <br/>
class MyException extends Exception <br/>
{ <br/>
    public MyException(String s) <br/>
    { <br/>
        // Call constructor of parent Exception <br/>
        super(s); <br/>
    } <br/>
} <br/>
  
// A Class that uses above MyException <br/>
public class Main <br/>
{ <br/>
    // Driver Program <br/>
    public static void main(String args[]) <br/>
    { <br/>
        try<br/>
        { <br/>
            // Throw an object of user defined exception <br/>
            throw new MyException("GeeksGeeks"); <br/>
        } <br/>
        catch (MyException ex) <br/>
        { <br/>
            System.out.println("Caught"); <br/>
  
            // Print the message from MyException object <br/>
            System.out.println(ex.getMessage()); <br/>
        } <br/>
    } <br/>
} 
       
       





## Default method in Interface 
The release of JDK8 has changed this by adding a new capability to interface called the **default method**. A primary motivation for the default method was to provide 
a means by which interfaces could be expanded without breaking existing code. It provides the flexibility to allow interface to define implementation which will use as 
the default in a situation where a concrete class fails.Default methods can be provided to an interface without affecting implementing classes as it includes an implementation. 
If each added method in an interface is defined with implementation, then no implementing class is affected. An implementing class can override the default implementation provided 
by the interface.For example : <br/>
public interface oldInterface { <br/>
    public void existingMethod(); <br/>
        default public void newDefaultMethod() { <br/>
        System.out.println("New default method is added in interface"); <br/>
    } <br/>
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

