 **What is functional programming?**

 - functional programming is a programming paradigm a style of building the structure and elements of computer programs that treats computation as the evaluation of *mathematical* functions and **avoids** changing-state and **mutable**.

**What are the two elements of a pure function?**
- A function must **pass two tests** to be considered   **pure**: *Same inputs* always return *same outputs*. No side-effects.

        - so any function that relies on a random number generator cannot be pure(Random number generation).
- **Benefits of Pure Functions**
1. are idempotent
2. are easier to test
3. offer referential transparency
4. are memoizable
5. are easier to parallelize
6. can be lazy

