<b>Temporal Decomposition</b> is a particular kind of information leakage; it occurs when a system's structure mirrors it’s execution order. For instance, consider a system that modifies a file with the following steps: read the file, make changes to the file's data, and write the file. A system that mirrors the execution of this sequence has three modules, one for each step. And in that case, the structure of the code - the three modules - reflects the execution - the three steps. 

Ousterhout considers temporal decomposition a red flag because it typically means reflecting a design decision in multiple modules. In the case above, the file format is reflected three times, once for each module. 

I also think, however, it's a problem for another reason; namely, it conflates interface design with problem decomposition. When you solve a problem, you break the problem into sub-problems that are solvable on their own and then code a solution for each. For instance, the problem of updating a file is decomposed into the problems of reading the file, making changes to the file's data, and writing the file. (Execution order closely follows problem decomposition because both break a task into steps).

At that point, it's tempting to create a single module that exposes each of these functions. The module solves the problem of updating a file, so surely its interface should include utilities that are relevant to updating the file. Right? I don't think so. The problem is to update a file, so that’s all the interface should be concerned with. Exposing the functions that solve the sub-problems amounts to showing how you solve the main problem. That is implementation and should be hidden within. The consumer of the module does not need to know how the system solves the problem.