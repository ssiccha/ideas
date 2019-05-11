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
