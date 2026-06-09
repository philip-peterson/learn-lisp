Basic Lisp ... Lesson 1, dotted pairs

`(x . y)`

Simplest data structure: a **cons cell**. This means a `struct{car=x, cdr=y}`

Each cons cell has 2 fields exactly (`car` and `cdr`), so you cannot have three.

`(w . x . y) X ERROR`

But you can chain two cons cells together
`(w . (x . y))`

There is a special cons cell called nil, sometimes denoted `nil` but often denoted as `()`.

If you have a cons cell with `()` in the `cdr` position, that is called a **proper list** of size 1.

`(x . ())`

This is a proper list with just `x` in it. We can also write it as

`(x)`

(Note that there *is* such thing as an **improper list**; it's `(a . b)` as we had before, i.e. when b is not necessarily nil, `()`. So improper lists do not end with nil.)

When you have many cons cells chained together with nil at the end, it's a longer proper list.

`(a . (b . (c . ())))`

This is also denoted

`(a b c)`

which is a proper list of size 3. Note that this list actually contains 4 cons cells, because `()` is a cons cell, and every proper list ends with nil. 

So you can think of this list as having an invisible nil at the end, and we can even write it that way:

`(a b c . ())`

---
