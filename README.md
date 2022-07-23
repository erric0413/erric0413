- 👋 Hi, I’m @erric0413
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...

<!---
erric0413/erric0413 is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
// Class A declaration. Methods defined somewhere else; 
class A
{
public:
   A();                    // Constructor
   ~A();                   // Destructor (called when the object goes out of scope or is deleted)
   void myMethod();        // Just a method
};

// Class B declaration. Methods defined somewhere else;
class B
{
public:
   B();                    // Constructor
   ~B();                   // Destructor
   void myMethod();        // Just a method
};

// Class C declaration. Methods defined somewhere else;
class C
{
public:
   C();                    // Constructor
   ~C();                   // Destructor
   void myMethod();        // Just a method
};

void myFunction()
{
   A a;                    // Constructor a.A() called. (Checkpoint 1)
   {                       
      B b;                 // Constructor b.B() called. (Checkpoint 2)
      b.myMethod();        //                           (Checkpoint 3)
   }                       // b.~B() destructor called. (Checkpoint 4)
   {                       
      C c;                 // Constructor c.C() called. (Checkpoint 5)
      c.myMethod();        //                           (Checkpoint 6)
   }                       // c.~C() destructor called. (Checkpoint 7)
   a.myMethod();           //                           (Checkpoint 8)
}                          // a.~A() destructor called. (Checkpoint 9)
