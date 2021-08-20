---
title: StructuredBuffer
description: Mémoire tampon en lecture seule, qui peut accepter un type T qui est une structure.
ms.assetid: fe2ec0b8-0e19-42b6-9dad-c992ecdeb19e
keywords:
- HLSL StructuredBuffer
topic_type:
- apiref
api_name:
- StructuredBuffer
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b3cdf9d81b04eee56991f7b7950421945d3a5038df4aef9b5e4d2a74b603e468
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117905546"
---
# <a name="structuredbuffer"></a>StructuredBuffer

Mémoire tampon en lecture seule, qui peut accepter un type T qui est une structure.



| Méthode                                                             | Description                            |
|--------------------------------------------------------------------|----------------------------------------|
| [**GetDimensions**](sm5-object-structuredbuffer-getdimensions.md) | Obtient les dimensions de ressource.          |
| [**Load**](structuredbuffer-load.md)                              | Lit les données de la mémoire tampon.                     |
| [**Opérateur\[\]**](sm5-object-structuredbuffer-operatorindex.md)  | Retourne une variable de ressource en lecture seule. |



 

Le format UAV lié à cette ressource doit être créé avec le format DXGI \_ \_ inconnu.

Pour en savoir plus sur les [mémoires tampons structurées](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-resources), consultez la documentation de présentation.

## <a name="minimum-shader-model"></a>Modèle de nuanceur minimal

Cet objet est pris en charge dans les modèles de nuanceur suivants.



| Modèle de nuanceur                                                                                                                                                                                                            | Pris en charge |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------|
| Shader [Model 5](d3d11-graphics-reference-sm5.md) et versions supérieures nuanceur Model [Shader Model 4](dx-graphics-hlsl-sm4.md) (disponible pour les nuanceurs de calcul et de pixel dans Direct3D 11 sur certains périphériques Direct3D 10.)<br/> | oui       |



 

Cet objet est pris en charge pour les types de nuanceurs suivants.



| Sommet | Forme | Domaine | Géométrie | Pixel | Calcul |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Objets Shader Model 5](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

