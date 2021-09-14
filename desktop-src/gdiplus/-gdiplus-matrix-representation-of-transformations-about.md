---
description: Une matrice m&\# 215 ; n est un ensemble de nombres organisés en m lignes et n colonnes. L’illustration suivante montre plusieurs matrices.
ms.assetid: 62215ae0-b095-42b2-911c-aa7607a8b61a
title: Représentation matricielle des transformations
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0577cae38c401e842cff2ff14179594f9118dfd2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127012421"
---
# <a name="matrix-representation-of-transformations"></a>Représentation matricielle des transformations

Une matrice *m × n* est un ensemble de nombres organisés en *m* lignes et *n* colonnes. L’illustration suivante montre plusieurs matrices.

![Illustration montrant six matrices de dimensions variables](images/aboutgdip05-art04.png)

Vous pouvez ajouter deux matrices de même taille en ajoutant des éléments individuels. L’illustration suivante montre deux exemples d’ajouts de matrice.

![illustration qui montre comment effectuer une addition de matrice](images/aboutgdip05-art05.png)

Une matrice *m × n* peut être multipliée par une matrice *n × p* , et le résultat est une matrice *m × p* . Le nombre de colonnes dans la première matrice doit être le même que le nombre de lignes dans la seconde matrice. Par exemple, une matrice 4 × 2 peut être multipliée par une matrice 2 × 3 pour produire une matrice 4 × 3.

Les points dans le plan et les lignes et les colonnes d’une matrice peuvent être considérés comme des vecteurs. Par exemple, (2, 5) est un vecteur avec deux composants, et (3, 7, 1) est un vecteur avec trois composants. Le produit scalaire de deux vecteurs est défini comme suit :

(a, b) • (c, d) = AC + BD

(a, b, c) • (d, e, f) = AD + is + cf

Par exemple, le produit scalaire de (2, 3) et (5, 4) est (2) (5) + (3) (4) = 22. Le produit scalaire de (2, 5, 1) et (4, 3, 1) est (2) (4) + (5) (3) + (1) (1) = 24. Notez que le produit scalaire de deux vecteurs est un nombre, et non un autre vecteur. Notez également que vous pouvez calculer le produit scalaire uniquement si les deux vecteurs ont le même nombre de composants.

LET A (i, j) est l’entrée de la matrice A dans la **énième** ligne et la **énième** colonne. Par exemple, un (3, 2) est l’entrée de la matrice A dans les 3 lignes **rd** et 2 **ème** colonne. Supposons que A, B et C sont des matrices, et AB = C. Les entrées de C sont calculées comme suit :

C (i, j) = (ligne i de A) • (colonne j sur B)

L’illustration suivante montre plusieurs exemples de multiplication de matrice.

![illustration qui montre comment effectuer une multiplication de matrice](images/aboutgdip05-art06.png)

Si vous pensez qu’un point du plan est une matrice 1 × 2, vous pouvez transformer ce point en le multipliant par une matrice 2 × 2. L’illustration suivante montre plusieurs transformations appliquées au point (2, 1).

![illustration qui montre comment utiliser la multiplication de matrice pour mettre à l’échelle, faire pivoter ou refléter un point dans un plan](images/aboutgdip05-art07.png)

Toutes les transformations présentées dans l’illustration précédente sont des transformations linéaires. Certaines autres transformations, telles que la translation, ne sont pas linéaires et ne peuvent pas être exprimées sous la forme d’une multiplication par une matrice 2 × 2. Supposons que vous souhaitiez commencer par le point (2, 1), le faire pivoter de 90 degrés, le convertir en 3 unités dans la direction x et traduire les unités informatiques 4 dans la direction y. Pour ce faire, vous pouvez effectuer une multiplication de matrice, suivie d’un ajout de matrice.

![Illustration montrant comment la multiplication et l’addition de matrices peuvent faire pivoter un point et le traduire deux fois](images/aboutgdip05-art08.png)

Une transformation linéaire (multiplication par une matrice 2 × 2) suivie d’une translation (ajout d’une matrice 1 × 2) est appelée une transformation affine. Une alternative au stockage d’une transformation affine dans une paire de matrices (une pour la partie linéaire et l’autre pour la translation) consiste à stocker l’intégralité de la transformation dans une matrice 3 × 3. Pour effectuer cette opération, un point dans le plan doit être stocké dans une matrice 1 × 3 avec une troisième coordonnée factice. La technique habituelle consiste à faire en sorte que toutes les 3 coordonnées soient égales à 1. Par exemple, le point (2, 1) est représenté par la matrice \[ 2 1 1 \] . L’illustration suivante montre une transformation affine (rotation de 90 degrés ; translation de 3 unités dans la direction x, 4 unités sur l’axe y), exprimées sous la forme d’une multiplication par une matrice 3 × 3 unique.

![Illustration montrant comment la multiplication de matrice peut effectuer une transformation affine](images/aboutgdip05-art09.png)

Dans l’exemple précédent, le point (2, 1) est mappé au point (2, 6). Notez que la troisième colonne de la matrice 3 × 3 contient les nombres 0, 0, 1. Ce sera toujours le cas pour la matrice 3 × 3 d’une transformation affine. Les nombres importants sont les six nombres des colonnes 1 et 2. La partie supérieure gauche 2 × 2 de la matrice représente la partie linéaire de la transformation, tandis que les deux premières entrées de la troisième ligne représentent la translation.

![Illustration montrant que les deux premières colonnes sont les plus significatives pour une matrice 3x3 d’une transformation affine](images/aboutgdip05-art10.png)

dans Windows GDI+ vous pouvez stocker une transformation affine dans un objet [**Matrix**](/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) . Étant donné que la troisième colonne d’une matrice qui représente une transformation affine est toujours (0, 0, 1), vous spécifiez uniquement les six nombres dans les deux premières colonnes quand vous construisez un objet de **matrice** . L’instruction `Matrix myMatrix(0.0f, 1.0f, -1.0f, 0.0f, 3.0f, 4.0f);` construit la matrice présentée dans la figure précédente.

## <a name="composite-transformations"></a>Transformations composites

Une transformation composite est une séquence de transformations, l’une suivie de l’autre. Tenez compte des matrices et des transformations figurant dans la liste suivante :

-   Matrice A pivoter de 90 degrés
-   Matrice B mise à l’échelle d’un facteur de 2 dans la direction x
-   La matrice C translate 3 unités sur l’axe y

Si vous commencez par le point (2, 1) (représenté par la matrice \[ 2 1 1) et que vous \] multipliez par A, puis B, puis C, le point (2, 1) subira les trois transformations dans l’ordre indiqué.

\[2 1 1 \] ABC = \[ – 2 5 1\]

Au lieu de stocker les trois parties de la transformation composite dans trois matrices distinctes, vous pouvez multiplier A, B et C ensemble pour obtenir une matrice 3 × 3 unique qui stocke l’intégralité de la transformation composite. Supposons que ABC = D. Un point multiplié par D donne le même résultat qu’un point multiplié par A, puis B, puis C.

\[2 1 1 \] D = \[ – 2 5 1\]

L’illustration suivante montre les matrices A, B, C et D.

![Illustration montrant comment effectuer plusieurs transformations en multipliant les matrices constitutives](images/aboutgdip05-art12.png)

Le fait que la matrice d’une transformation composite puisse être formée en multipliant les matrices de transformation individuelles signifie que toute séquence de transformations affines peut être stockée dans un objet de [**matrice**](/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) unique.

> [!Note]  
> L’ordre d’une transformation composite est important. En général, faire pivoter, puis mettre à l’échelle, puis translater n’est pas identique à l’échelle, faire pivoter, puis traduire. De même, l’ordre de multiplication des matrices est important. En général, ABC n’est pas le même que le BAA.

 

La [**classe Matrix**](/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) fournit plusieurs méthodes pour générer une transformation composite : [**Matrix :: Multiply**](/windows/desktop/api/Gdiplusmatrix/nf-gdiplusmatrix-matrix-multiply), [**Matrix :: Rotate**](/windows/desktop/api/Gdiplusmatrix/nf-gdiplusmatrix-matrix-rotate), [**Matrix :: RotateAt**](/windows/desktop/api/Gdiplusmatrix/nf-gdiplusmatrix-matrix-rotateat), [**Matrix :: Scale**](/windows/desktop/api/Gdiplusmatrix/nf-gdiplusmatrix-matrix-scale), [**Matrix :: Shear**](/windows/desktop/api/Gdiplusmatrix/nf-gdiplusmatrix-matrix-shear)et [**Matrix :: translate**](/windows/desktop/api/Gdiplusmatrix/nf-gdiplusmatrix-matrix-translate). L’exemple suivant crée la matrice d’une transformation composite qui fait pivoter d’abord 30 degrés, puis met à l’échelle d’un facteur de 2 sur l’axe y, puis convertit 5 unités dans la direction x.


```
Matrix myMatrix;
myMatrix.Rotate(30.0f);
myMatrix.Scale(1.0f, 2.0f, MatrixOrderAppend);
myMatrix.Translate(5.0f, 0.0f, MatrixOrderAppend);
```



L’illustration suivante montre la matrice.

![Illustration montrant une matrice avec des valeurs exprimées en tant que fonctions trigonométriques et une matrice avec des valeurs approximatives de ces fonctions](images/aboutgdip05-art13.png)

 

 



