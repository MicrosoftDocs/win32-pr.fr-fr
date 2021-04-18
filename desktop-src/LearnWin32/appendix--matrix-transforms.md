---
title: Transformations de matrices d’annexe
description: Cette rubrique fournit une vue d’ensemble mathématique des transformations de matrice pour les graphiques 2D.
ms.assetid: 8cc01f45-dd84-4f3e-a5f2-26edc5cbdfa1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a5a9b09f75b17e4baf8afe5e7fde8643c06982f
ms.sourcegitcommit: ee06501cc29132927ade9813e0888aaa4decc487
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/28/2021
ms.locfileid: "104570220"
---
# <a name="appendix-matrix-transforms"></a><span data-ttu-id="8f405-103">Annexe : transformations de matrice</span><span class="sxs-lookup"><span data-stu-id="8f405-103">Appendix: Matrix Transforms</span></span>

<span data-ttu-id="8f405-104">Cette rubrique fournit une vue d’ensemble mathématique des transformations de matrice pour les graphiques 2D.</span><span class="sxs-lookup"><span data-stu-id="8f405-104">This topic provides a mathematical overview of matrix transforms for 2-D graphics.</span></span> <span data-ttu-id="8f405-105">Toutefois, vous n’avez pas besoin de connaître les mathématiques de matrice pour pouvoir utiliser les transformations dans Direct2D.</span><span class="sxs-lookup"><span data-stu-id="8f405-105">However, you don't need to know matrix math in order to use transforms in Direct2D.</span></span> <span data-ttu-id="8f405-106">Lisez cette rubrique si vous êtes intéressé par les mathématiques. dans le cas contraire, n’hésitez pas à ignorer cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="8f405-106">Read this topic if you are interested in the math; otherwise, feel free to skip this topic.</span></span>

-   [<span data-ttu-id="8f405-107">Présentation des matrices</span><span class="sxs-lookup"><span data-stu-id="8f405-107">Introduction to Matrices</span></span>](#introduction-to-matrices)
    -   [<span data-ttu-id="8f405-108">Opérations de matrice</span><span class="sxs-lookup"><span data-stu-id="8f405-108">Matrix Operations</span></span>](#matrix-operations)
-   [<span data-ttu-id="8f405-109">Transformations affines</span><span class="sxs-lookup"><span data-stu-id="8f405-109">Affine Transforms</span></span>](#affine-transforms)
    -   [<span data-ttu-id="8f405-110">Transformation de traduction</span><span class="sxs-lookup"><span data-stu-id="8f405-110">Translation Transform</span></span>](#translation-transform)
    -   [<span data-ttu-id="8f405-111">Mise à l’échelle de la transformation</span><span class="sxs-lookup"><span data-stu-id="8f405-111">Scaling Transform</span></span>](#scaling-transform)
    -   [<span data-ttu-id="8f405-112">Rotation autour de l’origine</span><span class="sxs-lookup"><span data-stu-id="8f405-112">Rotation Around the Origin</span></span>](#rotation-around-the-origin)
    -   [<span data-ttu-id="8f405-113">Rotation autour d’un point arbitraire</span><span class="sxs-lookup"><span data-stu-id="8f405-113">Rotation Around an Arbitrary Point</span></span>](#rotation-around-an-arbitrary-point)
    -   [<span data-ttu-id="8f405-114">Transformation d’inclinaison</span><span class="sxs-lookup"><span data-stu-id="8f405-114">Skew Transform</span></span>](#skew-transform)
-   [<span data-ttu-id="8f405-115">Représentation des transformations dans Direct2D</span><span class="sxs-lookup"><span data-stu-id="8f405-115">Representing Transforms in Direct2D</span></span>](#representing-transforms-in-direct2d)
-   [<span data-ttu-id="8f405-116">Next</span><span class="sxs-lookup"><span data-stu-id="8f405-116">Next</span></span>](#next)

## <a name="introduction-to-matrices"></a><span data-ttu-id="8f405-117">Présentation des matrices</span><span class="sxs-lookup"><span data-stu-id="8f405-117">Introduction to Matrices</span></span>

<span data-ttu-id="8f405-118">Une matrice est un tableau rectangulaire de nombres réels.</span><span class="sxs-lookup"><span data-stu-id="8f405-118">A matrix is a rectangular array of real numbers.</span></span> <span data-ttu-id="8f405-119">L' *ordre* de la matrice est le nombre de lignes et de colonnes.</span><span class="sxs-lookup"><span data-stu-id="8f405-119">The *order* of the matrix is the number of rows and columns.</span></span> <span data-ttu-id="8f405-120">Par exemple, si la matrice contient 3 lignes et 2 colonnes, la commande est 3 × 2.</span><span class="sxs-lookup"><span data-stu-id="8f405-120">For example, if the matrix has 3 rows and 2 columns, the order is 3 × 2.</span></span> <span data-ttu-id="8f405-121">Les matrices sont généralement affichées avec les éléments de matrice placés entre crochets :</span><span class="sxs-lookup"><span data-stu-id="8f405-121">Matrices are usually shown with the matrix elements enclosed in square brackets:</span></span>

![matrice 3 x 2.](images/matrix01.png)

<span data-ttu-id="8f405-123">Notation : une matrice est désignée par une lettre majuscule.</span><span class="sxs-lookup"><span data-stu-id="8f405-123">Notation: A matrix is designated by a capital letter.</span></span> <span data-ttu-id="8f405-124">Les éléments sont désignés par des lettres minuscules.</span><span class="sxs-lookup"><span data-stu-id="8f405-124">Elements are designated by lowercase letters.</span></span> <span data-ttu-id="8f405-125">Les indices indiquent le numéro de ligne et de colonne d’un élément.</span><span class="sxs-lookup"><span data-stu-id="8f405-125">Subscripts indicate the row and column number of an element.</span></span> <span data-ttu-id="8f405-126">Par exemple, un *IJ* est l’élément situé à la IE ligne et à la colonne j’th de la matrice a.</span><span class="sxs-lookup"><span data-stu-id="8f405-126">For example, a *ij* is the element at the i'th row and j'th column of the matrix A.</span></span>

<span data-ttu-id="8f405-127">Le diagramme suivant montre une matrice i × j, avec les éléments individuels dans chaque cellule de la matrice.</span><span class="sxs-lookup"><span data-stu-id="8f405-127">The following diagram shows an i × j matrix, with the individual elements in each cell of the matrix.</span></span>

![matrice avec i lignes et j colonnes.](images/matrix15.png)

### <a name="matrix-operations"></a><span data-ttu-id="8f405-129">Opérations de matrice</span><span class="sxs-lookup"><span data-stu-id="8f405-129">Matrix Operations</span></span>

<span data-ttu-id="8f405-130">Cette section décrit les opérations de base définies sur les matrices.</span><span class="sxs-lookup"><span data-stu-id="8f405-130">This section describes the basic operations defined on matrices.</span></span>

<span data-ttu-id="8f405-131">*En outre*.</span><span class="sxs-lookup"><span data-stu-id="8f405-131">*Addition*.</span></span> <span data-ttu-id="8f405-132">La somme A + B de deux matrices est obtenue en ajoutant les éléments correspondants de A et B :</span><span class="sxs-lookup"><span data-stu-id="8f405-132">The sum A + B of two matrices is obtained by adding the corresponding elements of A and B:</span></span>

<dl> <span data-ttu-id="8f405-133">A + b = \[ a *IJ* \]  +  \[ B *IJ* \]  =  \[ a *IJ* + b *IJ*\]</span><span class="sxs-lookup"><span data-stu-id="8f405-133">A + B = \[ a *ij* \] + \[ b *ij* \] = \[ a *ij* + b *ij* \]</span></span>
</dl>

<span data-ttu-id="8f405-134">*Multiplication scalaire*.</span><span class="sxs-lookup"><span data-stu-id="8f405-134">*Scalar multiplication*.</span></span> <span data-ttu-id="8f405-135">Cette opération multiplie une matrice par un nombre réel.</span><span class="sxs-lookup"><span data-stu-id="8f405-135">This operation multiplies a matrix by a real number.</span></span> <span data-ttu-id="8f405-136">Étant donné un nombre réel *k*, le produit scalaire Ka est obtenu en multipliant chaque élément d’un par *k*.</span><span class="sxs-lookup"><span data-stu-id="8f405-136">Given a real number *k*, the scalar product kA is obtained by multiplying every element of A by *k*.</span></span>

<dl> <span data-ttu-id="8f405-137">Ka = k \[ a *IJ* \]  =  \[ k × a *IJ*\]</span><span class="sxs-lookup"><span data-stu-id="8f405-137">kA = k\[ a *ij* \] = \[ k × a *ij* \]</span></span>
</dl>

<span data-ttu-id="8f405-138">*Multiplication de matrice*.</span><span class="sxs-lookup"><span data-stu-id="8f405-138">*Matrix multiplication*.</span></span> <span data-ttu-id="8f405-139">À partir de deux matrices A et B avec l’ordre (m × n) et (n × p), le produit C = A × B est une matrice avec l’ordre (m × p), définie comme suit :</span><span class="sxs-lookup"><span data-stu-id="8f405-139">Given two matrices A and B with order (m × n) and (n × p), the product C = A × B is a matrix with order (m × p), defined as follows:</span></span>

![Affiche une formule pour la multiplication de matrice.](images/matrix02.png)

<span data-ttu-id="8f405-141">ou, de façon équivalente :</span><span class="sxs-lookup"><span data-stu-id="8f405-141">or, equivalently:</span></span>

<dl> <span data-ttu-id="8f405-142">c *IJ* = a *i* 1 x B1 *j* + a *i* 2 x B2 *j* +... + a *dans* + b *NJ*  
</span><span class="sxs-lookup"><span data-stu-id="8f405-142">c *ij* = a *i* 1 x b1 *j* + a *i* 2 x b2 *j* + ... + a *in* + b *nj*  
</span></span></dl>

<span data-ttu-id="8f405-143">Autrement dit, pour calculer chaque élément c *IJ*, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="8f405-143">That is, to compute each element c *ij*, do the following:</span></span>

1.  <span data-ttu-id="8f405-144">Prenez la IE ligne de et la colonne j’th de B.</span><span class="sxs-lookup"><span data-stu-id="8f405-144">Take the i'th row of A and the j'th column of B.</span></span>
2.  <span data-ttu-id="8f405-145">Multipliez chaque paire d’éléments dans la ligne et la colonne : la première entrée de ligne par la première entrée de colonne, la deuxième entrée de ligne par la deuxième entrée de colonne, etc.</span><span class="sxs-lookup"><span data-stu-id="8f405-145">Multiply each pair of elements in the row and column: the first row entry by the first column entry, the second row entry by the second column entry, and so forth.</span></span>
3.  <span data-ttu-id="8f405-146">Additionner le résultat.</span><span class="sxs-lookup"><span data-stu-id="8f405-146">Sum the result.</span></span>

<span data-ttu-id="8f405-147">Voici un exemple de multiplication d’une matrice (2 × 2) par une matrice (2 × 3).</span><span class="sxs-lookup"><span data-stu-id="8f405-147">Here is an example of multiplying a (2 × 2) matrix by a (2 × 3) matrix.</span></span>

![multiplication de matrice.](images/matrix03.png)

<span data-ttu-id="8f405-149">La multiplication de matrice n’est pas commutative.</span><span class="sxs-lookup"><span data-stu-id="8f405-149">Matrix multiplication is not commutative.</span></span> <span data-ttu-id="8f405-150">Autrement dit, A × B ≠ B × A. En outre, à partir de la définition, il s’ensuit que toutes les paires de matrices ne peuvent pas être multipliées.</span><span class="sxs-lookup"><span data-stu-id="8f405-150">That is, A × B ≠ B × A. Also, from the definition it follows that not every pair of matrices can be multiplied.</span></span> <span data-ttu-id="8f405-151">Le nombre de colonnes dans la matrice de gauche doit être égal au nombre de lignes dans la matrice de droite.</span><span class="sxs-lookup"><span data-stu-id="8f405-151">The number of columns in the left-hand matrix must equal the number of rows in the right-hand matrix.</span></span> <span data-ttu-id="8f405-152">Sinon, l’opérateur × n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="8f405-152">Otherwise, the × operator is not defined.</span></span>

<span data-ttu-id="8f405-153">*Identifiez la matrice*.</span><span class="sxs-lookup"><span data-stu-id="8f405-153">*Identify matrix*.</span></span> <span data-ttu-id="8f405-154">Une matrice d’identité, désignée I, est une matrice carrée définie comme suit :</span><span class="sxs-lookup"><span data-stu-id="8f405-154">An identity matrix, designated I, is a square matrix defined as follows:</span></span>

<dl> <span data-ttu-id="8f405-155">I *IJ* = 1 si *i*  =  *j*, ou 0 dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="8f405-155">I *ij* = 1 if *i* = *j*, or 0 otherwise.</span></span>  
</dl>

<span data-ttu-id="8f405-156">En d’autres termes, une matrice d’identité contient 1 pour chaque élément où le numéro de ligne est égal au numéro de colonne et zéro pour tous les autres éléments.</span><span class="sxs-lookup"><span data-stu-id="8f405-156">In other words, an identity matrix contains 1 for each element where the row number equals the column number, and zero for all other elements.</span></span> <span data-ttu-id="8f405-157">Par exemple, voici la matrice d’identité 3 × 3.</span><span class="sxs-lookup"><span data-stu-id="8f405-157">For example, here is the 3 × 3 identity matrix.</span></span>

![matrice d’identité.](images/matrix04.png)

<span data-ttu-id="8f405-159">Les égalités suivantes sont conservées pour n’importe quelle matrice M.</span><span class="sxs-lookup"><span data-stu-id="8f405-159">The following equalities hold for any matrix M.</span></span>

<dl> <span data-ttu-id="8f405-160">M x I = M</span><span class="sxs-lookup"><span data-stu-id="8f405-160">M x I = M</span></span>  
<span data-ttu-id="8f405-161">I x M = M</span><span class="sxs-lookup"><span data-stu-id="8f405-161">I x M = M</span></span>  
</dl>

## <a name="affine-transforms"></a><span data-ttu-id="8f405-162">Transformations affines</span><span class="sxs-lookup"><span data-stu-id="8f405-162">Affine Transforms</span></span>

<span data-ttu-id="8f405-163">Une *transformation affine* est une opération mathématique qui mappe un espace de coordonnées à un autre.</span><span class="sxs-lookup"><span data-stu-id="8f405-163">An *affine transform* is a mathematical operation that maps one coordinate space to another.</span></span> <span data-ttu-id="8f405-164">En d’autres termes, il mappe un ensemble de points à un autre ensemble de points.</span><span class="sxs-lookup"><span data-stu-id="8f405-164">In other words, it maps one set of points to another set of points.</span></span> <span data-ttu-id="8f405-165">Les transformations affines ont des fonctionnalités qui les rendent utiles dans les graphiques informatiques.</span><span class="sxs-lookup"><span data-stu-id="8f405-165">Affine transforms have some features that make them useful in computer graphics.</span></span>

-   <span data-ttu-id="8f405-166">Les transformations affines préservent la *colinéarité*.</span><span class="sxs-lookup"><span data-stu-id="8f405-166">Affine transforms preserve *collinearity*.</span></span> <span data-ttu-id="8f405-167">Si trois points ou plus se trouvent sur une ligne, ils forment toujours une ligne après la transformation.</span><span class="sxs-lookup"><span data-stu-id="8f405-167">If three or more points fall on a line, they still form a line after the transformation.</span></span> <span data-ttu-id="8f405-168">Les lignes droites restent droits.</span><span class="sxs-lookup"><span data-stu-id="8f405-168">Straight lines remain straight.</span></span>
-   <span data-ttu-id="8f405-169">La composition de deux transformations affines est une transformation affine.</span><span class="sxs-lookup"><span data-stu-id="8f405-169">The composition of two affine transforms is an affine transform.</span></span>

<span data-ttu-id="8f405-170">Les transformations affines pour l’espace 2D se présentent sous la forme suivante.</span><span class="sxs-lookup"><span data-stu-id="8f405-170">Affine transforms for 2-D space have the following form.</span></span>

![Affiche une transformation affine pour l’espace 2D.](images/matrix05.png)

<span data-ttu-id="8f405-172">Si vous appliquez la définition de la multiplication de matrice donnée précédemment, vous pouvez indiquer que le produit de deux transformations affinées est une autre transformation affine.</span><span class="sxs-lookup"><span data-stu-id="8f405-172">If you apply the definition of matrix multiplication given earlier, you can show that the product of two affine transforms is another affine transform.</span></span> <span data-ttu-id="8f405-173">Pour transformer un point 2D à l’aide d’une transformation affine, le point est représenté sous la forme d’une matrice 1 × 3.</span><span class="sxs-lookup"><span data-stu-id="8f405-173">To transform a 2D point using an affine transform, the point is represented as a 1 × 3 matrix.</span></span>

<dl> <span data-ttu-id="8f405-174">P = \| x y 1 \|</span><span class="sxs-lookup"><span data-stu-id="8f405-174">P = \| x y 1 \|</span></span>  
</dl>

<span data-ttu-id="8f405-175">Les deux premiers éléments contiennent les coordonnées x et y du point.</span><span class="sxs-lookup"><span data-stu-id="8f405-175">The first two elements contain the x and y coordinates of the point.</span></span> <span data-ttu-id="8f405-176">Le 1 est placé dans le troisième élément pour que les opérations mathématiques fonctionnent correctement.</span><span class="sxs-lookup"><span data-stu-id="8f405-176">The 1 is placed in the third element to make the math work out correctly.</span></span> <span data-ttu-id="8f405-177">Pour appliquer la transformation, multipliez les deux matrices comme suit.</span><span class="sxs-lookup"><span data-stu-id="8f405-177">To apply the transform, multiply the two matrices as follows.</span></span>

<dl> <span data-ttu-id="8f405-178">P' = P × M</span><span class="sxs-lookup"><span data-stu-id="8f405-178">P' = P × M</span></span>  
</dl>

<span data-ttu-id="8f405-179">Cela s’étend à ce qui suit.</span><span class="sxs-lookup"><span data-stu-id="8f405-179">This expands to the following.</span></span>

![transformation affine.](images/matrix06.png)

<span data-ttu-id="8f405-181">where</span><span class="sxs-lookup"><span data-stu-id="8f405-181">where</span></span>

<dl> <span data-ttu-id="8f405-182">x' = ax + CY + e</span><span class="sxs-lookup"><span data-stu-id="8f405-182">x' = ax + cy + e</span></span>  
<span data-ttu-id="8f405-183">y' = BX + dy + f</span><span class="sxs-lookup"><span data-stu-id="8f405-183">y' = bx + dy + f</span></span>  
</dl>

<span data-ttu-id="8f405-184">Pour récupérer le point transformé, prenez les deux premiers éléments de la matrice P.</span><span class="sxs-lookup"><span data-stu-id="8f405-184">To get the transformed point, take the first two elements of matrix P'.</span></span>

<dl> <span data-ttu-id="8f405-185">p = (x', y') = (ax + CY + e, BX + dy + f)</span><span class="sxs-lookup"><span data-stu-id="8f405-185">p = (x', y') = (ax + cy + e, bx + dy + f)</span></span>  
</dl>

> [!Note]  
> <span data-ttu-id="8f405-186">Une matrice 1 × *n* est appelée un *vecteur de ligne*.</span><span class="sxs-lookup"><span data-stu-id="8f405-186">A 1 × *n* matrix is called a *row vector*.</span></span> <span data-ttu-id="8f405-187">Direct2D et Direct3D utilisent tous deux des vecteurs de ligne pour représenter des points dans l’espace 2D ou 3D.</span><span class="sxs-lookup"><span data-stu-id="8f405-187">Direct2D and Direct3D both use row vectors to represent points in 2D or 3D space.</span></span> <span data-ttu-id="8f405-188">Vous pouvez obtenir un résultat équivalent en utilisant un vecteur de colonne (*n* × 1) et en transposant la matrice de transformation.</span><span class="sxs-lookup"><span data-stu-id="8f405-188">You can get an equivalent result by using a column vector (*n* × 1) and transposing the transform matrix.</span></span> <span data-ttu-id="8f405-189">La plupart des textes graphiques utilisent le format de vecteur de colonne.</span><span class="sxs-lookup"><span data-stu-id="8f405-189">Most graphics texts use the column vector form.</span></span> <span data-ttu-id="8f405-190">Cette rubrique présente le format de vecteur de ligne pour la cohérence avec Direct2D et Direct3D.</span><span class="sxs-lookup"><span data-stu-id="8f405-190">This topic presents the row vector form for consistency with Direct2D and Direct3D.</span></span>

 

<span data-ttu-id="8f405-191">Les différentes sections suivantes dérivent les transformations de base.</span><span class="sxs-lookup"><span data-stu-id="8f405-191">The next several sections derive the basic transforms.</span></span>

### <a name="translation-transform"></a><span data-ttu-id="8f405-192">Transformation de traduction</span><span class="sxs-lookup"><span data-stu-id="8f405-192">Translation Transform</span></span>

<span data-ttu-id="8f405-193">La matrice de transformation de traduction se présente sous la forme suivante.</span><span class="sxs-lookup"><span data-stu-id="8f405-193">The translation transform matrix has the following form.</span></span>

![transformation de traduction.](images/matrix07.png)

<span data-ttu-id="8f405-195">Le branchement d’un point *P* dans cette équation donne :</span><span class="sxs-lookup"><span data-stu-id="8f405-195">Plugging a point *P* into this equation yields:</span></span>

<dl> <span data-ttu-id="8f405-196">P' = (*x*  +  *DX*, *y*  +  *dy*)</span><span class="sxs-lookup"><span data-stu-id="8f405-196">P' = (*x* + *dx*, *y* + *dy*)</span></span>
</dl>

<span data-ttu-id="8f405-197">qui correspond au point (x, y) traduit par *DX* sur l’axe des abscisses et *dy* sur l’axe des y.</span><span class="sxs-lookup"><span data-stu-id="8f405-197">which corresponds to the point (x, y) translated by *dx* in the X-axis and *dy* in the Y-axis.</span></span>

![diagramme qui affiche la traduction de deux points.](images/graphics22.png)

### <a name="scaling-transform"></a><span data-ttu-id="8f405-199">Mise à l’échelle de la transformation</span><span class="sxs-lookup"><span data-stu-id="8f405-199">Scaling Transform</span></span>

<span data-ttu-id="8f405-200">La matrice de transformation de mise à l’échelle se présente sous la forme suivante.</span><span class="sxs-lookup"><span data-stu-id="8f405-200">The scaling transform matrix has the following form.</span></span>

![mise à l’échelle de la transformation.](images/matrix09.png)

<span data-ttu-id="8f405-202">Le branchement d’un point *P* dans cette équation donne :</span><span class="sxs-lookup"><span data-stu-id="8f405-202">Plugging a point *P* into this equation yields:</span></span>

<dl> <span data-ttu-id="8f405-203">P' = (*x* ∙ *DX*, *y* ∙ *dy*)</span><span class="sxs-lookup"><span data-stu-id="8f405-203">P' = (*x* ∙ *dx*, *y* ∙ *dy*)</span></span>
</dl>

<span data-ttu-id="8f405-204">qui correspond au point (x, y) mis à l’échelle par *DX* et *dy*.</span><span class="sxs-lookup"><span data-stu-id="8f405-204">which corresponds to the point (x,y) scaled by *dx* and *dy*.</span></span>

![diagramme qui affiche la mise à l’échelle de deux points.](images/graphics23.png)

### <a name="rotation-around-the-origin"></a><span data-ttu-id="8f405-206">Rotation autour de l’origine</span><span class="sxs-lookup"><span data-stu-id="8f405-206">Rotation Around the Origin</span></span>

<span data-ttu-id="8f405-207">La matrice pour faire pivoter un point autour de l’origine se présente sous la forme suivante.</span><span class="sxs-lookup"><span data-stu-id="8f405-207">The matrix to rotate a point around the origin has the following form.</span></span>

![Affiche une formule pour une transformation de rotation.](images/matrix11.png)

<span data-ttu-id="8f405-209">Le point transformé est le suivant :</span><span class="sxs-lookup"><span data-stu-id="8f405-209">The transformed point is:</span></span>

<dl> <span data-ttu-id="8f405-210">P' = (*x* CosΘ – ysinΘ, *x* sinΘ + *y* cosΘ)</span><span class="sxs-lookup"><span data-stu-id="8f405-210">P' = (*x* cosΘ – ysinΘ, *x* sinΘ + *y* cosΘ)</span></span>
</dl>

<span data-ttu-id="8f405-211">Preuve.</span><span class="sxs-lookup"><span data-stu-id="8f405-211">Proof.</span></span> <span data-ttu-id="8f405-212">Pour montrer que P’représente une rotation, examinez le diagramme suivant.</span><span class="sxs-lookup"><span data-stu-id="8f405-212">To show that P' represents a rotation, consider the following diagram.</span></span>

![diagramme qui affiche la rotation autour de l’origine.](images/graphics24.png)

<span data-ttu-id="8f405-214">Soit :</span><span class="sxs-lookup"><span data-stu-id="8f405-214">Given:</span></span>

<dl> <dt>

<span data-ttu-id="8f405-215"><span id="P____x_y_"></span><span id="p____x_y_"></span><span id="P____X_Y_"></span>P = (x, y)</span><span class="sxs-lookup"><span data-stu-id="8f405-215"><span id="P____x_y_"></span><span id="p____x_y_"></span><span id="P____X_Y_"></span>P = (x,y)</span></span>
</dt> <dd>

<span data-ttu-id="8f405-216">Point d’origine à transformer.</span><span class="sxs-lookup"><span data-stu-id="8f405-216">The original point to transform.</span></span>

</dd> <dt>

<span data-ttu-id="8f405-217">Φ</span><span class="sxs-lookup"><span data-stu-id="8f405-217">Φ</span></span>
</dt> <dd>

<span data-ttu-id="8f405-218">L’angle formé par la ligne (0,0) à P.</span><span class="sxs-lookup"><span data-stu-id="8f405-218">The angle formed by the line (0,0) to P.</span></span>

</dd> <dt>

<span data-ttu-id="8f405-219">Alors</span><span class="sxs-lookup"><span data-stu-id="8f405-219">Θ</span></span>
</dt> <dd>

<span data-ttu-id="8f405-220">Angle selon lequel pivoter (x, y) autour de l’origine.</span><span class="sxs-lookup"><span data-stu-id="8f405-220">The angle by which to rotate (x,y) about the origin.</span></span>

</dd> <dt>

<span data-ttu-id="8f405-221"><span id="P_____x__y__"></span><span id="p_____x__y__"></span><span id="P_____X__Y__"></span>P' = (x', y')</span><span class="sxs-lookup"><span data-stu-id="8f405-221"><span id="P_____x__y__"></span><span id="p_____x__y__"></span><span id="P_____X__Y__"></span>P' = (x',y')</span></span>
</dt> <dd>

<span data-ttu-id="8f405-222">Point transformé.</span><span class="sxs-lookup"><span data-stu-id="8f405-222">The transformed point.</span></span>

</dd> <dt>

<span data-ttu-id="8f405-223"><span id="R"></span><span id="r"></span>R</span><span class="sxs-lookup"><span data-stu-id="8f405-223"><span id="R"></span><span id="r"></span>R</span></span>
</dt> <dd>

<span data-ttu-id="8f405-224">Longueur de la ligne (0,0) à P. Également le rayon du cercle de rotation.</span><span class="sxs-lookup"><span data-stu-id="8f405-224">The length of the line (0,0) to P. Also the radius of the circle of rotation.</span></span>

</dd> </dl>

> [!Note]  
> <span data-ttu-id="8f405-225">Ce diagramme utilise le système de coordonnées standard utilisé dans Geometry, où l’axe des y positif pointe vers le haut.</span><span class="sxs-lookup"><span data-stu-id="8f405-225">This diagram uses the standard coordinate system used in geometry, where the positive y-axis points up.</span></span> <span data-ttu-id="8f405-226">Direct2D utilise le système de coordonnées Windows, où l’axe des y positif pointe vers le dessous.</span><span class="sxs-lookup"><span data-stu-id="8f405-226">Direct2D uses the Windows coordinate system, where the positive y-axis points down.</span></span>

 

<span data-ttu-id="8f405-227">L’angle entre l’axe des abscisses et la ligne (0,0) à P est Φ + Θ.</span><span class="sxs-lookup"><span data-stu-id="8f405-227">The angle between the x-axis and the line (0,0) to P' is Φ + Θ.</span></span> <span data-ttu-id="8f405-228">Les identités suivantes sont conservées :</span><span class="sxs-lookup"><span data-stu-id="8f405-228">The following identities hold:</span></span>

<dl> <span data-ttu-id="8f405-229">x = R cosΦ</span><span class="sxs-lookup"><span data-stu-id="8f405-229">x = R cosΦ</span></span>  
<span data-ttu-id="8f405-230">o = R sinΦ</span><span class="sxs-lookup"><span data-stu-id="8f405-230">y = R sinΦ</span></span>  
<span data-ttu-id="8f405-231">x' = R cos (Φ + Θ)</span><span class="sxs-lookup"><span data-stu-id="8f405-231">x' = R cos(Φ + Θ)</span></span>  
<span data-ttu-id="8f405-232">y' = R Sin (Φ + Θ)</span><span class="sxs-lookup"><span data-stu-id="8f405-232">y' = R sin(Φ+ Θ)</span></span>  
</dl>

<span data-ttu-id="8f405-233">À présent, résolvez les x et y en termes de Θ.</span><span class="sxs-lookup"><span data-stu-id="8f405-233">Now solve for x' and y' in terms of Θ.</span></span> <span data-ttu-id="8f405-234">Par les formules d’addition trigonométrique :</span><span class="sxs-lookup"><span data-stu-id="8f405-234">By the trigonometric addition formulas:</span></span>

<dl> <span data-ttu-id="8f405-235">x' = R (cosΦcosΘ – sinΦsinΘ) = RcosΦcosΘ – RsinΦsinΘ</span><span class="sxs-lookup"><span data-stu-id="8f405-235">x' = R(cosΦcosΘ – sinΦsinΘ) = RcosΦcosΘ – RsinΦsinΘ</span></span>  
<span data-ttu-id="8f405-236">y' = R (sinΦcosΘ + cosΦsinΘ) = RsinΦcosΘ + RcosΦsinΘ</span><span class="sxs-lookup"><span data-stu-id="8f405-236">y' = R(sinΦcosΘ + cosΦsinΘ) = RsinΦcosΘ + RcosΦsinΘ</span></span>  
</dl>

<span data-ttu-id="8f405-237">En remplaçant, nous obtenons :</span><span class="sxs-lookup"><span data-stu-id="8f405-237">Substituting, we get:</span></span>

<dl> <span data-ttu-id="8f405-238">x' = xcosΘ – ysinΘ</span><span class="sxs-lookup"><span data-stu-id="8f405-238">x' = xcosΘ – ysinΘ</span></span>  
<span data-ttu-id="8f405-239">y' = xsinΘ + ycosΘ</span><span class="sxs-lookup"><span data-stu-id="8f405-239">y' = xsinΘ + ycosΘ</span></span>  
</dl>

<span data-ttu-id="8f405-240">qui correspond au point transformé P’indiqué plus haut.</span><span class="sxs-lookup"><span data-stu-id="8f405-240">which corresponds to the transformed point P' shown earlier.</span></span>

### <a name="rotation-around-an-arbitrary-point"></a><span data-ttu-id="8f405-241">Rotation autour d’un point arbitraire</span><span class="sxs-lookup"><span data-stu-id="8f405-241">Rotation Around an Arbitrary Point</span></span>

<span data-ttu-id="8f405-242">Pour faire pivoter autour d’un point (x, y) autre que l’origine, la matrice suivante est utilisée.</span><span class="sxs-lookup"><span data-stu-id="8f405-242">To rotate around a point (x,y) other than the origin, the following matrix is used.</span></span>

![transformation de rotation.](images/matrix13.png)

<span data-ttu-id="8f405-244">Vous pouvez dériver cette matrice en utilisant le point (x, y) comme origine.</span><span class="sxs-lookup"><span data-stu-id="8f405-244">You can derive this matrix by taking the point (x,y) to be the origin.</span></span>

![diagramme qui montre une rotation autour d’un point.](images/graphics25.png)

<span data-ttu-id="8f405-246">Let (x1, Y1) est le point qui résulte de la rotation du point (x0, Y0) autour du point (x, y).</span><span class="sxs-lookup"><span data-stu-id="8f405-246">Let (x1, y1) be the point that results from rotating the point (x0, y0) around the point (x,y).</span></span> <span data-ttu-id="8f405-247">Nous pouvons dériver x1 comme suit.</span><span class="sxs-lookup"><span data-stu-id="8f405-247">We can derive x1 as follows.</span></span>

<dl> <span data-ttu-id="8f405-248">x1 = (x0 – x) cosΘ – (Y0 – y) sinΘ + x</span><span class="sxs-lookup"><span data-stu-id="8f405-248">x1 = (x0 – x)cosΘ– (y0 – y)sinΘ + x</span></span>  
<span data-ttu-id="8f405-249">x1 = x0cosΘ – y0sinΘ + \[ (1 – cosΘ) + ysinΘ \]</span><span class="sxs-lookup"><span data-stu-id="8f405-249">x1 = x0cosΘ – y0sinΘ + \[ (1 – cosΘ) + ysinΘ \]</span></span>  
</dl>

<span data-ttu-id="8f405-250">À présent, rebranchez cette équation à la matrice de transformation, en utilisant la formule x1 = aX0 + CY0 + e de la version antérieure.</span><span class="sxs-lookup"><span data-stu-id="8f405-250">Now plug this equation back into the transform matrix, using the formula x1 = ax0 + cy0 + e from earlier.</span></span> <span data-ttu-id="8f405-251">Utilisez la même procédure pour dériver Y1.</span><span class="sxs-lookup"><span data-stu-id="8f405-251">Use the same procedure to derive y1.</span></span>

### <a name="skew-transform"></a><span data-ttu-id="8f405-252">Transformation d’inclinaison</span><span class="sxs-lookup"><span data-stu-id="8f405-252">Skew Transform</span></span>

<span data-ttu-id="8f405-253">La transformation d’inclinaison est définie par quatre paramètres :</span><span class="sxs-lookup"><span data-stu-id="8f405-253">The skew transform is defined by four parameters:</span></span>

-   <span data-ttu-id="8f405-254">Θ : la valeur de l’inclinaison le long de l’axe x, mesurée en tant qu’angle à partir de l’axe y.</span><span class="sxs-lookup"><span data-stu-id="8f405-254">Θ: The amount to skew along the x-axis, measured as an angle from the y-axis.</span></span>
-   <span data-ttu-id="8f405-255">Φ : la valeur de l’inclinaison le long de l’axe y, mesurée en tant qu’angle à partir de l’axe x.</span><span class="sxs-lookup"><span data-stu-id="8f405-255">Φ: The amount to skew along the y-axis, measured as an angle from the x-axis.</span></span>
-   <span data-ttu-id="8f405-256">(*PX*, *py*) : coordonnées x et y du point sur lequel l’inclinaison est exécutée.</span><span class="sxs-lookup"><span data-stu-id="8f405-256">(*px*, *py*): The x- and y-coordinates of the point about which the skew is performed.</span></span>

<span data-ttu-id="8f405-257">La transformation d’inclinaison utilise la matrice suivante.</span><span class="sxs-lookup"><span data-stu-id="8f405-257">The skew transform uses the following matrix.</span></span>

![incliner la transformation.](images/matrix14.png)

<span data-ttu-id="8f405-259">Le point transformé est le suivant :</span><span class="sxs-lookup"><span data-stu-id="8f405-259">The transformed point is:</span></span>

<dl> <span data-ttu-id="8f405-260">P' = (*x*  +  *y* tanΘ – *py* tanΘ, *y*  +  *x* tanΦ) – *py* tanΦ</span><span class="sxs-lookup"><span data-stu-id="8f405-260">P' = (*x* + *y* tanΘ – *py* tanΘ, *y* + *x* tanΦ) – *py* tanΦ</span></span>
</dl>

<span data-ttu-id="8f405-261">ou équivalent :</span><span class="sxs-lookup"><span data-stu-id="8f405-261">or equivalently:</span></span>

<dl> <span data-ttu-id="8f405-262">P' = (*x* + (*y* – *py*) tanΘ, *y* + (*x* - *PX*) tanΦ)</span><span class="sxs-lookup"><span data-stu-id="8f405-262">P' = (*x* + (*y* – *py*)tanΘ, *y* + (*x* – *px*)tanΦ)</span></span>
</dl>

<span data-ttu-id="8f405-263">Pour voir comment cette transformation fonctionne, considérez chaque composant individuellement.</span><span class="sxs-lookup"><span data-stu-id="8f405-263">To see how this transform works, consider each component individually.</span></span> <span data-ttu-id="8f405-264">Le paramètre Θ déplace chaque point de la direction x d’une quantité égale à tanΘ.</span><span class="sxs-lookup"><span data-stu-id="8f405-264">The Θ parameter moves every point in the x direction by an amount equal to tanΘ.</span></span> <span data-ttu-id="8f405-265">Le diagramme suivant montre la relation entre Θ et l’inclinaison de l’axe x.</span><span class="sxs-lookup"><span data-stu-id="8f405-265">The following diagram shows the relation between Θ and the x-axis skew.</span></span>

![Diagramme qui affiche le décalage le long de l’axe x.](images/graphics26.png)

<span data-ttu-id="8f405-267">Voici la même inclinaison appliquée à un rectangle :</span><span class="sxs-lookup"><span data-stu-id="8f405-267">Here is the same skew applied to a rectangle:</span></span>

![Diagramme qui affiche le décalage le long de l’axe x lorsqu’il est appliqué à un rectangle.](images/graphics27.png)

<span data-ttu-id="8f405-269">Le paramètre Φ a le même effet, mais le long de l’axe y :</span><span class="sxs-lookup"><span data-stu-id="8f405-269">The Φ parameter has the same effect, but along the y-axis:</span></span>

![Diagramme qui affiche l’inclinaison le long de l’axe y.](images/graphics28.png)

<span data-ttu-id="8f405-271">Le diagramme suivant montre l’inclinaison de l’axe y appliquée à un rectangle.</span><span class="sxs-lookup"><span data-stu-id="8f405-271">The next diagram shows y-axis skew applied to a rectangle.</span></span>

![Diagramme qui affiche l’inclinaison le long de l’axe y lorsqu’il est appliqué à un rectangle.](images/graphics29.png)

<span data-ttu-id="8f405-273">Enfin, les paramètres *PX* et *py* déplacent le point central de l’inclinaison le long des axes x et y.</span><span class="sxs-lookup"><span data-stu-id="8f405-273">Finally, the parameters *px* and *py* shift the center point for the skew along the x- and y-axes.</span></span>

## <a name="representing-transforms-in-direct2d"></a><span data-ttu-id="8f405-274">Représentation des transformations dans Direct2D</span><span class="sxs-lookup"><span data-stu-id="8f405-274">Representing Transforms in Direct2D</span></span>

<span data-ttu-id="8f405-275">Toutes les transformations Direct2D sont des transformations affines.</span><span class="sxs-lookup"><span data-stu-id="8f405-275">All Direct2D transforms are affine transforms.</span></span> <span data-ttu-id="8f405-276">Direct2D ne prend pas en charge les transformations non affines.</span><span class="sxs-lookup"><span data-stu-id="8f405-276">Direct2D does not support non-affine transforms.</span></span> <span data-ttu-id="8f405-277">Les transformations sont représentées par la structure [**\_ \_ matrice \_ F de la matrice d2d1**](/windows/desktop/Direct2D/d2d1-matrix-3x2-f) .</span><span class="sxs-lookup"><span data-stu-id="8f405-277">Transforms are represented by the [**D2D1\_MATRIX\_3X2\_F**](/windows/desktop/Direct2D/d2d1-matrix-3x2-f) structure.</span></span> <span data-ttu-id="8f405-278">Cette structure définit une matrice 3 × 2.</span><span class="sxs-lookup"><span data-stu-id="8f405-278">This structure defines a 3 × 2 matrix.</span></span> <span data-ttu-id="8f405-279">Étant donné que la troisième colonne d’une transformation affine est toujours la même ( \[ 0, 0, 1 \] ) et parce que Direct2D ne prend pas en charge les transformations non affines, il n’est pas nécessaire de spécifier la totalité de la matrice 3 × 3.</span><span class="sxs-lookup"><span data-stu-id="8f405-279">Because the third column of an affine transform is always the same (\[0, 0, 1\]), and because Direct2D does not support non-affine transforms, there is no need to specify the entire 3 × 3 matrix.</span></span> <span data-ttu-id="8f405-280">En interne, Direct2D utilise 3 × 3 matrices pour calculer les transformations.</span><span class="sxs-lookup"><span data-stu-id="8f405-280">Internally, Direct2D uses 3 × 3 matrices to compute the transforms.</span></span>

<span data-ttu-id="8f405-281">Les membres de la [**\_ matrice d2d1 \_ matrice \_ F**](/windows/desktop/Direct2D/d2d1-matrix-3x2-f) sont nommés en fonction de leur position d’index : le membre **\_ 11** est l’élément (1, 1), le membre **\_ 12** est l’élément (1, 2), et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="8f405-281">The members of the [**D2D1\_MATRIX\_3X2\_F**](/windows/desktop/Direct2D/d2d1-matrix-3x2-f) are named according to their index position: the **\_11** member is element (1,1), the **\_12** member is element (1,2), and so forth.</span></span> <span data-ttu-id="8f405-282">Bien que vous puissiez initialiser les membres de la structure directement, il est recommandé d’utiliser la classe [**d2d1 :: Matrix3x2F**](/windows/desktop/api/d2d1helper/nl-d2d1helper-matrix3x2f) .</span><span class="sxs-lookup"><span data-stu-id="8f405-282">Although you can initialize the structure members directly, it is recommended to use the [**D2D1::Matrix3x2F**](/windows/desktop/api/d2d1helper/nl-d2d1helper-matrix3x2f) class.</span></span> <span data-ttu-id="8f405-283">Cette classe hérite de **d2d1 \_ Matrix \_ matrice \_ F** et fournit des méthodes d’assistance pour créer l’une des transformations affines de base.</span><span class="sxs-lookup"><span data-stu-id="8f405-283">This class inherits **D2D1\_MATRIX\_3X2\_F** and provides helper methods for creating any of the basic affine transforms.</span></span> <span data-ttu-id="8f405-284">La classe définit également l' [**opérateur \* ()**](/windows/desktop/api/d2d1helper/nf-d2d1helper-matrix3x2f-operator-mult) pour composer deux ou plusieurs transformations, comme décrit dans [application de transformations dans Direct2D](applying-transforms-in-direct2d.md).</span><span class="sxs-lookup"><span data-stu-id="8f405-284">The class also defines [**operator\*()**](/windows/desktop/api/d2d1helper/nf-d2d1helper-matrix3x2f-operator-mult) for composing two or more transforms, as described in [Applying Transforms in Direct2D](applying-transforms-in-direct2d.md).</span></span>

## <a name="next"></a><span data-ttu-id="8f405-285">Suivant</span><span class="sxs-lookup"><span data-stu-id="8f405-285">Next</span></span>

[<span data-ttu-id="8f405-286">Module 4. Entrée utilisateur</span><span class="sxs-lookup"><span data-stu-id="8f405-286">Module 4. User Input</span></span>](module-4--user-input.md)

 

 