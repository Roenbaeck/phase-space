Read [](file:///Users/lars/Documents/GitHub/phase-space/phase-space.tex#1-1), lines 1 to 100

Read [](file:///Users/lars/Documents/GitHub/phase-space/phase-space.tex#101-101), lines 101 to 300

Read [](file:///Users/lars/Documents/GitHub/phase-space/phase-space.tex#301-301), lines 301 to 500

Read [](file:///Users/lars/Documents/GitHub/phase-space/phase-space.tex#501-501), lines 501 to 700

Read [](file:///Users/lars/Documents/GitHub/phase-space/phase-space.tex#701-701), lines 701 to 900

Read [](file:///Users/lars/Documents/GitHub/phase-space/phase-space.tex#901-901), lines 901 to 1100

Read [](file:///Users/lars/Documents/GitHub/phase-space/phase-space.tex#1101-1101), lines 1101 to 1192

Created 6 todos

Here is my thorough review. I found several issues spanning mathematical errors, notation inconsistencies, prose/grammar, and LaTeX formatting.

---

## Critical Mathematical Errors

### 1. Spurious identity in Section 8 (Non-Gaussianity Witness)

At phase-space.tex, the display chain reads:

$$K_4^{\text{full}} = K_4^{\text{diag}} + 2\lambda c = 2K_4^{\text{full}} - K_4^{\text{diag}}$$

The second equality is **wrong**. $K_4^{\text{full}} = \lambda(a{+}b{+}2c)$ while $2K_4^{\text{full}} - K_4^{\text{diag}} = \lambda(a{+}b{+}4c)$. These differ by $2\lambda c$. The final implication $\lambda c = (K_4^{\text{full}} - K_4^{\text{diag}})/2$ is correct on its own — the middle term `= 2K_4^{full} - K_4^{diag}` should be deleted.

### 2. Wrong identity in Proposition 6.1

At phase-space.tex, the Proposition states:

$$3(a+b) - 2\sqrt{ab} = (\sqrt{a}+\sqrt{b})^2 + (\sqrt{a}-\sqrt{b})^2 + (a+b)$$

The **RHS evaluates to** $2(a+b) + (a+b) = 3(a+b)$, which is not equal to $3(a+b) - 2\sqrt{ab}$. The identity is off by $-2\sqrt{ab}$. The correct decomposition is, for example:

$$3(a+b) - 2\sqrt{ab} = (\sqrt{a} - \sqrt{b})^2 + 2(a + b)$$

Note: the *alternative* decomposition on the same line, $(\sqrt{3a}-\sqrt{b/3})^2 + 8b/3$, **is** correct, and so is the proof that follows in Proposition 6.1.

### 3. Kerr example: convention mismatch and arithmetic error

The Kerr section ([lines 1048–1068](phase-space.tex#L1048-L1068)) defines the quartic seam as:

$$s_4 = \tfrac{u^2{+}v^2}{2} + \lambda\bigl(a\,u^4 + b\,v^4 + c\,u^2v^2\bigr), \quad a=\tfrac14,\; b=\tfrac14,\; c=\tfrac12$$

This is a **different convention** from the general form $s_4 = \frac{u^2+v^2}{2} + \frac{\lambda}{4}(au^4 + bv^4 + 2cu^2v^2)$ used everywhere else. In the general convention, the isotropic Kerr case corresponds to $a=b=c=1$, giving:

$$\mathcal{W}_4 = \frac{\lambda(3+3+2)}{16} = \frac{\lambda}{2}$$

The paper claims $\mathcal{W}_4 = \lambda/8$, which is wrong by a factor of 4. Even plugging the Kerr-convention values directly into the formula gives $\lambda(3/4 + 3/4 + 1)/16 = 5\lambda/32 \neq \lambda/8$.

**Fix:** Either restate the Kerr coefficients in the general convention ($a=b=c=1$, $\mathcal{W}_4 = \lambda/2$), or adapt the formula to the local convention.

### 4. Kerr example: incorrect $\lambda$ identification

The paper states $\lambda = \beta\kappa$. Explicitly working through the scaling $u = x/\sigma_x$, $v = p/\sigma_p$ with $\sigma_x^2 = 1/(\beta m\omega^2)$, $\sigma_p^2 = m/\beta$, one finds:

$$p^2 + m^2\omega^2 x^2 = \frac{m}{\beta}(u^2+v^2)$$

so the quartic coefficient in scaled variables is $\kappa m^2/(4\beta)$, giving $\lambda = \kappa m^2/\beta$ (in the general convention), **not** $\lambda = \beta\kappa$. These agree only if $m = \beta$ in appropriate units.

### 5. Missing `+` sign in Kerr section

At phase-space.tex:

```tex
s_4=\tfrac{1}{2}(u^2+v^2)\tfrac{\lambda}{4}(u^2+v^2)^2
```

There is a **missing `+`** between the two terms.

---

## Notation / Consistency Issues

### 6. Abstract: single-mode vs. multi-mode mismatch

The abstract ([lines 38–43](phase-space.tex#L38-L43)) displays the seam in single-mode form ($x, p, \sigma_x, \sigma_p$) but then gives the volume as $\frac{\pi^d}{d!}\prod_i \sigma_{x_i}\sigma_{p_i}$, which is the multi-mode formula. Either display the multi-mode seam or give the single-mode volume ($\pi\sigma_x\sigma_p$ for $d=1$).

### 7. "Quadratic seam" vs. "diagonal quartic seam"

At phase-space.tex:

> "The quadratic seam studied in earlier work corresponds to the restriction $a=b=1$, $c=0$"

This should say "diagonal quartic seam" — setting $a=b=1$, $c=0$ still yields a quartic seam, not a quadratic one. The quadratic seam is obtained by $\lambda = 0$.

### 8. "Earlier work" without a citation

The same sentence references "earlier work" but provides no citation. Either cite it or rephrase (e.g., "the diagonal restriction").

---

## Grammar / Prose Issues

### 9. Abstract: sentence fragment

phase-space.tex:

> "In particular, for the quadratic seam [...] with positive width parameters $\sigma_x,\sigma_p$. Its sublevel set..."

The period after the displayed equation creates a fragment. The "In particular, for..." clause has no main verb. Suggested fix: "In particular, consider the quadratic seam [...] with positive width parameters $\sigma_x,\sigma_p$: its sublevel set $\{s \le 1/2\}$ is an ellipsoid..."

### 10. Placeholder email address

phase-space.tex: `lars@uptochange.com` — this is clearly a placeholder and should be replaced with an actual contact address before submission.

### 11. `\date{\today}`

phase-space.tex: This will render as the compilation date. For submission, you likely want a fixed date or no date (use `\date{}`).

---

## LaTeX / Formatting Issues

### 12. Unused packages

phase-space.tex: `tikz` and `tikzlibrary{shapes.geometric}` are loaded but never used. Remove them to keep the preamble clean.

### 13. Double section separator

Before the Kerr section ([lines 1033–1034](phase-space.tex#L1033-L1034)), there are two consecutive `%---` separator lines with nothing between them, unlike the single separator used elsewhere. Cosmetic but inconsistent.

---

## Summary of Fixes Needed

| # | Severity | Location | Issue |
|---|----------|----------|-------|
| 1 | **High** | §8, L920 | Spurious wrong identity `= 2K_4^full - K_4^diag` |
| 2 | **High** | Prop 6.1, L882 | Wrong algebraic identity (off by $-2\sqrt{ab}$) |
| 3 | **High** | Kerr §, L1065 | $\mathcal{W}_4 = \lambda/8$ is wrong; convention mismatch |
| 4 | **Medium** | Kerr §, L1054 | $\lambda = \beta\kappa$ likely wrong ($\lambda = \kappa m^2/\beta$) |
| 5 | **Medium** | Kerr §, L1058 | Missing `+` sign |
| 6 | **Medium** | Abstract, L38–43 | Single-mode / multi-mode notation mismatch |
| 7 | **Low** | L313 | "Quadratic seam" should be "diagonal quartic seam" |
| 8 | **Low** | L313 | "Earlier work" uncited |
| 9 | **Low** | Abstract, L40 | Sentence fragment |
| 10 | **Low** | L20 | Placeholder email |
| 11 | **Low** | L21 | `\date{\today}` |
| 12 | **Low** | L6–7 | Unused `tikz` packages |

The core mathematical results (Theorems 4.1, 5.2, 7.1, the universality theorem 7.2, and all the angular integral / double-trace derivations) are **correct** and internally consistent. The errors are concentrated in the Kerr example section (convention mismatch) and two display-formula typos (Prop 6.1 identity, §8 chain). Want me to apply the fixes?

---

Actions: 

1 - Fix 
2 - Fix
3 - Adapt Kerr to follow paper convention
4 - Fix
5 - Fix 
6 - Fix to what is most natural
7 - Fix
8 - Remove reference to earlier work if possible
9 - Fix
10 - No fix, lars@uptochange.com is my address
11 - Remove the date completely
12 - Remove import
