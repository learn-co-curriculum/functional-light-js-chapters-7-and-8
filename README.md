# Introduction

Chapters 7 and 8 cover Closure vs Objects and Recursion. Below are rough discussion notes.

## Objectives

- Understand closure vs objects
- Understand recursion as applied w/i Functional Programming

## Chapter 7: Closure vs Object

### Highlights

#### Closures and objects

##### Similarities

- Two different representations of the same thing (p180)
- Both ways to express collections of state (p184)
- Can both also bundle data with behavior, aka "express encapsulation" (p184-185)
- Both have identical mutation behavior (p187)
- "...closures and objects are isomorphic representations of state (and its associated functionality)." (p190)

##### Differences

- Structure of a closure is not mutable, but objects are mutable (p192)
- Privacy: closures have lexical closure hiding, but all properties on objects are public (p194)

### Discussion Topics

1. Did anyone read the [MIT paper cited in the opening koan](http://people.csail.mit.edu/gregs/ll1-discuss-archive-html/msg03277.html)? Anything good in there?
2. Did anyone do the example on p181 (representing object as a closure or vice versa)? What did you come up with?
3. On page 188, author states "...at the lowest level, all state data is primitives, and all primitives are value-immutable. Whether you represent this state with nested objects, or with nested closures, the values being held are all immutable." Let's break down this statement. Do we agree?
4. Author describes `const` as unhelpful, because scopes and closures control lexical reassignment, so this "special" declaration is essentially unnecessary. Do we agree?
5. Author talks about hard core FPers using `Object.freeze()` and `const` to keep functions pure and prevent reassignment, and how he disagrees with this. Author is pro-variable reassignment, as long as it's "used appropriately". Where do we fall on reassignment? Hard-core FP vs FP lite?

## Chapter 8: Recursion

### Highlights

Recursion jokes are the ultimate Dad programmer jokes.

Fun fact: "When two or more functions call each other in a recursive cycle, this is referred to as **mutual recursion.**" (p209)

Why are we talking about recursion in a book about FP? "Recursion fits the spirit of FP is because it trades...the explicit tracking of state with **implicit state on the call stack.**" (p211)

Use tail calls for performance boost (p218-219)

ES6 introduced Proper Tail Calls with guarantee PTC will "run without unbounded stack memory growth", but requires `strict` mode. (p219-220)

Readability > Recursion (p221)

#### Pros of using recursion

- Can replace conditional branching with recursion. See Kate's [post on pattern matching](https://medium.com/flatiron-labs/perfect-match-pattern-matching-in-elixir-9d49ced20b07).
- Helps avoid local variable reassignment, because instead you're just passing arguments through the same function repeatedly.
- More declarative, readable

#### Recursion strategies

- PTC (Proper Tail Calls)
- CPS (Continuous Passing Style)
- Trampolines

### Discussion Topics

1. Author lumps recursion in with regular expressions, as stuff that's powerful but dangerous. Unfair?
2. Where in our codebases could we replace conditional logic with recursion? Need some inspiration? Think about the Binary Tree Recursion example (p215)
3. Strict mode, should we use it? :troll-face:
4. Describe what you like/don't like about each recursion strategy listed above

## Resources
 tbd


<p class='util--hide'>View <a href='https://learn.co/lessons/functional-light-js-chapters-7-and-8'>Functional Light JS Chapters 7 and 8</a> on Learn.co and start learning to code for free.</p>
