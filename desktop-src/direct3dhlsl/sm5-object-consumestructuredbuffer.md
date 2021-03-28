---
title: ConsumeStructuredBuffer
description: Mémoire tampon d’entrée qui apparaît sous forme de flux à partir duquel le nuanceur peut extraire des valeurs. Seules les mémoires tampons structurées peuvent être des types de T qui sont des structures.
ms.assetid: 373bdd97-6186-4bce-99bf-738a153234f6
keywords:
- HLSL ConsumeStructuredBuffer
topic_type:
- apiref
api_name:
- ConsumeStructuredBuffer
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: af7a670713dc5b63839702a04a632dda61ebfa43
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104991021"
---
# <a name="consumestructuredbuffer"></a>ConsumeStructuredBuffer

Mémoire tampon d’entrée qui apparaît sous forme de flux à partir duquel le nuanceur peut extraire des valeurs. Seules les mémoires tampons structurées peuvent être des types de T qui sont des structures.



| Méthode                                                                    | Description                                 |
|---------------------------------------------------------------------------|---------------------------------------------|
| [**Utiliser**](sm5-object-consumestructuredbuffer-consume.md)             | Supprime une valeur à partir de la fin de la mémoire tampon. |
| [**GetDimensions**](sm5-object-consumestructuredbuffer-getdimensions.md) | Obtient les dimensions de ressource.               |



 

Le format UAV lié à cette ressource doit être créé avec le format DXGI \_ \_ inconnu.

Le UAV lié à cette ressource doit avoir été créé avec l’ajout de l' [**\_ \_ \_ indicateur \_ UAV de tampon d3d11**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_buffer_uav_flag).

Pour plus d’informations sur l’utilisation de mémoires tampons structurées, consultez les deux sections : [Append et consume](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-resources) buffer et [Structured buffer](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-resources).

## <a name="minimum-shader-model"></a>Modèle de nuanceur minimal

Cet objet est pris en charge dans les modèles de nuanceur suivants.



| Modèle de nuanceur                                                                | Prise en charge |
|-----------------------------------------------------------------------------|-----------|
| [Nuancier modèle 5](d3d11-graphics-reference-sm5.md) et modèles de nuanceur supérieurs | Oui       |



 

Cet objet est pris en charge pour les types de nuanceurs suivants :



| Sommet | Forme | Domain | Géométrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Objets Shader Model 5](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

 