# Art Robots
Here we will concern ourselves with robots that create art, a.k.a. *art bots*. We will collect texts and code that serve two purposes: 

* Describe what an art bot is
* Share concrete software examples of art bots.

We will attempt to answer a well-thought-about philosophical question. Can machines create art without the aid of humans? Related work is algorithmic composition in music.

## A Taxonomy of Art Robots

What is an art robot? Any good answer to that question will have some structure. Here the structure will be a taxonomy that will help us distinguish between different kinds of art robots.

### The I/O Bot

A function that accepts input and produces art. Valid input ranges from nothing to everything.

```
             ┌─────────────┐             
             │             │             
 Input ─────▶│   I/O Bot   │─────▶  Art  
             │             │             
             └─────────────┘             
```

### The Learner Bot

A function that accepts input and produces an I/O robot. Valid input must be "something", i.e. data that the bot can learn from in order to give birth to an I/O bot.

```
             ┌─────────────┐             
             │             │             
 Input ─────▶│ Learner Bot │─────▶  I/O Bot  
             │             │             
             └─────────────┘             
```

## Orthogonal variations

The taxonomy above is fairly open for interpretation. Below are some thematic variations on this non-sealed categorization. The variations apply to all categories.

* *Stateless vs. stateful*: A stateful bot updates some internal state each time its function is called with input. A stateless art bot does not. 
* Deterministic vs. probabilistic: A deterministic bot produces the same art given the same input, always. A probabilistic art bot might not.
