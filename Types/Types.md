## Types

##### Higher Kinded Types
1. Think of `List<A>` as a function that takes a type (A) in order to
make a concrete type.
2.  An HKT is something that takes a type like the above as a parameter
in order to create a concrete type.

Example Order 0 Type - Integer
Example Order 1 Type - List
Example Order 2 Type - Functor


#### Phantom Types
1.  A Phantom type is a type that is generic, but does not use its generic
parameter anywhere in its implementation

```
struct Phantom<A> {
  let string: String

  init(_ string: String) {
    self.string = string
  }
}
```
2.  Can use this extra generic parameter is a tag that can encode specific states.
3.  Can create function that take phantom types that have a specific type parameter in order to implement methods that are only possible in certain states.
