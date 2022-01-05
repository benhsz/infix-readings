# Infix Readings for Lisp
A DrRacket plugin to provide infix readability to prefix syntax

# Work In Progress

No working implemention yet.

# How It Works

If the programmer enters a specific function, such as `>` or `-`, the editor swaps its appearance with a special character. The editor may also visualize extra space between the operands in order to render the extra operators between the operands.

The special character shown in place of the actual operator can be thought of the same function, for example `>`, that has gained an 'infix visualization' function, which produces an infix reading.

Which functions are able to produce an infix reading depends on the user's preferences.

# Examples

Programmer inputs:

```racket
(> 9 8)
```

Result:

```racket
(⇨ 9 > 8)
````

After having typed `(`, `>`, pressing space creates the infix reading.
```racket
(⇨ 
```

When that happens, the operator is replaced by another symbol, and the operator is shown between the operands. 

Programmer inputs:

```racket
(> 9 8 7 6)
```

Result:

```racket
(⇨ 9 > 8 > 7 > 6)
````

Another example with infix readings on all operators

```racket
(- (+ 2 2) (* 3 4))
```

```racket
(⇨ (⇨ 2 + 2) - (⇨ 3 * 4))
```

Same inputs but infix readings only on `-`

```racket
(⇨ (+ 2 2) - (* 3 4))
```
