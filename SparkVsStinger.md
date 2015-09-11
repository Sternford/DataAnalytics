[Home](README.md) | 
[Installation](installation.md)

### Apache Spark GraphX
-----------------------
#### Class of data processing:
Distributed data flow based processing. Mostly suitable for iterative graph algorithms that can be divided into bunch of iterations with map, join and groub by operators.

In the efforts to make graph processing efficient, research was focused on developing specialized graph processing systems such as [Giraph](http://giraph.apache.org/), Pregel, etc. Spark tries to focus on providing generality of the processing. RDD are basic blocks of spark processing engines. Spark Streaming, Spark Graphx and Mlib are all built up on the top of RDD. This enables us to create the data processing pipeline in the form of lambda architecture.

#### Out of the box Algorithms provided:
- ConnectedComponents: Label Connected components in graph. 
- Label Propagation algorithm
- PageRank algorithm implementation
- Implementation of SVD++ algorithm
- ShortestPaths: Computes shortest paths to the given set of landmark vertices, returning a graph where each vertex attribute is a map containing the shortest-path distance to each reachable landmark
- Strongly connected components
- TriangleCount: Compute the number of triangles passing through each vertex
- In addition to that, there are many third party implementations of various algorithms available.

#### Supported Operators
#### Interface to various queuing technologies 
#### Support for various specialised graph data base
#### Examples

### STINGER (Spatio-Temporal Interaction Networks and Graphs (STING) Extensible Representation)
-----------------------------------------------------------------------------------------------
#### Class of data processing:
STINGER is designed to work for systems with massive shared memmory. The goal here is to develop algorithms that can run on machines with supercomputing powers (e.g XMT C, MTGL, PBGL). One of the main problems with these systems is **Portability**. Programs developed for one kind of architecture may not be portable to other. STINGER tries to solve this problem by providing a data structure that can be used reasonably well with all such types of shared memmory architectures.

#### Out of the box Algorithms provided:
- Streaming Connected components: Accurately tracks the connected components of a graph with insertions and deletions.
- Streaming Clustering coefficients: Tracks the local and global clustering coefficients of a graph under both edge insertions and deletions.
- Streaming Community detection: Track and update the community structures within the graph as they change.
- Parallel Agglomerative clustering: Find clusters that are optimized for a user-defined edge scoring function.
- Streaming Betweenness Centrality: Find the key points within information flows and structural vulnerabilities.
- K-core Extraction: Extract additional communities and filter noisy high-degree vertices.
- Classic breadth-first search: Performs a parallel breadth-first search of the graph starting at a given source vertex to find shortest paths.

#### Supported Operators
#### Interface to various queuing technologies 
#### Support for various specialised graph data base
#### Examples

Reference
---------
- STINGER introduction [link](http://www.stingergraph.com/index.php?id=introduction)
- Research paper on STINGER [link](http://cass-mt.pnnl.gov/docs/pubs/pnnlgeorgiatechsandiastinger-u.pdf)
- GraphX programming guide [link](http://spark.apache.org/docs/latest/graphx-programming-guide.html#graph-operators)
- GraphX Algorithms [link](http://spark.apache.org/docs/latest/api/scala/index.html#org.apache.spark.graphx.lib.package)
- Graphx reserach paper [link](https://amplab.cs.berkeley.edu/wp-content/uploads/2014/09/graphx.pdf)
- Difference between shared memmory (openMp) vs distributed memmory architectures for Big data processing [link](http://www.quora.com/What-are-the-advantages-of-Hadoop-over-openMP)
- Comparison of various graph processing technologies [link](http://www.stingergraph.com/data/uploads/papers/ppaa2014.pdf)
