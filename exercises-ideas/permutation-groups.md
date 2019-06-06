# General
- solutions that argue "GAP says so" won't be accepted

# Solutions
- Solutions to the "Permutation Groups" lecture from SS19 can be found under
  https://github.com/lbfm-rwth/PermGrpsSS19/
- "String Isomorphism" und "Coset Intersection" polynomial-zeit äquivalent,
  siehe Luks' paper "Permutation groups and polynomial-time computation"

# O'Nan-Scott
- Is true: If $G$ is primitive, then $\soc G _ \alpha$ is maximal in $\soc G$.
  Find counter example (use GAP)?
- Let G = A_5 \times A_5. Classify all faithful primitive actions of this group.
  Hint: Each A_5 must act transitively.
  Hint 2: Look for maximal subgroups.
  Solution: There is only one (?), namely the simple diagonal action.
  Alternative: Let G = A_5 \wreath C_2. This way we remind the students that
  a wreath product is an abstract group.

# Properties of alternating and symmetric groups
- See Dixon Mortimer Chapter 8
- Determine Aut(S_5) and Aut(S_6)
- Show `Aut(S_n) \cong S_n` für n = 5 oder n >= 7
  https://groupprops.subwiki.org/wiki/Symmetric_groups_on_finite_sets_are_complete
- proportions of some element types? even order, n-cycles
- Let N subgroup in S_n of index 2. Must N then be the A_n?
- Let m \neq 6? Consider alternating group in action on k-subsets `A_{k,m}`.
  What is normaliser in the corresponding full symmetric group?
  Ideas:
  - Use `A_{k,m}` primitive with transitive socle. Then its normaliser is
    almost simple.
  - Elementary

# Misc
- Prove or counterexample: Let $G, H \leq S_n$ perm groups with $H \leq G$.
  Let $G$ have a generating set of size $d$. Then $H$ has a generating set of
  size $\leq d$.

#
- matrix group given. Using the permutation action on natural module is
  inefficient. Why?
  - Calculate size of base and basic orbits?
  - compare "basic operations"?
- anschauliche Erklärung für "small base implies big support"
