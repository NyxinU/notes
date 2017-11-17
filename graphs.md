Graphs

ANYTHING with connections. Trees are graphs.

Vertices = data points
Edges = connections between points, like a joins table

How to solve a graph without using vertices & edges?
Adjacency Matrix - a square matrix used to represent a finite graph
   A  B  C  D
A  0  1  0  0
B  1  0  0  0
C  0  0  0  0
D  0  0  0  0

non directed acyclic graph? (DAG)


Kahn's? Algorithm - BFS
```

def topological_sort(vertices)
  queue = []
  in_edge_count = {}

  vertices.each do |vertex|
    in_edge_count(vertex) = vertex.in_edges.length
    if vertex.in_edges.empty?
      queue << vertex
    end
  end
  sorted = []

  until queue.empty?
    current = queue.shift
    sorted << current
    current.out_edges.each do |edge|
      in_edge_count[edge.to_vertex] -= 1

      return [] if in_edge_count[edge.to_vertex] < 0
      queue << edge.to_vertex if in_edge_count[edge.to_vertex] == 0
    end
  end

  return [] if in_edge_count.values.any? { |count| count != 0 }
  sorted
end

```

Tarjan's Algorithm - DFS to explore nodes until they have no children or no unvisited children
Once a node's connections have been exhausted, it is unshifted onto the result, nodes that have 'later' dependencies will be processed before those that have 'earlier' ones. Each node and edge is visited once so time complexity is linear.


Install Order

```
def install_order(arr)
  max = 0
  vertices = {}
  arr.each do |tuple|
    vertices[tuple[0]] = Vertex.new(tuple[0]) unless vertices[tuple[0]]
    vertices[tuple[1]] = Vertex.new(tuple[1]) unless vertices[tuple[1]]
    Edge.new(vertices[tuple[1]], vertices[tuple[0]])

    max = tuple.max if tuple.max > max
  end

  independent = []
  (1..max).....???????
end

```
