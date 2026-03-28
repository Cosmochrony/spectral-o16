This repository contains the source of the **O16** Cosmochrony paper  
[*Fibre Admissibility and Exponent Doubling in the Exact Weil Regime:
Resolution of the δ-Deficit via Conjugate Pair Observables*](out/SpectralO16.pdf).

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

> identify the correct observable entering the growth law in the exact-block regime.


# Core Result

The paper shows that the correct observable is defined at the level of
**conjugate pairs of Weil blocks**, not individual blocks.

Defining the pair observable:
\[
\sigma_{\mathrm{pair}}(n) = \sigma_c(n)\,\sigma_{q-c}(n),
\]

the asymptotic scaling becomes:
\[
\sigma_{\mathrm{pair}}(n) \sim n^{-\delta_{\mathrm{pair}}},
\quad
\delta_{\mathrm{pair}} = 2\,\delta_c.
\]

Numerically:
\[
\delta_c \approx 3.7
\quad \Longrightarrow \quad
\delta_{\mathrm{pair}} \approx 7.4,
\]

which matches the **lower bound of the phenomenological range**.


# Main Structural Results

## 1. Symmetry of conjugate blocks

The paper proves that:

- the Weil representations satisfy
  $\rho_{q-c} = \overline{\rho_c}$
- the Gram–Schmidt dynamics is identical for $(c, q-c)$
- therefore:
  \[
  \delta_c = \delta_{q-c}
  \]

This is an exact structural result, independent of numerical fitting.


## 2. Observable redefinition

The key correction is:

> admissibility is defined on fibres of the projection Π, not on individual preimages.

This leads to the pair observable:
\[
R_n^{\mathrm{pair}} = \frac{1}{m_{\mathrm{pairs}}}
\sum_{c} \sigma_c(n)\,\sigma_{q-c}(n)
\]

This observable:

- restores a clean power law (R² > 0.9999)
- reduces slope variance by a factor ≈ 6
- yields the correct exponent scale


## 3. Resolution of the δ-deficit

The discrepancy identified in O12–O15:
\[
\hat\delta_{\mathrm{exact}} \approx 3.7 \ll 7.4
\]

is resolved as:

> a single-branch measurement of a two-branch structure.

The correct exponent is:
\[
\delta_{\mathrm{pair}} = 2\,\hat\delta_{\mathrm{exact}}
\]

No modification of the model or dynamics is required.


## 4. Spectral lower bound

The pair spectrum satisfies:
\[
\delta_{\mathrm{pair}} \ge \delta_{\min} \approx 7.4,
\]

with no observed values below this bound.

This establishes:

- a **structural lower bound** imposed by the Weil representation
- independent of numerical or dynamical effects


## 5. Status of the factor r(c,q)

The multiplicative ratio:
\[
r(c,q) = \frac{\sigma_{q-c}}{\sigma_c}
\]

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

The key identification is:

\[
\alpha_{\mathrm{dyn}} = \delta_{\mathrm{pair}}
\]

under the fibre-admissibility prescription.


# Interpretation of the Result

The central conceptual outcome is:

> the exact-block mismatch was not due to the growth law,
> but to an incomplete definition of the observable.

More precisely:

- O15: scalar observable invalid
- O16: correct observable = fibre-level (pair) observable

This shifts the issue from:

- a failure of dynamics  
  to
- a misidentification of admissibility


# Structural Role of O16

O16 completes the chain:

- **O12–O13**: exact block extraction and asymptotics
- **O14**: observable mismatch identified
- **O15**: scalar-to-block failure localised
- **O16**: correct observable identified (fibre level)

So O16 establishes:

- the issue is **not dynamic**
- the issue is **not spectral**
- the issue is **observational (definition of admissibility)**


# What O16 Adds

- identification of the **pair observable**
- proof of **exponent doubling**
- demonstration of a **spectral lower bound**
- elimination of aggregation-based explanations (via O15)
- clarification of the role of **normalisation factors**
- restoration of consistency with the phenomenological scale


# Outcome

O16 resolves the core S2 discrepancy at leading order.

The exact Weil-block framework:

- reproduces the correct exponent scale
- requires no modification of O6–O7 at the structural level
- only requires a corrected observable


# Residual Open Problem

While the lower bound is now understood, the **upper bound**
of the phenomenological range remains open.

The pair spectrum extends beyond:
\[
\delta_{\mathrm{pair}} > 10.6
\]

but observed configurations satisfy:
\[
\delta_{\mathrm{pair}} \in [7.4, 10.6].
\]

The selection mechanism is not spectral.


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
   Establish conjugate pairing from first principles

4. **Extension to higher-rank structures**  
   Investigate multi-branch fibres beyond pairs

5. **Phenomenological mapping**  
   Relate positions within [7.4, 10.6] to particle hierarchy


# Status

The programme is now:

- free of derivational ambiguity (**O15**)
- equipped with the correct observable (**O16**)
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
