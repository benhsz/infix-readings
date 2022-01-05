# Infix Readings for Lisp
A DrRacket plugin to provide infix readability to prefix syntax

# Work In Progress

No working implemention yet.

# How It Works

If the programmer enters a specific function, such as `>` or `-`, the editor swaps its appearance with a special character. The editor may also visualize extra space between the operands in order to render the extra operators between the operands.

The special character shown in place of the actual operator can be thought of as an 'infix visualization' function, which produces an infix reading.

On which functions this occurs can depend on the user's preferences.

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
