# Erdős Problems #521 and #522


This folder contains two short papers on the random Littlewood (Rademacher Kac) polynomial
$$
f_n(z) = \sum_{k=0}^{n} \varepsilon_k z^k, \qquad \varepsilon_k \in \{-1, +1\},
$$
addressing two Erdős problems:

- **Erdős Problem #521** — [erdosproblems.com/521](https://www.erdosproblems.com/521): does the real-zero count $R_n$ satisfy $R_n / \log n \to 2/\pi$ almost surely?
- **Erdős Problem #522** — [erdosproblems.com/522]( https://www.erdosproblems.com/522): does the unit-disk zero count $R_n$ satisfy $R_n / (n/2) \to 1$ almost surely?

Claimed solutions to both problems were previously posted in the `erdosproblems website`'s problem threads (in April, 2026). The papers here arrive at the conclusions independently and via **different routes** and **stronger results**.

## `Erdos_521_final.pdf` — A cone-event obstruction (#521)

We refute the almost-sure form of #521 for Rademacher coefficients. Concretely, combining
1. an elementary **cone-event** (two simultaneous random-walk positivity
   conditions on the reversed coefficient sequence) that forces all zeros to
   stay inside $[-1,1]$,
2. a Lévy zero–one boost of a quantitative quadrant-survival estimate to the
   almost-sure statement $\{O_n = 0 \text{ infinitely often}\} = 1$, and
3. Do's strong law $I_n / \log n \to 1/\pi$ a.s. plus reversal symmetry,

we show
$$
\liminf_{n\to\infty} \tfrac{R_n}{\log n} = \tfrac{1}{\pi}, \qquad
\limsup_{n\to\infty} \tfrac{R_n}{\log n} \ge \tfrac{2}{\pi} \quad \text{a.s.}
$$
so $R_n / \log n$ does **not** converge almost surely. In particular, the
almost-sure version of #521 is false for $\pm 1$ coefficients. This differs
from claimed paths in the comment thread, which aim to confirm the $2/\pi$
limit.

## `Erdos_522_final.pdf` — A fourth-moment route to #522

We confirm #522 with a quantitative rate. Yakir (2021) had already established
convergence in probability $R_n/(n/2) \to 1$, and a claimed almost-sure
solution appears in the comments on the problem page. Our proof goes through
a different mechanism: a uniform **fourth-moment concentration estimate** for
the normalized logarithmic average
$$
L_n(r) = \int_{\mathbb T} \log|Z_r(\theta)| \, d\mu(\theta)
$$
on a thin annulus around the unit circle. The key ingredients are
- occupation-measure / small-ball bounds for $|P_n(re^{i\theta})|$ via a
  fixed-dimensional Rademacher anti-concentration lemma,
- a smoothing $F_\alpha$ at scale $\alpha = (\log n)^B n^{-1/2}$ controlled
  with **Pisier's inequality** on the discrete cube,
- removal of the smoothing using the **Nazarov–Nishry–Sodin** logarithmic
  integrability theorem, and
- Jensen's formula at three nearby radii combined with a Borel–Cantelli step.

This yields a quantitative almost-sure version
$$
R_n = \frac{n}{2} + O \left( n^{7/8+\delta} \right) \quad \text{a.s. for every } \delta>0,
$$
and in particular $R_n/(n/2) \to 1$ almost surely, providing an alternative
and quantitative route to #522 distinct from the approach circulated in the
problem's comments.

## Use of AI Tools

Portions of both papers were developed with the assistance of ChatGPT-5.5-Pro. It was used to help explore ideas, generate preliminary drafts, and refine exposition. All mathematical arguments, results, and conclusions have been carefully reviewed and verified by the author, who takes full responsibility for the content of the paper. Any limitations or errors remain solely the responsibility of the author.

## References
1. https://www.erdosproblems.com/521
2. https://www.erdosproblems.com/522