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
ms.openlocfilehash: 524078780ac28d691c4999491bed146a04d34439
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104990928"
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



| Modèle de nuanceur                                                                                                                                                                                                            | Prise en charge |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------|
| Shader [Model 5](d3d11-graphics-reference-sm5.md) et versions supérieures nuanceur Model [Shader Model 4](dx-graphics-hlsl-sm4.md) (disponible pour les nuanceurs de calcul et de pixel dans Direct3D 11 sur certains périphériques Direct3D 10.)<br/> | Oui       |



 

Cet objet est pris en charge pour les types de nuanceurs suivants.



| Sommet | Forme | Domain | Géométrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Objets Shader Model 5](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

