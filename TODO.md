Review of “Phase-Space Seams: Hessian Geometry and the Invariant First Variation of Quartic Sublevel Sets”

Summary: The manuscript introduces phase-space seams, defining a Riemannian metric from the Hessian of a scalar function on phase space, and studies volumes of sublevel sets of the seam. Its main result is that the first-order variation of the sublevel-set volume in small radius depends only on the full O(n)-invariant contraction (double trace) of the 4th-order jet of the scalar. Specializing to a quartic “seam” in 1 mode 
(
𝑑
=
1
)
(d=1), the paper computes the area correction to first order in the quartic strength and shows that normalisability forces a strictly positive correction. Quadratic (Gaussian) seams saturate the uncertainty-area bound 
𝜎
𝑥
𝜎
𝑝
≥
ℏ
/
2
σ
x
	​

σ
p
	​

≥ℏ/2. The note is self-contained and uses elementary multivariate calculus and inequalities.

The exposition is generally clear and organized with definitions, theorems, and proofs. To elevate the paper, we suggest placing it in broader context and connecting to related work in both information geometry and phase-space quantum mechanics. In particular:

Hessian Manifold / Information Geometry: The “Hessian rule” (metric 
𝑔
𝑖
𝑗
=
∂
𝑖
∂
𝑗
𝑠
g
ij
	​

=∂
i
	​

∂
j
	​

s) is exactly the structure of a Hessian metric or Hessian manifold, familiar in information geometry and convex geometry. It would strengthen the paper to cite standard sources on Hessian structures (e.g. Amari–Nagaoka’s Methods of Information Geometry, Shima’s Geometry of Hessian Structures) and explicitly note that the phase-space seam metric is a flat Hessian metric. For example, one could add a sentence like: “By definition this construction makes 
(
𝑅
2
𝑑
,
𝑔
)
(R
2d
,g) into a Hessian manifold (a flat affine manifold with metric given locally by the Hessian of a potential function).” This ties the work to the well-developed theory of Hessian geometries (e.g. Amari–Nagaoka, Shima).

Relation to Information Geometry: The remark that the Hessian of a log-density is the observed Fisher information is good. One might cite a standard statistics text or review of information geometry to support this link. For instance, Amari–Nagaoka (2000) note that for an exponential family the Fisher metric arises as the Hessian of the log-partition function. The text already references Rao (1945) and Amari–Nagaoka, which is appropriate. (If space permits, the explicit formula from the slides could be summarized: “In an exponential family the Fisher metric is the Hessian of the log-partition potential,” as a known example.)

Quantum Phase-Space Context: The motivation via Husimi 
𝑄
Q-functions is interesting. It may help readers to mention explicitly the concept of quantum blobs or symplectic capacity from quantum mechanics. De Gosson’s work defines quantum blobs as minimal symplectic-area ellipsoids consistent with the uncertainty principle. In particular, “quantum blobs are the smallest phase-space units compatible with the uncertainty principle, invariant under symplectic transformations.” This is directly related to the minimal-area ellipsoid of radius 
ℏ
ℏ
	​

 (area 
𝜋
ℏ
πℏ) often used in phase-space quantum mechanics. It could be worth mentioning that in this language, the minimal-area bound 
𝐴
≥
𝜋
ℏ
/
2
A≥πℏ/2 (per mode) is equivalent to the quantum blob bound (up to conventions). This connection would place the assumption 5.1 in context and highlight how symplectic geometry enters. (For example: “Indeed, de Gosson’s “quantum blobs” – minimal symplectic ellipsoids of area 
𝜋
ℏ
πℏ – represent the level sets of Gaussian coherent states. Our minimal-area assumption is thus a phase-space analogue of that quantum principle.”)

Integral Geometry and Volume Expansions: Theorem 3.1 (invariant first variation) is reminiscent of classical results in integral geometry (tube formulas, curvature integrals, Kac–Rice) for small-volume expansions. For example, Weyl’s tube formula expresses the volume of a small parallel neighborhood in terms of mean curvature integrals. Similarly, Jubin (2020) developed general formulas for intrinsic volumes of sublevel sets of smooth functions. It would strengthen the paper to cite these ideas: e.g. Jubin’s work describes how volumes of sublevel sets can be written in terms of integrals of curvature invariants. One could add: “This leading-order invariance is consistent with known integral-geometry formulas. For instance, in flat space the tube formula implies that only the full trace of the Hessian enters the first correction to small-volume growth. Jubin (arXiv 2019) provides a general framework (via Kac–Rice formulas) for volumes of excursion sets of functions, of which our result is a simple flat-space case.” Here [31†L55-L61] (from Jubin) could be cited to connect to Weyl’s and Minkowski’s formulas.

Volume of Generalized Ellipsoids: The paper could note that sublevel sets of higher-degree polynomials are a topic of interest in convex geometry and optimization (sometimes called “generalized ellipsoids”). For instance, recent work has studied sublevel sets of homogeneous convex polynomials (generalized 
ℓ
𝑝
ℓ
p
	​

-balls) and their volume/computational properties. While a full literature review is beyond scope, a reference to e.g. Ahmadi et al. (2024) on “generalized ellipsoids” might be mentioned for context (they characterize when sublevel sets of degree-
𝑑
d polynomials can be represented as convex bodies in certain cones). If nothing else, a short comment like “In convex geometry, sublevel sets of quartic forms are known as generalized ellipsoids of degree 2. Our expansion shows the first correction to their volume, complementing works on convexity and volume of such sets.” would link to known results. (No specific citation is required here unless there is a direct formula to compare.)

Higher-Order Jets: A natural extension is to consider jets beyond 4th order. Theorem 3.1 suggests a pattern: for an even-degree 
2
𝑘
2k jet, the first-order change in volume will involve only the unique O(n)-invariant contraction of the 
2
𝑘
2k-tensor. One could remark this explicitly as a conjecture: “By the same spherical-integration argument, the first correction from a general 
2
𝑘
2k-jet will depend only on the 
𝑂
(
𝑛
)
O(n)-scalar \mathrm{Tr}\,^{}\mathrm{Tr}\,T^{(2k)}. This suggests a hierarchy of non-Gaussian corrections at each even order, generalizing (5.3).” It may also help to note the known fact that the integral of 
𝑛
𝑖
𝑛
𝑗
𝑛
𝑘
𝑛
𝑙
𝑛
𝑚
𝑛
𝑝
n
i
	​

n
j
	​

n
k
	​

n
l
	​

n
m
	​

n
p
	​

 over the sphere again picks out only the fully symmetric contractions (via Wick’s theorem or isotropic tensor integrals). A brief mention (with or without a formula) that “the same method yields that only the total trace of the 6th-derivative tensor enters at 
𝑂
(
𝜀
3
)
O(ε
3
), etc.” would indicate the generality of the result.

Multimode (d>1) Details: Section 8 outlines the higher-dimensional case. It might be worth expanding slightly or giving a concrete example. For instance, in 
𝑑
>
1
d>1 one can have cross-terms coupling different modes (like 
𝑥
1
2
𝑝
2
2
x
1
2
	​

p
2
2
	​

), which would contribute to 
𝑇
𝑖
𝑗
𝑘
𝑙
T
ijkl
	​

 with new index patterns. The text could note that the angular integrals on 
𝑆
2
𝑑
−
1
S
2d−1
 again pick out only double traces of 
𝑇
𝑖
𝑗
𝑘
𝑙
T
ijkl
	​

, as in (3.12). Perhaps add a sentence like: “In the multimode case, mixed quartic terms 
𝑢
𝑖
2
𝑣
𝑗
2
u
i
2
	​

v
j
2
	​

 (with 
𝑖
≠
𝑗
i

=j) appear; however, by 
𝑂
(
2
𝑑
)
O(2d)-symmetry their contributions to the first variation are again encoded in the total double-trace 
𝑇
~
𝑖
𝑖
𝑗
𝑗
T
iijj
	​

. The ratio of coefficients (1/3) found in 2D persists in higher dimensions due to isotropy of the sphere (cf. Eq. (3.11)).” One could cite a standard formula for the 4th moments on 
𝑆
𝑛
−
1
S
n−1
 in general (analogous to (3.11) but for arbitrary 
𝑛
n), although that is elementary to derive.

Visual Illustration: A figure could help readers. For example, a contour plot of a sample quartic seam sublevel set (in normalized 
𝑢
,
𝑣
u,v coordinates) would illustrate how the level set deviates from an ellipse. A suggestion would be: “It would be illuminating to include a plot of 
{
𝑠
4
(
𝑢
,
𝑣
)
=
1
/
2
}
{s
4
	​

(u,v)=1/2} for representative parameters, showing the quadratic ellipse and its quartic perturbation.” If the journal allows it, a colored contour or filled region (as in a computational figure) could appear in the quartic section. (This is optional, but a well-labeled figure like “Figure: Sublevel set of 
𝑠
4
s
4
	​

 in the 
𝑢
,
𝑣
u,v plane, showing the effect of the 
𝑢
4
u
4
 and 
𝑢
2
𝑣
2
u
2
v
2
 terms, which shrink the area relative to the circle.” would add visual clarity.)

Notation and Definitions: The paper uses jets, Hessians, etc., which is clear. A couple of small points: the phrase “
𝑇
𝑖
𝑗
𝑘
𝑙
T
ijkl
	​

 counts with multiplicity 6 when fully symmetrised” might confuse some readers; it could be phrased as “note 
𝑇
𝑥
𝑥
𝑝
𝑝
T
xxpp
	​

 appears in 6 distinct index permutations” or similar. Also, the use of “
𝑂
(
𝑛
)
O(n)-scalar contraction” is apt but could be more explicit (e.g. “unique scalar invariant under orthogonal transformations”). These are minor wording suggestions.

References: The bibliography is light. In addition to suggestions above, consider citing Amari & Nagaoka (2000, which is already cited) for general info geometry, and de Gosson (e.g. his book “Symplectic Geometry and Quantum Mechanics” or “Phase Space Quantization”) for quantum blobs/symplectic perspective. If available, an explicit reference on the volume of general quartic level sets (perhaps in convex geometry or polynomial optimization literature) could be added, but this may be hard to find. The generalized ellipsoids paper [10] (Ahmadi et al., 2025) is quite recent and relevant but not essential to cite unless one wants to link to optimization; it is more about algorithmic tractability of such sets.

Additional Extensions: The conclusion mentions “curved-space extensions” and a variational interpretation. These are intriguing; one could explicitly suggest as future work to relate the Hessian metric 
𝑔
g to the symplectic form to get a Kähler structure, or to consider quantum state manifolds with curvature. Another trivial extension is to consider odd-order jets or asymmetries, but level sets of odd functions are unbounded so less directly applicable.

In summary, the technical content of the paper is correct and novel. The key improvement is to situate it in the broader literature: mention Hessian manifold theory, quantum blobs, and classical integral-geometry results. Adding a figure and clarifying some definitions would improve readability. These additions would not change the main theorems but would help readers appreciate the significance and potential generalizations of the work.

Specific improvement suggestions:

In the Introduction, explicitly cite one or two sources on Hessian geometry (e.g. Amari–Nagaoka, Shima) and mention that the Hessian rule makes the phase space into a flat Hessian manifold.

When interpreting 
exp
⁡
(
−
𝑠
)
exp(−s) as a quantum phase-space density, cite de Gosson on quantum blobs to motivate the area bound. Clarify the factor of 2 difference if any in conventions.

In Section 3, add a remark or citation that the spherical integrals of monomials (e.g. (3.11)) are standard (one could cite a formula from random matrix theory or spherical integrals, or just note “by isotropy of the sphere” as is done).

Possibly expand Section 8 a bit to mention how cross-mode quartic terms would appear, or at least point out that only their total trace enters first-order volume change.

Include a brief figure of the quartic sublevel set, for example by plotting 
{
(
𝑢
,
𝑣
)
:
𝑢
2
+
𝑣
2
2
+
𝜆
4
(
𝑎
𝑢
4
+
𝑏
𝑣
4
+
2
𝑐
𝑢
2
𝑣
2
)
=
1
/
2
}
{(u,v):
2
u
2
+v
2
	​

+
4
λ
	​

(au
4
+bv
4
+2cu
2
v
2
)=1/2}. A caption could explain the parameters and show area shrinkage visually.

In the Conclusion, one could add a final sentence tying back to quantum phase-space: e.g. “We leave for future work the explicit connection between this scalar-first geometry and symplectic invariants (quantum blobs) of phase-space distributions.”

By making these connections and adding a figure, the paper will read not only as a self-contained calculation but as part of a larger story linking geometry, statistics, and quantum physics.

References used in this review: We relied on standard results and the cited papers for context: Amari–Nagaoka (2000) on Hessian metrics; Jubin (2020) on intrinsic volumes of sublevel sets; and de Gosson on quantum blobs. These sources can be cited or paraphrased in the text to support the suggested points.