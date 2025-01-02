# Why read this book?

There are many books about tensors and/or differential forms, and probably all of them are written by people who know more about these concepts than me. So why read this book?

The reason is because the pedagogy in this book is superior, at least from the perspective of those who are dissatisfied with [presentations of mathematics that sacrifice understanding for logical or technical efficiency](https://github.com/rossgk2/physmath?tab=readme-ov-file#the-dreaded-efficency-pedagogy). I aim to give a *best* presentation of every topic covered. Examples of this in the book are:

* An intuitive definition for linear independence is used. A set of vectors is defined to be linearly independent if and only if every vector in the set is not in the span of all of the other vectors. The traditional definition of linear independence is proved to be equivalent to this alternative definition.
* A basis of a vector space is defined to be a spanning set for that vector space of minimal size. (The traditional approach of defining a basis to be a linearly independent spanning set has the downside of requiring a proof that the dimension of every finite-dimensional vector space is unique, which would ideally be an obvious fact that doesn't require a long proof). In the approach we use, it is an immediate consequence of minimality that dimension is unique. This alternative approach approach also uses the same idea as in the proof required by the traditional approach to prove that a set is a spanning set of minimal size if and only if it is a linearly independent spanning set, thus effectively switching a definition and a theorem from the traditional approach for pedadogical benefit.
* Extremely convenient notation for the matrix of a linear function $\mathbf{f}$ relative to bases $E$ and $F$, $\[\mathbf{f}(E)\]_F$, is used. I have not seen this notation used elsewhere.
* Tensors are presented in a linear algebra context before moving to the manifold context. Trying to learn tensors all at once in the manifold context is too much, in my opinion; there is plenty that needs investigation in the simpler setting of vector spaces. Most books on tensors take the approach that is "too much".
* The fundamental properties of tensor product spaces are made clear because we use an abstract implementation of the tensor product $\otimes$ that straightforwardly fulfills said properties. Most books that do address tensors in the linear algebra context get lost in implementation details. For instance, many books use the definition of a tensor product space in which $(f \otimes g)(\mathbf{v}\_1, \mathbf{v}\_2) = f(\mathbf{v}\_1) g(\mathbf{v}\_2)$. Readers can easily get distracted by this implementation detail and be led astray from realizing what is really important, which is the fact that the tensor product $\otimes$ appears to be a bilinear function.
  * Using abstract tensors makes the definitions of the various pushforward and pullback maps obvious. (The equivalence between the abstract tensor product space and the more common definition is also given, and the pushforward and pullback operations in this later space are deduced from the more understandable and  pushforward and pullback.)
* We explain tensor product spaces and dual spaces in the context of the key fact $\mathcal{L}(V \rightarrow V) \cong V \otimes V^{\*}$, which motivates using these concepts to define $(p, q)$ tensors. Typically, no such explanation about why tensor product spaces and dual spaces must be invented and involved is given. Most books also state the key fact *after* the definition of $(p, q)$ tensors and fail to emphasize its fundamental importance.
* Change of basis theorems for tensors and tangent vectors are easily understable because they can leverage the results of the earlier linear algebra chapter, which are stated using the intuitive notation $\[\mathbf{f}(E)\]_F$.
* The determinant is not immediately defined as the factor of multiplication on the top exterior power, as is done in most books that present this abstract characterization. Instead, the abstract characterization is proved as a theorem after establishing the more elementary characterization of the determinant as the unique multilinear alternating function $K^n \rightarrow K$, where $K$ is a field.
* The concept of orientation is properly built up from the ground up. The fact that the determinant of a set of column vectors gives the set's orientation is the culmination of theorems about definitions which formalize intuition, *not* a half-motivated definition. 
* Differential forms are defined by using an abstract wedge product analagous to the abstract tensor product.
  * The equivalence to the usual definition of differential form is also explained.
* The uncommon geometric definition of the exterior derivative involving flux through a parallelapiped is used and the most common algebraic definition is shown to be a consequence of this.

# Table of contents

Review sections:

1. Review of logic, proofs, and functions
2. Review of linear algebra

Part I: Multilinear algebra and tensors

3. A motivated introduction to tensors
4. Bilinear forms, metric tensors, and coordinates of tensors
5. Exterior powers, the determinant, and orientation

Part II: Calculus and basic topology

6. Review of calculus
7. Basic topology

Part III: Differential forms

8. Manifolds
9. Differential forms on manifolds

## Chapter 1: review of logic, proofs, and functions

As of Jan. 25 2021, an in-progress chapter on logic and proofs is now included in the book. Though incomplete, this section may still be helpful. In particular, a proof-writer of any level might appreciate the section on the implication operator =>, as this operator is often only halfway understood and badly explained. The chapter is complete up until the "Set difference and set complement" section. (A historical note: the content of this chapter that is complete was written in 2020, long before Jan. 25 2021; it is on Jan. 25 2021 that I decided to include this material in the compiled PDF). 

## Copyright

This textbook is intended to be downloaded and read for free. If you would like to repurpose the content of this book, please clearly state that you have done so and credit this textbook as a reference.
