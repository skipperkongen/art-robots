# Art Bots
Robots that create art, i.e. art bots, is the topic of this repository. The first goal of the repository is to describe what an art bot is. The second goal is to share concrete software examples of art bots.

## Taxonomy of Art Robots

### The I/O bot

The I/O bot takes input and produces art.

```
             ┌─────────────┐             
             │             │             
 Input ─────▶│   I/O bot   │─────▶  Art  
             │             │             
             └─────────────┘             
```

Variations on the theme:

* *Stateless vs. stateful I/O bots*: The stateful I/O bot updates some internal state each time its function is called with input. The stateless I/O bot does not. 
* Deterministic vs. probabilistic I/O bots: The deterministic I/O bot produces the same art given the same input, always. The probabilistic I/O bot might not.

### The learning art robot


