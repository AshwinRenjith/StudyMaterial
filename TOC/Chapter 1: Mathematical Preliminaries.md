# 📘 Chapter 1: Mathematical Preliminaries

<div align="center">
<h3>Theory of Computation: A Comprehensive Guide</h3>
<p><em>Document Version: 1.0.0 | Last Updated: 2025-07-18 12:41:12 UTC</em></p>
<p><em>Author: AshwinRenjith</em></p>
</div>

---

## 🎯 Chapter Overview

Welcome to the first chapter of our journey through the Theory of Computation! Before diving into automata, languages, and computability, we need to establish a solid mathematical foundation. This chapter introduces the key mathematical concepts that will serve as building blocks throughout this course.

Don't worry if you're new to these topics—we've designed this chapter to be accessible for second-year computer engineering students with minimal mathematical background. We'll build concepts from the ground up with plenty of examples and intuitive explanations.

---

## 1.1 Set Theory and Relations

### 📌 1.1.1 What is a Set?

A set is simply a collection of distinct objects. Think of it as a container that either has or doesn't have certain elements—there are no duplicates and no order.

**Examples:**
- The set of all vowels in the English alphabet: {a, e, i, o, u}
- The set of even numbers less than 10: {2, 4, 6, 8}
- The empty set (containing no elements): { } or ∅

We typically denote sets with capital letters (A, B, C) and use curly braces { } to list their elements.

### 📌 1.1.2 Set Notation

There are two main ways to describe sets:

1. **Roster notation**: Listing all elements inside braces
   - Example: A = {1, 2, 3, 4, 5}

2. **Set-builder notation**: Describing elements using a property
   - Example: B = {x | x is an integer and 0 < x < 6}
   - Read as "B is the set of all x such that x is an integer and 0 < x < 6"

We also use these symbols to indicate set membership:
- x ∈ A means "x is an element of set A"
- x ∉ A means "x is not an element of set A"

### 📌 1.1.3 Types of Sets

- **Finite sets**: Sets with a countable number of elements
  - Example: {1, 2, 3, 4, 5}

- **Infinite sets**: Sets with unlimited elements
  - Example: The set of all integers ℤ = {..., -2, -1, 0, 1, 2, ...}

- **Common number sets**:
  - Natural numbers: ℕ = {1, 2, 3, ...}
  - Whole numbers: W = {0, 1, 2, 3, ...}
  - Integers: ℤ = {..., -2, -1, 0, 1, 2, ...}
  - Rational numbers: ℚ = {p/q | p, q ∈ ℤ, q ≠ 0}
  - Real numbers: ℝ (all points on the number line)

### 📌 1.1.4 Set Operations

Sets can be combined and compared in various ways:

1. **Union (∪)**: Elements in either set
   - A ∪ B = {x | x ∈ A OR x ∈ B}
   - Example: {1, 2, 3} ∪ {3, 4, 5} = {1, 2, 3, 4, 5}

2. **Intersection (∩)**: Elements common to both sets
   - A ∩ B = {x | x ∈ A AND x ∈ B}
   - Example: {1, 2, 3} ∩ {3, 4, 5} = {3}

3. **Difference (-)**: Elements in one set but not the other
   - A - B = {x | x ∈ A AND x ∉ B}
   - Example: {1, 2, 3} - {3, 4, 5} = {1, 2}

4. **Complement (A')**: Elements not in the set (relative to a universe U)
   - A' = {x | x ∈ U AND x ∉ A}
   - Example: If U = {1, 2, 3, 4, 5} and A = {1, 3, 5}, then A' = {2, 4}

5. **Symmetric Difference (△)**: Elements in either set but not in both
   - A △ B = (A - B) ∪ (B - A)
   - Example: {1, 2, 3} △ {3, 4, 5} = {1, 2, 4, 5}

### 📌 1.1.5 Set Properties

Some important properties of sets include:

1. **Subset (⊆)**: Every element of A is also in B
   - A ⊆ B means ∀x(x ∈ A → x ∈ B)
   - Example: {1, 2} ⊆ {1, 2, 3}

2. **Proper subset (⊂)**: A is a subset of B, but A ≠ B
   - Example: {1, 2} ⊂ {1, 2, 3}

3. **Equality (=)**: Sets with exactly the same elements
   - A = B means A ⊆ B and B ⊆ A
   - Example: {1, 2, 3} = {3, 1, 2} (order doesn't matter!)

4. **Power set (P(A))**: Set of all possible subsets of A
   - Example: If A = {1, 2}, then P(A) = {∅, {1}, {2}, {1, 2}}
   - A set with n elements has 2^n subsets

### 📌 1.1.6 Set Identities (Laws)

These laws help manipulate set expressions:

1. **Commutative laws**:
   - A ∪ B = B ∪ A
   - A ∩ B = B ∩ A

2. **Associative laws**:
   - (A ∪ B) ∪ C = A ∪ (B ∪ C)
   - (A ∩ B) ∩ C = A ∩ (B ∩ C)

3. **Distributive laws**:
   - A ∩ (B ∪ C) = (A ∩ B) ∪ (A ∩ C)
   - A ∪ (B ∩ C) = (A ∪ B) ∩ (A ∪ C)

4. **De Morgan's laws**:
   - (A ∪ B)' = A' ∩ B'
   - (A ∩ B)' = A' ∪ B'

### 📌 1.1.7 Cartesian Product

The Cartesian product of sets A and B is the set of all ordered pairs (a, b) where a ∈ A and b ∈ B.

- A × B = {(a, b) | a ∈ A and b ∈ B}
- Example: If A = {1, 2} and B = {x, y}, then A × B = {(1, x), (1, y), (2, x), (2, y)}

This concept is crucial for understanding relations, which we'll cover next.

### 📌 1.1.8 Relations

A relation R from set A to set B is a subset of the Cartesian product A × B. In other words, it's a collection of ordered pairs (a, b) where a ∈ A and b ∈ B.

**Example**:
- Let A = {1, 2, 3} and B = {x, y}
- A possible relation R = {(1, x), (2, y), (3, y)} ⊆ A × B
- This relation could represent "maps to" or any other relationship between elements

If A = B, then R is a relation on set A.

### 📌 1.1.9 Properties of Relations

For a relation R on a set A:

1. **Reflexive**: Every element relates to itself
   - ∀a ∈ A, (a, a) ∈ R
   - Example: "is equal to" (=) is reflexive

2. **Symmetric**: If a relates to b, then b relates to a
   - ∀a, b ∈ A, if (a, b) ∈ R, then (b, a) ∈ R
   - Example: "is a sibling of" is symmetric

3. **Antisymmetric**: If a relates to b and b relates to a, then a = b
   - ∀a, b ∈ A, if (a, b) ∈ R and (b, a) ∈ R, then a = b
   - Example: "less than or equal to" (≤) is antisymmetric

4. **Transitive**: If a relates to b and b relates to c, then a relates to c
   - ∀a, b, c ∈ A, if (a, b) ∈ R and (b, c) ∈ R, then (a, c) ∈ R
   - Example: "is greater than" (>) is transitive

### 📌 1.1.10 Equivalence Relations

A relation R on set A is an equivalence relation if it is reflexive, symmetric, and transitive.

**Example**: "has the same birthday as" is an equivalence relation because:
- Everyone has the same birthday as themselves (reflexive)
- If Alice has the same birthday as Bob, then Bob has the same birthday as Alice (symmetric)
- If Alice has the same birthday as Bob and Bob has the same birthday as Charlie, then Alice has the same birthday as Charlie (transitive)

Equivalence relations partition a set into **equivalence classes**—disjoint subsets where all elements are related to each other.

### 📌 1.1.11 Partial and Total Orders

A relation R on set A is a:

1. **Partial order** if it is reflexive, antisymmetric, and transitive
   - Example: "is a subset of" (⊆) is a partial order on the power set of any set

2. **Total order** if it is a partial order and any two elements are comparable
   - ∀a, b ∈ A, either (a, b) ∈ R or (b, a) ∈ R
   - Example: "less than or equal to" (≤) on the set of real numbers

Understanding relations is crucial for many computational concepts, including state transitions in automata.

---

## 1.2 Functions and Cardinality

### 📌 1.2.1 Functions

A function f from set A to set B (written f: A → B) is a relation that associates each element in A with exactly one element in B.

**Key properties**:
- Every element in A must be mapped to some element in B (total function)
- Each element in A maps to exactly one element in B (well-defined)

We write:
- f(a) = b to indicate that a maps to b
- Domain of f = A (the input set)
- Codomain of f = B (the potential output set)
- Range of f = {f(a) | a ∈ A} (the actual outputs, a subset of B)

### 📌 1.2.2 Types of Functions

1. **Injective (One-to-One)**:
   - Different inputs map to different outputs
   - ∀a, b ∈ A, if a ≠ b, then f(a) ≠ f(b)
   - Example: f(x) = 2x from ℤ to ℤ

2. **Surjective (Onto)**:
   - Every element in B is mapped to by some element in A
   - ∀b ∈ B, ∃a ∈ A such that f(a) = b
   - Example: f(x) = x² from ℝ to [0, ∞)

3. **Bijective (One-to-One and Onto)**:
   - A function that is both injective and surjective
   - Creates a perfect pairing between elements of A and B
   - Example: f(x) = x + 3 from ℝ to ℝ

Bijections are particularly important because they establish that two sets have the same "size" or cardinality.

### 📌 1.2.3 Function Composition

Given functions f: A → B and g: B → C, the composition g ∘ f: A → C is defined as:

(g ∘ f)(a) = g(f(a)) for all a ∈ A

This means: apply f first, then apply g to the result.

**Example**:
- Let f(x) = x + 1 and g(x) = x²
- Then (g ∘ f)(x) = g(f(x)) = g(x + 1) = (x + 1)²
- And (f ∘ g)(x) = f(g(x)) = f(x²) = x² + 1

Note that function composition is generally not commutative: g ∘ f ≠ f ∘ g

### 📌 1.2.4 Inverse Functions

A function f: A → B has an inverse function f⁻¹: B → A if and only if f is bijective.

The inverse function "undoes" what f does:
- f⁻¹(f(a)) = a for all a ∈ A
- f(f⁻¹(b)) = b for all b ∈ B

**Example**:
- If f(x) = 3x + 1, then f⁻¹(x) = (x - 1)/3
- Verify: f⁻¹(f(2)) = f⁻¹(7) = 2 ✓

### 📌 1.2.5 Understanding Cardinality

Cardinality refers to the size or number of elements in a set.

1. **Finite sets**: Cardinality is simply the count of elements
   - |{a, b, c}| = 3

2. **Infinite sets**: More complex concept based on bijections

Two sets A and B have the same cardinality if there exists a bijection f: A → B.

### 📌 1.2.6 Countable and Uncountable Sets

1. **Countable sets**:
   - Can be put in a one-to-one correspondence with the natural numbers (ℕ) or a subset of ℕ
   - Examples: ℕ, ℤ, ℚ (rational numbers)
   - All finite sets are countable

2. **Uncountable sets**:
   - Cannot be put in a one-to-one correspondence with ℕ
   - Example: ℝ (real numbers), proven by Cantor's diagonal argument

This distinction is fundamental in computability theory, as computers can only process countable sets.

### 📌 1.2.7 Cantor's Diagonal Argument

This famous proof shows that the set of real numbers is uncountable:

1. Assume the real numbers between 0 and 1 could be listed: r₁, r₂, r₃, ...
2. Each real number has a decimal expansion (e.g., 0.12345...)
3. Construct a new number D where the nth digit differs from the nth digit of rₙ
4. D cannot be in the original list (it differs from each number in at least one position)
5. Therefore, the assumption that we could list all real numbers is false

This concept is crucial for understanding the limits of computation and the existence of non-computable functions.

---

## 1.3 Proof Techniques

### 📌 1.3.1 Introduction to Proofs

A mathematical proof is a rigorous argument that establishes the truth of a statement. Learning to construct and understand proofs is essential for computer science, especially for theoretical areas.

### 📌 1.3.2 Direct Proof

A direct proof proceeds straight from the hypothesis to the conclusion using logical steps.

**Example**: Prove that if n is an even integer, then n² is even.
- Proof: If n is even, then n = 2k for some integer k.
- Therefore, n² = (2k)² = 4k² = 2(2k²).
- Since 2k² is an integer, n² = 2(2k²) is even by definition.

### 📌 1.3.3 Proof by Contraposition

To prove "if P, then Q", we prove the contrapositive: "if not Q, then not P". This works because P → Q is logically equivalent to ¬Q → ¬P.

**Example**: Prove that if n² is odd, then n is odd.
- Contrapositive: If n is not odd (i.e., n is even), then n² is not odd (i.e., n² is even).
- If n is even, n = 2k for some integer k.
- Then n² = 4k², which is even.
- Thus, the contrapositive is true, so the original statement is true.

### 📌 1.3.4 Proof by Contradiction

We assume the statement is false and show that this assumption leads to a logical contradiction, thereby proving the statement must be true.

**Example**: Prove that √2 is irrational.
- Assume √2 is rational, so √2 = a/b where a and b are integers with no common factors.
- Then 2 = a²/b², which means a² = 2b².
- This implies a² is even, so a is even (a = 2c for some integer c).
- Substituting: 2b² = (2c)² = 4c², thus b² = 2c².
- This implies b is also even.
- But then a and b have 2 as a common factor, contradicting our assumption.
- Therefore, √2 cannot be rational.

### 📌 1.3.5 Proof by Cases

We break the problem into several cases and prove each case separately.

**Example**: Prove that |xy| = |x|·|y| for all real numbers x and y.
- Case 1: x ≥ 0, y ≥ 0. Then |xy| = xy = |x|·|y|.
- Case 2: x ≥ 0, y < 0. Then |xy| = |x·(-y)| = x·(-y) = |x|·|y|.
- Case 3: x < 0, y ≥ 0. Then |xy| = |(-x)·y| = (-x)·y = |x|·|y|.
- Case 4: x < 0, y < 0. Then |xy| = |(-x)·(-y)| = (-x)·(-y) = xy = |x|·|y|.
- Since the property holds in all cases, the proof is complete.

### 📌 1.3.6 Proof by Induction

Mathematical induction is used to prove that a statement P(n) is true for all natural numbers n.

Steps:
1. Base case: Prove P(1) is true.
2. Inductive step: Assume P(k) is true for some k, then prove P(k+1) is true.

**Example**: Prove that 1 + 2 + 3 + ... + n = n(n+1)/2 for all n ≥ 1.
- Base case: For n = 1, we have 1 = 1(1+1)/2 = 1. ✓
- Inductive hypothesis: Assume 1 + 2 + ... + k = k(k+1)/2 for some k ≥ 1.
- Inductive step: Need to prove 1 + 2 + ... + k + (k+1) = (k+1)(k+2)/2
  - (1 + 2 + ... + k) + (k+1) = k(k+1)/2 + (k+1)
  - = k(k+1)/2 + 2(k+1)/2
  - = (k+1)(k+2)/2 ✓
- By induction, the formula is true for all n ≥ 1.

### 📌 1.3.7 Strong Induction

Similar to regular induction, but we assume P(1), P(2), ..., P(k) are all true when proving P(k+1).

**Example**: Prove that any amount of postage of 12 cents or more can be formed using just 4-cent and 5-cent stamps.
- Base cases: Check for n = 12, 13, 14, 15:
  - 12 = 3×4, 13 = 2×4 + 5, 14 = 4 + 2×5, 15 = 3×5 ✓
- Inductive hypothesis: Assume the statement is true for all postages from 12 to k, where k ≥ 15.
- Inductive step: For postage k+1, remove one 4-cent stamp to get k-3 cents.
  - By the inductive hypothesis, k-3 ≥ 12 can be formed with 4- and 5-cent stamps.
  - Adding the 4-cent stamp back gives k+1 cents. ✓
- By strong induction, the statement is true for all n ≥ 12.

### 📌 1.3.8 Proof by Counterexample

To disprove a universal statement ("for all x, P(x)"), we find a single counterexample where P(x) is false.

**Example**: Disprove "All prime numbers are odd."
- Counterexample: 2 is a prime number, but 2 is even.
- A single counterexample is sufficient to disprove the statement.

---

## 1.4 Mathematical Induction

### 📌 1.4.1 The Principle of Mathematical Induction

Mathematical induction is a powerful technique for proving statements about natural numbers. We've already introduced it briefly, but let's explore it more thoroughly since it's so important in computer science.

The principle of mathematical induction states that if:
1. P(1) is true (base case), and
2. For any k ≥ 1, if P(k) is true, then P(k+1) is also true (inductive step)

Then P(n) is true for all natural numbers n.

Think of induction like knocking over a row of dominoes:
- You knock over the first domino (base case).
- Each domino knocks over the next one (inductive step).
- Therefore, all dominoes eventually fall.

### 📌 1.4.2 Application Examples

**Example 1**: Prove that 1 + 3 + 5 + ... + (2n-1) = n² for all n ≥ 1.

- Base case (n = 1): Left side = (2×1-1) = 1, Right side = 1² = 1 ✓
- Inductive hypothesis: Assume 1 + 3 + ... + (2k-1) = k² for some k ≥ 1
- Inductive step: Need to prove 1 + 3 + ... + (2k-1) + (2(k+1)-1) = (k+1)²
  - Left side = k² + (2k+1)
  - = k² + 2k + 1
  - = (k+1)² ✓
- Therefore, the formula holds for all n ≥ 1

**Example 2**: Prove that n! > 2ⁿ for all n ≥ 4.

- Base case (n = 4): 4! = 24 > 2⁴ = 16 ✓
- Inductive hypothesis: Assume k! > 2ᵏ for some k ≥ 4
- Inductive step: Need to prove (k+1)! > 2ᵏ⁺¹
  - (k+1)! = (k+1) × k!
  - > (k+1) × 2ᵏ (by inductive hypothesis)
  - > 2 × 2ᵏ (since k+1 > 2 for k ≥ 4)
  - = 2ᵏ⁺¹ ✓
- Therefore, n! > 2ⁿ for all n ≥ 4

### 📌 1.4.3 Common Induction Pitfalls

1. **Incorrect base case**: Make sure you start with the appropriate value (not always n = 1).
2. **Insufficient base cases**: Sometimes multiple base cases are needed, especially with recursion.
3. **Weak inductive hypothesis**: If you can't complete the inductive step, you might need to strengthen your hypothesis.
4. **Assuming what you need to prove**: Be careful not to use P(k+1) in proving P(k+1).

### 📌 1.4.4 Strong Induction Revisited

In strong induction, we assume P(1), P(2), ..., P(k) are all true when proving P(k+1), not just P(k).

This is particularly useful for problems where the next step depends on multiple previous steps, such as recurrence relations and divisibility proofs.

**Example**: Prove every integer n > 1 can be factored as a product of prime numbers.

- Base case (n = 2): 2 is already prime ✓
- Inductive hypothesis: Assume any integer m where 2 ≤ m ≤ k can be factored into primes
- Inductive step: Consider k+1
  - If k+1 is prime, we're done
  - If k+1 is not prime, then k+1 = a × b where 2 ≤ a, b ≤ k
  - By the inductive hypothesis, both a and b can be factored into primes
  - Therefore, k+1 can be factored into primes ✓
- By strong induction, every integer n > 1 can be factored as a product of prime numbers

### 📌 1.4.5 Structural Induction

Structural induction extends the induction principle to prove properties about recursively defined structures like trees, lists, and grammars.

For a recursively defined structure:
1. Prove P holds for all base structures
2. Prove that if P holds for the components of a composite structure, then P holds for the composite structure

**Example**: Prove that for any binary tree T, the number of leaf nodes = number of internal nodes + 1.

- Base case: A tree with just one node has 1 leaf and 0 internal nodes: 1 = 0 + 1 ✓
- Inductive step: Assume the property holds for trees T₁ and T₂
- Consider a tree T formed by joining T₁ and T₂ under a new root
  - Leaves in T = leaves in T₁ + leaves in T₂
  - Internal nodes in T = internal nodes in T₁ + internal nodes in T₂ + 1 (the new root)
  - By induction: leaves in T = (internal nodes in T₁ + 1) + (internal nodes in T₂ + 1)
  - = internal nodes in T₁ + internal nodes in T₂ + 2
  - = (internal nodes in T) + 1 ✓
- By structural induction, the property holds for all binary trees

---

## 1.5 Combinatorics and Counting

### 📌 1.5.1 Basic Counting Principles

Combinatorics deals with counting objects and arrangements. These principles are essential for analyzing algorithm efficiency and probability.

#### The Product Rule
If a task consists of k steps, where step i can be done in nᵢ ways, the entire task can be done in n₁ × n₂ × ... × nₖ ways.

**Example**: A password consists of 2 letters followed by 3 digits. How many possible passwords are there?
- Number of ways to choose 2 letters = 26² (26 choices for each position)
- Number of ways to choose 3 digits = 10³ (10 choices for each position)
- Total number of passwords = 26² × 10³ = 676 × 1,000 = 676,000

#### The Sum Rule
If a task can be done in either n₁ ways OR n₂ ways, and these ways are disjoint, then the task can be done in n₁ + n₂ ways.

**Example**: A club elects either a male or female president. There are 15 male and 12 female members. How many ways can they elect a president?
- Number of ways to elect a male president = 15
- Number of ways to elect a female president = 12
- Total number of ways = 15 + 12 = 27

### 📌 1.5.2 Permutations

A permutation is an ordered arrangement of distinct objects.

#### Permutations of n distinct objects
The number of ways to arrange n distinct objects in order is:
P(n,n) = n! = n × (n-1) × (n-2) × ... × 2 × 1

**Example**: How many ways can 5 students line up for a photo?
- P(5,5) = 5! = 5 × 4 × 3 × 2 × 1 = 120 ways

#### Permutations of r objects from n distinct objects
The number of ways to select and arrange r objects from a set of n distinct objects is:
P(n,r) = n! / (n-r)! = n × (n-1) × ... × (n-r+1)

**Example**: How many 3-character codes can be formed using the letters A through F with no repetition?
- P(6,3) = 6! / (6-3)! = 6! / 3! = 6 × 5 × 4 = 120 codes

### 📌 1.5.3 Combinations

A combination is a selection of objects where order doesn't matter.

The number of ways to select r objects from a set of n distinct objects (regardless of order) is:
C(n,r) = n! / (r! × (n-r)!) = P(n,r) / r!

Also denoted as (n choose r) or ⁿCᵣ.

**Example**: A committee of 3 people is formed from a group of 8. How many different committees are possible?
- C(8,3) = 8! / (3! × 5!) = 56 committees

#### Useful combination properties:
1. C(n,r) = C(n,n-r)
2. C(n,0) = C(n,n) = 1
3. C(n+1,r) = C(n,r) + C(n,r-1) (This generates Pascal's triangle)

### 📌 1.5.4 Binomial Theorem

The binomial theorem gives the expansion of (x + y)ⁿ:

(x + y)ⁿ = Σ(k=0 to n) C(n,k) × xⁿ⁻ᵏ × yᵏ

**Example**: Expand (x + 2)³
- (x + 2)³ = C(3,0)x³(2)⁰ + C(3,1)x²(2)¹ + C(3,2)x¹(2)² + C(3,3)x⁰(2)³
- = 1·x³·1 + 3·x²·2 + 3·x·4 + 1·1·8
- = x³ + 6x² + 12x + 8

### 📌 1.5.5 Inclusion-Exclusion Principle

To count elements in the union of sets while avoiding double-counting:
|A ∪ B| = |A| + |B| - |A ∩ B|

For three sets:
|A ∪ B ∪ C| = |A| + |B| + |C| - |A ∩ B| - |A ∩ C| - |B ∩ C| + |A ∩ B ∩ C|

**Example**: In a class of 50 students, 30 study math, 25 study physics, and 15 study both. How many students study at least one of these subjects?
- |Math ∪ Physics| = |Math| + |Physics| - |Math ∩ Physics|
- = 30 + 25 - 15
- = 40 students

### 📌 1.5.6 Pigeonhole Principle

If n+1 or more objects are placed into n boxes, then at least one box contains two or more objects.

Generalized: If N objects are placed into k boxes, then at least one box contains at least ⌈N/k⌉ objects.

**Example**: In a group of 13 people, at least 2 people were born in the same month.
- We have 13 people (pigeons) and 12 months (pigeonholes)
- By the pigeonhole principle, at least 2 people share a birth month

### 📌 1.5.7 Counting with Repetition

#### Permutations with repetition
If we have n positions and k types of objects, with unlimited supply of each type, the number of permutations is kⁿ.

**Example**: How many 4-digit numbers can be formed using the digits 0-9?
- First digit: 9 choices (1-9, can't start with 0)
- Each remaining digit: 10 choices (0-9)
- Total: 9 × 10 × 10 × 10 = 9,000 numbers

#### Permutations with indistinguishable objects
The number of distinct permutations of n objects, where n₁ are of type 1, n₂ are of type 2, etc., is:
n! / (n₁! × n₂! × ... × nₖ!)

**Example**: How many different arrangements of the letters in "MISSISSIPPI"?
- Total letters: 11
- M: 1, I: 4, S: 4, P: 2
- Number of arrangements = 11! / (1! × 4! × 4! × 2!) = 34,650

#### Combinations with repetition
The number of ways to select r objects from n types with repetition allowed is:
C(n+r-1, r)

**Example**: How many ways can you select 6 fruits from 4 types of fruits if repetition is allowed?
- C(4+6-1, 6) = C(9, 6) = 84 ways

---

## 1.6 Graph Theory Essentials

### 📌 1.6.1 Introduction to Graphs

A graph G = (V, E) consists of:
- V: a set of vertices (or nodes)
- E: a set of edges connecting pairs of vertices

Graphs model relationships between objects and are fundamental in computer science for representing networks, web pages, social connections, and computational problems.

### 📌 1.6.2 Types of Graphs

#### Undirected Graph
Edges have no direction; if (u,v) is an edge, then u and v are mutually connected.
- Example: Friendship networks (if Alice is friends with Bob, Bob is friends with Alice)

#### Directed Graph (Digraph)
Edges have direction; an edge (u,v) goes from u to v, but not necessarily from v to u.
- Example: Web pages (page A links to page B, but page B might not link to page A)

#### Simple Graph
A graph with no self-loops (edges connecting a vertex to itself) and no multiple edges between the same pair of vertices.

#### Multigraph
Allows multiple edges between the same pair of vertices.

#### Complete Graph
Every pair of distinct vertices is connected by a unique edge. A complete graph with n vertices has n(n-1)/2 edges and is denoted Kₙ.

#### Bipartite Graph
Vertices can be divided into two disjoint sets such that no edge connects vertices within the same set.
- Example: Students and courses, where edges represent enrollment

### 📌 1.6.3 Graph Terminology

#### Adjacent vertices
Two vertices connected by an edge.

#### Incident edge
An edge connected to a vertex.

#### Degree of a vertex
The number of edges incident to the vertex.
- In a directed graph, we distinguish between in-degree (incoming edges) and out-degree (outgoing edges).

#### Path
A sequence of vertices connected by edges, with no repeated edges.

#### Simple path
A path with no repeated vertices.

#### Cycle
A path that starts and ends at the same vertex.

#### Simple cycle
A cycle with no repeated vertices except the start/end.

#### Connected graph
There is a path between any two vertices.

#### Connected component
A maximal connected subgraph.

#### Tree
A connected graph with no cycles.

#### Forest
A graph with no cycles (a collection of trees).

### 📌 1.6.4 Graph Representation

#### Adjacency Matrix
An n×n matrix A where A[i,j] = 1 if there is an edge from vertex i to vertex j, and 0 otherwise.

Pros:
- O(1) time to check if an edge exists
- Good for dense graphs

Cons:
- O(n²) space regardless of the number of edges
- Inefficient for sparse graphs

#### Adjacency List
An array of lists, where each list contains the neighbors of a vertex.

Pros:
- Space-efficient for sparse graphs (O(|V| + |E|))
- Efficient iteration over neighbors

Cons:
- O(degree) time to check if an edge exists
- Less efficient for dense graphs

### 📌 1.6.5 Graph Traversals

#### Breadth-First Search (BFS)
Explores all neighbors at the current depth before moving to vertices at the next depth level.

Algorithm outline:
1. Start at a vertex s
2. Visit all neighbors of s
3. Visit all unvisited neighbors of those neighbors
4. Continue until all reachable vertices are visited

Uses a queue data structure and is good for finding shortest paths in unweighted graphs.

#### Depth-First Search (DFS)
Explores as far as possible along each branch before backtracking.

Algorithm outline:
1. Start at a vertex s
2. Visit an unvisited neighbor of s
3. Recursively apply DFS to that neighbor
4. Backtrack when no unvisited neighbors remain

Uses a stack (or recursion) and is good for topological sorting and finding connected components.

### 📌 1.6.6 Special Types of Graphs

#### Trees
A connected acyclic graph. Properties:
- |E| = |V| - 1
- Exactly one simple path between any two vertices
- Adding any edge creates a cycle
- Removing any edge disconnects the graph

#### Spanning Trees
A subgraph that is a tree and includes all vertices of the original graph.
- Minimum Spanning Tree (MST): A spanning tree with minimum total edge weight

#### Directed Acyclic Graph (DAG)
A directed graph with no cycles, essential for representing dependencies and task scheduling.
- Can be topologically sorted (vertices ordered so that all edges go from earlier to later vertices)

### 📌 1.6.7 Graph Problems in Computer Science

#### Shortest Path Problem
Find the shortest path between two vertices.
- Dijkstra's algorithm: For graphs with non-negative edge weights
- Bellman-Ford algorithm: Handles negative edge weights

#### Minimum Spanning Tree
Find a spanning tree with minimum total edge weight.
- Kruskal's algorithm
- Prim's algorithm

#### Graph Coloring
Assign colors to vertices so that no adjacent vertices have the same color.
- Chromatic number: Minimum number of colors needed

#### Connectivity
Determine if a graph is connected or find its connected components.

#### Eulerian Path and Circuit
A path that visits every edge exactly once.
- Eulerian circuit: Starts and ends at the same vertex
- Exists when all vertices have even degree

#### Hamiltonian Path and Circuit
A path that visits every vertex exactly once.
- Hamiltonian circuit: Starts and ends at the same vertex
- NP-complete problem (no efficient algorithm known)

Understanding graph theory is crucial for designing efficient algorithms and solving computational problems in networks, routing, scheduling, and many other areas.

---

## 1.7 Logic and Boolean Algebra

### 📌 1.7.1 Propositional Logic

Propositional logic deals with propositions (statements that are either true or false) and logical operations on them.

#### Basic components:
- **Propositions**: Simple declarative statements (e.g., "It is raining.")
- **Logical connectives**: Operators that combine propositions

#### Logical Operators:

1. **Negation (NOT, ¬p)**:
   - Reverses the truth value
   - "It is not raining"
   
   | p | ¬p |
   |---|-----|
   | T | F   |
   | F | T   |

2. **Conjunction (AND, p ∧ q)**:
   - True only when both statements are true
   - "It is raining AND it is cold"
   
   | p | q | p ∧ q |
   |---|---|-------|
   | T | T | T     |
   | T | F | F     |
   | F | T | F     |
   | F | F | F     |

3. **Disjunction (OR, p ∨ q)**:
   - True when at least one statement is true
   - "It is raining OR it is snowing"
   
   | p | q | p ∨ q |
   |---|---|-------|
   | T | T | T     |
   | T | F | T     |
   | F | T | T     |
   | F | F | F     |

4. **Implication (IF-THEN, p → q)**:
   - False only when p is true and q is false
   - "If it is raining, then the ground is wet"
   
   | p | q | p → q |
   |---|---|-------|
   | T | T | T     |
   | T | F | F     |
   | F | T | T     |
   | F | F | T     |

   Note: p → q is logically equivalent to ¬p ∨ q

5. **Biconditional (IF AND ONLY IF, p ↔ q)**:
   - True when p and q have the same truth value
   - "It rains if and only if the weather forecast predicts rain"
   
   | p | q | p ↔ q |
   |---|---|-------|
   | T | T | T     |
   | T | F | F     |
   | F | T | F     |
   | F | F | T     |

### 📌 1.7.2 Truth Tables and Logical Equivalence

A truth table shows all possible combinations of truth values for the variables in a logical expression.

Two logical expressions are equivalent if they have the same truth table.

**Example**: Show that p → q is equivalent to ¬p ∨ q.

| p | q | p → q | ¬p | ¬p ∨ q |
|---|---|-------|-----|--------|
| T | T | T     | F   | T      |
| T | F | F     | F   | F      |
| F | T | T     | T   | T      |
| F | F | T     | T   | T      |

Since the columns for p → q and ¬p ∨ q are identical, the expressions are equivalent.

### 📌 1.7.3 Important Logical Equivalences

1. **Double Negation**: ¬(¬p) ≡ p
2. **Commutative Laws**:
   - p ∧ q ≡ q ∧ p
   - p ∨ q ≡ q ∨ p
3. **Associative Laws**:
   - (p ∧ q) ∧ r ≡ p ∧ (q ∧ r)
   - (p ∨ q) ∨ r ≡ p ∨ (q ∨ r)
4. **Distributive Laws**:
   - p ∧ (q ∨ r) ≡ (p ∧ q) ∨ (p ∧ r)
   - p ∨ (q ∧ r) ≡ (p ∨ q) ∧ (p ∨ r)
5. **De Morgan's Laws**:
   - ¬(p ∧ q) ≡ ¬p ∨ ¬q
   - ¬(p ∨ q) ≡ ¬p ∧ ¬q
6. **Implication Law**: p → q ≡ ¬p ∨ q
7. **Contrapositive**: p → q ≡ ¬q → ¬p
8. **Biconditional**: p ↔ q ≡ (p → q) ∧ (q → p)

### 📌 1.7.4 Logical Inference and Rules

Logical inference allows us to derive new conclusions from known premises.

#### Common Rules of Inference:

1. **Modus Ponens**: From p and p → q, infer q
2. **Modus Tollens**: From ¬q and p → q, infer ¬p
3. **Hypothetical Syllogism**: From p → q and q → r, infer p → r
4. **Disjunctive Syllogism**: From p ∨ q and ¬p, infer q

**Example**: Given "If it rains, the picnic is canceled" and "It is raining," we can infer "The picnic is canceled" using Modus Ponens.

### 📌 1.7.5 Boolean Algebra

Boolean algebra is a mathematical system dealing with binary variables and logic operations.

#### Basic Operations:
- NOT (complement): x' or x̄
- AND (conjunction): x·y
- OR (disjunction): x+y

#### Basic Properties:
1. **Identity**:
   - x·1 = x
   - x+0 = x
2. **Null**:
   - x·0 = 0
   - x+1 = 1
3. **Idempotent**:
   - x·x = x
   - x+x = x
4. **Involution**: (x')' = x
5. **Complement**:
   - x·x' = 0
   - x+x' = 1

### 📌 1.7.6 Boolean Functions and Logic Gates

A Boolean function maps input Boolean variables to an output Boolean value.

#### Basic Logic Gates:
- **NOT gate**: Output is the negation of the input
- **AND gate**: Output is true only when all inputs are true
- **OR gate**: Output is true when at least one input is true
- **XOR gate**: Output is true when an odd number of inputs are true
- **NAND gate**: Negation of AND (Universal gate)
- **NOR gate**: Negation of OR (Universal gate)

Boolean functions can be represented using truth tables, logic gate diagrams, or Boolean expressions.

### 📌 1.7.7 Normal Forms

Boolean expressions can be standardized into normal forms:

#### Disjunctive Normal Form (DNF):
- OR of ANDs
- Sum of products
- Example: (x ∧ y) ∨ (¬x ∧ z)

#### Conjunctive Normal Form (CNF):
- AND of ORs
- Product of sums
- Example: (x ∨ y) ∧ (¬x ∨ z)

Every Boolean function can be represented in both DNF and CNF.

### 📌 1.7.8 Applications in Computer Science

1. **Circuit Design**: Boolean algebra is used to design and optimize digital circuits.
2. **Logic Programming**: Languages like Prolog use logical inference.
3. **Database Queries**: SQL queries use Boolean operations.
4. **Search Algorithms**: Boolean conditions guide search processes.
5. **Formal Verification**: Proving program correctness using logic.

Understanding logic and Boolean algebra is essential for computer science as they form the foundation of digital computing, from circuit design to algorithm development and formal reasoning.

---

## 🔄 Chapter Summary

In this chapter, we've built a solid mathematical foundation that will support our journey through the Theory of Computation:

1. **Set Theory and Relations**: We learned about sets as collections of elements and relations as connections between elements, providing a framework for understanding computational structures.

2. **Functions and Cardinality**: We explored functions as mappings between sets and cardinality as a measure of set size, crucial concepts for understanding computational mappings and limits.

3. **Proof Techniques**: We developed skills in constructing logical arguments through direct proofs, contradiction, contraposition, and induction—essential for proving properties of computational models.

4. **Mathematical Induction**: We mastered a powerful technique for proving statements about natural numbers, which will be invaluable for proving properties of recursive definitions and algorithms.

5. **Combinatorics and Counting**: We studied methods for counting arrangements and selections of objects, which help in analyzing algorithm complexity and possibilities.

6. **Graph Theory**: We explored graphs as representations of relationships, providing tools for modeling and solving problems involving networks and connections.

7. **Logic and Boolean Algebra**: We examined formal logical systems and operations, which form the foundation of digital computation and formal reasoning.

These mathematical tools will serve as our building blocks as we explore automata, formal languages, computability, and complexity in the chapters ahead. A strong grasp of these concepts will make the more abstract notions in computation theory much more accessible.

---

## 🧠 Practice Problems

1. Prove that the union of a countable number of countable sets is countable.

2. Show that if G is a simple graph with n vertices where each vertex has degree at least n/2, then G is connected.

3. Using mathematical induction, prove that n³ - n is divisible by 3 for all positive integers n.

4. Construct the truth table for (p → q) ∧ (q → r) → (p → r).

5. How many different 7-digit phone numbers are possible if the first digit cannot be 0 or 1?

6. Prove that any simple connected graph with n vertices has at least n-1 edges.

7. Find the number of different boolean functions of 3 variables.

8. Prove that the relation R on Z defined by aRb if a-b is divisible by 5 is an equivalence relation.

9. Convert the following Boolean expression to CNF: (a ∧ b) ∨ (¬a ∧ c).

10. Prove that in any group of 6 people, there are either 3 mutual friends or 3 mutual strangers (assuming friendship is symmetric).

---

## 📚 Further Reading

- Rosen, K.H. "Discrete Mathematics and Its Applications"
- Graham, R.L., Knuth, D.E., and Patashnik, O. "Concrete Mathematics"
- Velleman, D.J. "How to Prove It: A Structured Approach"
- Diestel, R. "Graph Theory"
- Grimaldi, R.P. "Discrete and Combinatorial Mathematics"
- Enderton, H.B. "A Mathematical Introduction to Logic"