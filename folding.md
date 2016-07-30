# Folding

Also called reduce in some languages, a fold goes through elements of a list and returns a single value. Folds require a function pass to it, which will be applied to each element of the list. This function can be a named, or an anonymous function. Anonymous functions are also called lambda functions. Key to learning to use folds is thinking of what the function you will pass to fold takes as and argument, and what it should return. You can fold from left to right through a list, `List.foldl`, or from right to left, `List.foldr`. In general you should prefer `foldl `over `foldr `because it is more efficient.

### Problem 4

Solve [Problem 4](../p/p04.md) by writing a version of `countElements` that uses `List.foldl`. Think about the function you want to pass to `foldl`. Its first argument of the same type as the elements of the list you folding. The second argument will be the same type that we want to return. So, what do we want to return? In this case we are counting, so let's return an Int.
Now we know the form of the function we want to pass to List.foldl, it should be of this type.
`foo : a -> Int -> Int`
Next write this function which increments the count.

### Problem 5

Solve [Problem 5](../p/p05.md) by writing a version of `myReverse` that uses `List.foldl`. Think about the function you want to pass to `foldl`. Its first argument of the same type as the elements of the list you folding. The second argument will be the same type that we want to return. So, what do we want to return? In this case our goal is to arrive as a List, so let's return a List.
Now we know the form of the function we want to pass to `List.foldl`, it should be of this type.
`foo : a -> List a - > List a`
Before you can write a function that will build our reversed list, is there a built in function you can use? What functions do we know that have this type? \(Remember, operators are functions too!\)

### Problem 8

`noDupes : List a -> List a`
In [Problem 8](../p/p08.md), like problem 5, you'll want a function of type
`foo : a -> List a - > List a`

### Problem 14

`duplicate : List a -> List a`
Write a function for duplicate that uses fold

### Problem 4

`countElements : List a -> Int`
Elm's List package provides some specialized folds. `List.sum` is really a fold equivalent to the following function for a list of Ints.
`sum -> List Int -> Int
sum xs = List.foldl (+) 0 xs`
Use `List.map` and `List.sum` to implement `countElements`.
