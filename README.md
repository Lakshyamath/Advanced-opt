# Advanced-opt
Advanced optimization or optimization of dynamic processes under uncertainty

This is a eighth semester course on quantitative and data science at Birla Institute of Technology Mesra Ranchi. The course ia having three folds, first we discuss convex program (as a single-stage optimzation), then we discuss dynamic programming & stochastic control (as multi-stages optimization) and at the last we discuss metaheuristic optimization (as a derivative free optimization).

In the dynamic programmic & stochastic control, we have discussed the following examples:

Exa-01: Inventory control where a store must decide how much stock to order based on fluctuating customer demand, 

Exa-02: Shortest path problems,

Exa-03: Managing a portfolio of investments with uncertain market returns,

Exa-04: A gambler's problem where betting decisions are made based on uncertain outcomes (win/loss probabilities), 

Exa-05: Optimizing robot movement in a noisy environment.

Lecture-wise description:

Lecture-06 (05-02-2025): Expected cost function:
1. Expected cost function for stochastic control of a dynamical system ($x_{k+1}=f_k(x_k,u_k,\omega_k), k=0,1,...N-1$) with a feedback policy $\pi$ :

$J_{pi}(x_0) =E(c_N(x_N)+\sum_{k=0}^{N-1}c_k(x_k,\mu_k(x_k),\omega_k))$


2. Dynamic programming for optimizing the expected cost function as sequential tail-subproblems from backward:
Step-a. Initialization from backward (Nth tail subproblem):

$J_N (x_N )=c_N (x_N )⇒V(x_N )=J_N (x_N )=J_N^∗ (x_N )$

b. N-1 tail subproblem:

$J_{N-1}(x_{N-1})=E(c_{N-1}(x_{N-1})+J_N^∗(x_N)) ⇒ V(x_{N-1})=J_{N-1}^∗ (x_{N-1})=inf_{\mu{N-1}}⁡{J_{N-1}(x_{N-1})}$

c. N-2 tail sub-problem:

$J_{N-2}(x_{N-2})=E(c_{N-2}(x_{N-2})+J_{N-1}^∗ (x_{N-1})) ⇒ V(x_{N-2})=J_{N-2}^∗ (x_{N-2})=inf_(\mu_{N-2})⁡ {J_{N-2} (x_{N-2})}$

d. kth tail-subproblem:

$J_k(x_k)=E(c_k(x_k) + J_{k+1}^∗(x_{k+})) ⇒ V(x_k)=J_k^∗(x_k)=inf_{\mu_k}⁡ {J_k(x_k)}$

e. 0th tail-subproblem:

$J(x_0 )=E(c_0 (x_0) + J_1^∗(x_1)) ⇒ V(x_0 )=J^∗(x_0)=inf_{\mu_0} {⁡J(x_0)}$

Example:
Modeling an inventory system as a stochastic control system where states represent inventory levels and control represent order quantities, and using dynamic programming to find the optimal ordering policy to minimize costs.
Shortest path problems.

Lecture-09 (07-02-2025): Convex program

Recap:
Convex optimization problem as minimizing a convex function f over a convex set C or maximizing a concave function f over a convex set C

Lecture content
Convexity of a function f is defined by Jensen's inequality as image of convex combination of any two points is less than equal to convex combination of the corresponding images of the points.

In order to characterize further there is a need to recall separating hyperplane and supporting hypothesis alongwith separation lemma, and theorem of alternative.and orthogonal projection.

Precap:
In next lecture we will discuss optimality condition for a convex programming.
