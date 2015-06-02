From wikipedia:

cut vertices can be connected to multiple biconnected components.

The Polish mathematician Kazimierz Kuratowski provided a characterization of planar graphs in terms of forbidden graphs, now known as Kuratowski's theorem:

A finite graph is planar if and only if it does not contain a subgraph that is a subdivision of K5 (the complete graph on five vertices) or K3,3 (complete bipartite graph on six vertices, three of which connect to each of the other three, also known as the utility graph).
A subdivision of a graph results from inserting vertices into edges (for example, changing an edge •——• to •—•—•) zero or more times.

bipartite graph: has no odd-length cycles, two independent sets of vertices where every edge connects a vertex in one set to one in the other.

Algorithm accepts a graph G from which each edge is added to a structure to maintain biconnected components. Inputs are processed
in the reverse order of the depth-first search indices. This insures that the last vertex processed is the DFS root

edges: http://en.wikipedia.org/wiki/Depth-first_search#Output_of_a_depth-first_search

externally active: Let w denote a DFS descendant of v in, a biconnected component B. We say that w is externally active if there is a path from w to a DFS ancestor u of v consisting of a back edge plus zero or more DFS descendants of w, none of which are in B. This definition does not apply to virtual vertices. Still not sure what this means. Regardless, externally active vertices must remain so after processing, thus the 'flipping' operation which allows adding a "back edge" (which points from a node to one of its ancestors) to connect components while preserving its external face, since we can switch the the side of a biconnected component's external face and use the back edge to link from one biconnected component's external face to another.

pertinence: describes a vertex descendant from from a back edge to be embedded, as well as any cut vertex on the DFS path from beginning to end of the back edge to be embedded. Any vertex along the path that has a pertinent root (a biconnected component in the embedding along the back edge) is also considered pertinent. This is determined by traversing the external face of each biconnected component that contains part of the back edge.

planarity:
For a simple, connected, planar graph with v vertices and e edges, the following simple conditions hold:

Theorem 1. If v ≥ 3 then e ≤ 3v − 6;
Theorem 2. If v ≥ 3 and there are no cycles of length 3, then e ≤ 2v − 4.

Additional Reading:
Auslander, L. and Parter, S. "On Imbedding Graphs in the Sphere." J. Math. Mechanics 10, 517-523, 1961.
Battle, J.; Harary, F.; and Kodama, Y. "Every Planar Graph with Nine Points has a Nonplanar Complement." Bull. Amer. Math. Soc. 68, 569-571, 1962.
Beineke, L. W. and Harary, F. "On the Thickness of the Complete Graph." Bull. Amer. Math. Soc. 70, 618-620, 1964.
Beineke, L. W. and Harary, F. "The Thickness of the Complete Graph." Canad. J. Math. 17, 850-859, 1965.
Booth, K. S. and Lueker, G. S. "Testing for the Consecutive Ones Property, Interval Graphs, and Graph Planarity using PQ-Tree Algorithms." J. Comput. System Sci. 13, 335-379, 1976.
Bryant, V. W. "Straight Line Representation of Planar Graphs." Elem. Math. 44, 64-66, 1989.
Cai, J.; Han, X.; and Tarjan, R. "New Solutions to Four Planar Graph Problems." Technical Report. New York University, 1990.
Di Battista, G.; Eades, P.; Tamassia, R.; and Tollis, I. G. Graph Drawing: Algorithms for the Visualization of Graphs. Englewood Cliffs, NJ: Prentice-Hall, 1998.
Eades, P. and Tamassia, R. "Algorithms for Drawing Graphs: An Annotated Bibliography." Technical Report CS-89-09. Department of Computer Science. Providence, RI: Brown University, Feb. 1989.
Eppstein, D. "Layered Graph Drawing." http://www.ics.uci.edu/~eppstein/junkyard/thickness/.
Even, S. Graph Algorithms. Rockville, MD: Computer Science Press, 1979.
Fáry, I. "On Straight Line Representations of Planar Graphs." Acta Sci. Math. (Szeged( 11, 229-233, 1948.
Gardner, M. The Sixth Book of Mathematical Games from Scientific American. Chicago, IL: University of Chicago Press, pp. 91-94, 1984.
Harary, F. "Planarity." Ch. 11 in Graph Theory. Reading, MA: Addison-Wesley, pp. 102-125, 1994.
Harborth, H. and Möller, M. "Minimum Integral Drawings of the Platonic Graphs." Math. Mag. 67, 355-358, 1994.
Hopcroft, J. and Tarjan, R. "Efficiency Planarity Testing." J. ACM 21, 549-568, 1974.
Kocay, W. and Pantel, C. "An Algorithm for Finding a Planar Layout of a Graph with a Regular Polygon as Outer Face." Util. Math. 48, 161-178, 1995.
Le Lionnais, F. Les nombres remarquables. Paris: Hermann, p. 56, 1983.
Meyer, J. "L'épaisseur des graphes completes K_(34) et K_(40)." J. Comp. Th. 9, 1970.
Nishizeki, T. and Rahman, M. S. Planar Graph Drawing. Singapore: World Scientific, 2004.
Read, R. C. "A New Method for Drawing a Planar Graph Given the Cyclic Order of the Edges at Each Vertex." Congr. Numer. 56, 31-44, 1987.
Scheinerman, E. and Wilf, H. S. "The Rectilinear Crossing Number of a Complete Graph and Sylvester's 'Four Point' Problem of Geometric Probability." Amer. Math. Monthly 101, 939-943, 1994.
Skiena, S. "Planar Graphs." §6.5 in Implementing Discrete Mathematics: Combinatorics and Graph Theory with Mathematica. Reading, MA: Addison-Wesley, pp. 247-253, 1990.
Sloane, N. J. A. Sequences A003094/M1652, A005470/M1252, A049370, A049371, A049372, and A049373 in "The On-Line Encyclopedia of Integer Sequences."
Steinbach, P. Field Guide to Simple Graphs. Albuquerque, NM: Design Lab, 1990.
Stony Brook Algorithm Repository. §1.4.12. "Planarity Detection and Embedding." http://www.cs.sunysb.edu/~algorith/files/planar-drawing.shtml.
Wagon, S. "Coloring Planar Maps and Graphs." Ch. 24 in Mathematica in Action, 2nd ed. New York: Springer-Verlag, pp. 507-537, 1999.
West, D. B. Introduction to Graph Theory, 2nd ed. Englewood Cliffs, NJ: Prentice-Hall, p. 243, 2000.
Whitney, H. "Non-Separable and Planar Graphs." Trans. Amer. Math. Soc. 34, 339-362, 1932.
Whitney, H. "Planar Graphs." Fund. Math. 21, 73-84, 1933.
