---
description: Les sommets de l’espace de la caméra sont calculés en transformant les vertex de l’objet avec la matrice de la vue du monde.
ms.assetid: 889dd0d8-1933-4901-9bbc-06c3caa26d3e
title: Transformations d’espace de caméra (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e621fa8318fa45023cee13ffc6fcfc65abcf8f5b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110767"
---
# <a name="camera-space-transformations-direct3d-9"></a>Transformations d’espace de caméra (Direct3D 9)

Les sommets de l’espace de la caméra sont calculés en transformant les vertex de l’objet avec la matrice de la vue du monde.

V = V \* wvMatrix

Les normales des sommets, dans l’espace de l’appareil photo, sont calculées en transformant les normales de l’objet avec la transposer inverse de la matrice de la vue du monde. La matrice de la vue du monde peut être ou non orthogonale.

N = N \* (wvMatrix ⁻ ¹)<sup>T</sup>

L’inversion de matrice et la permutation de matrice fonctionnent sur une matrice 4x4. La multiplication combine la normale avec la partie 3x3 de la matrice 4x4 résultante.

Si l’état de rendu D3DRENDERSTATE \_ NORMALIZENORMALS est défini sur **true**, les vecteurs normaux de vertex sont normalisés après la transformation en espace de caméra comme suit :

N = normal (N)

La position de la lumière dans l’espace de l’appareil photo est calculée en transformant la position de la source de lumière avec la matrice de vue.

LP = LP \* vMatrix

La direction de la lumière dans l’espace de caméra pour une lumière directionnelle est calculée en multipliant la direction de la source de lumière par la matrice de vue, en normalisant et en annulant le résultat.

L<sub>Rép</sub> =-normal (L<sub>Rép</sub> \* wvMatrix)

Pour le point de D3DLIGHT \_ et D3DLIGHT, \_ le sens de la lumière est calculé comme suit :

L<sub>Rép</sub> = normal (V \* LP), où les paramètres sont définis dans le tableau suivant.



| Paramètre       | Valeur par défaut | Type      | Description                                               |
|-----------------|---------------|-----------|-----------------------------------------------------------|
| <sub>Rép</sub> . | N/A           | D3DVECTOR | Vecteur de direction du sommet de l’objet vers la lumière          |
| V               | N/A           | D3DVECTOR | Position du vertex dans l’espace de l’appareil photo                           |
| wvMatrix        | Identité      | D3DMATRIX | Matrice composite contenant les transformations universelles et de vue |
| N               | N/A           | D3DVECTOR | Vertex-normal                                             |
| Aid              | N/A           | D3DVECTOR | Position de la lumière dans l’espace de l’appareil photo                            |
| vMatrix         | Identité      | D3DMATRIX | Matrice contenant la transformation de la vue                      |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Mathématiques d’éclairage](mathematics-of-lighting.md)
</dt> </dl>

 

 



