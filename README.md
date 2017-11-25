# Generalized_McCormick_Relaxations_Library
#### Author: Yuanxun Shao

### 1. Introduction
**MCPy** is a python library for automatically calculate convex\concave relaxations and subgradients of factorable nonconvex functions according to McCormick relaxation rules and interval arithmetic. The library could be quite useful for prototyping and testing new global optimization algorithms.

Theory and implementation for the global optimization of a wide class of algorithms is presented via convex/affine relaxations [1]. Similar to the convex\concave relaxation, the subgradient propagation relies on the recursive application of specific rules, which could provide us affine relaxations of McCormick relaxations. This library automatedly implements those theorems based on normal and reverse operator overloading.

### 2. Instruction
Supported rules so far: +, -, /, \*, sqrt, log, exp, \*\*(restricted to odd and even integer power).
<br />
Upcoming rules: sin, cos.

There are three instance variables in the class, MCPy.IA, MCPy.MC, MCPy.SG.
<br />
**MCPy.IA**: 
<br />1-D numpy array of two elements [LB, UB]. LB/UB are the lower/upper bounds the function calculated by intervarl arithmetic.
<br />
**MCPy.MC**: 
<br />1-D numpy array of two elements [cv, cc]. cv/cc are the convex underestimator/concave overestimator of the function calculated by McCormick rules.
<br />
**MCPy.SG**: 
<br />2-D numpy $n_x \times 2$ matrix

### References:
[1] Mitsos, A., B. Chachuat, P.I. Barton, [McCormick-based relaxations of algorithms](http://epubs.siam.org/doi/abs/10.1137/080717341), SIAM Journal on Optimization, 20(2):573-601, 2009
<br />
[2] Bompadre, A., A. Mitsos, [Convergence rate of McCormick relaxations](https://link.springer.com/article/10.1007%2Fs10898-011-9685-2), Journal of Global Optimization 52(1):1-28, 2012
