# SOM solving TSP
Solving Traveling Salesman Problem using Self-Organizing Maps.

### Input:
The distances between each pair of vertices. There are two methods available in the code for reading the input. 
1.  At line `i`, there should be `n-i` space-separated integers; The `j`th integer indicates the distance between vertex `i` and `i+j`. 
2.  At line `i`, there should be three space-separated integers; First, the index of the vertex, second and third integers indicates the coordinate of the vertex.

### Process:
Here, we have a set of cities:

<p float="left">
  <img src="https://user-images.githubusercontent.com/12760574/130592580-c57b4ede-2ee0-429c-9222-3d09ffb8a4a2.png" width="400" />
</p>

The variable `k` determines the number of the clusters. Here are some clustering for different `k`s:

<p float="left">
  <img src="https://user-images.githubusercontent.com/12760574/130632332-e3906332-303f-487c-9387-e6f481b1edd2.png" width="250" />
  <img src="https://user-images.githubusercontent.com/12760574/130632345-3ede9374-dca2-4d9e-b0f5-de3f6a5b1e70.png" width="250" />
  <img src="https://user-images.githubusercontent.com/12760574/130632350-3fcc1b52-0cc9-478e-b99f-0d2de1ccbdf9.png" width="250" />
</p>

Here is another example. The left figure is the starting positioning of the clusters, and the right figure is the "organized" one:
<p float="left">
  <img src="https://user-images.githubusercontent.com/12760574/130633746-bc516a7d-dda5-4e05-a182-dca7bafed46b.png" width="250" />
  <img src="https://user-images.githubusercontent.com/12760574/130633754-f4e01538-9a03-4d07-a145-731fb25aca3b.png" width="250" />
</p>

Then for every cluster, it finds the best path connecting all the vertices by brute force: Checking all the permutations possible. Then connects these paths together. We can use Brute force here too; Although I didn't; I've implemented this part with greedy.


<p float="left">
  <img src="https://user-images.githubusercontent.com/12760574/130633754-f4e01538-9a03-4d07-a145-731fb25aca3b.png" width="250" />
  <img src="https://user-images.githubusercontent.com/12760574/130635185-f9bea225-38a9-448e-9256-865847b144c2.png" width="250" />
  <img src="https://user-images.githubusercontent.com/12760574/130634832-499190a1-a0bd-41e9-9622-e08bb99e2083.png" width="250" />
</p>

Here's another example of this code functioning for the same testcase:

<p float="left">
  <img src="https://user-images.githubusercontent.com/12760574/130635729-a4f179a7-2703-4a43-878b-fc55aeba644f.png" height="250" />
</p>

The best answer for this testcase:
<p float="left">
  <img src="https://user-images.githubusercontent.com/12760574/130592580-c57b4ede-2ee0-429c-9222-3d09ffb8a4a2.png" width="350" />
  <img src="https://user-images.githubusercontent.com/12760574/130636053-d6de26d8-030f-4f91-9c43-98e86c086bbc.png" width="350" />
</p>


### Output:
It outputs the minimal cost and the cycle itself. The code for visualing the answer is present in the code.
