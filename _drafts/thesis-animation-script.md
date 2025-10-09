---
layout: single
title:  "Mutation of Torsion Pairs via Extriangulated Hereditary Categories"
header:
  teaser: ""
categories: 
  - Jekyll
tags:
  - edge case
---

This is a script for an animated exposition of my PhD thesis. It is divided into four sections.
1. Algebras, modules and torsion pairs (Introduction & motivation)  [general public]
1. Cosilting complexes (Preliminaries) [undergraduate students]
1. $n$-Cosilting bijections and mutation [graduate students]
1. Mutation of torsion pairs [PhD students and researchers]

The prerequisites for the first three sections are the following.
1. Basic module theory; basic category theory (helpful); basic $\tau$-tilting theory (not essential)
2. The derived category of a module category; finite injective coresolutions in the derived category (helpful); the canonical $t$-structure (not essential)
3. Extriangulated categories; hereditary complete cotorsion pairs; silting subcategories; Aihara-Iyama mutation of silting subcategories (helpful)

Together, these three sections form the prerequisites for the final one.

# Algebras, module categories and torsion pairs

## Algebras

In the _field_ of abstract algebra, one of the main algebraic structures of interest is a generalization of a ring which is simply called an _algebra_.
>_[Throughout, all rings and algebras will be assumed to be associative and unital.]_
Recall that a ring is a commutative group endowed with an additional binary operation called _multiplication_ which is associative, has an identity element, and distributes with respect to the usual group operation. Thus, any ring can be thought of as being acted upon by the integers in a way that is compatible with the ring's group structure.
>_[Pause and *really* think this through before continuing; it is *crucial* for understanding what comes next.]_
Notice that the integers themselves also have a ring structure. From this perspective, we could more generally consider a ring which is acted upon by another ring in a way that is compatible with the first ring's group structure. This is what we call an _algebra_.
_>[Explicitely, we speak of an ''algebra over a ring $\ring$'' (or ''$\ring$-algebra'') for a given ring $\ring$.]_

In particular, when an algebra is acted upon by a field, it becomes a vector space over that field. However, this is no ordinary vector space, since the algebra's inherent ring structure means that we can multiply vectors, making it a particular case of interest.

## Module categories

### Representation theory

In general, an algebra's structure is very abstract and complex, so several methods have been developed in order to study them. For example, one method involves assigning a matrix to each element of an algebra in such a way that the available matrix operations correspond to actual operations in the algebra<, while being compatible with its overall structure>. An important caveat is that our understanding of the algebra will then be limited by how much of its strucure can actually be mimicked through a chosen set of matrices. Moreover, for any given algebra, many such correspondences usually exist, and each one of them will give us but a _linear approximation_ of the algebra's <overall> structure, which is known as a _representation_ of that algebra. This has both pros and cons; namely, we know that we have a wide _range_ of representations to study from, but _which ones should we focus on_?
>_[The subfield dedicated to studying algebras via their representations is known as the ''Representation Theory of Algebras''.]_

### Category theory

Well... what if it were possible to study _all_ representations of an algebra _at the same time_? The language of Category Theory allows us to do precisely this.

Plainly speaking, a category is a collection of objects with some common mathematical structure and maps between them which preserve this structure, such that each object has an identity map--which is trivially structure-preserving--and composition of maps is associative whenever possible.

### Module theory

Let us make a brief detour to introduce one more algebraic structure: modules. I promise it'll be worth it. Modules are simpler than algebras, but they can be introduced in a similar way: a _module_ is a commutative group which is acted upon by a ring in a way that is compatible with the former's group structure. 
_>[Explicitely, we speak of a ''module over a ring $\ring$'' (or ''$\ring$-module'') for a given ring $\ring$.]_

Notice that commutative groups are just modules over the ring of integers. Moreover, vector spaces over a field $\mathbbm{k}$ are just $\mathbbm{k}$-modules! Furthermore, any algebra over a ring is a module over the same ring if we just ''forget'' about the algebra's inherent ring structure. And here comes the real kicker...
>_[Again, pause and *really* think this through before continuing.]_
Remember _representations_, those structure-preserving correspondences we mentioned earlier? Well, with a little bit of work one can show that representations of an algebra and modules over the same algebra _actually coincide_! Thus, modules offer a way of studying representations of an algebra from a perspective which is much closure to the algebraic structures we are familiar with.
>_[The same holds more generally for representations of/modules over a ring .]_

In categorical language, we say that the category of representations of an algebra and the category of modules over the same algebra are _equivalent_. We can thus study the category of modules over an algebra as a way of understanding the structure of the algebra via the entirety of its representations.
_[For experts: In the following, ''modules'' will always refer to (not necessarily finitely generated) modules over a ring.]_

## Torsion pairs

In the _field_ of Homological Algebra, a torsion pair is a tool which allows us to decompose a category by ``twisting'' it into a pair of subcategories which are orthogonal, in the sense that there are no non-zero morphisms from one of them to the other, and which we can further ``untwist'', allowing us to recover the whole category. Each torsion pair provides a unique decomposition, by which being able to control them offers a powerful tool for the study of the category as a whole.

### $\tau$-tilting theory

Let $\Lambda$ be a finite-dimensional algebra over an algebraicaly closed field $\mathbbm{k}$.
>_[In essence, this means that $\Lambda$ is simultaneously a finite-dimensional vector space over $\mathbbm{k}$ and a ring in and of itself.]_

# Cosilting complexes

## Finite injective coresolutions in the derived category

Let us consider the derived category of our module category.
>_[In this exposition, ''derived category'' will always refer to the unbounded derived category.]_
Its objects are cochain complexes of modules, which we choose to visualize vertically, with their center fixed around degree zero and their positive degrees going in the upward direction. Notice that by this convention a positive shift will push a complex _downwards_.
>_[Again, pause and *really* think this through.]_

Recall that the heart of the canonical $t$-structure on our derived category is equivalent to the module category. 
>_[In this exposition, we consider objects in a category up to isomorphism.]_
This heart is just the subcategory of complexes concentrated in degree zero, so from now on we will identify modules with their inclusion into the derived category in this way. We can further identify these modules with their injective coresolutions, which by the previous convention are complexes of injective modules concentrated in degrees greater than or equal to zero. In particular, modules with finite injective coresolutions are bounded above. Since injective modules are closed under arbitrary direct products, it follows that finite injective coresolutions are closed under categorical products, which simply amounts to taking direct products of modules in each degree.

## ($n$)-Cosilting complexes

A finite injective coresolution $\omega$ is a _cosilting complex_ if it satisfies two conditions. The first is that there are no non-zero morphisms from any arbitrary product of copies of $\omega$ to any positive shift of $\omega$. The second is that all finite injective coresolutions can be generated by taking products of copies of $\omega$, as well as summands, extensions, and positive and negative shifts thereof. There is a small technicality involved with the second condition, since by our previous convention the subcategory of injective coresolutions is not closed under positive shifts. To circumvent this, we can more loosely consider finite injective coresolutions to be bounded complexes of injective modules, which we consider up to shifts by convention. From this viewpoint, the subcategory of all finite injective coresolutions is equal to the bounded homotopy category of injective modules, which is closed under products, summands, extensions and shifts in the derived category.

In particular, a cosilting complex which is an injective coresolution of finite length $n$ is called an $n$-_cosilting complex_. Since this implies that it is concentrated in $n+1$ degrees, it is also refered to as an $(n+1)$-_term complex_.

## Silting subcategories

It is apparent that a cosilting complex $\omega$ is intimately related to the subcategory of all products of copies of $\omega$, which becomes additive if we close it under summands. Let us denote the closure of $\omega$ under products and summands by $\text{Prod}(\omega)$ and, moreover, _its_ closure under summands, extensions, and positive and negative shifts by $\text{thick}(\text{Prod}(\omega))$. Since the Hom bifunctor, the shift functor and its inverse are all additive functors, it follows that, up to shifts, a cosilting complex is a bounded complex of injective modules which satisfies the following conditions
$$\text{Hom}_{\mathcal{D}(\text{Mod}(\ring))}(\text{Prod}(\omega),\text{Prod}(\omega)[>0])=0 \quad \text{and} \quad \text{thick}(\text{Prod}(\omega))=\mathcal{K}^b(\text{Inj}\ring),$$_
which can be rephrased by saying that $\text{Prod}(\omega)$ is a silting subcategory of $\mathcal{K}^b(\text{Inj}\ring)$. For this reason, two cosilting complexes $\omega$ and $\omega'$ are said to be _equivalent_ if $\text{Prod}(\omega)=\text{Prod}(\omega')$.

Since Aihara and Iyama have developed a general theory of mutation for silting subcategories of triangulated categories, we could try to mutate cosilting complexes by putting them in one-to-one correspondence with a certain subclass of silting subcategories, which would have to be product closed, and seeing if this operation restricts or can be adapted to this subclass. However, when mutating an $n$-cosilting complex in this way, the resulting cosilting complex would a priori not necessarily have to be $n$-cosilting.

# $n$-Cosilting bijections and mutation


