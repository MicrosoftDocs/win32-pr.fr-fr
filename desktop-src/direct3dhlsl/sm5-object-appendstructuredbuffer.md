---
title: AppendStructuredBuffer
description: Mémoire tampon de sortie qui apparaît sous forme de flux auquel le nuanceur peut être ajouté. Seules les mémoires tampons structurées peuvent être des types de T qui sont des structures.
ms.assetid: 377b0358-0f9d-4021-9140-19c3d1bfed38
keywords:
- HLSL AppendStructuredBuffer
topic_type:
- apiref
api_name:
- AppendStructuredBuffer
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 23efdb58b8effc0ccdaf32da31ad93dfaf8f6eae602c6769c947ffa0c0f505d7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118510108"
---
# <a name="appendstructuredbuffer"></a>AppendStructuredBuffer

Mémoire tampon de sortie qui apparaît sous forme de flux auquel le nuanceur peut être ajouté. Seules les mémoires tampons structurées peuvent être des types de T qui sont des structures.



| Méthode                                                                   | Description                               |
|--------------------------------------------------------------------------|-------------------------------------------|
| [**Append**](sm5-object-appendstructuredbuffer-append.md)               | Ajoute une valeur à la fin de la mémoire tampon. |
| [**GetDimensions**](sm5-object-appendstructuredbuffer-getdimensions.md) | Obtient les dimensions de ressource.             |



 

Le format UAV lié à cette ressource doit être créé avec le format DXGI \_ \_ inconnu.

Le UAV lié à cette ressource doit avoir été créé avec l’ajout de l' [**\_ \_ \_ indicateur \_ UAV de tampon d3d11**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_buffer_uav_flag).

Pour plus d’informations sur l’ajout d’une mémoire tampon structurée, consultez les deux sections : [Append et consume](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-resources) buffer et [Structured buffer](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-resources).

## <a name="minimum-shader-model"></a>Modèle de nuanceur minimal

Cet objet est pris en charge dans les modèles de nuanceur suivants.



| Modèle de nuanceur                                                                | Pris en charge |
|-----------------------------------------------------------------------------|-----------|
| [Nuancier modèle 5](d3d11-graphics-reference-sm5.md) et modèles de nuanceur supérieurs | oui       |



 

Cet objet est pris en charge pour les types de nuanceurs suivants :



| Sommet | Forme | Domaine | Géométrie | Pixel | Calcul |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Objets Shader Model 5](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

 