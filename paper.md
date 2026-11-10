# Complementary tensor relations and bipartite matching kernels

Author: Ignoramus

Email: ignoramus110926@gmail.com

Version 3.2 - November 10, 2026

## Abstract

Let $D_i$ be a nonzero tensor occupying every leaf space except $V_i$, with a common additional factor space $X$. We study relations $\sum_i v_iD_i=0$ with $v_i\in V_i$. For $n$ leaves, we prove the characteristic-free bound $\dim R\leq n-1$ and characterize equality by a common factor in $X$ and signed maximal minors of a matrix with separated column variables. This gives sharp bounds for completing any nonempty subset of the last row of a bipartite matching tensor. We then classify maximal kernels for two fixed rows and three leaves, over every field and with zero edge blocks allowed, provided the three complementary tensors are nonzero. In characteristic different from two, a maximal kernel with six nonzero blocks forces common root lines and at least two aligned leaf pairs. In characteristic two, the combined space of contracted rows must have dimension two; this criterion extends to all square determinant tensors, and hence to matching tensors in characteristic two. A separate normal form treats zero blocks. Finally, the necessity of the root-line conclusion gives a sharp cut-rank obstruction on an eight-vertex matching network, with nonzero examples attaining the bound for every positive dimension of the vertex space at vertex 8, over every field of characteristic different from two.

## 1. Introduction

Expanding a multilinear tensor construction in one row produces a map of the form

\[
\Phi:\bigoplus_{i=1}^n V_i\longrightarrow X\otimes\bigotimes_{i=1}^n V_i,
\qquad \Phi(v_1,\ldots,v_n)=\sum_{i=1}^n v_iD_i,
\tag{1}
\]

where $D_i\in X\otimes\bigotimes_{j\ne i}V_j$. The coefficient of $D_i$ occupies precisely the missing leaf space. The relation space $R=\ker\Phi$ therefore records the ambiguity of that row. This coefficient restriction is essential: $R$ is a vector space of admissible leaf-linear relations, rather than the whole polynomial syzygy module.

One motivating construction is the perfect-matching tensor of $K_{n,n}$. Assign spaces $U_1,\ldots,U_{n-1}$ and $N$ to its roots and $V_1,\ldots,V_n$ to its leaves. Fix blocks $E_{ai}\in U_a\otimes V_i$ on the first $n-1$ rows and let $C_i\in N\otimes V_i$ vary on the last row. The output is the unsigned sum over perfect matchings, with tensor factors placed in vertex order. If $D_i$ is the complementary matching tensor after deleting the last root and leaf $i$, then

\[
\Psi(C_1,\ldots,C_n)=\sum_i C_iD_i
= (\operatorname{id}_N\otimes\Phi)(C_1,\ldots,C_n).
\tag{2}
\]

The graph description of coherent superpositions in quantum-optical state generation begins with unweighted graphs [1]; complex edge weights and their interference are treated in [10]. The tensor notation makes a local inverse problem explicit: with most edge blocks fixed, which changes of the remaining blocks preserve all output amplitudes? The kernel measures this ambiguity, and its maximal case identifies the configurations with the largest ambiguity allowed by the number of unknown blocks.

This interpretation applies beyond bipartite graphs. For a finite graph $G$ with an even number of vertices and edge blocks $B_{uv}\in V_u\otimes V_v$, define

\[
P_G=\sum_{M\in\operatorname{PM}(G)}\prod_{uv\in M}B_{uv},
\]

where $\operatorname{PM}(G)$ is the set of perfect matchings and products are placed in vertex order. Choose a basis at each vertex and write the edge coordinates as $b_{uv}^{cd}$. The coefficient at a vertex colouring $\kappa$ is

\[
[P_G]_{\kappa}=\sum_{M\in\operatorname{PM}(G)}\prod_{uv\in M}b_{uv}^{\kappa(u)\kappa(v)}.
\]

Over $\mathbb C$ this is precisely the vertex-colouring weight in the weighted, half-edge-coloured graph formalism of [11, Section 1.1]: an entry $b_{uv}^{cd}$ combines any parallel edges with endpoint colours $c,d$. Thus equality of these tensors means equality of all vertex-colouring weights. Our completion results describe local ambiguity in that coordinate problem, and the rank obstruction in Section 10 restricts its attainable outputs under a stated cofactor constraint. We do not claim that these results settle an open case of the Krenn--Gu conjecture or make every prescribed output attainable. The finite-field results concern the algebraic construction itself.

The first result is an elementary general theorem: nonzero complementary tensors have $\dim R\leq n-1$, with a sharper fraction-field rank bound. Equality has a signed-maximal-minor description. The proof uses coefficient comparison in disjoint variable groups; it does not assume that independence over the ground field survives passage to a fraction field. The independence step also follows from the independent-representative rank formula in [9, Proposition 3.2], credited there to Le and O'Dorney as a generalization of Rado's theorem [7]; the coefficient proof here is self-contained. Its equality model is a column-graded matrix of the kind studied in [8]. We give the direct proof because the precise leaf-coefficient restriction is needed in the applications.

The matching-specific question is which original edge blocks realize equality. For $n=3$ we answer it completely, subject only to nonvanishing of the three complementary tensors. Theorem 3.1 handles six nonzero blocks in characteristic different from two. Section 7 gives the characteristic-two criterion, as part of a determinant family valid for every order over every field. Section 8 gives a normal form whenever an edge block vanishes. These alternatives cover every field and every six-block pattern under the standing complementary-nonvanishing condition.

All vector spaces are finite-dimensional over a field $F$. Tensor products are over $F$. A product of factors in different vertex slots means their tensor product followed by the permutation into the indicated slot order. Polynomial identities below are identities in formal variables, including over finite fields.

The three-leaf classification can be stated in one theorem. Put $E=V_1\oplus V_2\oplus V_3$. For two rows $A_i\in U\otimes V_i$, $B_i\in W\otimes V_i$, let $H\subseteq E$ be the sum of the images of the contraction maps from $U^*$ and $W^*$, respectively,

\[
\alpha\longmapsto((\alpha\otimes\operatorname{id})A_i)_{i=1}^3,
\qquad
\beta\longmapsto((\beta\otimes\operatorname{id})B_i)_{i=1}^3.
\]

**Theorem 1.1 (complete three-leaf equality classification).** Over any field, assume all three $D_i=A_jB_k+A_kB_j$ are nonzero, where $\{i,j,k\}=\{1,2,3\}$, and put $R=\{(v_i)\in E:\sum_i v_iD_i=0\}$. Then $\dim R\leq2$. Equality holds exactly under the condition in the applicable case below.

**(a)** If $\operatorname{char}F=2$, the condition is $\dim H=2$; in that case $R=H$.

**(b)** If $\operatorname{char}F\ne2$ and all six blocks are nonzero, the condition is that $A_i=ua_i$ and $B_i=wb_i$ for common nonzero $u\in U$, $w\in W$ and nonzero $a_i,b_i\in V_i$, with at least two pairs $(a_i,b_i)$ linearly dependent.

**(c)** If $\operatorname{char}F\ne2$ and some block vanishes, interchange the two rows if necessary (the names $U$ and $W$ are then interchanged as well) and permute the leaves so that $A_1=0$. The condition is the existence of nonzero $u\in U$, $w\in W$, $a_2\in V_2$, $a_3\in V_3$, $b_1\in V_1$, and arbitrary $v\in W$, $b_2\in V_2$, $b_3\in V_3$ such that

\[
\begin{aligned}
A_1&=0,&A_2&=ua_2,&A_3&=ua_3,\\
B_1&=wb_1,&B_2&=wb_2+va_2,&B_3&=wb_3-va_3,
\end{aligned}
\]

with $a_2b_3+b_2a_3\ne0$. The corresponding relation basis is $(0,a_2,-a_3)$ and $(b_1,-b_2,-b_3)$.

The bound is Theorem 2.1. Cases (a), (b) and (c) are proved in Corollary 7.2, Theorem 3.1 and Theorem 8.1, respectively. The normal form in (c) also holds in characteristic two, but the disjoint cases above give a single exhaustive statement. Nonvanishing of the complementary tensors is a hypothesis in every case; zero edge blocks are a separate matter.

Section 9 describes completion with any subset of attachments known. Section 10 gives a different application: a sharp rank obstruction on an eight-vertex graph. Its proof uses the necessity direction of Theorem 3.1 to obtain a root line, then uses a cofactor constraint to remove an incident edge. The explicit sharp examples show that the hypotheses are simultaneously realizable.

The nearest commutative-algebra context is the theory of permanental ideals. Efremenko, Landsberg, Schenck and Weyman compute linear strands for generic subpermanental ideals in characteristic zero [5]. Gesmundo, Huang, Schenck and Weyman explain that the absence of linear first syzygies for the two-by-two subpermanents of a generic two-row matrix follows from that work, and reprove it in Lemma 2.13 of their arXiv version [2]. Zoromski studies the generic two-row ideal over the complex numbers [3]. This absence statement concerns two fixed rows; it is not a statement about all subpermanents of a generic three-row matrix. Section 12 explains why our restricted relations are not direct polynomial specializations of generic syzygies. Splitting results for scalar dependencies among fixed product tensors [4] provide another context, but here the original blocks may have arbitrary matrix rank and the relation coefficients are vectors.

## 2. Relations among complementary tensors

Let $n\geq2$, and assume

\[
0\ne D_i\in X\otimes\bigotimes_{j\ne i}V_j
\qquad(1\leq i\leq n).
\tag{3}
\]

Define $\Phi$ and $R$ by (1). Choose bases of the leaf spaces and identify $V_i$ with the linear forms in a disjoint variable group $Z_i$. Put

\[
S=F[Z_1,\ldots,Z_n],\qquad K=\operatorname{Frac}(S),\qquad
K_i=F(Z_1,\ldots,\widehat{Z_i},\ldots,Z_n).
\tag{4}
\]

Let $\rho$ be the rank of the $K$-linear map $K^n\to X\otimes_F K$ with columns $D_i$.

**Theorem 2.1.** Over every field,

\[
\dim_F R\leq n-\rho\leq n-1.
\tag{5}
\]

Equality $\dim_F R=n-1$ holds if and only if there are an $(n-1)\times n$ matrix $M$ with $M_{ai}\in V_i$ and a nonzero $g\in X$ such that

\[
\Delta_i=(-1)^{i+1}\det M_{\widehat i}\ne0,
\qquad D_i=g\Delta_i\quad(1\leq i\leq n).
\tag{6}
\]

Here $M_{\widehat i}$ deletes column $i$, and each determinant is expanded using one factor from each remaining leaf space. In the equality case the rows of $M$ form a basis of $R$, and any basis of $R$ may be used in this way.

We first establish the independence step needed for the bound.

**Lemma 2.2.** Let $M$ be an $r\times n$ matrix whose $i$th column is linear in $Z_i$, with coefficients in $F^r$. Suppose its rows are independent over $F$, and every column lies in the $K$-span of the remaining columns. Then $\operatorname{rank}_K M=r$.

*Proof.* Write $M_i=\sum_a z_{ia}u_{ia}$ with $u_{ia}\in F^r$. The vectors $u_{ia}$, over all $i,a$, span $F^r$: otherwise a nonzero functional annihilating them would give an $F$-linear relation among the rows.

For fixed $i$, let $W_i$ be the $K_i$-span of the columns $M_j$ with $j\ne i$. These columns are defined over $K_i$. By hypothesis $M_i\in W_i\otimes_{K_i}K$. If $\ell\in(K_i^r)^*$ annihilates $W_i$, then

\[
0=\ell(M_i)=\sum_a z_{ia}\ell(u_{ia}).
\tag{7}
\]

Algebraic independence of $Z_i$ over $K_i$ forces every coefficient to vanish. The double-annihilator property gives $u_{ia}\in W_i$. Hence every coefficient vector belongs to the $K$-column span of $M$. Since those vectors span $F^r$, that column span is $K^r$.

*Proof of Theorem 2.1.* Put $r=\dim_F R$. The bound is immediate if $r=0$. Otherwise form $M$ from an $F$-basis of $R$. In a basis $(e_b)$ of $X$, write $D_i=\sum_b e_bD_{i,b}$. Every coordinate relation is

\[
\sum_i M_iD_{i,b}=0.
\tag{8}
\]

For each $i$, some $D_{i,b}$ is nonzero, so (8) expresses $M_i$ as a $K$-linear combination of the other columns. Lemma 2.2 shows that the $r$ relation rows are $K$-independent. They belong to the kernel of a rank-$\rho$ map with domain $K^n$, proving (5), since $\rho\geq1$ by nonvanishing of the complementary tensors.

Suppose now that $r=n-1$. Since every column of $M$ is in the span of the others, deleting any one column preserves rank $n-1$. Thus every $\Delta_i$ in (6) is nonzero. The signed-minor identity gives $M\Delta=0$, and the kernel of $M$ over $K$ is one-dimensional. Consequently, for each coordinate $b$ there is $\mu_b\in K$ such that $D_{i,b}=\mu_b\Delta_i$ for all $i$. Both numerator and denominator in $\mu_b=D_{i,b}/\Delta_i$ omit $Z_i$, so

\[
\mu_b\in\bigcap_{i=1}^n K_i=F.
\tag{9}
\]

For completeness, the field intersection follows by iteration from $L(Y)\cap L(Z)=L$ for disjoint indeterminate groups. Indeed, $p(Y)/q(Y)=r(Z)/s(Z)$ gives $p(Y)s(Z)=q(Y)r(Z)$; comparison at a $Z$-monomial with nonzero coefficient in $s$ makes $p/q$ a scalar in $L$. Taking shared variable groups as the base field proves the corresponding intersection for any two subsets of the groups, and then (9). No evaluation at field elements is involved.

Set $g=\sum_b\mu_be_b$. It is nonzero and gives (6). Conversely, (6) and the signed-minor identity put all rows of $M$ in $R$. A nonzero maximal minor makes these $n-1$ rows independent, and the bound makes them a basis. This proves the theorem.

Changing a relation basis by $P\in\operatorname{GL}_{n-1}(F)$ multiplies every minor by $\det P$ and replaces $g$ by $(\det P)^{-1}g$. Thus the common line $Fg$ is intrinsic. For $n=3$, if the basis rows are $(v_i)$ and $(v_i')$, the form reads

\[
\begin{aligned}
D_1&=g(v_2v_3'-v_2'v_3),\\
D_2&=g(v_3v_1'-v_3'v_1),\\
D_3&=g(v_1v_2'-v_1'v_2).
\end{aligned}
\tag{10}
\]

The converse also has a classical determinantal proof. Since every nonzero $\Delta_i$ omits $Z_i$, a common divisor of all the minors must omit every group and is therefore constant. Their ideal in the polynomial ring $S$ has grade at least two: it lies in no height-one prime, and $S$ is Cohen--Macaulay. Hilbert--Burch [6, Theorem 2.2] then identifies its syzygy module with the image of $M^{\mathsf T}$. The minors have total degree $n-1$ and the columns of $M^{\mathsf T}$ have degree one, so a syzygy with linear entries is a constant combination of those columns. This recovers the converse; the direct proof above avoids these additional algebraic facts.

The equality matrices are column-graded. Conca, De Negri and Gorla study their maximal-minor ideals in [12, Theorem 3.2] and [8]. The former proves a linear resolution and the relevant projective-dimension statement, in a proof that assumes without loss of generality that the field is infinite; the latter develops the broader Cartwright--Sturmfels setting. The structural comparison does not import an infinite-field hypothesis or a resolution theorem into our tensor proof. These classical ingredients do not by themselves constitute a new result on determinantal ideals.

## 3. Matching blocks and the equality classification

Let $F$ be a field of characteristic different from two. Let $U,W,V_1,V_2,V_3$ be finite-dimensional $F$-vector spaces. Choose nonzero tensors

\[
A_i\in U\otimes V_i,\qquad B_i\in W\otimes V_i\qquad(1\leq i\leq3).
\tag{11}
\]

Tensor products are always placed in the order $U,W,V_1,V_2,V_3$, omitting a leaf slot when appropriate. Thus $A_jB_k$ denotes the ordinary tensor product followed by the permutation of factors that puts it in these slots. No conjugation or signed matching convention is used.

For $\{i,j,k\}=\{1,2,3\}$ define

\[
D_i=A_jB_k+A_kB_j\in U\otimes W\otimes V_j\otimes V_k.
\tag{12}
\]

The notation is independent of the order of $j,k$. We assume throughout that $D_1,D_2,D_3$ are all nonzero. Define

\[
\Phi:V_1\oplus V_2\oplus V_3\longrightarrow U\otimes W\otimes V_1\otimes V_2\otimes V_3,\qquad
\Phi(n_1,n_2,n_3)=\sum_{i=1}^{3}n_iD_i,
\tag{13}
\]

and write $R=\ker\Phi$. A vector $n_i$ in (13) is inserted in the missing leaf slot.

**Theorem 3.1.** Under the preceding hypotheses, $\dim R=2$ if and only if there are nonzero vectors $u\in U$, $w\in W$, and nonzero vectors $a_i,b_i\in V_i$ such that

\[
A_i=u\otimes a_i,\qquad B_i=w\otimes b_i\qquad(1\leq i\leq3),
\tag{14}
\]

and at least two of the pairs $(a_i,b_i)$ are linearly dependent.

More explicitly, after renumbering those two leaves as 2 and 3, write $b_2=\lambda_2a_2$ and $b_3=\lambda_3a_3$. Then $\lambda_2,\lambda_3$ and $\lambda_2+\lambda_3$ are nonzero, and every element of $R$ is uniquely of the form

\[
n_2=sa_2,\qquad n_3=ta_3,
\tag{15}
\]

\[
n_1=-\frac{s(\lambda_3a_1+b_1)+t(\lambda_2a_1+b_1)}{\lambda_2+\lambda_3},
\qquad s,t\in F.
\tag{16}
\]

The root image of $A_i$ is the image of the contraction map $V_i^*\to U$. Thus (14) says that all three root images on each side are the same line. This formulation is independent of choices of bases. The leaf alignment condition is also invariant under the rescalings used to choose $u$ and $w$.

The proof first works over an infinite field. Section 6 supplies the descent needed for finite fields.

## 4. Relations after contracting the roots

We begin with a statement involving only the leaf spaces.

**Lemma 4.1.** Assume that the field has characteristic different from two. Let $a_i,b_i$ be nonzero vectors in $V_i$, and put $d_i=a_jb_k+b_ja_k$. If at least two pairs $(a_i,b_i)$ are linearly independent, the kernel of $\sum_i n_id_i$ has dimension at most one. It has dimension zero when all three pairs are independent, and dimension one when exactly two are independent.

*Proof.* Suppose first that all three pairs are independent. Each $d_i$ is nonzero. Quotient the relation at leaf $i$ by $\operatorname{span}(a_i,b_i)$. The other two summands vanish, so $n_i$ belongs to that span. Here we use that tensoring with a fixed nonzero tensor is injective over a field. Write $n_i=x_i a_i+y_i b_i$.

The eight tensor products obtained by choosing $a_i$ or $b_i$ at each leaf are independent. The coefficients with exactly one $b$ imply $x_i+x_j=0$ for each pair $i\ne j$. Since the characteristic is not two, all $x_i$ vanish. The coefficients with exactly two $b$ similarly force all $y_i$ to vanish.

Now suppose exactly two pairs are independent, at leaves $i,j$. At the remaining leaf write $b_k=\lambda a_k$, where $\lambda\ne0$, and set $L_i=\lambda a_i+b_i$ and $L_j=\lambda a_j+b_j$. Then

\[
d_i=L_j a_k,\qquad d_j=L_i a_k,\qquad d_k=a_i b_j+b_i a_j.
\tag{17}
\]

All three tensors are nonzero. Quotienting at leaf $k$ by $F a_k$ gives $n_k=c a_k$. Cancelling the common nonzero factor $a_k$, the relation becomes

\[
n_iL_j+L_in_j+c(a_ib_j+b_ia_j)=0.
\tag{18}
\]

Quotient simultaneously by $F L_i$ and $F L_j$. The first two terms disappear. In these quotients, the last parenthesis is $-2\lambda$ times the nonzero product of the images of $a_i,a_j$. Therefore $c=0$. Equation (18) then has exactly the solutions $n_i=sL_i$, $n_j=-sL_j$, with $s\in F$. This proves the lemma.

**Lemma 4.2.** Retain the nonzero-block hypotheses of Section 3 and assume that $F$ is infinite of characteristic different from two. If $\dim R\geq2$, then at least two leaves, say $j,k$, admit factorizations

\[
A_j=u_jp_j,\quad B_j=w_jp_j,\qquad
A_k=u_kp_k,\quad B_k=w_kp_k,
\tag{19}
\]

in which every displayed factor is nonzero.

*Proof.* For $\alpha\in U^*$ and $\beta\in W^*$ define

\[
a_i(\alpha)=(\alpha\otimes\operatorname{id})A_i,\qquad
b_i(\beta)=(\beta\otimes\operatorname{id})B_i.
\tag{20}
\]

Every element of $R$ remains a relation after these root contractions, with exactly the same coefficient vectors $n_i$. Thus every contracted relation kernel contains $R$.

Suppose two leaves have $a_i(\alpha)\wedge b_i(\beta)$ not identically zero as a polynomial function of $\alpha,\beta$. Choose one nonzero coordinate polynomial of each such wedge. For each of the six blocks choose a contracted coordinate polynomial that is not identically zero; such a coordinate exists because the block is nonzero. The product of these finitely many polynomials is nonzero. Over an infinite field it has a point where it is nonzero. At that point all six contracted vectors are nonzero and at least two leaf pairs are independent. Lemma 4.1 makes the contracted kernel at most one-dimensional, contradicting its containment of $R$.

Consequently, at least two leaves satisfy $a_i(\alpha)\wedge b_i(\beta)=0$ for every $\alpha,\beta$. At such a leaf choose $\beta_0$ with $b_i(\beta_0)=p_i\ne0$. Every $a_i(\alpha)$ belongs to $F p_i$. Some such contraction is nonzero, so fixing it shows in turn that every $b_i(\beta)$ belongs to the same line. Both blocks therefore factor as in (19).

The nonzero-polynomial argument selects covectors for six fixed blocks. It places no genericity condition on the blocks and does not exclude covectors at which individual contractions vanish.

## 5. Lifting alignment to the roots

Continue over an infinite field, and suppose $\dim R\geq2$. Choose the aligned leaves $j,k$ from Lemma 4.2, and let $i$ be the remaining leaf. Define

\[
H=u_jw_k+u_kw_j,\qquad
K_j=A_iw_j+u_jB_i,\qquad
K_k=A_iw_k+u_kB_i.
\tag{21}
\]

The three original matching tensors are

\[
D_i=Hp_jp_k,\qquad D_j=K_kp_k,\qquad D_k=K_jp_j.
\tag{22}
\]

Their nonvanishing implies $H,K_j,K_k\ne0$. Quotienting a relation at leaves $j$ and $k$ gives $n_j=sp_j$ and $n_k=tp_k$. Cancelling $p_jp_k$ leaves

\[
Hn_i+sK_k+tK_j=0.
\tag{23}
\]

The map $R\to F^2$ sending the relation to $(s,t)$ is injective, because $H\ne0$. The general bound in Theorem 2.1 and the current assumption give $\dim R=2$, so this injection is surjective. In particular, there are nonzero $z_j,z_k\in V_i$ with

\[
K_j=Hz_j,\qquad K_k=Hz_k.
\tag{24}
\]

It remains to prove that both pairs of root vectors in (19) are dependent and that the remaining blocks use the same root lines.

For any $\theta\in V_i^*$ put $a=(\operatorname{id}\otimes\theta)A_i$, $b=(\operatorname{id}\otimes\theta)B_i$, and $c_j=\theta(z_j)$, $c_k=\theta(z_k)$. Equation (24) gives

\[
aw_j+u_jb=c_jH,\qquad aw_k+u_kb=c_kH.
\tag{25}
\]

These equations hold for every $\theta$, including those for which some of $a,b,c_j,c_k$ vanish.

Suppose first that both pairs $u_j,u_k$ and $w_j,w_k$ are independent. Quotienting (25) puts $a$ and $b$ in their respective two-dimensional spans. Write $a=xu_j+yu_k$ and $b=zw_j+vw_k$. Comparing coefficients in the first equation yields

\[
x+z=0,\qquad y=v=c_j,
\tag{26}
\]

and the second yields

\[
x=z=c_k,\qquad y+v=0.
\tag{27}
\]

Since two is invertible, $x=y=z=v=0$. This holds for every $\theta$, forcing $A_i=B_i=0$, a contradiction.

Next suppose $u_j,u_k$ are independent and $w_k=\lambda w_j$. Put $w=w_j$ and $h=\lambda u_j+u_k$. Quotienting the first equation of (25) by $F w$ forces $b=\eta w$. The equations reduce to

\[
a+\eta u_j=c_jh,\qquad \lambda a+\eta u_k=c_kh.
\tag{28}
\]

Subtracting $\lambda$ times the first from the second gives

\[
\eta(u_k-\lambda u_j)=(c_k-\lambda c_j)(u_k+\lambda u_j).
\tag{29}
\]

The vectors $u_k-\lambda u_j$ and $u_k+\lambda u_j$ are independent, since $\lambda\ne0$ and the characteristic is not two. Thus $\eta=0$ for every $\theta$, which would make $B_i=0$.

If $u_k=\rho u_j$ and $w_j,w_k$ are independent, quotienting instead by $F u_j$ gives $a=\eta u_j$. Eliminating $b$ yields

\[
\eta(w_k-\rho w_j)=(c_k-\rho c_j)(w_k+\rho w_j).
\tag{30}
\]

The vectors $w_k-\rho w_j$ and $w_k+\rho w_j$ are independent, so $a=0$ for every $\theta$, contradicting $A_i\ne0$.

Only the case in which both root pairs are dependent remains. Write $u_k=\rho u_j$, $w_k=\lambda w_j$, and put $u=u_j$, $w=w_j$. Then $H=(\lambda+\rho)uw$, with $\lambda+\rho\ne0$. In the uncontracted equation $A_iw+uB_i=Hz_j$, quotienting by $F u$ proves $A_i\in F u\otimes V_i$. Quotienting by $F w$ proves $B_i\in F w\otimes V_i$. Together with (19), these are exactly the common root-line conditions (14). The two leaves already aligned in (19) supply the required leaf condition.

We have proved the necessity direction of Theorem 3.1 over an infinite field. The dimension bound itself is the characteristic-free statement of Theorem 2.1.

## 6. Converse and descent to arbitrary fields

Assume (14), and suppose $b_2=\lambda_2a_2$, $b_3=\lambda_3a_3$. Cancelling the common root factors $u,w$, the three complementary tensors are

\[
d_1=(\lambda_2+\lambda_3)a_2a_3,\qquad
d_2=(\lambda_3a_1+b_1)a_3,\qquad
d_3=(\lambda_2a_1+b_1)a_2.
\tag{31}
\]

All are nonzero by hypothesis. In particular, $\lambda_2+\lambda_3\ne0$. Quotienting a relation by $F a_2$ and $F a_3$ shows that $n_2=sa_2$ and $n_3=ta_3$. The remaining equation is precisely (16). Every choice of $s,t$ satisfies it, proving sufficiency and the claimed parameterization over any field of characteristic different from two.

For completeness, let $F$ now be finite and extend scalars to an algebraic closure $E$. This is an infinite field of the same characteristic. Tensor nonvanishing and the rank of the linear map $\Phi$ are preserved under field extension. Consequently

\[
R_E=R\otimes_F E,\qquad \dim_E R_E=\dim_F R.
\tag{32}
\]

The general upper bound already holds over $F$. If $\dim_F R=2$, then $\dim_E R_E=2$. The infinite-field argument of Sections 4 and 5, applied over $E$, gives common root lines and at least two aligned leaves over $E$. These conditions descend to $F$, as follows.

Define the aggregate root image to be the sum of the root images of the three $A_i$. Its dimension is the rank of a matrix with entries in $F$, obtained by concatenating the three contraction maps. Its rank over $E$ is one, so its rank over $F$ is also one. Thus the common root line has a nonzero generator $u\in U$. The same argument gives $w\in W$ for the $B_i$.

For each aligned leaf, the sum of the leaf images of $A_i$ and $B_i$ also has rank one after extending scalars, hence already has rank one over $F$. Writing the blocks with the chosen $u,w$ therefore gives dependent $a_i,b_i$ over $F$. This proves the necessity conditions over $F$. The explicit converse above completes the proof of Theorem 3.1.

## 7. Determinant tensors and characteristic two

There is a block-level family criterion when the matching sum is alternating. Let $E=\bigoplus_{i=1}^nV_i$, fix $n-1$ rows $A_{ai}\in U_a\otimes V_i$, and put $X=\bigotimes_{a=1}^{n-1}U_a$. Let $D_i^{\det}$ be $(-1)^{i+1}$ times the determinant tensor of the fixed rows with column $i$ deleted. The last-row determinant differs from $\sum_i C_iD_i^{\det}$ only by the common sign $(-1)^{n-1}$, which does not affect its kernel. Define the combined contracted-row space

\[
H=\sum_{a=1}^{n-1}\operatorname{im}\left(
U_a^*\longrightarrow E,\quad
\alpha\longmapsto((\alpha\otimes\operatorname{id})A_{ai})_{i=1}^n
\right).
\tag{33}
\]

**Theorem 7.1.** Over every field, assume $D_i^{\det}\ne0$ for all $i$. For the relation space of these signed complementary tensors,

\[
\dim R=n-1\quad\Longleftrightarrow\quad\dim H=n-1.
\tag{34}
\]

When these conditions hold, $R=H$. Individual edge blocks may vanish.

*Proof.* Introduce independent variables for the coordinates of a covector at each root and let $L$ be their rational-function field. Contract each root with its formal covector. The fixed rows become tuples $a_1,\ldots,a_{n-1}\in E\otimes_F L$. Every contracted complementary tensor $d_i$ is nonzero: its root-variable coefficients are precisely the coordinates of the nonzero tensor $D_i^{\det}$. The determinant identities put each $a_a$ in the contracted relation kernel. A nonzero complementary minor shows that these $n-1$ rows are independent over the leaf rational-function field over $L$, hence over $L$.

Suppose $\dim R=n-1$. The contracted kernel contains $R\otimes_F L$, also of dimension $n-1$. Theorem 2.1 over $L$ bounds the contracted kernel by $n-1$, so it equals $R\otimes_F L$. In particular every $a_a$ belongs to that space. Projecting its expression as a linear combination of independent root variables into $E/R$ forces every coefficient row into $R$. Hence $H\subseteq R$. The $n-1$ independent formal rows lie in $H\otimes_F L$, giving $\dim H\geq n-1$, and thus $H=R$.

Conversely suppose $\dim H=n-1$, and choose a basis as the rows of $M$. Every contraction of each fixed row lies in $H$, and the rows of $M$ are a basis of $H$. Consequently each fixed tensor row has a unique expansion

\[
A_{ai}=\sum_{b=1}^{n-1}u_{ab}M_{bi},\qquad u_{ab}\in U_a.
\tag{35}
\]

Multilinearity and alternation give $D_i^{\det}=g\Delta_i$, where $\Delta_i$ is the signed minor of $M$ and

\[
g=\sum_{\sigma\in\mathfrak S_{n-1}}\operatorname{sgn}(\sigma)
u_{1,\sigma(1)}\otimes\cdots\otimes u_{n-1,\sigma(n-1)}.
\tag{36}
\]

The assumed nonvanishing of all $D_i^{\det}$ forces $g\ne0$ and all $\Delta_i\ne0$. Theorem 2.1 now gives $R=H$ and the required dimension.

In characteristic two signs disappear. Therefore Theorem 7.1 applies to the unsigned perfect-matching tensor of every $K_{n,n}$. For nonzero complementary tensors, it classifies the fixed edge blocks realizing the maximal last-row kernel in that characteristic, including patterns with zero edge blocks.

**Corollary 7.2.** For $n=3$ in characteristic two, assume all $D_i=A_jB_k+A_kB_j$ are nonzero. Then $\dim R=2$ exactly when the sum of the images of the two root-contraction maps into $V_1\oplus V_2\oplus V_3$ has dimension two. Equivalently, there are independent triples $p=(p_i),q=(q_i)$ and root vectors $u,u'\in U$, $w,w'\in W$ such that

\[
A_i=up_i+u'q_i,\qquad B_i=wp_i+w'q_i,
\tag{37}
\]

with $uw'+u'w\ne0$ and $p_jq_k+q_jp_k\ne0$ for each complementary pair. In this case $R=\operatorname{span}\{p,q\}$.

*Proof.* Apply Theorem 7.1 and write both tensor rows in a basis $p,q$ of $H$. Expanding (37) gives

\[
D_i=(uw'+u'w)(p_jq_k+q_jp_k).
\tag{38}
\]

Conversely this formula and the signed-minor identities give two independent relations, which form the whole kernel by Theorem 2.1. Individual components or root vectors in (37) may vanish. By (38), the displayed nonvanishing conditions are equivalent to the standing requirement that every $D_i$ be nonzero.

## 8. A normal form when an edge block vanishes

Return to three leaves, over any field, and continue to assume every $D_i=A_jB_k+A_kB_j$ is nonzero. If at least one block vanishes, interchange the rows if necessary and permute leaves so that $A_1=0$. Interchanging the rows interchanges the names $U$ and $W$ and changes only the order of the two root slots in each $D_i$.

**Theorem 8.1.** Under these hypotheses, $\dim R=2$ if and only if there are nonzero $u\in U$, $w\in W$, $a_2\in V_2$, $a_3\in V_3$, $b_1\in V_1$, and arbitrary $v\in W$, $b_2\in V_2$, $b_3\in V_3$, such that

\[
\begin{aligned}
A_1&=0,& A_2&=ua_2,& A_3&=ua_3,\\
B_1&=wb_1,& B_2&=wb_2+va_2,& B_3&=wb_3-va_3,
\end{aligned}
\tag{39}
\]

and $a_2b_3+b_2a_3\ne0$. In this case

\[
\begin{aligned}
D_1&=uw(a_2b_3+b_2a_3),&
D_2&=uwb_1a_3,&D_3&=uwb_1a_2,\\
R&=\operatorname{span}\{(0,a_2,-a_3),(b_1,-b_2,-b_3)\}.
\end{aligned}
\tag{40}
\]

*Proof.* Suppose first that $\dim R=2$. Since $D_2=A_3B_1$ and $D_3=A_2B_1$ are nonzero, $A_2,A_3,B_1$ are nonzero. Theorem 2.1 gives a common root factor $g\in U\otimes W$. Thus each $D_i$ has rank one across the combined-root versus combined-leaf flattening.

For $A\in U\otimes V_k$ and $B\in W\otimes V_j$, that flattening of $AB$ is the tensor product of their two linear maps, so its rank is $\operatorname{rank}(A)\operatorname{rank}(B)$. This follows over every field by reducing both maps to identity blocks and zero blocks. Applying it to $D_2,D_3$ makes $A_2,A_3,B_1$ rank one. Write $B_1=wb_1$, $A_2=u_2a_2$, $A_3=u_3a_3$. The two root-image lines $F(u_2w)$ and $F(u_3w)$ both equal $Fg$. Absorbing a nonzero scalar into one leaf factor gives $u_2=u_3=u$.

Now $D_1\in F(uw)\otimes V_2\otimes V_3$. Quotienting $W$ by $Fw$ therefore gives

\[
a_2\overline B_3+\overline B_2a_3=0.
\tag{41}
\]

Quotient $V_2$ by $Fa_2$ to obtain $\overline B_2=\overline v a_2$; similarly $\overline B_3=\overline v' a_3$. Since $a_2a_3\ne0$, (41) gives $\overline v'=-\overline v$. Lift $\overline v$ to $v\in W$. The residual blocks lie in $Fw\otimes V_i$, which gives (39). Nonvanishing of $D_1$ is exactly $a_2b_3+b_2a_3\ne0$.

Conversely expansion of (39) cancels the $v$ terms and gives (40). Both displayed triples are relations. They are independent because the second has nonzero first component and the first does not. Theorem 2.1 makes them a basis. The blocks $B_2$ or $B_3$ may vanish; no additional zero-pattern exclusion is needed.

Theorem 3.1, Corollary 7.2 and Theorem 8.1 now give a complete classification of the equality $\dim R=2$ for three matching complementary tensors: use Corollary 7.2 in characteristic two; in other characteristics use Theorem 3.1 when all six blocks are nonzero and Theorem 8.1 otherwise. Theorem 8.1 also applies in characteristic two, so those descriptions agree on their overlap. We do not impose nonzero blocks on the general relation theorem, nor classify cases in which a complementary tensor vanishes.

## 9. Completion with specified attachments

Let $N$ have positive dimension $m$, and let $D_i$ satisfy (3). For the map (2), tensoring over a field is exact, so

\[
\ker\Psi=N\otimes R.
\tag{42}
\]

If only the blocks indexed by a nonempty set $J\subseteq\{1,\ldots,n\}$ remain unknown, put

\[
R_J=R\cap\bigoplus_{j\in J}V_j,\qquad
X_J=X\otimes\bigotimes_{i\notin J}V_i.
\tag{43}
\]

**Proposition 9.1.** For compatible specified blocks and an attainable output, the remaining completion fiber is an affine translate of $N\otimes R_J$. Its dimension is at most $m(|J|-1)$. For $|J|\geq2$, this maximum occurs exactly when the $D_j$, viewed as complementary tensors with root space $X_J$, have the signed-minor form of Theorem 2.1. For $|J|=1$ the remaining block is unique.

*Proof.* Subtract any one solution. The resulting homogeneous map is $\operatorname{id}_N$ tensored with the restriction of $\Phi$ to the coordinates in $J$. Absorb the other leaf factors into $X_J$ and apply Theorem 2.1. When $|J|=1$, tensoring the remaining vector with nonzero $D_j$ is injective.

In particular, these conclusions apply to every $K_{n,n}$ whose complementary matching tensors are nonzero. They give the sharp bound $m(n-1)$ for an entirely unknown last row, and they show that $n-1$ known blocks always determine the remaining one, when compatible.

**Corollary 9.2.** Any nonempty completion fiber with exactly two unknown blocks $C_j,C_k$ is either a single point or has dimension $m$. The latter case occurs exactly when there are nonzero $G\in X_J$, $p_j\in V_j$, $p_k\in V_k$ with

\[
D_j=Gp_k,\qquad D_k=Gp_j.
\tag{44}
\]

The output-preserving perturbations are then $\Delta C_j=T\otimes p_j$, $\Delta C_k=-T\otimes p_k$, with $T\in N$.

*Proof.* This is the two-column case of Theorem 2.1. Directly, a nonzero relation $v_jD_j+v_kD_k=0$ has both components nonzero. Contracting at leaf $j$ with a functional taking $v_j$ to one, and then at leaf $k$, forces a common factor and gives (44), after absorbing a sign. The leaf images of the nonzero tensors then fix the component lines, so the relation space is one-dimensional. Conversely the displayed perturbations cancel.

For three matching tensors in characteristic different from two, assume throughout the rest of this paragraph that all six blocks and all three $D_i$ are nonzero. Proposition 9.1 and Theorem 3.1 give a fiber of dimension $2m$ exactly when (14) and at least two aligned leaf pairs hold. If either aggregate root image has dimension greater than one, the fiber dimension is at most $m$. Here and below, the equality conditions of Theorem 3.1 include all its standing hypotheses, in particular $D_i\ne0$; alignment alone does not imply them.

Under those equality conditions write, as in (16),

\[
c=\lambda_2+\lambda_3,\qquad
\ell_3=\lambda_3a_1+b_1,\qquad \ell_2=\lambda_2a_1+b_1.
\tag{45}
\]

All three quantities are nonzero because all $D_i$ are nonzero. The complementary tensors and all output-preserving perturbations are

\[
D_1=cuw a_2a_3,\qquad D_2=uw\ell_3a_3,\qquad D_3=uw\ell_2a_2,
\tag{46}
\]

\[
\begin{aligned}
\Delta C_2&=S\otimes a_2,&\Delta C_3&=T\otimes a_3,\\
\Delta C_1&=-c^{-1}(S\otimes\ell_3+T\otimes\ell_2),&S,T&\in N.
\end{aligned}
\tag{47}
\]

**Corollary 9.3.** In this maximal three-leaf case, knowing $C_1$ removes all ambiguity exactly when $\ell_2,\ell_3$ are independent; otherwise an $m$-dimensional ambiguity remains. Knowing $C_2$ alone or $C_3$ alone always leaves an $m$-dimensional ambiguity. Equivalently, one known attachment removes the ambiguity exactly when it is at a leaf whose pair $(a_i,b_i)$ is independent and the alignment ratios at the other two leaves differ. If all three leaf pairs are aligned, no single attachment suffices.

*Proof.* Fixing $C_1$ imposes $S\otimes\ell_3+T\otimes\ell_2=0$. Independence forces $S=T=0$; dependence of the two nonzero vectors leaves one free vector in $N$. Fixing $C_2$ gives $S=0$ and leaves $T$ free, and fixing $C_3$ gives the symmetric conclusion. Finally, $\ell_2,\ell_3$ are independent exactly when $a_1,b_1$ are independent and $\lambda_2\ne\lambda_3$. This proves all assertions.

Formulas (46)--(47) and this corollary hold in every characteristic whenever the common-root form, alignment and $D_i\ne0$ are assumed; only their necessity as a description of all six-nonzero-block maximal kernels requires characteristic different from two. Corollary 9.2 is more general than the known-attachment criterion and requires no matching classification.

## 10. A sharp cut-rank obstruction using matching rigidity

We give an application in which the necessity of Theorem 3.1 is essential to the proof. Let $F$ have characteristic different from two, let $V_1,\ldots,V_8$ be vertex spaces, and let $r=\dim V_8>0$. On the graph with edge set

\[
\begin{aligned}
\mathcal E=\{&13,15,16,17,18,24,25,26,27,28,\\
&35,36,37,38,45,46,47,48,57,68\},
\end{aligned}
\tag{48}
\]

put blocks $B_{ab}\in V_a\otimes V_b$. All other edge blocks are zero. Write $P$ for the perfect-matching tensor, and $C_{ab}$ for the matching tensor after deleting vertices $a,b$, whether or not $B_{ab}$ vanishes. The cut rank across $S\mid S^c$ is the matrix rank of the corresponding tensor flattening.

Fix all blocks away from vertex 2. Assume the six blocks $B_{35},B_{36},B_{37},B_{45},B_{46},B_{47}$ and the following three tensors are nonzero:

\[
\begin{aligned}
D_5&=B_{36}B_{47}+B_{37}B_{46},\\
D_6&=B_{35}B_{47}+B_{37}B_{45},\\
D_7&=B_{35}B_{46}+B_{36}B_{45}.
\end{aligned}
\tag{49}
\]

Define a map on $V_4\oplus V_5\oplus V_6\oplus V_7$ and its kernel by

\[
q(n_4,n_5,n_6,n_7)=n_4B_{36}B_{57}+n_5D_5+n_6D_6+n_7D_7,
\qquad \mathcal K=\ker q.
\tag{50}
\]

**Theorem 10.1.** Suppose $\dim\mathcal K=2$ and every element of $\mathcal K$ has vertex-4 component $n_4=0$. Then there is a line $L_4\subset V_4$, determined by the fixed blocks, such that every choice of the blocks at vertex 2 satisfying the actual cofactor constraint $C_{18}=0$ obeys

\[
\operatorname{rank}_{\{4,8\}\mid\{1,2,3,5,6,7\}}
((\pi_4\otimes\operatorname{id})P)\leq1,
\qquad \pi_4:V_4\to V_4/L_4,
\tag{51}
\]

and consequently the same cut rank of $P$ is at most $r+1$. Both bounds are attained over every field of characteristic different from two, for every $r\geq1$.

*Proof of the bounds.* The relation space on coordinates $5,6,7$ is $\mathcal K$ with its zero $V_4$-coordinate omitted, and has dimension two. Apply Theorem 3.1 with roots at vertices 3 and 4. Its necessity conclusion puts the vertex-4 images of $B_{45},B_{46},B_{47}$ in one line $L_4$.

Deleting vertices 1 and 8 leaves the seven perfect matchings permitted by the graph, represented by

\[
C_{18}=B_{24}B_{36}B_{57}+B_{25}D_5+B_{26}D_6+B_{27}D_7.
\tag{52}
\]

Thus $C_{18}=0$ puts every $V_2$-coordinate row of $(B_{24},B_{25},B_{26},B_{27})$ in $\mathcal K$. The hypothesis on its $V_4$-component forces $B_{24}=0$. Expansion by the partner of vertex 4 now gives

\[
P=B_{45}C_{45}+B_{46}C_{46}+B_{47}C_{47}+B_{48}C_{48}.
\tag{53}
\]

The first three terms vanish after applying $\pi_4$, leaving $\overline B_{48}\otimes C_{48}$, a single product across the stated cut. This proves (51). The kernel of $V_4\otimes V_8\to(V_4/L_4)\otimes V_8$ has dimension $r$. Applying that quotient to the flattening image can lower its rank by at most $r$, giving the bound $r+1$.

*Sharpness.* Over any field of characteristic different from two, choose bases

\[
\begin{aligned}
V_1&=\langle v\rangle,&V_3&=\langle u\rangle,&V_4&=\langle w,z\rangle,\\
V_5&=\langle p,q\rangle,&V_6&=\langle a\rangle,&V_7&=\langle e,f\rangle,\\
V_8&=\langle r_1,\ldots,r_r\rangle,&
V_2&=\langle t,h_1,\ldots,h_r\rangle.
\end{aligned}
\tag{54}
\]

Set

\[
\begin{aligned}
B_{35}&=up,&B_{36}&=ua,&B_{37}&=ue,\\
B_{45}&=wp,&B_{46}&=wa,&B_{47}&=wf,\\
B_{57}&=qe,&B_{13}&=vu,&B_{48}&=zr_1,&B_{68}&=ar_1.
\end{aligned}
\tag{55}
\]

All other fixed blocks away from vertex 2 are zero. Then

\[
D_5=uw a(f+e),\qquad D_6=uw p(f+e),\qquad D_7=2uwpa
\tag{56}
\]

are nonzero, and direct comparison of coefficients yields

\[
\mathcal K=\{(0,xp,ya,-(x+y)(e+f)/2):x,y\in F\}.
\tag{57}
\]

To verify exactness, write $n_4=\alpha w+\beta z$ and $n_5=xp+\gamma q$. After removing the nonzero $u,a$ factors, the $zqe$ coefficient first gives $\beta=0$, the $wqf$ coefficient gives $\gamma=0$, and the $wqe$ coefficient gives $\alpha=0$. The remaining $p$ coefficient determines $n_7$ as in (57).

Finally choose

\[
B_{24}=B_{25}=0,\qquad B_{26}=ta,\qquad
B_{27}=-t(e+f)/2,\qquad B_{28}=\sum_{i=1}^r h_ir_i.
\tag{58}
\]

Equation (57) verifies $C_{18}=0$. Since vertex 1 has only edge 13 with nonzero block, the surviving full matchings are $13/26/48/57$, $13/27/45/68$, and $13/28/46/57$. Removing the fixed nonzero factors $v,u,a$, their tensor across the cut is

\[
(zr_1)\otimes(tqe)+
\sum_{i=1}^r(wr_i)\otimes
\left(h_iqe-\delta_{i1}tp(e+f)/2\right).
\tag{59}
\]

The $r+1$ left factors are independent. The right factors are independent as well: comparison of the $h_i$ components first makes every coefficient in the sum zero, after which the nonzero $tqe$ factor makes the remaining coefficient zero. Hence the cut rank is $r+1$, and its quotient rank is one.

When $(\dim V_4-1)r=1$, the quotient rank bound follows already from the cut dimensions; the family above gives nontrivial rank restrictions for $r>1$. The example permits zero allowed blocks, as the theorem does. The six specified matching blocks and the three tensors (49) are explicitly assumed nonzero. The kernel hypothesis also forces $B_{57}\ne0$: otherwise every vector supported at vertex 4 would belong to $\mathcal K$, contradicting its zero $V_4$-coordinate property. The theorem is a constraint on attainable outputs under an explicit local cofactor condition; it assumes no special target tensor.

## 11. Sharpness and boundary cases

The general last-row bound is sharp for every order and every field. Choose nonzero $u_a\in U_a$, $v_i\in V_i$, and take the scalar coefficient matrix $B=[I_{n-1}\mid\mathbf1]$. Set $E_{ai}=B_{ai}u_av_i$. Every complementary permanent of $B$ equals one: deleting its last column leaves the identity; deleting column $i<n$ forces row $i$ to use the last column and every other row its own identity column. Consequently

\[
D_i=(u_1\cdots u_{n-1})\prod_{j\ne i}v_j\ne0.
\tag{60}
\]

For each $i<n$, the tuple supported on $i,n$ with components $v_i,-v_n$ is a relation. These $n-1$ relations are independent, giving a last-row fiber of dimension $m(n-1)$. More precisely, quotienting the relation at leaf $i$ by $Fv_i$ shows that its $i$th component lies in $Fv_i$, since all the other summands vanish in that quotient. Therefore

\[
R=\{(x_iv_i)_{i=1}^n:\sum_i x_i=0\}.
\]

For every nonempty subset $J$, its supported part $R_J$ has dimension $|J|-1$. Thus the same family attains all the subset-completion bounds of Proposition 9.1. For $n\geq3$ this family contains zero edge blocks; at $n=2$ its scalar matrix is $[1\ 1]$. Its nonvanishing claim concerns the complementary tensors.

For three leaves in characteristic different from two, all three kernel dimensions occur with six nonzero blocks. Choose common nonzero root factors $u,w$ and independent $e_i,f_i\in V_i$. Taking $A_i=ue_i$, $B_i=wf_i$ at all leaves gives dimension zero by Lemma 4.1. Taking those choices at leaves 1 and 2 and $A_3=ue_3$, $B_3=we_3$ gives dimension one. Taking $A_i=ue_i$, $B_i=we_i$ at every leaf gives

\[
R=\{(x_1e_1,x_2e_2,x_3e_3):x_1+x_2+x_3=0\}.
\tag{61}
\]

In characteristic different from two, the bound of $m$ when an aggregate root image has dimension greater than one is also sharp. Let $V_i=Fp_i$, choose independent $u,v\in U$ and nonzero $w\in W$, and put $A_1=up_1$, $A_2=up_2$, $A_3=vp_3$, $B_i=wp_i$. The three complementary root factors are $(u+v)w,(u+v)w,2uw$. They span a two-dimensional space, so $\dim R=1$.

Characteristic two permits different block geometry. With common root factors and independent $a_i,b_i$ at each leaf, the combined row space has dimension two, and $R=\{(sa_i+tb_i)_i:s,t\in F\}$, with no aligned leaf pair. Root lines can fail too: take independent $u_1,u_2$, nonzero $w$, independent $e,f\in V_1$, and generators $p_2,p_3$ of one-dimensional leaf spaces, and set

\[
\begin{aligned}
A_1&=u_1(e+f)+u_2f,&A_2&=u_2p_2,&A_3&=u_1p_3,\\
B_1&=we,&B_2&=wp_2,&B_3&=wp_3.
\end{aligned}
\tag{62}
\]

In characteristic two, with $g=(u_1+u_2)w$, the complementary tensors are $gp_2p_3$, $gfp_3$, $g(e+f)p_2$, and

\[
R=\{(sf+t(e+f),sp_2,tp_3):s,t\in F\}.
\tag{63}
\]

Here all blocks are nonzero and $A_1$ has rank two. This is included in Corollary 7.2, rather than excluded by a characteristic assumption. In other characteristics the same blocks give $D_2=(2u_1e+(u_1+u_2)f)wp_3$ and a one-dimensional kernel.

Nonvanishing of the complementary tensors is essential even for the general bound. If $D_1=0$, then $V_1\oplus0\oplus\cdots\oplus0\subset R$. For three matching leaves in characteristic different from two, this can happen with six nonzero blocks: take common root factors, independent $a_1,b_1$, and $b_2=a_2$, $b_3=-a_3$. Then $D_1=0$ whereas $D_2,D_3\ne0$, and $\dim V_1$ can be arbitrarily large.

## 12. Polynomial interpretation

For the two-row matching construction, choose root variable groups $x,y$ and leaf variable groups $z_i$. The admissible relation equation is

\[
\sum_{i=1}^3 v_i(z_i)
\bigl(A_j(x,z_j)B_k(y,z_k)+A_k(x,z_k)B_j(y,z_j)\bigr)=0,
\qquad\{i,j,k\}=\{1,2,3\}.
\tag{64}
\]

It has degree one in each root group and each leaf group. It is the expansion of the $K_{3,3}$ permanent along a third row independent of the first two root groups.

Here a generic polynomial syzygy has coefficients in the polynomial ring $F[t_{ai}]$ on the independent entries of a generic matrix. Under the substitution of these entries by the bilinear edge forms, each entry acquires total root degree one. Every positive-degree monomial in the generic entries therefore acquires positive total root degree. The root-degree-zero part of any specialized polynomial coefficient is a scalar. A nonzero admissible coefficient $v_i(z_i)$ instead has root degree zero and leaf degree one. Thus an admissible relation is not a direct polynomial specialization of a generic syzygy of the subpermanents studied in [2,3,5]. This assertion concerns polynomial specialization; no assertion is made about localized formulas allowing division.

Theorem 2.1 concerns complementary tensors of arbitrary order. For nonzero complementary tensors, Theorem 1.1 collects the complete classification of maximal three-leaf matching kernels in terms of their original blocks. Under the same complementary-nonvanishing hypothesis, Theorem 7.1 gives the corresponding block criterion for determinant tensors of every order, and for unsigned matching tensors in characteristic two. A block-level classification for unsigned $K_{n,n}$ in other characteristics and $n>3$ is not asserted. The determinant-family proof uses the vanishing of an alternating sum with two identical rows. This mechanism fails for unsigned sums outside characteristic two: the permanent of two identical rows $(x,y)$ is $2xy$, which is not the zero polynomial. The three-leaf proof instead uses its specific two-term complementary tensors and the exhaustive root-pair cases in Section 5. The general cofactor criterion of Theorem 2.1 remains valid for every $n$, but these arguments do not translate it into a classification of arbitrary higher-order unsigned edge blocks.

## AI generation, contributions and verification

This manuscript and its mathematical arguments were generated and revised through an AI-led workflow using OpenAI Codex and Anthropic Claude. The systems proposed results, generated proofs and prose, searched the literature, reviewed the arguments and produced verification code. Their role was substantive mathematical generation, not solely language editing. Claude's review rounds supplied a characteristic-free three-tensor bound and a two-unknown-block criterion; Codex developed the arbitrary-order extensions, assembled the block classifications and the cut-rank application, and prepared the manuscript. Claude's review of version 3 also supplied the modified sharp family used in Theorem 10.1, the subset-sharpness formula of Section 11 and several of the references. The project records also contain earlier AI-generated matching and signed-minor arguments.

The human user directed the project and selected the author name Ignoramus. No independent human mathematical verification is claimed. Checks performed by the generating systems and their agents are AI checks, not external peer review. The proofs are included in full and do not depend on the finite computations. A complete model-version history for all generation and review steps has not been verified. No AI system is listed as an author.

## References

[1] M. Krenn, X. Gu, and A. Zeilinger. Quantum Experiments and Graphs: Multiparty States as Coherent Superpositions of Perfect Matchings. Physical Review Letters 119 (2017), no. 24, 240403. https://doi.org/10.1103/PhysRevLett.119.240403

[2] F. Gesmundo, Hang (Amy) Huang, H. Schenck, and J. Weyman. Bernstein-Gelfand-Gelfand meets geometric complexity theory: resolving the $2\times2$ permanents of a $2\times n$ matrix. Transactions of the American Mathematical Society 378 (2025), no. 5, 3573-3596. https://doi.org/10.1090/tran/9376. Preprint version used for lemma numbering: arXiv:2312.12247v2, https://arxiv.org/html/2312.12247v2

[3] J. Zoromski. Equivariant Syzygies of the Ideal of $2\times2$ Permanents of a $2\times n$ Matrix. arXiv:2502.05358 (2025). https://arxiv.org/abs/2502.05358

[4] B. Lovitz and F. Petrov. A generalization of Kruskal's theorem on tensor decomposition. Forum of Mathematics, Sigma 11 (2023), e27. https://doi.org/10.1017/fms.2023.20

[5] K. Efremenko, J. M. Landsberg, H. Schenck, and J. Weyman. On minimal free resolutions of sub-permanents and other ideals arising in complexity theory. Journal of Algebra 503 (2018), 8-20. https://doi.org/10.1016/j.jalgebra.2018.01.021

[6] D. Eisenbud, with a chapter by J. Sidman. Lectures on the Geometry of Syzygies. In Trends in Commutative Algebra, Mathematical Sciences Research Institute Publications 51 (2004), 115-152. https://eisenbud.github.io/papers/pdfs/2004-003.pdf

[7] R. Rado. A theorem on independence relations. Quarterly Journal of Mathematics os-13 (1942), no. 1, 83-89. https://doi.org/10.1093/qmath/os-13.1.83

[8] A. Conca, E. De Negri, and E. Gorla. Universal Gröbner bases and Cartwright-Sturmfels ideals. International Mathematics Research Notices 2020, no. 7, 1979-1991. https://doi.org/10.1093/imrn/rny075


[9] I. Le. Intersection Pairings for Higher Laminations. Algebraic Combinatorics 4 (2021), no. 5, 823-841. https://doi.org/10.5802/alco.182

[10] X. Gu, M. Erhard, A. Zeilinger, and M. Krenn. Quantum Experiments and Graphs II: Quantum Interference, Computation and State Generation. Proceedings of the National Academy of Sciences 116 (2019), no. 10, 4147-4155. https://doi.org/10.1073/pnas.1815884116

[11] L. Sunil Chandran, R. Gajjala, and A. M. Illickan. Krenn-Gu conjecture for sparse graphs. In 49th International Symposium on Mathematical Foundations of Computer Science (MFCS 2024), Leibniz International Proceedings in Informatics 306 (2024), 41:1-41:15. https://doi.org/10.4230/LIPIcs.MFCS.2024.41. Preprint version used for section numbering: arXiv:2407.00303v1, https://arxiv.org/html/2407.00303v1

[12] A. Conca, E. De Negri, and E. Gorla. Universal Gröbner bases for maximal minors. International Mathematics Research Notices 2015, no. 11, 3245-3262. https://doi.org/10.1093/imrn/rnu032
