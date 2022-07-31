From the data structure point of view, following are some important **categories of algorithms** −

- Search − Algorithm to search an item in a data structure.

- Sort − Algorithm to sort items in a certain order.

- Insert − Algorithm to insert item in a data structure.

- Update − Algorithm to update an existing item in a data structure.

- Delete − Algorithm to delete an existing item from a data structure.


An algorithm should have the following **characteristics** −

- Unambiguous − Algorithm should be clear and unambiguous. Each of its steps (or phases), and their inputs/outputs should be clear and must lead to only one meaning.

- Input − An algorithm should have 0 or more well-defined inputs.

- Output − An algorithm should have 1 or more well-defined outputs, and should match the desired output.

- Finiteness − Algorithms must terminate after a finite number of steps.

- Feasibility − Should be feasible with the available resources.

- Independent − An algorithm should have step-by-step directions, which should be independent of any programming code.


There are no well-defined standards for writing algorithms. Rather, it is problem and resource dependent. Algorithms are never written to support a particular programming code.

We write algorithms in a step-by-step manner, but it is not always the case. Algorithm writing is a process and is executed after the problem domain is well-defined. That is, we should know the problem domain, for which we are designing a solution.

Efficiency of an algorithm can be analyzed at two different stages, before implementation and after implementation. 

#### Algorithm Complexity
Suppose X is an algorithm and n is the size of input data, the time and space used by the algorithm X are the two main factors, which decide the efficiency of X.

Time Factor − Time is measured by counting the number of key operations such as comparisons in the sorting algorithm.

Space Factor − Space is measured by counting the maximum memory space required by the algorithm.

#### Space complexity
It represents the amount of memory space required by the algorithm in its life cycle. The space required by an algorithm is equal to the sum of the following two components

- A fixed part that is a space required to store certain data and variables, that are independent of the size of the problem. For example, simple variables and constants used, program size, etc.

- A variable part is a space required by variables, whose size depends on the size of the problem. For example, dynamic memory allocation, recursion stack space, etc.

Space complexity S(P) of any algorithm P is S(P) = C + SP(I), where C is the fixed part and S(I) is the variable part of the algorithm, which depends on instance characteristic I.

Example:

`Algorithm: SUM(A, B)
Step 1 -  START
Step 2 -  C ← A + B + 10
Step 3 -  Stop`

Here we have three variables A, B, and C and one constant. Hence S(P) = 1 + 3. Now, space depends on data types of given variables and constant types and it will be multiplied accordingly.

**Time complexity** of an algorithm represents the amount of time required by the algorithm to run to completion. Time requirements can be defined as a numerical function T(n), where T(n) can be measured as the number of steps, provided each step consumes constant time.

For example, addition of two n-bit integers takes n steps. Consequently, the total computational time is T(n) = c ∗ n, where c is the time taken for the addition of two bits. Here, we observe that T(n) grows linearly as the input size increases.

Example (may be wrong):
26
37

63

Step1: adding 6+7 in ones place
Step2: adding 2+3+1(step 1 carry) in tens place

**Asymptotic analysis** of an algorithm refers to defining the mathematical boundation/framing of its run-time performance. Using asymptotic analysis, we can very well conclude the best case, average case, and worst case scenario of an algorithm.

Asymptotic analysis is input bound i.e., if there's no input to the algorithm, it is concluded to work in a constant time. Other than the "input" all other factors are considered constant.
