# Classifying Lattice Structures
Hardcode version
This program uses both a machine learning algorithm (random forests) and hardcode to determine the structure of a
theoretical unit crystal by the location of intensity modes on a theoretical diffractogram (do I have the right term here?).
With this number of classes (7), random forests cannot untangle the overlapping conditions on a point-by-point basis, which
is to be expected, because many points fulfill more than 1 condition and humans could not do better. The hardcode considers
all points from one theoretical crystal at once and counts the number of different mod 2 or mod 3 combinations of the
(h,k,l) coordinates. The goal is to have random forests be able to consider points as a group as well - in other words we
want it to learn that, if certain combinations are absent or present, the unit cell could not be of certain lattice
structures.
