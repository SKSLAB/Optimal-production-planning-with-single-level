# Optimal production planning with single-level
##### An optimization test suite involving 54 continuous variables

This submission can be used to evaluate the performance of optimization techniques on problems with continuous variables. This optimization problem arises for maximization of profit in production planning. However these files can be used as black-box optimization problems.

There are eight minimization optimization problems in this suite (case1.p, case2.p, case3.p, case4.p, case5.p, case6.p, case7.p and cas8.p).

Each of them has the following format
```
[ F, XCorrected] = case1(X);
```
Input: population (or solution, denoted by X) and its <br>
Output: (i) the corrected population (denoted by XCorrected), and <br>
(ii) the objective function value of the corrected population members (F). X is corrected to XCorrected as most algorithms fail to satisfy the complex constraints and XCorrected is not worse to X.

The file ProblemDetails.p can be used to determine the lower and upper bounds along with the function handle for each of the cases.

The format is `[lb, ub, fobj] = ProblemDetails(ca);`

Input: ca is an integer from 1 to 8. <br>
Output: (i) the lower bound (lb), <br>
	    (ii) the upper bound (ub), and <br>
	    (iii) function handle (fobj).

The file Script.m shows how to use these files along with an optimization algorithm (SanitizedTLBO).

All cases (Case1 to Case 8) have a problem dimension of 54 continuous variables.

**Note:** <br> 
  1. The inbuilt optimization algorithms in MATLAB require that the objective function file return only the values of the objective function and cannot be directly used to solve these problems.

  2. Conventionally, the algorithm provides the solutions (X) and requires the objective function values (F). But in these problems, in addition to F, the corrected solutions (XCorrected) are provided by the objective function file.

  3. The current best known solutions (rounded to two decimals), using computational intelligence algorithms, are <br>
  Case 1: -690.34; Case 2: -758.93; Case 3: -891.40; Case 4: -1097.98 <br>
  Case 5: -724.93; Case 6: -832.29; Case 7: -1164.64; Case 8: -1452.82

  4. Case 1 - 4 have the same problem structure but employ different data; Case 5 - 8 has same set of data as compared to Case 1 - 4, but do not employ a certain feature (flexible) of the problem.

  5. The objective function files are capable of determining the objective function values of multiple solutions (i.e., if required, the entire population can be sent to the objective function file).

<br>
**Reference:** <br> 
  1. Chauhan, S., S., and Kotecha P. (2016) Single level production planning in petrochemical industries using Moth-flame optimization,IEEE Region 10 Conference (TENCON), Singapore, https://doi.org/10.1109/TENCON.2016.7848003. <br>
  2. Chauhan, S., S., and Kotecha P. (2018), Single-Level Production Planning in Petrochemical Industries using Novel Computational Intelligence Algorithms,Metaheuristic Optimization Methods: Algorithms and Engineering Applications, Springer.
  