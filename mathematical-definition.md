# Mathematical Definition of TIRARIT

**Author: Lowioo**

## 1. The Generalized Rayo Function

Let L be a fixed formal language with a precisely defined symbol-counting convention.

Let D_n be the set of all natural numbers that can be uniquely defined using fewer than n symbols in L.

Define the generalized Rayo function as:

R(n) = 1 + max(D_n)

This definition applies whenever D_n is nonempty.

The function R is nondecreasing because increasing the symbol limit cannot remove previously definable numbers.

For this construction, let:

G = 10^100

Under the strict fewer-than-G-symbols convention, R(G) represents the Rayo benchmark.

## 2. The TREE Function

TREE(k) denotes the standard TREE function from Kruskal's tree theorem.

It is defined using finite rooted trees whose vertices are labeled with one of k available labels.

TREE(k) is the maximum length of a finite sequence:

T_1, T_2, ..., T_m

subject to these conditions:

- The i-th tree contains at most i vertices.
- No earlier tree can be embedded into a later tree.
- The embedding follows the standard label-preserving rooted tree embedding relation.

The standard TREE function is finite for every positive integer k.

## 3. The TIRARIT Function

First, define the composition:

F(x) = TREE(R(x))

The TIRARIT function is defined as:

TIRARIT(n) = F^n(TREE(3))

Equivalently:

TIRARIT(n) = (TREE ∘ R)^n(TREE(3))

Here, the superscript n represents n-fold function composition, not exponentiation.

For n = 0, no composition is applied:

TIRARIT(0) = TREE(3)

For n = 1:

TIRARIT(1) = TREE(R(TREE(3)))

For n = 2:

TIRARIT(2) = TREE(R(TREE(R(TREE(3)))))

For n = 3:

TIRARIT(3) = TREE(R(TREE(R(TREE(R(TREE(3)))))))

## 4. General Convention

TIRARIT is a sequence of finite natural numbers generated through repeated composition of the standard TREE function and the generalized Rayo function.

Each iteration applies R first and TREE second.

The construction depends on the chosen formal language and symbol-counting convention used to define R.
