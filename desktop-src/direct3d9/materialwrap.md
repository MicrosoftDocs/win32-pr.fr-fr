---
description: Définit un ensemble de deux valeurs booléennes utilisées dans le modèle MeshFaceWraps pour définir la topologie de texture d’une face individuelle. Utilisez à la place de Boolean2d lorsque les coordonnées de texture (u, v) s’étendent à la plage de 0 à 2 au lieu de 0 à 1.
ms.assetid: 0d1755fc-66cb-4372-b9d0-fb320c55d6a7
title: MaterialWrap
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 656c5f7d4eaad52a75cffca0189a1e6fa36e3e89714d8ee0225a3aeec21c8e10
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118798920"
---
# <a name="materialwrap"></a>MaterialWrap

Définit un ensemble de deux valeurs booléennes utilisées dans le modèle [**MeshFaceWraps**](meshfacewraps.md) pour définir la topologie de texture d’une face individuelle. Utilisez à la place de [**Boolean2d**](boolean2d.md) lorsque les coordonnées de texture (u, v) s’étendent à la plage de 0 à 2 au lieu de 0 à 1.

``` syntax
template MaterialWrap
{
    < 4885ae60-78e8-11cf-8f52-0040333594a3 >
    Boolean u;
    Boolean v;
} 
```

Où :

-   valeur u-Boolean. Consultez [**Boolean**](boolean.md).
-   v-valeur booléenne. Consultez [**Boolean**](boolean.md).

> [!Note]  
> Le modèle [**MeshFaceWraps**](meshfacewraps.md) n’est plus utilisé.

 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Modèles](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



