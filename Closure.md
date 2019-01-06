# Closure

A closure is a block of code that excutes its code.
A closure can caputre and store references to any constants and variables from the context in which they are defined.
A closure is a reference type, can apture values.

```
let names = ["Ana", "EWA", "Chris", "Joy", "Jag"]

func backward(_ s1: String, _ s2: String) -> Bool {
return s1 > s2
}

names.sorted(by: backward)

names.sorted(by: { (_ s1: String, _ s2: String) -> Bool in
return s1 > s2
})

// 1) type inference
names.sorted(by: { (s1, s2) in
return s1 > s2
} )

// 2) implicit return
names.sorted(by: {(s1, s2) in
s1 > s2
})

// 3) shorthand argument
names.sorted(by: {($0 > $1) })

// 4) trailing closure syntax
names.sorted() { $0 > $1 }

// 5) trailing closure syntax
names.sorted { $0 > $1 }

// 6) or
names.sorted(by: > )
```

## Escaping closure
A closure is said to escape a function when the closure is passed as an argument to the function, but is called after the function returns.
practical explain [Link](https://medium.com/@bestiosdevelope/what-do-mean-escaping-and-nonescaping-closures-in-swift-d404d721f39d)

- Storage
- Asynchronous Execution

complition handler
[Link](https://blog.bobthedeveloper.io/completion-handlers-in-swift-with-bob-6a2a1a854dc4)
[Link](https://hcn1519.github.io/articles/2017-09/swift_escaping_closure)
