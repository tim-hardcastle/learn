# The Syntax Tree

The syntax tree consists of flexible nodes called LNodes. The structure is like [s-expressions](https://en.wikipedia.org/wiki/S-expression). A node has a target, arguments and attributes.

Calling Conventions of Targets:

' is an operator, for example: `1 + 2`
    ```
        '+(1, 2)
    ```

 
\# is a keyword, for example: `while true {}`
    ```
    #while(#Boolean(true), '{})
    ```
    
Literals are automaticly typed by the parser. A type is a call and a literal node as argument. So the number `42` will be treated as `#Int32(42)`. Modifiers like `public` are attributes on a node.
The `quote` macro expand code to its actual tree. So you can use it to figure out a tree of a certain language construct.

## Exercices

1. If you have an expression `42`. What tree will be used?
    [ ] #uint(42)
    [ ] #literal(42)
    [ ] #Int32(42)

2. Translate this code snippet to the actual tree:

```back
public static func main() {
    let userInput = System.Console::ReadLine();

    if userInput == ":q" {
        print("The application will now close");
    }
}
```

3. Translate this tree to valid backlang code:

`@[mutable] #var(#type(#(@'', #of())), errorCode = #uint64(0));`