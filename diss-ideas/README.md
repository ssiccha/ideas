# Constructive Recognition of Primitive Groups
- I can constructively recognise PA type primitive groups where I construct a
  permutation isomorphism.
  Can I do the same for all non-regular socle primitive groups?
- applications for "Normaliser", "Conjugacy of groups", "canonical image for
  conjugacy of groups"
  and more?
- do this in LV NLTime?

# Construction of normaliser of socle for PA type in LV NLTime?
- constructive recognition of simple groups in LV NLTime possible, see
  references.md

# Cartesian Decompositions
- bijection between CDs and direct factorization of perm groups?
- Is there a bijection between CDs respected by a group in PA and block systems
  (BS) respected by its counterpart in imprimitive action?
- Orthogonal embedding => rename to ordered cartesian decomposition
- algorithm to compute CDs?

# Next steps
- How to efficiently compute intersection with large primitive groups?
- extend Primitive Group Library with help of CDs?
  Have a look at Theissen's PhD thesis, chapter 4,
  "Konstruktion primitiver Permutationsgruppen"
- canonical image of groups under conjugation: can CDs help for primitive
  groups?

# Normalisers
- from Luks and Miyazaki, Normalisers in Poly Time for restricted comp factors
    normalizer problem even for permutation groups naturally leads to instances
    of finding stabilizers of subspaces in certain matrix groups

# Parallelization of Recog
- do the large primitive group case
- can I use the old-hpcgap to check the guards?
- is it in principle possible to be able to encourage HPC-GAP to run
  recognition tasks concurrently? After all we don't want the only "applicable"
  recognition method to wait in the task list while all others are running.
# How useful is Colva's backtrack in practice?
- try to incorporate it into partition backtrack, implement it in
  backtrack-kit
- if non-abelian socle cases are very efficient: can it improve the abelian
  socle case?

# Which algorithms could be implemented with my code?
## definitely possible
- given primitive PA type group. Find generators of a "top group"

## maybe possible
- given primitive PA type groups. make it easier to decide isomorphy and
  permutation isomorphy?
- Have constructive algorithms to do Cheryl and Csaba's theory with explicit examples?
  Would this be helpful? Or is it sufficient for them to only look at "standard" examples?
- normalizers of imprimitive groups: leverage chapter 3 in cheryl and csaba's book? In which
  cases can we associate a block system to a transitive minimal normal subgroup?
  Can compute all block systems. Can I connect the block systems to cartesian decompositions?
  Cartesian decompositions correspond to minimal normal
  subgroups, right? Maybe that the normalizer can map two cartesian decompositions to each
  other is equivalent to conjugating the two minimal normal subgroups. Would this be helpful?
  See Praeger and Schneider, p. 6

