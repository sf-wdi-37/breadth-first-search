Choose two of the graphs representations below. Draw the graph described by the data you chose.

### Graph Representations


We often think of graphs as we'd draw them on the page. But they're stored differently in a computer.  We've seen an OOP tree implementation, but graphs can be stored in less space with simple combinations of more fundamental data structures.

![graph](https://cloud.githubusercontent.com/assets/3254910/19509277/e2f49b22-9592-11e6-91be-adc6c827ea07.png)


Adjacency lists store each node along with a list of other nodes it has edges going to.

```
  A: B -> C,
  B: None,
  C: B
```

Adjacency matrices store all the possible edges as an array of arrays (called a "matrix"). A `1` represents that there is an edge from the node in the "big" array to the node in the "little" array. A `0` means there's no edge there.  In the example below, the `1` at `graph[2][1]` means there's an edge from node C to node B. 

```
[
  # A  B  C  
	[ 0, 1, 1 ], # A
	[ 0, 0, 0 ], # B
	[ 0, 1, 0 ], # C
]
```





### Do Now

1. Choose one of the graphs from the "adjacency list examples" section and one from the "adjacency matrix examples" section.

1. Draw the graphs you picked.

1. For each of your graphs, answer:

  - Is the graph a tree?  
  - If the graph is a tree, what is its root?  
  - If the graph is a tree, is it a binary tree?  
  - If the graph is a tree, is it a binary search tree?   

1. Check your findings with a partner.


### Adjacency List Examples

<details><summary>A</summary>

```
  1: 2,
  2: 1,
  3: 2 -> 5,
  4: None,
  5: 4 -> 6,
  6: 5
```
</details>

<details><summary>B</summary>

```
  1: 4,
  2: 3,
  3: None,
  4: None,
  5: 1 -> 2 -> 4 -> 6,
  6: None
```
</details>

<details><summary>C</summary>

```
  1: 6,
  2: 1,
  3: 5,
  4: 3,
  5: 2,
  6: 4
```
</details>

<details><summary>D</summary>

```
  1: 4,
  2: 1 -> 4,
  3: None,
  4: 3 -> 6,
  5: 2,
  6: 1 -> 3,
```
</details>

<details><summary>E</summary>

```
  1: None,
  2: 1,
  3: 2 -> 5,
  4: None,
  5: 4 -> 6,
  6: None
```
</details>

<details><summary>F</summary>

```
  1: None,
  2: 3,
  3: None,
  4: None,
  5: 1 -> 2 -> 4 -> 6,
  6: None
```
</details>

<details><summary>G</summary>

```
  1: 6,
  2: None,
  3: 5,
  4: 3,
  5: 2,
  6: 4
```
</details>

<details><summary>H</summary>

```
  1: None,
  2: None,
  3: 1 -> 2,
  4: 3 -> 6,
  5: None,
  6: 5
```
</details>


### Adjacency Matrix


<details><summary>A</summary>
```
[
  # 1  2  3  4  5  6
	[ 0, 1, 0, 0, 0, 0 ], # 1
	[ 1, 0, 0, 0, 0, 0 ], # 2
	[ 0, 1, 0, 0, 1, 0 ], # 3
	[ 0, 0, 0, 0, 0, 0 ], # 4
	[ 0, 0, 0, 1, 0, 1 ], # 5
	[ 0, 0, 0, 0, 1, 0 ]  # 6
]
```
</details>

<details><summary>B</summary>
```
[
  # 1  2  3  4  5  6
	[ 0, 0, 0, 1, 0, 0 ], # 1
	[ 0, 0, 1, 0, 0, 0 ], # 2
	[ 0, 0, 0, 0, 0, 0 ], # 3
	[ 0, 0, 0, 0, 0, 0 ], # 4
	[ 1, 1, 0, 1, 0, 1 ], # 5
	[ 0, 0, 0, 0, 0, 0 ]  # 6
]
```
</details>

<details><summary>C</summary>
```
[
  # 1  2  3  4  5  6
	[ 0, 0, 0, 0, 0, 1 ], # 1
	[ 1, 0, 0, 0, 0, 0 ], # 2
	[ 0, 0, 0, 0, 1, 0 ], # 3
	[ 0, 0, 1, 0, 0, 0 ], # 4
	[ 0, 1, 0, 0, 0, 0 ], # 5
	[ 0, 0, 0, 1, 0, 0 ]  # 6
]
```
</details>

<details><summary>D</summary>
```
[
  # 1  2  3  4  5  6
	[ 0, 0, 0, 1, 0, 0 ], # 1
	[ 1, 0, 0, 1, 0, 0 ], # 2
	[ 0, 0, 0, 0, 0, 0 ], # 3
	[ 0, 0, 1, 0, 0, 1 ], # 4
	[ 0, 1, 0, 0, 0, 0 ], # 5
	[ 1, 0, 1, 0, 0, 0 ]  # 6
]
```
</details>

<details><summary>E</summary>
```
[
  # 1  2  3  4  5  6
	[ 0, 0, 0, 0, 0, 0 ], # 1
	[ 1, 0, 0, 0, 0, 0 ], # 2
	[ 0, 1, 0, 0, 1, 0 ], # 3
	[ 0, 0, 0, 0, 0, 0 ], # 4
	[ 0, 0, 0, 1, 0, 1 ], # 5
	[ 0, 0, 0, 0, 0, 0 ]  # 6
]
```
</details>

<details><summary>F</summary>
```
[
  # 1  2  3  4  5  6
	[ 0, 0, 0, 0, 0, 0 ], # 1
	[ 0, 0, 1, 0, 0, 0 ], # 2
	[ 0, 0, 0, 0, 0, 0 ], # 3
	[ 0, 0, 0, 0, 0, 0 ], # 4
	[ 1, 1, 0, 1, 0, 1 ], # 5
	[ 0, 0, 0, 0, 0, 0 ]  # 6
]
```
</details>

<details><summary>G</summary>
```
[
  # 1  2  3  4  5  6
	[ 0, 0, 0, 0, 0, 1 ], # 1
	[ 0, 0, 0, 0, 0, 0 ], # 2
	[ 0, 0, 0, 0, 1, 0 ], # 3
	[ 0, 0, 1, 0, 0, 0 ], # 4
	[ 0, 1, 0, 0, 0, 0 ], # 5
	[ 0, 0, 0, 1, 0, 0 ]  # 6
]
```
</details>

<details><summary>H</summary>
```
[
  # 1  2  3  4  5  6
	[ 0, 0, 0, 0, 0, 0 ], # 1
	[ 0, 0, 0, 0, 0, 0 ], # 2
	[ 1, 1, 0, 0, 0, 0 ], # 3
	[ 0, 0, 1, 0, 0, 1 ], # 4
	[ 0, 0, 0, 0, 0, 0 ], # 5
	[ 0, 0, 0, 0, 1, 0 ]  # 6
]
```
</details>
