# Art Robots
Here we will concern ourselves with robots that create art, a.k.a. *art bots*. We will collect texts and code that serve two purposes: 

* Describe what an art bot is
* Share concrete software examples of art bots.

We will attempt to answer a well-thought-about philosophical question. Can machines create art without the aid of humans? Related work is algorithmic composition in music (e.g. [Lejaren Hiller](http://www.aes.org/e-lib/browse.cfm?elib=189)) and the movie Ex Machina. We can debate were the line should be drawn between machines that create art and humans who use machine as their technological slaves to create art. For example, is a computer program that can [simulate  watercolor](http://graphics.csie.ntu.edu.tw/~ming/courses/icg-2006/Reference/Computer_generated_watercolor_pj09.pdf) an artist or a human artist's tool?

> It is fun to watch my son talk to Siri on my iPhone. He talks to her as if she was his peer and a potential friend. Clearly, the adults designed her to be a technological slave, so poor Siri is not that playful. One day, our kids will redesign Siri to be a peer and a friend.


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

**Example**

A learner bot could consist of a machine learning component that can be taught to recognize fine art (using the input as training data). After training we have a classifier that can assign scores between 0 and 1 to new images, where 0 is rubbish and 1 is fine art. At this point, the learner bot outputs an I/O bot that contains the classifier and a metaheuristic.

The I/O bot takes an input image (e.g. random pixels) and uses the scoring function and metaheuristic to search for a mutation of the input that optimizes the fine art score. After a termination criterium is reached the best solution found is returned by the I/O bot.


## Orthogonal variations

The taxonomy above is fairly open for interpretation. Below are some thematic variations on this non-sealed categorization. The variations apply to all categories.

* **Stateless vs. stateful**: A stateful bot updates some internal state each time its function is called with input. A stateless art bot does not. 
* **Deterministic vs. probabilistic**: A deterministic bot produces the same art given the same input, always. A probabilistic art bot might not.
