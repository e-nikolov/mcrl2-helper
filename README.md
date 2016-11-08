# mcrl2-helper
A set of helper scripts used for the simplification of the verification steps in the mCRL2 tool-set.

./run model tool - Generates an LTS out of an mCRL2 specification and runs a specified visualisation tool on it.

./conv - Reduces the state space of an LTS by applying a divergence preserving branching bisimilarity using 
signature refinement reduction.

./runc - Performs ./run and subsequently a ./conv

./test formula lts - verifies a formula in the /modal_formulas folder against an LTS.

Notes:

1. The extensions must be skipped when specifying formulas and models (e.g. ./test req1 solar-car instead of ./test req1.mcf solar-car.mcrl2)

2. All modal formulas should be located in the /modal_formulas folder.

3. In all scripts, an argument can be skipped by not specifying it if it is the last argument or by using a "_" if it is not the last (e.g. ./test _ solar-car, ./test req1, ./test). Doing so will be equivalent to executing the script with the same value for the skipped arguments as their value in the previous execution of the script.
