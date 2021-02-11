
# Cartesian Decompositions

- generalize CDs for simple diagonal type?
- compute a CD for PA type with a randomized algorithm?

- bijection between CDs and direct factorization of perm groups?
- Is there a bijection between CDs respected by a group in PA and block systems
  (BS) respected by its counterpart in imprimitive action?
- Orthogonal embedding => rename to ordered cartesian decomposition
- algorithm to compute CDs?

# Which algorithms could be implemented with my code?
## definitely possible
- given primitive PA type group. Find generators of a "top group"

## maybe possible
- given primitive PA type groups. make it easier to decide isomorphy and
  permutation isomorphy?
- Have constructive algorithms to do Cheryl and Csaba's theory with explicit
  examples?  Would this be helpful? Or is it sufficient for them to only look
  at "standard" examples?
- normalizers of imprimitive groups: leverage chapter 3 in cheryl and csaba's
  book? In which cases can we associate a block system to a transitive minimal
  normal subgroup?  Can compute all block systems. Can I connect the block
  systems to cartesian decompositions?  Cartesian decompositions correspond to
  minimal normal subgroups, right? Maybe that the normalizer can map two
  cartesian decompositions to each other is equivalent to conjugating the two
  minimal normal subgroups. Would this be helpful?  See Praeger and Schneider,
  p. 6

## CD + Randomised alg to compute socle of primitive groups (Seb. K.s B Thesis)
- If _n = d ^ l_, then orbits of MNSGs of socle must have length d!
  When generating elements of soc G with territory size 1 we can get
  elements with too big territory. These should then correspond to groups with
  orbits of length _d ^ |terr(x)|_.
- use some kind of graph datastructure for
    - connecting generated involutions if they do not commute
    - connecting points of _\Delta ^ \ell_ if they have identical _i_-th
      component?
- Use ideas for Sebastian's B.Th. + CDs to do a non-black-box probabilistic
  socle construction algorithm!
  Could this be an alternative for MC COMP SERIES algorithm by Seress?
- for primitive groups potentially faster than computing derived groups? (see
  Cannon Holt)
- can we use this to improve composition series computation for primitive
  groups? Akos books says that diagonal cases are "hard" if there exist two
  minimal normal subgroups (MNSG) because need to compute centraliser of one
  MNSG to get the other one.

## Randomised computation of cartesian decompositions of any group

Compute cartesian decompositions randomized?
```
gap> m := 4; d := 2;
gap> W := WreathProductProductAction(SymmetricGroup(m), SymmetricGroup(d));; mSet := Combinations([1 .. m ^ d], m ^ (d - 1));;
gap> Set(List(mSet, set -> Collected(SortedList(List(W, x -> Size(Intersection(set, OnSets(set, x))))))));
```
For a set A of size `m ^ (d - 1)` we count the possible sizes of `A intersect A ^ g` for g in W.
A set of the form `omega_i = delta` has output `[ [ [ 0, 432 ], [ 1, 576 ], [ 4, 144 ] ] ]`.
The code above computes this for all such sets A. The output is:
```
[ [ [ 0, 296 ], [ 1, 608 ], [ 2, 208 ], [ 3, 32 ], [ 4, 8 ] ],
  [ [ 0, 300 ], [ 1, 600 ], [ 2, 216 ], [ 3, 24 ], [ 4, 12 ] ],
  [ [ 0, 304 ], [ 1, 576 ], [ 2, 256 ], [ 4, 16 ] ],
  [ [ 0, 316 ], [ 1, 560 ], [ 2, 240 ], [ 3, 32 ], [ 4, 4 ] ],
  [ [ 0, 318 ], [ 1, 548 ], [ 2, 256 ], [ 3, 28 ], [ 4, 2 ] ],
  [ [ 0, 352 ], [ 1, 512 ], [ 2, 256 ], [ 4, 32 ] ],
  [ [ 0, 364 ], [ 1, 480 ], [ 2, 256 ], [ 3, 48 ], [ 4, 4 ] ],
  [ [ 0, 380 ], [ 1, 456 ], [ 2, 256 ], [ 3, 56 ], [ 4, 4 ] ],
  [ [ 0, 432 ], [ 1, 384 ], [ 2, 288 ], [ 4, 48 ] ],
  [ [ 0, 432 ], [ 1, 576 ], [ 4, 144 ] ] ]
```
