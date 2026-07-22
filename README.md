This repository contains the source of the **O16** Cosmochrony paper  
*Fibre Admissibility and Exact Pair-Exponent Doubling*.

**Version 1.0.1.** The exact conjugate-pair relation and exponent doubling are retained.
The numerical overlap with the capacity-to-rate target is convention-sensitive and is not a native
Heisenberg derivation of the cascade exponent.

This work extends the **spectral admissibility sub-programme** by resolving the
open problem left by **O15**:

> What is the correct dynamic observable in the exact Weil-block regime?


# Context

**O15** established that:

- the scalar growth law of **O6–O7** does not transfer to exact Weil blocks
- the block-mean observable
  $\bar\Sigma_n = \frac{1}{q-1}\sum_c \Sigma_n^{(c)}$
  is not the correct dynamic observable
- no aggregation or reweighting of blocks can recover the target range
  $\delta \in [7.4, 10.6]$

This left a single well-posed problem:

> identify a fibre-level observable in the exact-block regime and determine its exponent.


# Core Result

The paper constructs a proposed fibre-level observable from
**conjugate pairs of Weil blocks**, not individual blocks.

Defining the pair observable:
$\sigma_{\mathrm{pair}}(n) = \sigma_c(n)\,\sigma_{q-c}(n),$

the finite-window scaling is:
$\sigma_{\mathrm{pair}}(n) \sim n^{-\delta_{\mathrm{pair}}},
\quad
\delta_{\mathrm{pair}} = 2\,\delta_c.$

Numerically:
$\delta_c \approx 3.7
\quad \Longrightarrow \quad
\delta_{\mathrm{pair}} \approx 7.4,$

which meets the lower edge of the phenomenological comparison range under the production
$\log(n+1)$ convention.
On the same finite windows, conversion to $\log n$ gives approximately $6.6$--$6.9$, below that edge.


# Main Structural Results

## 1. Symmetry of conjugate blocks

The paper proves that:

- the Weil representations satisfy
  $\rho_{q-c} = \overline{\rho_c}$
- the Gram–Schmidt dynamics is identical for $(c, q-c)$
- therefore:
  $  \delta_c = \delta_{q-c}
  \]

This is an exact structural result, independent of numerical fitting.


## 2. Observable redefinition

The key correction is:

> admissibility is defined on fibres of the projection Π, not on individual preimages.

This leads to the pair observable:
$R_n^{\mathrm{pair}} = \frac{1}{m_{\mathrm{pairs}}}
\sum_{c} \sigma_c(n)\,\sigma_{q-c}(n)$

This observable:

- restores a clean power law (R² > 0.9999)
- reduces slope variance by a factor ≈ 6
- yields the exactly doubled pair exponent under the chosen fitting convention


## 3. Exact doubling and the apparent δ-deficit

The discrepancy identified in O12–O15:
$\hat\delta_{\mathrm{exact}} \approx 3.7 \ll 7.4$

is re-expressed at pair level as:

> a single-branch measurement of a two-branch structure.

The pair exponent is:
$\delta_{\mathrm{pair}} = 2\,\hat\delta_{\mathrm{exact}}$

No modification of the exact Weil-block computation is required.
This statement does not identify a native growth law carrying the pair observable.


## 4. Production-window comparison

The reported production-window values lie near $7.4$ under the $\log(n+1)$ convention.
They do not establish a structural lower bound: the estimator conversion to $\log n$ moves the same
finite-window values to approximately $6.6$--$6.9$.


## 5. Status of the factor r(c,q)

The multiplicative ratio:
$r(c,q) = \frac{\sigma_{q-c}}{\sigma_c}$

is shown to:

- arise from block-dependent normalisation in σ
- depend on parameters $(b_1, b_2)$
- not affect asymptotic exponents

Thus:

> r(c,q) is not a structural invariant of the representation.


# Observable Hierarchy (Updated)

O16 refines the hierarchy introduced in O15:

- \(\hat\delta_{\mathrm{exact}}\):  
  single-block exponent (branch-level)

- \(\delta_{\mathrm{pair}}\):  
  fibre-level exponent (physical observable)

- \(\alpha_{\mathrm{dyn}}\):  
  dynamic exponent entering the growth law

The cross-substrate prescription would identify:

$\alpha_{\mathrm{dyn}} = \delta_{\mathrm{pair}}$

under an additional hypothesis linking the O7 reduced-model growth variable to the Heisenberg pair observable.
No such native pair-capacity growth process is defined or derived in the frozen corpus.


# Interpretation of the Result

The central conceptual outcome is:

> conjugate Weil blocks define a cleaner fibre-level observable with an exactly doubled exponent.

More precisely:

- O15: scalar observable invalid
- O16: proposed fibre observable = conjugate-pair observable

This resolves the pair-observable construction.
It leaves the independent capacity-to-rate dynamics unresolved.


# Structural Role of O16

O16 extends the chain:

- **O12–O13**: exact block extraction and asymptotics
- **O14**: observable mismatch identified
- **O15**: scalar-to-block failure localised
- **O16**: conjugate-pair observable constructed at fibre level

So O16 establishes:

- the pair exponent is an exact consequence of conjugate-profile proportionality
- the fibre interpretation remains structurally motivated
- the pair exponent is not automatically the exponent of a native growth equation


# What O16 Adds

- identification of the **pair observable**
- proof of **exponent doubling**
- finite-window comparison with the phenomenological range
- elimination of aggregation-based explanations (via O15)
- clarification of the role of **normalisation factors**
- exact separation of the pair-exponent result from the capacity-to-rate prescription


# Outcome

O16 resolves the exact pair-exponent component of the S2 discrepancy.

The exact Weil-block framework:

- produces an exactly doubled pair exponent
- gives a convention-sensitive numerical overlap with the comparison range
- does not supply the O6--O7 growth carrier on the Heisenberg substrate


# Residual Open Problem

The asymptotic pair exponent and its relation to any native growth process remain open.
The finite-window values do not establish either endpoint of a structural admissible spectrum.


# Emerging Direction (O17)

Preliminary analysis indicates that the upper bound arises from:

- a **dynamical coherence constraint**
- defined on the full trajectory $\sigma(n)$
- not reducible to local or single-scale criteria

Admissibility likely requires:

- multi-scale regularity of relaxation
- absence of spikes or incoherent transitions
- sufficient persistence across BFS shells

This defines the next programme step.


# Open Directions

1. **Analytical characterization of trajectory coherence (O17)**  
   Derive a global criterion selecting admissible profiles

2. **Relation between δ and persistence length**  
   Connect exponent values to n_active and trajectory shape

3. **Derivation of fibre structure from Π**
   Establish conjugate pairing from first principles.

4. **Native capacity-to-rate bridge**
   Construct a growth process carrying the pair observable, or state an explicitly cross-substrate hypothesis.

5. **Extension to higher-rank structures**
   Investigate multi-branch fibres beyond pairs

6. **Phenomenological mapping**
   Relate positions within [7.4, 10.6] to particle hierarchy


# Status

The programme is now:

- free of derivational ambiguity (**O15**)
- equipped with the conjugate-pair observable (**O16**)
- consistent with phenomenological scales

Remaining work is:

- dynamical selection
- trajectory-level admissibility
- structural derivation of Π-fibres

# Repository Structure

```text
paper/
├── out/      # Compiled O16 PDF
├── tex/      # LaTeX sources
└── README.md
```
# Citation

If you reference this work, please cite:

J. Beau, Fibre Admissibility and Exponent Doubling in the Exact Weil Regime:
Resolution of the δ-Deficit via Conjugate Pair Observables,
Zenodo, 2026.

# Acknowledgements

Portions of the derivations, conceptual synthesis, numerical strategy,
and editorial refinement benefited from iterative interactions with
large language models used as analytical assistants.
All theoretical results, computations, and interpretations remain the
sole responsibility of the author.

# Contributions

This repository is intended as a research reference.

Critical feedback, independent verification, and further analysis of:

- fibre-level observables
- trajectory coherence criteria
- exact-block growth laws

are welcome.

Please open an issue to discuss conceptual points,
technical details, or possible extensions.
