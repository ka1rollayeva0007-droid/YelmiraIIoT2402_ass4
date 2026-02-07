# Graph Implementation (Assignment 4)

### How to Run Each Scenario
To execute all testing scenarios (Empty graph, Single vertex, Disconnected graph, Multiple components, Cycles, BFS shortest path, DFS determinism, and Invalid inputs), use the following commands:

1. **Compile:** `javac src/*.java`
2. **Run:** `java Main`

Running the `Main` class will automatically trigger the test suite for all 8 scenarios and start the **Stress Test**, which measures runtime performance for increasing $|V|$ and $|E|$.

---

### Neighbor Ordering Handling
To ensure the output of BFS and DFS is **deterministic** (identical every time), neighbor ordering is handled by **sorting the adjacency lists in ascending order**. 

When the algorithm explores a vertex, it retrieves the neighbors and sorts them by their IDs before pushing them to the queue (BFS) or stack (DFS). This way, the neighbor with the smallest value is always processed first.

---

### Testing & Deliverables
* **8 Core Tests:** Covered in the automated test suite.
* **Stress Test:** Included in the run command, measuring $O(V+E)$ and $O(V^2)$ performance.
* **Graph API:** Supports both Adjacency List and Adjacency Matrix representations.
* **Report:** See `Report.pdf` for design decisions and applied problem results.
