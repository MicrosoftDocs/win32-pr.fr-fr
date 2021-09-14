---
title: instance
description: Utilisez cet attribut pour instancier un nuanceur Geometry.
ms.assetid: 0e487e52-53d0-4193-99b2-fd018a061b42
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4749e11db00b38e5e223e11315de86656b2f6488
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127232242"
---
# <a name="instance"></a>instance

Utilisez cet attribut pour instancier un nuanceur Geometry.


```
instance(X)   
```



## <a name="remarks"></a>Notes

X est un index d’entiers qui indique le nombre d’instances à exécuter pour chaque élément dessiné (par exemple, pour chaque triangle). Lorsque vous utilisez cet attribut, utilisez [SV \_ GSInstanceID](sv-gsinstanceid.md) pour identifier l’instance d’un nuanceur Geometry qui est exécutée.

Cet attribut est pris en charge dans les types de nuanceurs suivants :



| Sommet | Forme | Domain | Géométrie | Pixel | Calcul |
|--------|------|--------|----------|-------|---------|
|        |      |        | x        |       |         |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Attributs du modèle de nuanceur 5](d3d11-graphics-reference-sm5-attributes.md)
</dt> <dt>

[Shader, modèle 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




