# Mathematical Notation

**Author: Lowioo**

This document explains the mathematical symbols and notation used in TIRARIT.

## 1. Basic Symbols

| Symbol | Meaning |
|---|---|
| `n` | A natural number used as an input or iteration count. |
| `k` | The number of available tree labels. |
| `G` | The value `10^100`, used as the symbol limit in the Rayo benchmark. |
| `L` | The fixed formal language used to define numbers. |
| `D_n` | The set of natural numbers uniquely definable using fewer than n symbols in L. |
| `max(D_n)` | The largest element of the set D_n. |
| `R(n)` | The generalized Rayo function, defined as `1 + max(D_n)`. |
| `TREE(k)` | The standard TREE function evaluated at k. |
| `T_i` | The i-th tree in a sequence of finite rooted trees. |

## 2. Function Notation

### Function Composition

`(f ∘ g)(x)` means that g is applied to x first, followed by f.

Therefore:

`(TREE ∘ R)(x) = TREE(R(x))`

### Iterated Composition

`F^n(x)` means applying the function F to x exactly n times.

It does not mean raising F to the power n.

For example:

- `F^0(x) = x`
- `F^1(x) = F(x)`
- `F^2(x) = F(F(x))`
- `F^3(x) = F(F(F(x)))`

## 3. TIRARIT Notation

The main definition is:

`TIRARIT(n) = (TREE ∘ R)^n(TREE(3))`

This means that the composition of TREE and R is applied n times, starting from TREE(3).

Examples:

- `TIRARIT(0) = TREE(3)`
- `TIRARIT(1) = TREE(R(TREE(3)))`
- `TIRARIT(2) = TREE(R(TREE(R(TREE(3)))))`

## 4. Comparison Symbols

| Symbol | Meaning |
|---|---|
| `=` | Equal to |
| `>` | Greater than |
| `<` | Less than |
| `≥` | Greater than or equal to |
| `≤` | Less than or equal to |
| `∘` | Function composition |
| `^n` | Repeated function composition when applied to a function in this construction |
| `→` | Maps to or leads to |

## 5. Important Conventions

- All inputs to R and TREE are natural numbers.
- The TREE function refers to the standard mathematical TREE function.
- R is the generalized Rayo function defined in `mathematical-definition.md`.
- Under the adopted formal language, semantics, and symbol-counting convention, R(G) represents Rayo's Number when the symbol limit is strictly fewer than G symbols.
- Function iteration is not ordinary exponentiation.
- All TIRARIT values are finite natural numbers.
