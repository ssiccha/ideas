# Normalizer
## Matrix groups
- how to backtrack over matrix groups?

## Construction of normaliser of socle for PA type in LV NLTime?
- constructive recognition of simple groups in LV NLTime possible, see
  references.md

## Normalisers
- from Luks and Miyazaki, Normalisers in Poly Time for restricted comp factors
    normalizer problem even for permutation groups naturally leads to instances
    of finding stabilizers of subspaces in certain matrix groups

## How useful is Colva's backtrack in practice?
- try to incorporate it into partition backtrack, implement it in
  backtrack-kit
- if non-abelian socle cases are very efficient: can it improve the abelian
  socle case?

# Permutation Groups
- diagonal structures: find categorical description of projective structure

## Twisted wreath
From mail from Colva:
> There is a paper by Tim Burness on base size where he talks about the
> twisted wreath product groups, and describes the embedding
into compound diagonal groups.

If I find small permutation reps of TW groups, maybe I can do some experiments
and see whether the normalizer behaves nicely.

# Diss improvements
- use natural transformation in Lemma 5.1.4
(\label{lem:pa-product-dec-of-soc})
- unify lemmas 8.2.15 ff
  \label{lem:gen-set-normsoc-SD}
- in section WCF for diagonal:
  - come up with better naming convention for indices. What do I use d for
    usually? Can I take r = l - 1?
- writing style:
  - let x be a X, let y be a Y, let z be a Z -> let x be a X, y a Y, and z a Z

- make a proper definition of socle-component which refers to the other
  defs. define "a socle component" if G is not in WCF.
- Turn this into an actual lemma: Let $G \leq \Sym \Omega$ be a permutation
  group and $f : \Omega \to \Delta$ a surjective map compatible with $G$.
  Then there exist a unique group $H \leq \Sym \Delta$
  and a unique group homomorphism $\phi : G \to H$
  such that $F := (f, \phi)$ is a permutation epimorphism,
  see \cite[Corollary~4.2.7]{siccha:phd-thesis}.
  We call $F$ the \emph{permutation epimorphism}
  and $\phi$ the
  \emph{group epimorphism of $G$ induced by $f$}.




## Small perm reps of primitive groups
From diss:
```
Is this efficient? Can we use weak canonical form to speed up the non
computation?

Can I also do this without computing normalizer of soc $G$
or without computing $M$?
\\
- find isomorphism
  $\soc G$ to base group of imprimitive $T \wr S_\ell$
\\
A)
\\
- construct $M := N_{\sym \Delta}(T) \wr S_\ell$
  or $M := \aut T \wr S_\ell$.
\\
- set up isomorphism from normalizer of soc to $M$
\\
- map $G$
\\
B)
\\
- for every generator $x$ of $G$:
  find automorphism it induces on $\soc G$
    (maybe find permutation on $T_i$
    an then use projection);
  then find element of $M$
%
\\[2em]
- quicker way to determine how a $g$ in $G$
  acts on the minimal normal subgroups $T_i$
  per conjugation?
```
