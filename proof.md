# Proof that TIRARIT(1) > Rayo's Number

**Author: Lowioo**

## 1. Definitions

Let:

G = 10^100

Define the generalized Rayo function:

R(n) = 1 + max(D_n)

where D_n is the set of natural numbers uniquely definable using fewer than n symbols in a fixed formal language.

Under the strict fewer-than-G-symbols convention, the Rayo benchmark is represented by:

R(G)

Define TREE as the standard TREE function based on finite rooted trees and the usual label-preserving embedding relation.

We use the known fact:

TREE(3) > Graham's Number > G

TIRARIT is defined by:

TIRARIT(n) = (TREE ∘ R)^n(TREE(3))

Therefore:

TIRARIT(1) = TREE(R(TREE(3)))

## 2. Proof

Since:

TREE(3) > G

and R is nondecreasing:

R(TREE(3)) ≥ R(G)

Let:

X = R(G)

Then:

R(TREE(3)) ≥ X

For every natural number X ≥ 2, the standard TREE function satisfies:

TREE(X) > X

Also, TREE is strictly increasing. Therefore:

TREE(R(TREE(3))) ≥ TREE(X) > X

Substituting X = R(G):

TREE(R(TREE(3))) > R(G)

Since:

TIRARIT(1) = TREE(R(TREE(3)))

we conclude:

TIRARIT(1) > R(G)

## 3. Conclusion

TIRARIT(1) is greater than the Rayo benchmark R(G), under the stated formal-language and symbol-counting conventions.

**Q.E.D.**
