## PYTHON PROGRAM

```
ENTER YOUR CODE HERE
"""
A Python program to demonstrate the adjacency
list representation of the graph
"""

# A class to represent the adjacency list of the node


class AdjNode:
	def __init__(self, data):
		self.vertex = data
		self.next = None


# A class to represent a graph. A graph
# is the list of the adjacency lists.
# Size of the array will be the no. of the
# vertices "V"
class Graph:
	def __init__(self, vertices):
		self.V = vertices
		self.graph = [None] * self.V

	# Function to add an edge in an undirected graph
	def add_edge(self, src, dest):
		# Adding the node to the source node
		node = AdjNode(dest)
		node.next = self.graph[src]
		self.graph[src] = node

		# Adding the source node to the destination as
		# it is the undirected graph
		node = AdjNode(src)
		node.next = self.graph[dest]
		self.graph[dest] = node

	
	def print_graph(self):
	    for i in range(self.V):
	        print('Adjacency list of vertex {}\n'.format(i,i),end="")
	        print("",i,"",end="")
	        
	        temp=self.graph[i]
	        while temp:
	            print('-> {}'.format(temp.vertex),end=" ")
	            temp=temp.next
	        print('\n')
		
		
		#Write Code here





# Driver program to the above graph class
if __name__ == "__main__":
	V = 5
	graph = Graph(V)
	graph.add_edge(0, 1)
	graph.add_edge(0, 4)
	graph.add_edge(1, 2)
	graph.add_edge(1, 3)
	graph.add_edge(1, 4)
	graph.add_edge(2, 3)
	graph.add_edge(3, 4)

	graph.print_graph()

```

## OUTPUT
```
```
<img width="791" height="459" alt="image" src="https://github.com/user-attachments/assets/08482a04-a492-4304-adaa-bebc7653068d" />

## RESULT

## RESULT
Thus,a Python program to demonstrate the **adjacency list representation** of the given graph is successfully executed.
