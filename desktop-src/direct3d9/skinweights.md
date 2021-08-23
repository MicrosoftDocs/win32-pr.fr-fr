---
description: Ce modèle est instancié au niveau de chaque maille.
ms.assetid: ac5289c6-989c-43b4-9190-ac8f831a05f0
title: SkinWeights
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0bb76b1c0860e64f2e1e8b42cb7ed4d2af984cc043425b97e03cf997714d0e63
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119627909"
---
# <a name="skinweights"></a>SkinWeights

Ce modèle est instancié au niveau de chaque maille. Au sein d’une maille, une séquence de n instances de ce modèle s’affiche, où n est le nombre d’OS (images de fichiers X) qui influencent les vertex de la maille. Chaque instance du modèle définit fondamentalement l’influence d’un segment particulier sur la maille. Il existe une liste d’index de vertex et une liste correspondante de poids.

``` syntax
template SkinWeights 
{ 
    < 6F0D123B-BAD2-4167-A0D0-80224F25FABB > 
    STRING transformNodeName; 
    DWORD nWeights; 
    array DWORD vertexIndices[nWeights]; 
    array float weights[nWeights]; 
    Matrix4x4 matrixOffset; 
} 
```

Où :

-   Le nom du segment dont l’influence est définie est transformNodeName et nWeights est le nombre de vertex affectés par ce segment.
-   Les vertex influencés par ce segment sont contenus dans vertexIndices et les poids de chacun des vertex influencés par ce segment sont contenus dans les pondérations.
-   La matrice matrixOffset transforme les sommets de maillage en espace du segment. En cas de concaténation à la transformation du segment, les coordonnées de l’espace universel du maillage sont affectées par le segment. Consultez [**Matrix4x4**](matrix4x4.md).

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Modèles](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



