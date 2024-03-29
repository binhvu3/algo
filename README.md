# Data Strutures and Algorithms
-  <a href="https://www.youtube.com/playlist?list=PLRdD1c6QbAqJn0606RlOR6T3yUqFWKwmX ">Video lectures from ROBERT SEDGWIG</a>

## Search
![search summary](resource/search_summary.png)

## Undiracted Graphs
- **DFS**: Go Deep down use recursion/stack to check adj node(s). 
- **BFS**: Queue each node and check the adj. Use df {edge (index), edgeTo[] (int), disTo[] (int)}
- **CC (connected components)**: Each cluster into 1 category. Each node in category is connected.

## Directed Graph
- **Strong Component**: digraph that have in and out. Similar to CC.
- **Kosaraju-Sharir**: (1) reverse graph and dfs -> return list of nodes list (2) Use node list to run dfs on og graph
![https://www.youtube.com/watch?v=zFgkK4g65ys&list=PLRdD1c6QbAqJn0606RlOR6T3yUqFWKwmX&index=40](resource/digraph.png)

## Minimum Spanning Tree (MST)
- Graph with weights -> find the lowest
- Kruskal's: sort weight lowest to highest, go down and add unless it create a cycle
- Prim's: Start at node #0, check node 1 step away, take the lowest using Priority Queue (PQ). 
  - Two version (1) Lazy and (2) Eager
- 
### Priority Queue
- Use binary heap as data structure  <a href="https://www.youtube.com/watch?v=AE5I0xACpZs">What is a Binary Heap?</a>

## Shortest Path
- Generic Shortest-path: check from 0-inf and relax any edge.
- <a href="https://youtu.be/_lHSawdgXpI?t=31">What is edge relaxation?</a> Initalize first node w/ 0 and everything else inf. Update/relax edge based on weights.
- <a href="https://youtu.be/_lHSawdgXpI">Dijkstra's algo (non-negative weights)</a>: similar start to Generic, keep track of total distance from root, update path if better weight found. check all nodes. <a href="https://youtu.be/uzHJXbToiIU?list=PLRdD1c6QbAqJn0606RlOR6T3yUqFWKwmX&t=127">demo</a>
- <a href="test">Topological Sort (no directed cycles)</a>: Find the lowest weight from the choosen node.<a href="https://youtu.be/Qp9zy9qMJzE?list=PLRdD1c6QbAqJn0606RlOR6T3yUqFWKwmX&t=42">demo</a>
- <a href="https://www.youtube.com/watch?v=obWXjtg0L64">Bellman-Ford (no negative cycle)</a>: Double relaxation w/ v-1 iteration <a href="https://youtu.be/A54rUI6CPSs?list=PLRdD1c6QbAqJn0606RlOR6T3yUqFWKwmX&t=406">demo</a>

### Application
- <a href="https://youtu.be/_lHSawdgXpI?t=31">Seam Carving</a>: non-linear scaling algorithm that determine the shortest path given the energy
- Parallel job scheduling problem

### Definition
- <a href="https://youtu.be/A54rUI6CPSs?list=PLRdD1c6QbAqJn0606RlOR6T3yUqFWKwmX&t=182">Negative Cycle</a>: Negative loop that traps shortest path algo
- <a href="https://www.youtube.com/watch?v=9PHkk0UavIM">Differences b/w Dijkstra vs Bellman-Ford</a>

![Shortest path summary](resource/shortest_path.png)

## Maximum Flow
- <a href="https://www.youtube.com/watch?v=Tl90tNtKvxs">Ford-Fulkerson</a>:  

### Mincut Porblem
- Find the minimum capacity (capacity == weights)

#### Application
- Cold-war: Cut of railroad network of adversary at the cheapest cose
- Government-in-power: Cut of communication to a set of people

### Maxflow Problem
- Flow = weight w/ capacity. Water through a pipe. 
- Every node need to have a balance inflow & outflow

![Min Cut Max Flow](resource/min_cut_max_flow.png)

# String Symbol
## Key-Indexed Counting
- count all element in list -> Create a cumulative sum of that count as index limits -> sort using that cumulative sum. 

## Radix LSD (Least Significant Digit) Sort
- Search from left to right using separate for loop. <a href="https://youtu.be/n7jfknr2Bxw?list=PLRdD1c6QbAqJn0606RlOR6T3yUqFWKwmX&t=191">Demo</a>

### MSD (Most Significant Digit)
- Start from right and recursively order each column. <a href="https://youtu.be/1XdrDjreqJM?list=PLRdD1c6QbAqJn0606RlOR6T3yUqFWKwmX&t=101">Demo</a>

## 3-ways String Quicksort
- Similar to quick sort but segmented. <a href="https://youtu.be/QwzPkViilYA?list=PLRdD1c6QbAqJn0606RlOR6T3yUqFWKwmX&t=139">Demo</a> 

## Suffix Sorting
- Use a <a href="https://youtu.be/V2yMD-vpndA?list=PLRdD1c6QbAqJn0606RlOR6T3yUqFWKwmX&t=406">form suffixes</a> and sort MSD then binary search. <a href="https://youtu.be/V2yMD-vpndA?list=PLRdD1c6QbAqJn0606RlOR6T3yUqFWKwmX&t=137">Demo</a>
### Application 
- keyword-in-context search: crt+f, highlight the desired word and the wording around it.

- Longest repeated substring: 
[README.md](README.md)
## Suffix Array - Manber-Mybers Algo:
- O(N): Linear time complexity. <a href="https://youtu.be/V2yMD-vpndA?list=PLRdD1c6QbAqJn0606RlOR6T3yUqFWKwmX&t=790">Demo</a>

## R-ways Tries (data type)
- <a href="https://youtu.be/el9-Vb6iNPM?list=PLRdD1c6QbAqJn0606RlOR6T3yUqFWKwmX&t=431">Tries Demo</a>: 
- <a href="https://www.youtube.com/watch?v=qvZGUFHWChY">Red-Black BST (Binary Search Tree) </a>: Type of balanced search tree 
### Patricia Trie/Radix Tree
- Remove one-way branching

### Suffix Tree
- Patricia Trie/Radix Tree of suffixes of a string

## TST -Ternary Search Tries
- Data structure with exact three child nodes. Left < val, Mid == val, Right > val.
- Search: match go down.
- <a href="https://youtu.be/CqE9My0ErRI?list=PLRdD1c6QbAqJn0606RlOR6T3yUqFWKwmX&t=444">Demo1</a>
- <a href="https://www.youtube.com/watch?v=bWaXdxEHaag">Demo2</a>

### Alternative Version
- TST with R^2 branching at root

![String search](resource/string_search.png)

# Sub-string Search
## Knuth-Morris-Pratts
- Build on top of the idea of <a href="https://youtu.be/wpcXh0RylPw?list=PLRdD1c6QbAqJn0606RlOR6T3yUqFWKwmX&t=193">Deterministic Finite State Automaton (DFA)</a> 

## Boyer-Moore

## Rabin-Karp
- Hash target val and compare with list.

![sub-String search](resource/substring_search.png)


# Regular Expression
- <a href="https://www.youtube.com/@lydia-.">Good YouTube Channel to Watch</a>`


## Nondeterministic Finite Automaton (NFA)
- Similar to char matching algo but with 2 transition state. <a href="https://youtu.be/DFTF_SG9pgI?list=PLRdD1c6QbAqJn0606RlOR6T3yUqFWKwmX&t=572">Demo</a>
- Find set of state that is reachable {1,2,3}

### Application
- GREP used in Unix bak in the day

### Differences between DFA and NFA
- DFA state is known is predetermined, NFA have could have multiple states
___
<a href="link">Demo</a>



