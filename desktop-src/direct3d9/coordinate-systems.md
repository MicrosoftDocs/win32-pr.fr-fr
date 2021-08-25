---
description: 'En général, les applications graphiques 3D utilisent deux types de systèmes de coordonnées cartésiennes : droitier et droitier.'
ms.assetid: 268c3024-85a5-4fd5-b575-e126dd4be97c
title: Systèmes de coordonnées (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e47b87ae6374d68b8c836dfb4818781e83e77c288f7bf05b121dbb4426c9aad
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119857573"
---
# <a name="coordinate-systems-direct3d-9"></a>Systèmes de coordonnées (Direct3D 9)

En général, les applications graphiques 3D utilisent deux types de systèmes de coordonnées cartésiennes : droitier et droitier. Dans les deux systèmes de coordonnées, l’axe x positif pointe vers la droite et l’axe y positif pointe vers le haut. Vous pouvez vous souvenir de la direction vers laquelle pointe l’axe z positif en pointant les doigts de votre gauche ou de droite dans la direction x positive et en les faisant passer à l’axe y positif. La direction vers laquelle votre Thumb pointe, que ce soit vers vous ou en dehors, est la direction dans laquelle les points positifs de l’axe z pour ce système de coordonnées. L’illustration suivante montre ces deux systèmes de coordonnées.

![illustration des systèmes de coordonnées cartésiens droitiers et droitiers de droite](images/leftrght.png)

Direct3D utilise un système de coordonnées droitier. Si vous portez une application basée sur un système de coordonnées droitier, vous devez apporter deux modifications aux données transmises à Direct3D.

-   Retournez l’ordre des sommets triangles afin que le système les traverse à partir du début. En d’autres termes, si les vertex sont v0, v1, v2, transmettez-les à Direct3D en tant que v0, v2, v1.
-   Utilisez la matrice de vue pour mettre à l’échelle l’espace universel de-1 dans l’axe z. Pour ce faire, retournez le signe du \_ membre 31, \_ 32, \_ 33 et \_ 34 de la structure [**D3DMATRIX**](d3dmatrix.md) que vous utilisez pour votre matrice d’affichage.

Pour obtenir ce qui se trouve dans un monde de droite, utilisez les fonctions [**D3DXMatrixPerspectiveRH**](d3dxmatrixperspectiverh.md) et [**D3DXMatrixOrthoRH**](d3dxmatrixorthorh.md) pour définir la transformation de projection. Toutefois, veillez à utiliser la fonction [**D3DXMatrixLookAtRH**](d3dxmatrixlookatrh.md) correspondante, à inverser l’ordre de sélection de face arrière et à disposer les mappages de cube en conséquence.

Bien que les coordonnées de gauche et de droite sont les systèmes les plus courants, il existe un large éventail d’autres systèmes de coordonnées utilisés dans les logiciels 3D. Par exemple, il n’est pas rare pour les applications de modélisation 3D d’utiliser un système de coordonnées dans lequel l’axe des y pointe vers la visionneuse et l’éloigne de celle-ci, et l’axe z pointe vers le haut.

Formellement, l’orientation d’un ensemble de vecteurs de base (par exemple, un système de coordonnées) peut être trouvée par le calcul du déterminant de la matrice définie par l’ensemble de vecteurs de base. Si le déterminant est positif, on dit qu’il s’agit d’une « orientation positive » (ou droitier). Si le déterminant est négatif, la base est dite « orientée négativement » (ou gauche). Pour obtenir une explication de ce qu’est un déterminante, consultez toute ressource algébrique linéaire.

De manière informelle, vous pouvez utiliser la « règle de droite/gauche » pour déterminer si un ensemble donné de vecteurs de base forme un système de coordonnées droitier ou gauche.

Les opérations essentielles effectuées sur les objets définis dans un système de coordonnées 3D sont la translation, la rotation et la mise à l’échelle. Vous pouvez combiner ces transformations de base pour créer une matrice de transformation. Pour plus d’informations, consultez [transformations (Direct3D 9)](transforms.md).

Lorsque vous combinez ces opérations, les résultats ne sont pas commutatés ; l’ordre dans lequel vous multipliez les matrices est important.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Systèmes de coordonnées et géométrie](coordinate-systems-and-geometry.md)
</dt> </dl>

 

 



