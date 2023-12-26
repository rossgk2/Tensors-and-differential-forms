# Why read this book?

There are many books about tensors and/or differential forms, and probably all of them are written by people who know more about differential forms than me. So why read this book? Well, here is why.

* Extremely convenient notation for the matrix of a linear function $\mathbf{f}$ relative to bases $E$ and $F$, $\[\mathbf{f}(E)\]_F$, is given. I have not seen this notation used elsewhere.
* Tensors are presented in a linear algebra context before moving to the manifold context. Trying to learn tensors all at once in the manifold context is too much, in my opinion; there is plenty that needs investigation in the simpler setting of vector spaces. But this is how books on manifolds proceed.
* Too many books use the definition of a tensor product space in which $(f \otimes g)(\mathbf{v}\_1, \mathbf{v}\_2) = f(\mathbf{v}\_1) g(\mathbf{v}\_2)$. This implementation detail of this definition is distracting. We use the definition of an abstract tensor product space, which emphasizes the algebraic properties of tensors.
  * Using abstract tensors makes the definitions of the various pushforward and pullback maps obvious. (The equivalence between the abstract tensor product space and the more common definition, is also given, and the pushforward and pullback operations in this later space are deduced from the more understandable and  pushforward and pullback.)
* It is explained why $(p, q)$ tensors are defined to be what they are and it is explained why dual spaces and tensor product spaces are important. Unfortunately, I have found that no other book satisfactorily does this.
* Change of basis theorems for tensors and tangent vectors are easily understable because they can leverage the results of the earlier linear algebra chapter, which are stated using the intuitive notation $\[\mathbf{f}(E)\]_F$.
* The determinant is not immediately defined as the factor of multiplication on the top exterior power, as is done in most books that present this abstract characterization. Instead, the abstract characterization is proved as a theorem after establishing the more elementary characterization of the determinant as the unique multilinear alternating function on $K^n$, where $K$ is a field.
* Differential forms are defined by using an abstract wedge product analagous to the abstract tensor product.
  * The equivalence to the usual definition of differential form is explained.
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
