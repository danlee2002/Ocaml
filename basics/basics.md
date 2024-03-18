# Basics of OCAML:
## Ocaml toplevel:
- Expressions are building block of OCAML
- Syntax: key word in punctuation
- Semantics: meaning
  - Static semantics: type-checking 
  - Evaluation rules: dynamic semantics
    - Tell us how program produces a value, exception or program never terminates
  ### Values:
  - A value is an expression that doesn't require any further evaluations
  - All values are expressions
  ### Utop 
  - to run utop type `utop` 
  ```ocaml
  3110;;  (*to end expression we use double colon*)
  "big";; (*written in same way as normal strings)
  "big" ^ " red";; (*the karat operator is often used to concatenate strings*)
  ```
  ### Operators:
  - In OCAML, there are two types of operators for numerical operations 
  ```ocaml
  (*Consider multiplying two values 2.1 and 3.1*)
  2.1 * 3.1;;
  (*Will yield error, must use the *. operator to indicate FLOP *)
  2.1 *. 3.1;;

  ```
### Type inference:
- OCAML often infers types
- Does type-checking at compile time but uses infering
- We can also declare types using type annotation 
```ocaml
(3110:int);; (*tells type-checker to verify types*)
```
### Definitions:
```ocaml
let x = 42;; (*binds 42 to value, can't change value*)
```
- Definitions give names to value, defined as `let x = e`
- e is identifier
- evaluates a value e to value v then binds v to x or a memory location x associated with v
### Functions:
- Consider the following expression:
- `let inc x = x + 1;;`
- When running this in UTOP, one may get the following:
  - `val inc: int -> int = <fun>`
  - Let's break it down:
    - The incr is the identifier in which the value is bound, int-> int tells us the function maps an int to an int
    - The <fun> operator is a placeholder for the <fun> value
    - Assume we run utop and have the following function in the following file `example.ml` we can import the following function using the `#use "example.ml;;"` command  
### An introduction to compiling OCAML:
- Assume we have the following executable
```ocaml
let _ = print_endline "Hello World!"
```
- We can compile the following file using the following command:
  - `ocamlc -o hello.byte hello hello.ml`
  - 