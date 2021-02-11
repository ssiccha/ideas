# Nicer representation of primitive groups
- extend library
- compute nice representations of TW type groups, see TW.md
- compute with TW type groups.
  - construct examples where normalizer of TW type group becomes SD?

# Canonization of Primitive Groups
- I can 'constructively recognise' PA type primitive groups where I construct a
  permutation isomorphism.
  Can I do the same for all non-regular socle primitive groups?
- applications for "Normaliser", "Conjugacy of groups", "canonical image for
  conjugacy of groups"
  and more?
- do this in LV NLTime?
- can I also do canonization?

# Next steps
- How to efficiently compute intersection with large primitive groups?
- extend Primitive Group Library with help of CDs?
  Have a look at Theissen's PhD thesis, chapter 4,
  "Konstruktion primitiver Permutationsgruppen"
- canonical image of groups under conjugation: can CDs help for primitive
  groups?

# Parallelization of Recog
- do the large primitive group case
- can I use the old-hpcgap to check the guards?
- is it in principle possible to be able to encourage HPC-GAP to run
  recognition tasks concurrently? After all we don't want the only "applicable"
  recognition method to wait in the task list while all others are running.
