# Art Robots
Robots that create art, a.k.a. *art bots*, is the topic of this repository. The collection of text and code within serves to purposes: 

* Describe what an art bot is
* Share concrete software art bots.

## Taxonomy of Art Robots

### The artist robot

A function that accepts input and produces art. The input ranges from nothing to everything.

```
             ┌─────────────┐             
             │             │             
 Input ─────▶│ Artist Bot  │─────▶  Art  
             │             │             
             └─────────────┘             
```

Variations on the theme:

* *Stateless vs. stateful*: A stateful art bot updates some internal state each time its function is called with input. A stateless art bot does not. 
* Deterministic vs. probabilistic: A deterministic art bot produces the same art given the same input, always. A probabilistic art bot might not.

### The learner robot

A function that accepts input and produces an artist robot. The input must be something.

```
             ┌─────────────┐             
             │             │             
 Input ─────▶│ Learner Bot │─────▶  Artist Bot  
             │             │             
             └─────────────┘             
```
