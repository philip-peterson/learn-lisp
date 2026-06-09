Lesson 2, the cons function

We know `(3 4 5)` is a proper list. This means it ends with nil, aka `()`

Because `(3 4 5)` is a list, it is represented by a chain of cons cells. The first in this chain, the cons cell containing 3, 
is considered "the list itself," even though it is just the first chain.

In other words, we say that the first chain in `(3 4 5)` is identical to the list `(3 4 5)`, in terms of Lisp.

So we have `(3 4 5)` which is a list, which part of is list `(4 5)`, which part of is another list `(5)`. Incidentally, part of `(5)`
is also `()` or nil, the empty list.

This is why we can write the same list as `(3 . (4 . (5)))`, a nested structure.

We can even write it as `(3 . (4 . (5 . ())))` to be fully verbose.

This also means that `(3 4 5)` may in fact be part of a larger list, such as `(2 3 4 5)` or `(7 3 4 5)`. In fact, it may be part of several larger lists.

To form a list, we can use the list function, as you can see via the REPL output:

```
1 ]=> (list 3 4 5)

;Value: (3 4 5)
```
