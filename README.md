This repository contains the source of the **O16** Cosmochrony paper
*Fibre Admissibility and Exact Pair-Exponent Doubling*.

**Version 1.1 — corrective revision.** This version withdraws the numerical baseline and the central
proposition of v1.0/v1.0.1, which were found to be unsourced and unreproducible respectively. What
survives is a conditional, purely algebraic remark about exponent doubling, plus the genuine
representation-theoretic conjugation identity it was built on. See **Correction (v1.1)** below.

This work extends the **spectral admissibility sub-programme** by proposing a fibre-level observable
in the exact Weil-block regime, defined on conjugate pairs $\{c, q-c\}$.


# Correction (v1.1)

The original draft (v1.0/v1.0.1) opened by asserting an established O-series baseline
$\hat\delta_{\mathrm{exact}} \approx 3.72 \pm 0.06$ and a corollary (O15's aggregation no-go) ruling
out any reweighting resolution. Neither claim can be traced to any source in the current, corrected
O12–O15 texts:

- the $3.72 \pm 0.06$ figure appears in no table of the current O12, O13, or O14 texts, nor in O15's
  per-prime column;
- O15's own corrective revision found the unconditional no-go **false as originally stated**, with an
  explicit counterexample, and replaced it with a narrower, conditional corollary that applies only to
  O15's specific dynamical weights and whose hypothesis is not verified at any tested prime.

Both are withdrawn.

The paper's central proposition (conjugate-pair sigma profiles differ by an integer factor
$r(c,q)\in\{1,2,3,4\}$, "confirmed to machine precision") identified its scalar observable $\sigma_c(n)$,
indexed by $c \in (\mathbb{Z}/q\mathbb{Z})^*$, with O12/O13's exact block observable
$\Sigma_n^{(c_1,c_2,c_3)}$, indexed by a generic triple. This identification was never established, and
the specific claim it supported would directly contradict O12's own proved exact fact,
Proposition "Exact rank formula": $\Sigma_n^{(c)} = \Sigma_n^{(-c)}$, if the two observables were the
same — which forces the conjugate-pair ratio to be identically $1$, not a variable integer. (This is
distinct from the inter-block variance ratio $V_n$ used elsewhere in the O-series, which carries no
per-block index and is not the quantity O12 proves invariant.) Independently of that identification,
this repository has
never carried code computing $\sigma_c(n)$ or $r(c,q)$: `code/` holds only the compiled figure, not a
generating script. The proposition is withdrawn on both grounds, along with the numerical table and
figure built on it (retained in the paper for provenance, explicitly marked as non-reproducible).

What remains, independent of any pipeline identification: the Weil representation obeys the exact
conjugation identity $\rho_{q-c} = \overline{\rho_c}$, and the elementary Cauchy–Schwarz inequality
$\langle\sigma_c^2\rangle \geq \langle\sigma_c\rangle^2$ holds for any non-negative sequence — the
opposite direction from what the original draft's "distinction from $\bar\sigma^2$" remark asserted.
On the real pipeline, where $r(c,q)\equiv1$, this gives $R_n^{\mathrm{pair}} \geq \bar\sigma(n)^2$, not
$\leq$. The exponent-doubling argument is restated as a conditional, purely algebraic remark (see
**Core Result** below), with no numerical value asserted.


# Core Result

*If* a per-block observable $\sigma_c(n)$ has a conjugate-pair ratio
$r(c,q) = \sigma_{q-c}(n)/\sigma_c(n)$ independent of the shell index $n$, *then* the pair-level product
$\sigma_{\mathrm{pair}}(n) = \sigma_c(n)\,\sigma_{q-c}(n)$ has log-log slope exactly double that of
$\sigma_c(n)$:
$\delta_{\mathrm{pair}} = 2\,\delta_c.$

This is a direct consequence of differentiating a product of two power laws with a constant ratio — not
a numerical discovery, and not asserted of any specific sourced observable in this revision.

Applied to the real O12/O13 pipeline, where the exact conjugate-block identity forces $r(c,q) \equiv 1$,
the pair observable reduces definitionally to $\sigma_c(n)^2$: there is no doubling phenomenon left to
explain, only a squared power law.

No value of $\delta_{\mathrm{pair}}$, and no O7 prescription for $\beta^*$, is asserted in this revision.


# What Is Established vs. What Is Open

**Established, unconditionally:**

- $\rho_{q-c} = \overline{\rho_c}$ — standard representation theory of the Weil representation.
- The elementary Cauchy–Schwarz bound $\langle\sigma_c^2\rangle \geq \langle\sigma_c\rangle^2$ on any
  non-negative sequence.
- The conditional doubling statement above, given its stated premise.

**Open — two independent questions, not one:**

- Whether the identification of conjugate pairs with the fibres of the projection $\Pi$ can be derived
  from first principles within Cosmochrony (already flagged as open in v1.0/v1.0.1).
- Whether *any* sourced, reproducible $\sigma_c(n)$ satisfies the doubling premise (an $n$-independent
  conjugate-pair ratio) at all — this question is *newly* open in v1.1, since the original draft's claim
  to this effect (Proposition on conjugate sigma-profile proportionality) is withdrawn.


# Numerical Content — Reclassified as Non-Reproducible

Table 1 and Figure 1 of the paper reproduce the original draft's numbers exactly, for provenance, and
are explicitly marked in-text as **not** established results in this revision. This repository has never
contained a script computing $\sigma_c(n)$, $r(c,q)$, or the reported fits; `code/` contains only the
compiled figure file. Regenerating this content would require an explicit, sourced definition of
$\sigma_c(n)$ that this paper does not supply.


# Downstream Propagation: O17–O21

The withdrawn baseline and the withdrawn proposition were cited, directly or through this paper, in
O17–O21. Their correctness does not follow automatically from this correction — each must be reassessed
on its own text — but any argument in that range relying on either withdrawn item without independent
support no longer has the support it cites here. O17's corrective revision is addressed as a separate,
standalone paper; O18–O21 are audited separately.


# Status

- Free of any withdrawn numerical claim (this revision).
- Equipped with a conditional, algebraically valid exponent-doubling remark, not yet tied to a sourced
  observable.
- The identification of conjugate pairs with fibres of $\Pi$ remains an open, structurally motivated
  hypothesis.

Remaining work:

- A sourced, reproducible definition of a per-block observable satisfying the doubling premise (or a
  demonstration that the real O12/O13 pipeline's own $\Sigma_n^{(c)}$, for which $r\equiv1$, is the
  right object to study at the pair level in the first place).
- Structural derivation of the fibre/conjugate-pair identification from $\Pi$.
- A native capacity-to-rate bridge, independent of and not addressed by this paper.


# Repository Structure

```text
paper/
├── out/      # Compiled O16 PDF
├── code/     # Original draft's figure (no generating script)
├── tex/      # LaTeX sources
└── README.md
```

# Citation

If you reference this work, please cite:

J. Beau, Fibre Admissibility and Exact Pair-Exponent Doubling,
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
