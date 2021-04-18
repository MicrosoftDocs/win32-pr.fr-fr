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
# <a name="appendix-matrix-transforms"></a>Annexe : transformations de matrice

Cette rubrique fournit une vue d’ensemble mathématique des transformations de matrice pour les graphiques 2D. Toutefois, vous n’avez pas besoin de connaître les mathématiques de matrice pour pouvoir utiliser les transformations dans Direct2D. Lisez cette rubrique si vous êtes intéressé par les mathématiques. dans le cas contraire, n’hésitez pas à ignorer cette rubrique.

-   [Présentation des matrices](#introduction-to-matrices)
    -   [Opérations de matrice](#matrix-operations)
-   [Transformations affines](#affine-transforms)
    -   [Transformation de traduction](#translation-transform)
    -   [Mise à l’échelle de la transformation](#scaling-transform)
    -   [Rotation autour de l’origine](#rotation-around-the-origin)
    -   [Rotation autour d’un point arbitraire](#rotation-around-an-arbitrary-point)
    -   [Transformation d’inclinaison](#skew-transform)
-   [Représentation des transformations dans Direct2D](#representing-transforms-in-direct2d)
-   [Next](#next)

## <a name="introduction-to-matrices"></a>Présentation des matrices

Une matrice est un tableau rectangulaire de nombres réels. L' *ordre* de la matrice est le nombre de lignes et de colonnes. Par exemple, si la matrice contient 3 lignes et 2 colonnes, la commande est 3 × 2. Les matrices sont généralement affichées avec les éléments de matrice placés entre crochets :

![matrice 3 x 2.](images/matrix01.png)

Notation : une matrice est désignée par une lettre majuscule. Les éléments sont désignés par des lettres minuscules. Les indices indiquent le numéro de ligne et de colonne d’un élément. Par exemple, un *IJ* est l’élément situé à la IE ligne et à la colonne j’th de la matrice a.

Le diagramme suivant montre une matrice i × j, avec les éléments individuels dans chaque cellule de la matrice.

![matrice avec i lignes et j colonnes.](images/matrix15.png)

### <a name="matrix-operations"></a>Opérations de matrice

Cette section décrit les opérations de base définies sur les matrices.

*En outre*. La somme A + B de deux matrices est obtenue en ajoutant les éléments correspondants de A et B :

<dl> A + b = \[ a *IJ* \]  +  \[ B *IJ* \]  =  \[ a *IJ* + b *IJ*\]
</dl>

*Multiplication scalaire*. Cette opération multiplie une matrice par un nombre réel. Étant donné un nombre réel *k*, le produit scalaire Ka est obtenu en multipliant chaque élément d’un par *k*.

<dl> Ka = k \[ a *IJ* \]  =  \[ k × a *IJ*\]
</dl>

*Multiplication de matrice*. À partir de deux matrices A et B avec l’ordre (m × n) et (n × p), le produit C = A × B est une matrice avec l’ordre (m × p), définie comme suit :

![Affiche une formule pour la multiplication de matrice.](images/matrix02.png)

ou, de façon équivalente :

<dl> c *IJ* = a *i* 1 x B1 *j* + a *i* 2 x B2 *j* +... + a *dans* + b *NJ*  
</dl>

Autrement dit, pour calculer chaque élément c *IJ*, procédez comme suit :

1.  Prenez la IE ligne de et la colonne j’th de B.
2.  Multipliez chaque paire d’éléments dans la ligne et la colonne : la première entrée de ligne par la première entrée de colonne, la deuxième entrée de ligne par la deuxième entrée de colonne, etc.
3.  Additionner le résultat.

Voici un exemple de multiplication d’une matrice (2 × 2) par une matrice (2 × 3).

![multiplication de matrice.](images/matrix03.png)

La multiplication de matrice n’est pas commutative. Autrement dit, A × B ≠ B × A. En outre, à partir de la définition, il s’ensuit que toutes les paires de matrices ne peuvent pas être multipliées. Le nombre de colonnes dans la matrice de gauche doit être égal au nombre de lignes dans la matrice de droite. Sinon, l’opérateur × n’est pas défini.

*Identifiez la matrice*. Une matrice d’identité, désignée I, est une matrice carrée définie comme suit :

<dl> I *IJ* = 1 si *i*  =  *j*, ou 0 dans le cas contraire.  
</dl>

En d’autres termes, une matrice d’identité contient 1 pour chaque élément où le numéro de ligne est égal au numéro de colonne et zéro pour tous les autres éléments. Par exemple, voici la matrice d’identité 3 × 3.

![matrice d’identité.](images/matrix04.png)

Les égalités suivantes sont conservées pour n’importe quelle matrice M.

<dl> M x I = M  
I x M = M  
</dl>

## <a name="affine-transforms"></a>Transformations affines

Une *transformation affine* est une opération mathématique qui mappe un espace de coordonnées à un autre. En d’autres termes, il mappe un ensemble de points à un autre ensemble de points. Les transformations affines ont des fonctionnalités qui les rendent utiles dans les graphiques informatiques.

-   Les transformations affines préservent la *colinéarité*. Si trois points ou plus se trouvent sur une ligne, ils forment toujours une ligne après la transformation. Les lignes droites restent droits.
-   La composition de deux transformations affines est une transformation affine.

Les transformations affines pour l’espace 2D se présentent sous la forme suivante.

![Affiche une transformation affine pour l’espace 2D.](images/matrix05.png)

Si vous appliquez la définition de la multiplication de matrice donnée précédemment, vous pouvez indiquer que le produit de deux transformations affinées est une autre transformation affine. Pour transformer un point 2D à l’aide d’une transformation affine, le point est représenté sous la forme d’une matrice 1 × 3.

<dl> P = \| x y 1 \|  
</dl>

Les deux premiers éléments contiennent les coordonnées x et y du point. Le 1 est placé dans le troisième élément pour que les opérations mathématiques fonctionnent correctement. Pour appliquer la transformation, multipliez les deux matrices comme suit.

<dl> P' = P × M  
</dl>

Cela s’étend à ce qui suit.

![transformation affine.](images/matrix06.png)

where

<dl> x' = ax + CY + e  
y' = BX + dy + f  
</dl>

Pour récupérer le point transformé, prenez les deux premiers éléments de la matrice P.

<dl> p = (x', y') = (ax + CY + e, BX + dy + f)  
</dl>

> [!Note]  
> Une matrice 1 × *n* est appelée un *vecteur de ligne*. Direct2D et Direct3D utilisent tous deux des vecteurs de ligne pour représenter des points dans l’espace 2D ou 3D. Vous pouvez obtenir un résultat équivalent en utilisant un vecteur de colonne (*n* × 1) et en transposant la matrice de transformation. La plupart des textes graphiques utilisent le format de vecteur de colonne. Cette rubrique présente le format de vecteur de ligne pour la cohérence avec Direct2D et Direct3D.

 

Les différentes sections suivantes dérivent les transformations de base.

### <a name="translation-transform"></a>Transformation de traduction

La matrice de transformation de traduction se présente sous la forme suivante.

![transformation de traduction.](images/matrix07.png)

Le branchement d’un point *P* dans cette équation donne :

<dl> P' = (*x*  +  *DX*, *y*  +  *dy*)
</dl>

qui correspond au point (x, y) traduit par *DX* sur l’axe des abscisses et *dy* sur l’axe des y.

![diagramme qui affiche la traduction de deux points.](images/graphics22.png)

### <a name="scaling-transform"></a>Mise à l’échelle de la transformation

La matrice de transformation de mise à l’échelle se présente sous la forme suivante.

![mise à l’échelle de la transformation.](images/matrix09.png)

Le branchement d’un point *P* dans cette équation donne :

<dl> P' = (*x* ∙ *DX*, *y* ∙ *dy*)
</dl>

qui correspond au point (x, y) mis à l’échelle par *DX* et *dy*.

![diagramme qui affiche la mise à l’échelle de deux points.](images/graphics23.png)

### <a name="rotation-around-the-origin"></a>Rotation autour de l’origine

La matrice pour faire pivoter un point autour de l’origine se présente sous la forme suivante.

![Affiche une formule pour une transformation de rotation.](images/matrix11.png)

Le point transformé est le suivant :

<dl> P' = (*x* CosΘ – ysinΘ, *x* sinΘ + *y* cosΘ)
</dl>

Preuve. Pour montrer que P’représente une rotation, examinez le diagramme suivant.

![diagramme qui affiche la rotation autour de l’origine.](images/graphics24.png)

Soit :

<dl> <dt>

<span id="P____x_y_"></span><span id="p____x_y_"></span><span id="P____X_Y_"></span>P = (x, y)
</dt> <dd>

Point d’origine à transformer.

</dd> <dt>

Φ
</dt> <dd>

L’angle formé par la ligne (0,0) à P.

</dd> <dt>

Alors
</dt> <dd>

Angle selon lequel pivoter (x, y) autour de l’origine.

</dd> <dt>

<span id="P_____x__y__"></span><span id="p_____x__y__"></span><span id="P_____X__Y__"></span>P' = (x', y')
</dt> <dd>

Point transformé.

</dd> <dt>

<span id="R"></span><span id="r"></span>R
</dt> <dd>

Longueur de la ligne (0,0) à P. Également le rayon du cercle de rotation.

</dd> </dl>

> [!Note]  
> Ce diagramme utilise le système de coordonnées standard utilisé dans Geometry, où l’axe des y positif pointe vers le haut. Direct2D utilise le système de coordonnées Windows, où l’axe des y positif pointe vers le dessous.

 

L’angle entre l’axe des abscisses et la ligne (0,0) à P est Φ + Θ. Les identités suivantes sont conservées :

<dl> x = R cosΦ  
o = R sinΦ  
x' = R cos (Φ + Θ)  
y' = R Sin (Φ + Θ)  
</dl>

À présent, résolvez les x et y en termes de Θ. Par les formules d’addition trigonométrique :

<dl> x' = R (cosΦcosΘ – sinΦsinΘ) = RcosΦcosΘ – RsinΦsinΘ  
y' = R (sinΦcosΘ + cosΦsinΘ) = RsinΦcosΘ + RcosΦsinΘ  
</dl>

En remplaçant, nous obtenons :

<dl> x' = xcosΘ – ysinΘ  
y' = xsinΘ + ycosΘ  
</dl>

qui correspond au point transformé P’indiqué plus haut.

### <a name="rotation-around-an-arbitrary-point"></a>Rotation autour d’un point arbitraire

Pour faire pivoter autour d’un point (x, y) autre que l’origine, la matrice suivante est utilisée.

![transformation de rotation.](images/matrix13.png)

Vous pouvez dériver cette matrice en utilisant le point (x, y) comme origine.

![diagramme qui montre une rotation autour d’un point.](images/graphics25.png)

Let (x1, Y1) est le point qui résulte de la rotation du point (x0, Y0) autour du point (x, y). Nous pouvons dériver x1 comme suit.

<dl> x1 = (x0 – x) cosΘ – (Y0 – y) sinΘ + x  
x1 = x0cosΘ – y0sinΘ + \[ (1 – cosΘ) + ysinΘ \]  
</dl>

À présent, rebranchez cette équation à la matrice de transformation, en utilisant la formule x1 = aX0 + CY0 + e de la version antérieure. Utilisez la même procédure pour dériver Y1.

### <a name="skew-transform"></a>Transformation d’inclinaison

La transformation d’inclinaison est définie par quatre paramètres :

-   Θ : la valeur de l’inclinaison le long de l’axe x, mesurée en tant qu’angle à partir de l’axe y.
-   Φ : la valeur de l’inclinaison le long de l’axe y, mesurée en tant qu’angle à partir de l’axe x.
-   (*PX*, *py*) : coordonnées x et y du point sur lequel l’inclinaison est exécutée.

La transformation d’inclinaison utilise la matrice suivante.

![incliner la transformation.](images/matrix14.png)

Le point transformé est le suivant :

<dl> P' = (*x*  +  *y* tanΘ – *py* tanΘ, *y*  +  *x* tanΦ) – *py* tanΦ
</dl>

ou équivalent :

<dl> P' = (*x* + (*y* – *py*) tanΘ, *y* + (*x* - *PX*) tanΦ)
</dl>

Pour voir comment cette transformation fonctionne, considérez chaque composant individuellement. Le paramètre Θ déplace chaque point de la direction x d’une quantité égale à tanΘ. Le diagramme suivant montre la relation entre Θ et l’inclinaison de l’axe x.

![Diagramme qui affiche le décalage le long de l’axe x.](images/graphics26.png)

Voici la même inclinaison appliquée à un rectangle :

![Diagramme qui affiche le décalage le long de l’axe x lorsqu’il est appliqué à un rectangle.](images/graphics27.png)

Le paramètre Φ a le même effet, mais le long de l’axe y :

![Diagramme qui affiche l’inclinaison le long de l’axe y.](images/graphics28.png)

Le diagramme suivant montre l’inclinaison de l’axe y appliquée à un rectangle.

![Diagramme qui affiche l’inclinaison le long de l’axe y lorsqu’il est appliqué à un rectangle.](images/graphics29.png)

Enfin, les paramètres *PX* et *py* déplacent le point central de l’inclinaison le long des axes x et y.

## <a name="representing-transforms-in-direct2d"></a>Représentation des transformations dans Direct2D

Toutes les transformations Direct2D sont des transformations affines. Direct2D ne prend pas en charge les transformations non affines. Les transformations sont représentées par la structure [**\_ \_ matrice \_ F de la matrice d2d1**](/windows/desktop/Direct2D/d2d1-matrix-3x2-f) . Cette structure définit une matrice 3 × 2. Étant donné que la troisième colonne d’une transformation affine est toujours la même ( \[ 0, 0, 1 \] ) et parce que Direct2D ne prend pas en charge les transformations non affines, il n’est pas nécessaire de spécifier la totalité de la matrice 3 × 3. En interne, Direct2D utilise 3 × 3 matrices pour calculer les transformations.

Les membres de la [**\_ matrice d2d1 \_ matrice \_ F**](/windows/desktop/Direct2D/d2d1-matrix-3x2-f) sont nommés en fonction de leur position d’index : le membre **\_ 11** est l’élément (1, 1), le membre **\_ 12** est l’élément (1, 2), et ainsi de suite. Bien que vous puissiez initialiser les membres de la structure directement, il est recommandé d’utiliser la classe [**d2d1 :: Matrix3x2F**](/windows/desktop/api/d2d1helper/nl-d2d1helper-matrix3x2f) . Cette classe hérite de **d2d1 \_ Matrix \_ matrice \_ F** et fournit des méthodes d’assistance pour créer l’une des transformations affines de base. La classe définit également l' [**opérateur \* ()**](/windows/desktop/api/d2d1helper/nf-d2d1helper-matrix3x2f-operator-mult) pour composer deux ou plusieurs transformations, comme décrit dans [application de transformations dans Direct2D](applying-transforms-in-direct2d.md).

## <a name="next"></a>Suivant

[Module 4. Entrée utilisateur](module-4--user-input.md)

 

 