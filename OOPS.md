# OOPS Concepts

Pointer is a variable in C++ that holds the address of another variable.

```
int *p, var
p = &var;
```

The this pointer holds the address of current object, in simple words you can say that this pointer points to the current object of the class.

```
class Demo {
private:
  int num;
  char ch;
public:
  void setMyValues(int num, char ch){
    this->num =num;
    this->ch=ch;
  }
};
```

Object oriented programming is a way of solving complex problems by breaking them into smaller problems using objects.

A class is like a blueprint of data member and functions and object is an instance of class.

Constructor is a special member function of a class that initializes the object of the class. 

A default constructor doesn’t have any arguments (or parameters)

When you don’t specify any constructor in the class, a default constructor with no code (empty body) would be inserted into your code by compiler.

```
#include <iostream>
using namespace std;
class Website{
public:
   //Default constructor
   Website() {
      cout<<"Welcome to BeginnersBook"<<endl;
   }
};
int main(void){
   /*creating two objects of class Website.
    * This means that the default constructor
    * should have been invoked twice.
    */
   Website obj1;
   Website obj2;
   return 0;
}
```

Constructors with parameters are known as Parameterized constructors.

```
#include <iostream>
using namespace std;
class Add{
public:
   //Parameterized constructor
   Add(int num1, int num2) {
     cout<<(num1+num2)<<endl;
   }
};
int main(void){
   /* One way of creating object. Also
    * known as implicit call to the
    * constructor
    */
   Add obj1(10, 20);
   /* Another way of creating object. This
    * is known as explicit calling the
    * constructor.
    */
   Add obj2 = Add(50, 60);
   return 0;
}
```

A Copy constructor is an overloaded constructor used to declare and initialize an object from another object.

```
    #include <iostream>  
    using namespace std;  
    class A  
    {  
       public:  
        int x;  
        A(int a)                // parameterized constructor.  
        {  
          x=a;  
        }  
        A(A &i)               // copy constructor  
        {  
            x = i.x;  
        }  
    };  
    int main()  
    {  
      A a1(20);               // Calling the parameterized constructor.  
     A a2(a1);                //  Calling the copy constructor.  
     cout<<a2.x;  
      return 0;  
    }  
```

A destructor is a special member function that works just opposite to constructor, unlike constructors that are used for initializing an object, destructors destroy (or delete) the object.

A destructor is automatically called when:
1) The program finished execution.
2) When a scope (the { } parenthesis) containing local variable ends.
3) When you call the delete operator.

```
#include <iostream>
using namespace std;
class HelloWorld{
public:
  //Constructor
  HelloWorld(){
    cout<<"Constructor is called"<<endl;
  }
  //Destructor
  ~HelloWorld(){
    cout<<"Destructor is called"<<endl;
   }
   //Member function
   void display(){
     cout<<"Hello World!"<<endl;
   }
};
int main(){
   //Object created
   HelloWorld obj;
   //Member function called
   obj.display();
   return 0;
}
```
Enum is a user defined data type where we specify a set of values for a variable and the variable can only take one out of a small set of possible values.

```
#include <iostream>
using namespace std;
enum direction {East, West, North, South};
int main(){
   direction dir;
   dir = South; 
   cout<<dir;   
   return 0;
}
```

**Inheritance**

Inheritance is one of the feature of Object Oriented Programming System(OOPs), it allows the child class to acquire the properties (the data members) and functionality (the member functions) of parent class.

Single inheritance

In Single inheritance one class inherits one class exactly.

```
#include <iostream>
using namespace std;
class A {
public:
  A(){
     cout<<"Constructor of A class"<<endl;
  }
};
class B: public A {
public:
  B(){
     cout<<"Constructor of B class";
  }
};
int main() {
   //Creating object of class B
   B obj;
   return 0;
}
```

Multilevel Inheritance

In this type of inheritance one class inherits another child class.

```
#include <iostream>
using namespace std;
class A {
public:
  A(){
     cout<<"Constructor of A class"<<endl;
  }
};
class B: public A {
public:
  B(){
     cout<<"Constructor of B class"<<endl;
  }
};
class C: public B {
public:
  C(){
     cout<<"Constructor of C class"<<endl;
  }
};
int main() {
  //Creating object of class C
  C obj;
  return 0;
}
```

Multiple Inheritance

In multiple inheritance, a class can inherit more than one class. This means that in this type of inheritance a single child class can have multiple parent classes.

```
#include <iostream>
using namespace std;
class A {
public:
  A(){
     cout<<"Constructor of A class"<<endl;
  }
};
class B {
public:
  B(){
     cout<<"Constructor of B class"<<endl;
  }
};
class C: public A, public B {
public:
  C(){
     cout<<"Constructor of C class"<<endl;
  }
};
int main() {
   //Creating object of class C
   C obj;
   return 0;
}
```

Hierarchical Inheritance

In this type of inheritance, one parent class has more than one child class. 

```
#include <iostream>
using namespace std;
class A {
public:
  A(){
     cout<<"Constructor of A class"<<endl;
  }
};
class B: public A {
public:
  B(){ 
     cout<<"Constructor of B class"<<endl;
  }
};
class C: public A{
public:
  C(){
     cout<<"Constructor of C class"<<endl;
  }
};
int main() {
   //Creating object of class C
   C obj;
   return 0;
}
```
Hybrid Inheritance

Hybrid inheritance is a combination of more than one type of inheritance. For example, A child and parent class relationship that follows multiple and hierarchical inheritance both can be called Hybrid Inheritance.

**Polymorphism**

Polymorphism is a feature of OOPs that allows the object to behave differently in different conditions.

**Compile time Polymorphism (Function Overloading)**

The easiest way to remember this rule is that the function parameters should qualify any one or more of the following conditions, they should have different type, number or sequence of parameters.

```
#include <iostream>
using namespace std;
class Addition {
public:
    int sum(int num1,int num2) {
        return num1+num2;
    }
    int sum(int num1,int num2, int num3) {
       return num1+num2+num3;
    }
};
int main(void) {
    Addition obj;
    cout<<obj.sum(20, 15)<<endl;
    cout<<obj.sum(81, 100, 10);
    return 0;
}
```
**Run time Polymorphism (Function Overriding)**

Function overriding is a feature that allows us to have a same function in child class which is already present in the parent class. To override a function you must have the same signature in child class.

Note: In function overriding, the function in parent class is called the overridden function and function in child class is called overriding function.

```
#include <iostream>
using namespace std;
class BaseClass {
public:
   void disp(){
      cout<<"Function of Parent Class";
   }
};
class DerivedClass: public BaseClass{
public:
   void disp() {
      cout<<"Function of Child Class";
   }
};
int main() {
   DerivedClass obj = DerivedClass();
   obj.disp();
   return 0;
}
```

Output:

```
Function of Child Class
```
If you want to call the Overridden function from overriding function then you can do it like this:

```
BaseClass::disp();
```
**Difference between function overloading and function**

1) Function Overloading happens in the same class when we declare same functions with different arguments in the same class. Function Overriding is happens in the child class when child class overrides parent class function.
2) In function overloading function signature should be different for all the overloaded functions. In function overriding the signature of both the functions (overriding function and overridden function) should be same.
3) Overloading happens at the compile time thats why it is also known as compile time polymorphism while overriding happens at run time which is why it is known as run time polymorphism.
4) In function overloading we can have any number of overloaded functions. In function overriding we can have only one overriding function in the child class.

**Virtual functions in C++: Runtime Polymorphism**

Why we declare a function virtual? To let compiler know that the call to this function needs to be resolved at runtime (also known as late binding and dynamic linking) so that the object type is determined and the correct version of the function is called.

Example codes to understand Virtual Function:

```
#include<iostream>
using namespace std;
//Parent class or super class or base class
class Animal{
public:
   void animalSound(){
      cout<<"This is a generic Function";
   }
};
//child class or sub class or derived class
class Dog : public Animal{
public:
   void animalSound(){ 
      cout<<"Woof";
   }
};
int main(){
   Animal *obj;
   obj = new Dog();
   obj->animalSound();
   return 0;
}
```
Output:

```
This is a generic Function
```

```
#include<iostream>
using namespace std;
//Parent class or super class or base class
class Animal{
public:
   virtual void animalSound(){
      cout<<"This is a generic Function";
   }
};
//child class or sub class or derived class
class Dog : public Animal{
public:
   void animalSound(){ 
      cout<<"Woof";
   }
};
int main(){
   Animal *obj;
   obj = new Dog();
   obj->animalSound();
   return 0;
}
```

Output:

```
Woof
```
**Encapsulation**

Encapsulation is a process of combining data members and functions in a single unit called class. This is to prevent the access to the data directly, the access to them is provided through the functions of the class. It is one of the popular feature of Object Oriented Programming(OOPs) that helps in data hiding.

```
#include<iostream>
using namespace std;
class ExampleEncap{
private:
   /* Since we have marked these data members private,
    * any entity outside this class cannot access these
    * data members directly, they have to use getter and
    * setter functions.
    */
   int num;
   char ch;
public:
   /* Getter functions to get the value of data members.
    * Since these functions are public, they can be accessed
    * outside the class, thus provide the access to data members
    * through them
    */
   int getNum() const {
      return num;
   }
   char getCh() const {
      return ch;
   }
   /* Setter functions, they are called for assigning the values
    * to the private data members.
    */
   void setNum(int num) {
      this->num = num;
   }
   void setCh(char ch) {
      this->ch = ch;
   }
};
int main(){
   ExampleEncap obj;
   obj.setNum(100);
   obj.setCh('A');
   cout<<obj.getNum()<<endl;
   cout<<obj.getCh()<<endl;
   return 0;
}
```

**Abstraction**

Abstraction is one of the feature of Object Oriented Programming, where you show only relevant details to the user and hide irrelevant details.

```
#include <iostream>
using namespace std;
class AbstractionExample{
private:
   /* By making these data members private, I have
    * hidden them from outside world.
    * These data members are not accessible outside
    * the class. The only way to set and get their
    * values is through the public functions.
    */
   int num;
   char ch;

public:
   void setMyValues(int n, char c) {
      num = n; ch = c;
   }
   void getMyValues() {
      cout<<"Numbers is: "<<num<< endl;
      cout<<"Char is: "<<ch<<endl;
   }
};
int main(){
   AbstractionExample obj;
   obj.setMyValues(100, 'X');
   obj.getMyValues();
   return 0;
}
```

**Interfaces** 

A class with pure virtual function is known as abstract class. 

```
#include<iostream>
using namespace std;
class Animal{
public:
   //Pure Virtual Function
   virtual void sound() = 0;

   //Normal member Function
   void sleeping() {
      cout<<"Sleeping";
   }
};
class Dog: public Animal{
public:
   void sound() {
      cout<<"Woof"<<endl;
   }
};
int main(){
   Dog obj;
   obj.sound();
   obj.sleeping();
   return 0;
}
```

**Rules of Abstract Class**

1) As we have seen that any class that has a pure virtual function is an abstract class.
2) We cannot create the instance of abstract class. For example: If I have written this line Animal obj; in the above program, it would have caused compilation error.
3) We can create pointer and reference of base abstract class points to the instance of child class. For example, this is valid:

```
Animal *obj = new Dog();
obj->sound();
```

4) Abstract class can have constructors.
5) If the derived class does not implement the pure virtual function of parent class then the derived class becomes abstract.


**Friend Class:**

A friend class is a class that can access the private and protected members of a class in which it is declared as friend. 

```
#include <iostream>
using namespace std;
class XYZ {
private:
   char ch='A';
   int num = 11;
public:
   /* This statement would make class ABC
    * a friend class of XYZ, this means that
    * ABC can access the private and protected
    * members of XYZ class. 
    */
   friend class ABC;
};
class ABC {
public:
   void disp(XYZ obj){
      cout<<obj.ch<<endl;
      cout<<obj.num<<endl;
   }
};
int main() {
   ABC obj;
   XYZ obj2;
   obj.disp(obj2);
   return 0;
}
```

**Friend Function**:

Similar to friend class, this function can access the private and protected members of another class. A global function can also be declared as friend as shown in the example below:

```
#include <iostream>
using namespace std;
class XYZ {
private:
   int num=100;
   char ch='Z';
public:
   friend void disp(XYZ obj);
};
//Global Function
void disp(XYZ obj){
   cout<<obj.num<<endl; 
   cout<<obj.ch<<endl;
}
int main() {
   XYZ obj;
   disp(obj);
   return 0;
}

```

**Output:**

```
100
Z
```
**Real Life Examples**

    ABSTRACTION:

    Suppose you are driving your car.., so when you are driving, at that time you only need to know about the basic functionalities of the car., like how steering works n all. And you are not going into the much detail about the internal working of the car. Same is in the case of programming, there are some information which is not important for users. So that kind of information is made private by the programmers. So in short, abstraction is a mechanism with the help of which programmers hide the unnecessary details from the users.

    INHERITANCE: 

    Inheritance in simple terms means,,,getting some characteristics from the older ones. For example, when child takes birth it inherit some qualities from his parents. Same in the case of programming., the derived class takes some characteristics from the base class. The inheritance is beneficial for programming because with the help of this we can make our code as short as possible and there will be not any kind of redundancy.

    POLYMORPHISM:

    Let’s take an simple example, we use milk for drinking..,but milk can also be used to make curd, butter etc. So, the term polymorphism means to use something in different forms. In programming, to maintain the code and to maintain the simplicity of the code we use the concept of polymorphism. Very popular example of this is, “function overloading”, in which we use the same name but the operations are different.

    ENCAPSULATION:
    It means to bind things. For example, the pencil box which you use daily, that pencil box contains other things also like eraser, sharpner etc. Same in the case of programming,.the OOPS gives us the advantage of gathering the data and functions in the same box which is called “Class”.
