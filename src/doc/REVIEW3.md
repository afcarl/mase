### Simulated Annealing

  1. In a few lines, define ordered and unordered search. In what way are they different?
  2. In a few lines, compare and contrast: (1) Greedy search; (2) Local Search; and (3) Stochastic search. What, if any, are the trade-offs in using a Stochastic search?
  3. In about 10 lines, write down the pseudo-code for SA. Number each line.
  4. In the pseudo-code for SA, you used a neighbourhood function `Neighbour()`. Write down an expression for this.
  5. 4. In the pseudo-code for SA, you used a probability function `P(e_new, e_old, t)`. What would be a valid mathematical expression for this?
  6. With respect to function `P(e_new, e_old, t)`, justify the following statements:
      * Initially, SA is like a drunk, then it sobers up.
      * SA consumes lower memory.
  7. How would you terminate a stochastic algorithms such as SA sooner? (*HINT: Look at variances of epochs*)
  8. When finding a solution, you can either mutate towards ''Heaven'' (A better spot) or you can choose to mutate away from "Hell" (A worse spot). Why would you choose one over the other? (*HINT: One of them has a better diversity of search.*)
