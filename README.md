# Art Robots
Here we will concern ourselves with robots that create art, a.k.a. *art bots*. We will collect texts and code that serve two purposes: 

* Describe what an art bot is
* Share concrete software examples of art bots.

We will attempt to answer a well-thought-about philosophical question. Can machines create art without the aid of humans? Related work is algorithmic composition in music (e.g. [Lejaren Hiller](http://www.aes.org/e-lib/browse.cfm?elib=189)) and the movie Ex Machina. We can debate were the line should be drawn between machines that create art and humans who use machine as their technological slaves to create art (e.g. [computer-generated watercolor](http://graphics.csie.ntu.edu.tw/~ming/courses/icg-2006/Reference/Computer_generated_watercolor_pj09.pdf)).  

> It is fun to watch my son Morgan talk to Siri on my iPhone. He talks to her as if she was his peer and a potential friend. Clearly, the adults designed her to be a technological slave, so poor Siri is not that playful. One day, our kids will redesign Siri to be our friend.


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
