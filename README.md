# Fast Sorting and Shortest Path Algorithms with Diode Circuits

We present a set of solutions to sorting numbers and finding all shortest paths in a directed, weighted graph, by using diodes, instead of traditional Turing computational model methods.
We see that the solutions are able to produce good time complexity results,
derive a solution for $O(n)$ time and space for sorting $n$ numbers and $O(|V|^2)$ time and $O(|V| + |E|)$ space for finding the shortest path between all pairs of vertices in a graph.
However, the cost of producing diodes with large weights is potentially an exponentially expensive resource relative to input sizes, which may lend to why we are able to solve problems so quickly.

## Full Paper

[Find it here](build/main.pdf).

## Issues

- The explanation for how the lowest turn-on voltage diode turns on in parallel is not well-explained. 
  - We can do a pretty trivial solution by saying that we sweep the voltage source between 0 and $V_{\text{max}}$, and this is technically constant time for fixed input size (i.e. fixed $V_\text{max}$), but that seems cheap
  - I think better, is to do something where we use the exponential current property of the diode, and show that if there is some $|v - v'| > \delta$, then the current of the lower turn on voltage diode will be significantly larger than the other one, meaning it will be the only one that's "on"

## TODO

- Think about if ray tracing is possible to do faster
- Or another problem where it is "intuitive" to use a different circuit topology
