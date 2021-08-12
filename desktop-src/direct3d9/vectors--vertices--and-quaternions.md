---
description: Tout au long de Direct3D, les sommets décrivent la position et l’orientation. Chaque vertex dans une primitive est décrit par un vecteur qui donne sa position, sa couleur, ses coordonnées de texture et un vecteur normal qui donne son orientation.
ms.assetid: f18b235c-97ff-4779-8584-8e96b62c7ca3
title: Vecteurs, vertex et quaternions (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 601b6a71dcb00356d4de4637a6aabb1eba5c02e49c62380b32732351d15bfcb4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118290439"
---
# <a name="vectors-vertices-and-quaternions-direct3d-9"></a>Vecteurs, vertex et quaternions (Direct3D 9)

Tout au long de Direct3D, les sommets décrivent la position et l’orientation. Chaque vertex dans une primitive est décrit par un vecteur qui donne sa position, sa couleur, ses coordonnées de texture et un vecteur normal qui donne son orientation.

Les quaternions ajoutent un quatrième élément aux \[ valeurs x, y, z \] qui définissent un vecteur à trois composants. Les quaternions sont une alternative aux méthodes de matrice qui sont généralement utilisées pour les rotations 3D. Un Quaternion représente un axe dans l’espace 3D et une rotation autour de cet axe. Par exemple, un Quaternion peut représenter un axe (1, 1, 2) et une rotation de 1 radian. Les quaternions contiennent des informations précieuses, mais leur véritable puissance est celle des deux opérations que vous pouvez effectuer sur ces derniers : la composition et l’interpolation.

L’exécution de la composition sur des quaternions est semblable à la combinaison de ces éléments. La composition de deux quaternions est nonotée comme dans l’illustration suivante.

![illustration de la notation de Quaternion](images/quateq.png)

La composition de deux quaternions appliquée à une géométrie signifie « faire pivoter la géométrie autour de l’axe ₂ par rotation ₂, puis la faire pivoter autour de l’axe ₁ par rotation ₁ ». Dans ce cas, Q représente une rotation autour d’un axe unique qui est le résultat de l’application de q ₂, puis q ₁ à la géométrie.

À l’aide de l’interpolation Quaternion, une application peut calculer un chemin lisse et raisonnable d’un axe et d’une orientation vers une autre. Par conséquent, l’interpolation entre q ₁ et q ₂ offre un moyen simple d’effectuer une animation d’une orientation à une autre.

Lorsque vous utilisez la composition et l’interpolation ensemble, elles vous offrent un moyen simple de manipuler une géométrie de manière à ce qu’elle s’affiche complexe. Par exemple, imaginez que vous avez une géométrie que vous souhaitez faire pivoter vers une orientation donnée. Vous savez que vous souhaitez le faire pivoter de r ₂ degrés autour de ₂ d’axe, puis le faire pivoter de r ₁ degrés autour de l’axe ₁, mais vous ne connaissez pas le Quaternion final. En utilisant la composition, vous pouvez combiner les deux rotations sur la géométrie pour obtenir un seul Quaternion qui est le résultat. Ensuite, vous pouvez interpoler du Quaternion d’origine vers le Quaternion composé pour effectuer une transition en douceur de l’un à l’autre.

La bibliothèque de l’utilitaire D3DX comprend des fonctions qui vous aident à utiliser les quaternions. Par exemple, la fonction [**D3DXQuaternionRotationAxis**](d3dxquaternionrotationaxis.md) ajoute une valeur de rotation à un vecteur qui définit un axe de rotation et retourne le résultat dans un Quaternion défini par une structure [**D3DXQUATERNION**](d3dxquaternion.md) . En outre, la fonction [**D3DXQuaternionMultiply**](d3dxquaternionmultiply.md) compose les quaternions et [**D3DXQuaternionSlerp**](d3dxquaternionslerp.md) effectue une interpolation linéaire sphérique entre deux quaternions.

Les applications Direct3D peuvent utiliser les fonctions suivantes pour simplifier l’utilisation des quaternions.

-   [**D3DXQuaternionBaryCentric**](d3dxquaternionbarycentric.md)
-   [**D3DXQuaternionConjugate**](d3dxquaternionconjugate.md)
-   [**D3DXQuaternionDot**](d3dxquaterniondot.md)
-   [**D3DXQuaternionExp**](d3dxquaternionexp.md)
-   [**D3DXQuaternionIdentity**](d3dxquaternionidentity.md)
-   [**D3DXQuaternionInverse**](d3dxquaternioninverse.md)
-   [**D3DXQuaternionIsIdentity**](d3dxquaternionisidentity.md)
-   [**D3DXQuaternionLength**](d3dxquaternionlength.md)
-   [**D3DXQuaternionLengthSq**](d3dxquaternionlengthsq.md)
-   [**D3DXQuaternionLn**](d3dxquaternionln.md)
-   [**D3DXQuaternionMultiply**](d3dxquaternionmultiply.md)
-   [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md)
-   [**D3DXQuaternionRotationAxis**](d3dxquaternionrotationaxis.md)
-   [**D3DXQuaternionRotationMatrix**](d3dxquaternionrotationmatrix.md)
-   [**D3DXQuaternionRotationYawPitchRoll**](d3dxquaternionrotationyawpitchroll.md)
-   [**D3DXQuaternionSlerp**](d3dxquaternionslerp.md)
-   [**D3DXQuaternionSquad**](d3dxquaternionsquad.md)
-   [**D3DXQuaternionToAxisAngle**](d3dxquaterniontoaxisangle.md)

Les applications Direct3D peuvent utiliser les fonctions suivantes pour simplifier l’utilisation des vecteurs à trois composants.

-   [**D3DXVec3Add**](d3dxvec3add.md)
-   [**D3DXVec3BaryCentric**](d3dxvec3barycentric.md)
-   [**D3DXVec3CatmullRom**](d3dxvec3catmullrom.md)
-   [**D3DXVec3Cross**](d3dxvec3cross.md)
-   [**D3DXVec3Dot**](d3dxvec3dot.md)
-   [**D3DXVec3Hermite**](d3dxvec3hermite.md)
-   [**D3DXVec3Length**](d3dxvec3length.md)
-   [**D3DXVec3LengthSq**](d3dxvec3lengthsq.md)
-   [**D3DXVec3Lerp**](d3dxvec3lerp.md)
-   [**D3DXVec3Maximize**](d3dxvec3maximize.md)
-   [**D3DXVec3Minimize**](d3dxvec3minimize.md)
-   [**D3DXVec3Normalize**](d3dxvec3normalize.md)
-   [**D3DXVec3Project**](d3dxvec3project.md)
-   [**D3DXVec3Scale**](d3dxvec3scale.md)
-   [**D3DXVec3Subtract**](d3dxvec3subtract.md)
-   [**D3DXVec3Transform**](d3dxvec3transform.md)
-   [**D3DXVec3TransformCoord**](d3dxvec3transformcoord.md)
-   [**D3DXVec3TransformNormal**](d3dxvec3transformnormal.md)
-   [**D3DXVec3Unproject**](d3dxvec3unproject.md)

De nombreuses fonctions supplémentaires qui simplifient les tâches à l’aide des vecteurs à deux et quatre composants sont incluses parmi les [fonctions mathématiques](dx9-graphics-reference-d3dx-functions-math.md) fournies par la bibliothèque de l’utilitaire D3DX.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Systèmes de coordonnées et géométrie](coordinate-systems-and-geometry.md)
</dt> </dl>

 

 



