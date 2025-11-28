What this program shows

This Java program demonstrates runtime polymorphism (also called dynamic method dispatch) using method overriding.


---

👉 Breakdown of the Code

1. Parent Class: Animal

class Animal{
    void sound(){
        System.out.println("Animals make sounds");
    }
}

Has a method sound()

This is the general version of the method.



---

2. Child Class: Dog

class Dog extends Animal{
    void sound(){
        System.out.println("Dog barks: Woof Woof!");
    }
}

Overrides the parent class method

Gives Dog-specific behavior



---

3. Child Class: Cat

class Cat extends Animal{
    void sound(){
        System.out.println("Cat meows");
    }
}

Also overrides the sound() method

Gives Cat-specific behavior



---

4. Main Method

public static void main(String[] args) {
    Animal a;

    a = new Animal();
    a.sound();  // Calls Animal's sound()

    a = new Dog();
    a.sound();  // Calls Dog's sound()

    a = new Cat();
    a.sound();  // Calls Cat's sound()
}

How it works

The reference type is Animal, but the object changes at runtime.

Java decides which sound() method to call at runtime, not compile time → this is runtime polymorphism.



---

👉 Output

Animals make sounds
Dog barks: Woof Woof!
Cat meows


---

👉 Important Viva Points

✔ Method Overriding

Child class provides its own implementation of a parent class method.

✔ Polymorphism

Same method name → different behaviors depending on object type.

✔ Dynamic Method Dispatch

The decision of which method to call happens at runtime.

✔ Why Animal a works

Because:

Parent reference can store child object

But child reference cannot store parent object (reverse is not allowed)



---

If you want, I can also create:

A diagram showing the runtime linking

Viva questions and answers

A simplified version for handwritten notes
