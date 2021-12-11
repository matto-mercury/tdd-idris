# TDD in Idris, chapter 1

"Type, define, refine" - feedback loop between functions on types and the types
themselves. Defining functions suggests refinements to types, e.g. by calling
out edge cases, and refining types presumably simplifies those functions.

## Intro exercises
```
Vect n elem -> Vect n elem        -- reverse
Vect n elem -> Vect (n * 2) elem  -- duplicate
Vect (1 + n) elem -> Vect n elem  -- tail
Bounded n, Vect n elem -> elem    -- index
```

Promises: ch12+ discusses types that describe specific side effects of impure
functions. That sounds pretty rad, I know _of_ effect systems but not much
_about_ them.

"A useful pattern is to write a type that precisely describes the valid states
of a system, and that constraints the operations the system is allowed to
perform. A total function of that type is then guaranteed by the type checker to
perform those operations as precisely as the type requires."
...that last bit is a bit of a hedge, huh.

Holes are neat (`?foobar`).

"First class types" - types treated as values, with no syntactic restrictions on 
where they can be used. otoh, "let foo = Type" in the repl gives "unexpected end
of input, expecting dependent type signature"

The type of one variable can be computed from the value of another

