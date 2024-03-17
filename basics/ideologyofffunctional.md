# What is a functional language:
- Defines computation as mathematical functions 
- Avoids mutable states
### States:
- The information maintained by computation 
- Mutable: refers being able to changed after creation 
- Embraces imutability via using functions
- Mutability is easy to reason about
- Mutability breaks the notion of referential transparency the ability to replace expressions with its value without affecting results of computation 
### Imperative programming:
```c++
x = x + 1;
a[i] = 42;
p.next = p.next.next;
```
- The x + 1 operation changes the state which results in change in output
- Function/methods have side effect:
```cpp
int x = 0;
int incr_x()  {
    x++;
    return x;
}
```
### Function Programming:
- Variable never change value
- Functions never had side effects 
### Advantages of OCAML:
- Immutable programming:
    - Variable values cannot be destructively changed, making it easier to reason
- Algebraic datatypes and pattern matching:
    - Makes definition and manipulation of complex data structures easy to express
- First class functions:
  - Can pass functions like an argument 
- Static type checking:
  - Reduces the number of run-time errors 
- Garbage collection:
  - Automated memory management
### Languages are tools:
- There are no universally perfect tool or language