This repository contains the source of the **O16** Cosmochrony paper
*Fibre Admissibility Hypotheses and Conditional Pair-Exponent Doubling*.

This work extends the **spectral admissibility sub-programme** by proposing a fibre-level observable
in the exact Weil-block regime, defined on conjugate pairs $\{c, q-c\}$.


# Core Result

*If* a per-block observable $\sigma_c(n)$ has a conjugate-pair ratio
$r(c,q) = \sigma_{q-c}(n)/\sigma_c(n)$ independent of the shell index $n$, *then* the pair-level product
$\sigma_{\mathrm{pair}}(n) = \sigma_c(n)\,\sigma_{q-c}(n)$ has log-log slope exactly double that of
$\sigma_c(n)$:
$\delta_{\mathrm{pair}} = 2\,\delta_c.$

This is a direct consequence of differentiating a product of two power laws with a constant ratio — not
a numerical discovery, and not asserted of any specific sourced observable.

Applied to the real O12/O13 pipeline, where the exact conjugate-block identity forces $r(c,q) \equiv 1$,
the pair observable reduces definitionally to $\sigma_c(n)^2$: there is no doubling phenomenon left to
explain, only a squared power law.

No value of $\delta_{\mathrm{pair}}$, and no O7 prescription for $\beta^*$, is asserted.


# What Is Established vs. What Is Open

**Established, unconditionally:**

- $\rho_{q-c} = \overline{\rho_c}$ — standard representation theory of the Weil representation.
- The elementary Cauchy–Schwarz bound $\langle\sigma_c^2\rangle \geq \langle\sigma_c\rangle^2$ on any
  non-negative sequence.
- The conditional doubling statement above, given its stated premise.
- The exact conjugate-block identity of the real O12/O13 pipeline,
  $\Sigma_n^{(c_1,c_2,c_3)} = \Sigma_n^{(-c_1,-c_2,-c_3)}$, which forces $r(c,q)\equiv1$ there.

**Open — three independent premises, not one, and not to be blended together:**

- That $\Pi$ carries some parity involution at all ($\Pi(x)=\Pi(-x)$).
- That this specific involution is realised, in the Weil representation, as the character map
  $c\mapsto q-c$ — a separate, independent choice, not a consequence of the proved conjugation identity
  $\rho_{q-c}=\overline{\rho_c}$, which holds regardless of any involution on $\Pi$. Only given *both*
  this and the previous premise are conjugate pairs the fibres of $\Pi$.
- Whether *any* sourced, reproducible $\sigma_c(n)$ satisfies the doubling premise (an $n$-independent
  conjugate-pair ratio) at all, for a nontrivial pair-level observable distinct from the block squared.


# Downstream Propagation: O17–O21

O16's fibre-level proposal and its two open premises are cited, directly or through O17, in O18–O21.
Their correctness does not follow automatically from this paper — each must be reassessed on its own
text. O17 develops the raw-dynamics question independently, within its own scalar toy model; O18–O21
are audited separately.


# Status

- The identification of conjugate pairs with fibres of $\Pi$ remains open, and rests on two independent,
  structurally motivated premises (that $\Pi$ carries a parity involution, and that this involution is
  realised as $c\mapsto q-c$), neither implied by the other or by the proved conjugation identity.
- The exponent-doubling remark is conditional and algebraically valid, not yet tied to a sourced
  observable other than the real pipeline's own $\Sigma_n^{(c)}$ (for which it holds trivially, since
  $r\equiv1$ there).

Remaining work:

- A sourced, reproducible definition of a per-block observable, distinct from the pipeline's own block
  squared, that satisfies the doubling premise.
- Structural derivation of the fibre/conjugate-pair identification from $\Pi$.
- A native capacity-to-rate bridge, independent of and not addressed by this paper.


# Version History

- **v1.0 / v1.0.1** — initial release. Asserted a finite-window baseline
  $\hat\delta_{\mathrm{exact}} \approx 3.72 \pm 0.06$ and a numeric conjugate-pair ratio
  $r(c,q)\in\{1,2,3,4\}$, both since found unsourced or unreproducible.
- **v1.1** — corrective revision. Withdrew the baseline and the numeric-ratio proposition (the latter
  would have contradicted O12's proved exact identity $\Sigma_n^{(c)}=\Sigma_n^{(-c)}$, had the two
  observables been the same, an identification never established). Replaced the central claim with the
  conditional, purely algebraic doubling remark above, corrected a backwards Cauchy–Schwarz direction,
  and separated the fibre identification into two independent hypotheses. The withdrawn numerical table
  and figure were retained in the PDF body for provenance, explicitly marked non-reproducible.
- **v1.2** — the PDF body was rewritten to state only the current, established content natively, with no
  narrative of what was withdrawn or corrected; that history is preserved here and in this paper's
  Zenodo record notes instead. The non-reproducible table and figure from v1.1 were dropped from the PDF
  (no current-true content remained to present); `code/` still holds the original compiled figure file
  for reference. No mathematical content changed between v1.1 and v1.2.


# Repository Structure

```text
paper/
├── out/      # Compiled O16 PDF
├── code/     # Superseded figure from v1.0/v1.0.1 (no generating script; not cited in v1.2's PDF)
├── tex/      # LaTeX sources
└── README.md
```

# Citation

If you reference this work, please cite:

J. Beau, Fibre Admissibility Hypotheses and Conditional Pair-Exponent Doubling,
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
- a sourced definition of the per-block observable $\sigma_c(n)$
- the capacity-to-rate bridge

are welcome.

Please open an issue to discuss conceptual points,
technical details, or possible extensions.
