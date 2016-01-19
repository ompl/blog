---
title: Finding Diverse Short Paths
author: cvoss
---
\[Cross-posted from Caleb Voss' web site; see the original article titled “Randomizing Graph Searches for Robustness” [here](http://calebvoss.com/research/)\]

Finding the shortest path through a weighted graph is a well-understood task. With a cost heuristic, A* is the way to go. But what if the graph is not reliable? A broken edge or an incorrect weight can make the apparent shortest path a poor choice. The client wants options. So how can we find paths other than the shortest one? And what criteria can we use to evaluate the set of proposed alternatives?

It is still good for alternatives to be short. We could try the second shortest path, but in a moderately dense graph, it is likely to share almost all its edges with the original. The *n*th shortest, for large *n*, is probably better, but systematically checking all these options is expensive. Instead, consider an algorithm that encourages random deviations from known paths: it says, “What if *this* area of the graph, along the shortest path, is broken? Then what would the shortest path be? Now what about *that* area? Or both?” and so on, iteratively building a set of increasingly diverse alternatives. Intuitively, this heuristic simulates random breaking of the graph to build an arsenal that we hope will stand up against any specific issue with the actual graph.

This is the core of the contribution in [my 2015 ICRA paper](http://calebvoss.com/publications/), together with applications for robotic motion planning and an analysis of the efficiency and quality of this approach. Also have a look at [my code repository](code repository) for this research.
