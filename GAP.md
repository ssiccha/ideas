# Things to improve in GAP
- Minimal normal subgroups
  - this is slow even for the socle of a PA type group
- TransposedMat should return matrix of same mutability
- `1 * CMat` is a lot slower than `One(..) * CMat`

# HPC-GAP
- compile task code?
- does the Boehm GC (is that HPC-GAP's GC?) try to hard not to allocate more
  memory?
- compute orbits or blocks in parallel?
- document 'task stop on error' global variable
