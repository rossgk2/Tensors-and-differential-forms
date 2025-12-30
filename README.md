# Why read this book?

There are many books about tensors and/or differential forms, and probably all of them are written by people who know more about these concepts than me. So why read this book?

The reason is because the pedagogy in this book is superior, at least from the perspective of those who are dissatisfied with [presentations of mathematics that sacrifice understanding for logical or technical efficiency](https://github.com/rossgk2/physmath?tab=readme-ov-file#the-dreaded-efficency-pedagogy). I aim to give a *best* presentation of every topic covered. There are many examples of this in each of the topics the book covers:

## Tensors
* Tensors are presented in a linear algebra context before moving to the manifold context. Trying to learn tensors all at once in the manifold context is too much, in my opinion; there is plenty that needs investigation in the simpler setting of vector spaces. Most books on tensors take the approach that is "too much".
* The fundamental property of tensor product spaces- that $\otimes$ appears to be a multilinear function- is made clear because we use an abstract implementation of the tensor product $\otimes$ that straightforwardly fulfills said property. Most books that do address tensors in the linear algebra context get lost in implementation details. For instance, many books use the definition of a tensor product space in which $(\phi \otimes \psi)(\mathbf{v}\_1, \mathbf{v}\_2) = \phi(\mathbf{v}\_1) \psi(\mathbf{v}\_2)$. Readers can easily get distracted by this implementation detail and be led astray from realizing what is really important, which is the fact that the tensor product $\otimes$ appears to be a multilinear function.
* We explain tensor product spaces and dual spaces in the context of the key fact $\mathcal{L}(V \rightarrow W) \cong V \otimes W^{\*}$, which allows for the natural next step of using the special case $\mathcal{L}(V \rightarrow V) \cong V \otimes V^{\*}$ to motivate defining a $(p, q)$ *tensor* to be an element of $V^{\otimes p} \otimes (V^{\*})^{\otimes q}$. Most books state the special case $\mathcal{L}(V \rightarrow W) \cong V \otimes V^{\*}$ *after* the definition of $(p, q)$ tensors and fail to emphasize that this fact is no coincidence.
   * It is even possible to gain intutition for the fact that there should exist a notion of $W^{\*}$ and of $V \otimes W^{\*}$ for which $\mathcal{L}(V \rightarrow W) \cong V \otimes W^{\*}$ is true, and to then invent the definitions of $W^{\*}$ and $\otimes$ so as to fulfill this wish. In my opinion, it's unfortunately a little too complicated to invent both of these concepts at once, so, the approach that this book takes is to first motivate tensor product spaces as providing the means to obtain linear functions from multilinear functions, notice that $\mathcal{L}(V \rightarrow W) \cong V \otimes \mathcal{L}(W \rightarrow K)$, and define $W^{\*} := \mathcal{L}(W \rightarrow K)$. After understanding this argument, though, one can clearly see the perspective that yes, both tensor product spaces and dual spaces can be seen as being invented to faciliate the expression of the fact $\mathcal{L}(V \rightarrow W) \cong V \otimes W^{\*}$.
* We organize three key natural isomorphisms pertaining to tensors that assist greatly. For some reason, these isomorphisms are scattered throughout other books and not organized together.
    * $\mathcal{L}(V_1 \times ... \times V_k \rightarrow W) \cong \mathcal{L}(V_1 \otimes ... \otimes V_k \rightarrow W)$
    * $\mathcal{L}(V \rightarrow W) \cong W \otimes V^*$
    * $(V \otimes W)^* \cong V^* \otimes W^*$
* When $g$ is a metric tensor on a vector space, we define $g^{ij}$, with upper indices, to be the coordinates of the induced metric tensor on the dual space. Since the induced metric tensor is a $(2, 0)$ tensor, use of upper indices is justified. The typical approach just defines $g^{ij}$ to be such that the matrix $(g^{ij})$ is the inverse of the matrix $(g_{ij})$ and does not explain why the indices are upper.
* Using an abstract implementation of the tensor product also has the advantage of making the definitions of the various pushforward and pullback maps obvious. (The equivalence between the abstract tensor product space and the more common definition is also given, and the pushforward and pullback operations in this later space are deduced from the more understandable and  pushforward and pullback.)
* Change of basis theorems for tensors and tangent vectors are easily understable because they can leverage the results of the earlier linear algebra chapter, which are stated using the intuitive notation $\[\mathbf{f}(E)\]_F$ introduced in that chapter.

 ## Antisymmetric objects

 ### The determinant
* We derive the permutation formula from the determinant from intuitive axioms pertaining to $n$-dimensional volume.
* The determinant is not immediately defined as the factor of multiplication on the top exterior power, as is done in most books that present this abstract characterization. Instead, the abstract characterization is proved as a theorem after establishing the permutation formula.

### Orientation
* We fully explain the concepts of orientation and rotation by building them from the ground up. We define orientation and rotation *without* the determinant, and then develop a series of theorems that formalize intuition and *prove* that yes, orientation does indeed correspond to the sign of the determinant, and yes, rotations do indeed have determinant 1. We do *not* just out of the blue state these facts without motivation, as most books do, since this leads to circular reasoning.
  * It's worth having an idea of what's avoided by the correct approach. In the typical way of doing things, we would have the following circular series of questions and answers. Regarding orientation, we have:
    * Q: "Why is orientation defined to correspond to the sign of the determinant?".
    * A: "Because orientation should have antisymmetric behaivor. Since the determinant exhibits antisymmetric behaivor, we can use it to define orientation."
    * Q: "But why should orientation have antisymmetric behaivor?"
    * A: "Notice that whenever one ordered basis is antisymmetrically related to another, it is also a rotation of the other. Since orientation should be preserved by rotation, it follows that antisymmetrically related ordered bases should have the same orientation."
    * A:" But why do rotations preserve orientation?"
    * Q: "Because rotations are defined to have determinant 1. Since orientation corresponds to the sign of the determinant, it follows from the product rule for determinants that the orientation of a rotated ordered basis is just 1 times the orientation of the original ordered basis."
    * A: "Okay. But why is orientation defined to correspond to the sign of the determinant?"🤦‍♂️
  
  Regarding rotations, we have:
    * Q: "Why are rotations defined to be linear functions with determinant $1$?"
    * A: "Rotations preserve the absolute value of volume, so every rotation $\mathbf{R}$ satisfies $\det(\mathbf{R}) = \pm 1$. Since rotations also preserve orientation, and since orientation corresponds to the sign of the determinant, it follows from the product rule for determinants that rotations $\mathbf{R}$ must in particular satisfy $\det(\mathbf{R}) = 1$."
    * A: "But why is orientation defined to correspond to the sign of the determinant?" 🤦‍♂️🤦‍♂️
* Differential forms are defined by using an abstract wedge product analagous to the abstract tensor product.
  * The equivalence to the usual definition of differential form is also explained.
 
## Manifolds
* The differential $d\mathbf{F}$ of a map $\mathbf{F}:U \subseteq M \rightarrow V \subseteq N$ between smooth charts on smooth manifolds is not simply defined, without motivation, to be $d\mathbf{F}\_\mathbf{p}(v_\mathbf{p})(f) = v_\mathbf{p}(f \circ \mathbf{F})$. Instead, we define $d\mathbf{F}\_\mathbf{p}$ to be the function $T\_\mathbf{p}(U) \rightarrow T\_{\mathbf{F}(\mathbf{p})}(V)$ whose matrix relative to the charts' coordinate bases is the Jacobian matrix of the coordinate representation of $\mathbf{F}(\mathbf{p})$.
* The uncommon geometric definition of the exterior derivative involving flux through a parallelapiped is used and the most common algebraic definition is shown to be a consequence of this.

## Linear algebra

* An intuitive definition for linear independence is used: a set of vectors is defined to be linearly independent if and only if every vector in the set is not in the span of all of the other vectors. The traditional definition of linear independence is proved to be equivalent to this alternative definition.
* A basis of a vector space is defined to be a spanning set for that vector space of minimal size. (The traditional approach of defining a basis to be a linearly independent spanning set has the downside of requiring a proof that the dimension of every finite-dimensional vector space is unique, which would ideally be an obvious fact that doesn't require a long proof). In the approach we use, it is an immediate consequence of minimality that dimension is unique. This alternative approach approach also uses the same idea as in the proof required by the traditional approach to prove that a set is a spanning set of minimal size if and only if it is a linearly independent spanning set, thus effectively switching a definition and a theorem from the traditional approach for pedadogical benefit.
* Extremely convenient notation for the matrix of a linear function $\mathbf{f}$ relative to bases $E$ and $F$, $\[\mathbf{f}(E)\]_F$, is used. I have not seen this notation used elsewhere.

# Table of contents

1. Review of logic, proofs, and functions
2. Linear algebra

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

## Copyright

This textbook is intended to be downloaded and read for free. If you would like to repurpose the content of this book, please clearly state that you have done so and credit this textbook as a reference.
