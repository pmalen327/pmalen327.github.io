---
layout: post
title: 'Basic Classification of Operators in $C^*$-Algebras'
tags: []
description: ''
---

Ok I have finally migrated things over to a github.io repo and now things are infinitely
easier on my end. So as a sort of "test-drive", I will walk through the basic
classification of operators in $C^\*$-algebras with respect to the given involution.
I will also give some statements of some fundamental theorems in operator algebra
theory.

Let's start small with the definition.

<ins>**Def:**</ins> Let $A$ be a Banach algebra over a field $\mathbb{F}$ with an
involution $a \mapsto a^\*$. Then $A$ is a $C^\*$-algebra.

Note that I didn't really mention what the involution *does* or the requirements
therein. I will gloss over those for now but keep in mind there are certain properties
required by the involution. The only one to be concerned about for now it the
$C^\*$-identity $\|aa^\*\| = \|a^\*a\|$.

For an ideal $I \subset A$, the quotient algebra $A/I = \{a+I \mid a \in A \}$ is
also a $C^\*$-algebra with norm $\| a+I\| = \inf \{ \| a+x \| \mid x \in I\}$. Recall
also that an algebra is ***simple*** if its only ideals are trivial.

Now, the biggest and most foundational theorem in operator algebras.

<ins>**Thm: Gelfand-Naimark (Gelfand duality)**</ins> Every commutative $C^\*$-algebra
is isometrically isomorphic to an algebra $C_0(X)$ for a locally compact Hausdorff
space $X$.

As usual, $C_0(X)$ is the algebra of compactly supported functions on $X$. Further,
**every** commutative $C^\*$-algebra is isometrically isomorphic to a closed $C^\*$-
subalgebra of some $\mathcal B(H)$, the algebra of bounded linear operators on a 
Hilbert space $H$.

The Gelfand duality theorem is hugely important. Most $C^\*$-algebras are not necessarily
"nice" to work with but compactly supported functions are very nice to work with.
Gelfand duality gives us a robust way to bounce between the two. Note also that
we get an isometric isomorphism, so even the metric and norms are equivalent in some
way. The theory of compactly supported functions is extensive and runs very deep,
so identifying the right isomorphism allows us to work in $C^\*$-algebras as if we
were working in a more familiar function algebra.

I could spew operator algebra theorems all day, but my intent here is really just
to classify the most common/useful classes of operators in $C^\*$-algebras. First,
lets look at the spectrum of an operator and some neat properties.

<ins>**Def:**</ins> Let $A$ be a $C^\*$-algebra. Then for some $a \in A$, the ***spectrum***
of $a$ is the set
$$
\operatorname{sp}_A (a) := \{ \lambda \in \mathbb{C} \mid a - \lambda 1_A \text{  not invertible} \}
$$

The spectrum of an operator enjoys lots of nice properties.
The spectrum of an operator enjoys lots of nice properties:

$$
\begin{enumerate}
  \item $A = \{0\} \implies \operatorname{sp}_A (0) = \varnothing$
  \item $\operatorname{sp}_A (\lambda 1_A) = \{\lambda\}$
  \item $a$ is invertible iff $0 \notin \operatorname{sp}_A(a)$
  \item For a complex polynomial $P$, $\operatorname{sp}_A (P(a)) = P(\operatorname{sp}_A (a))$
  \item If $a$ is nilpotent then $\operatorname{sp}_A (a) = \{0\}$
  \item If $\varphi:A \to B$ is a morphism of complex unital algebras, then $\operatorname{sp}_B (\varphi(a)) \subseteq \operatorname{sp}_A (a)$
  \item If $(a,b) \in A \oplus B$ then $\operatorname{sp}_{A \oplus B}((a,b)) = \operatorname{sp}_A(a) \cup \operatorname{sp}_B(b)$
\end{enumerate}
$$

Studying the spectra of operators is once again a very deep and interesting field,
but beyond the context of this entry. Now, the basic classification of operators.
Let $a \in A$ be an operator in a $C^\*$-algebra $A$, then we can classify $a$ as
$$
\begin{itemize}
  \item \textbf{normal} if $ aa^* = a^*a $;
  \item \textbf{self-adjoint} if $ a^* = a $;
  \item \textbf{positive} if normal and $ \operatorname{sp}_A(a) \subseteq \mathbb{R}_+ $;
  \item \textbf{projection} if $ a^* = a = a^2 $.
\end{itemize}
$$

And we denote by $A^+$ the set of all positive operators in $A$. 

There are many more classifications of operators (trace class, Hilber-Schmidt etc.)
but the definitions are a little bit more involved. But you will not be able to read
a single paper in functional analysis or operator algebras without bumping into
the operator classifications given above. These are super important defintions and
the properties of each classification could each easily populate their own entry.

I don't have much more today, like I mentioned, this is mostly to get some kinks
worked out with git and markdown etc. but I figured I may as well mention something
foundational in operator theory and ultimately, noncommutative geometry.