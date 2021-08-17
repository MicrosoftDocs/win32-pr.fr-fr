---
title: RWTexture2DArray
description: Ressource en lecture/écriture. | RWTexture2DArray
ms.assetid: 6a6f3655-f1c0-4d5b-91a2-d79da65858b8
keywords:
- HLSL RWTexture2DArray
topic_type:
- apiref
api_name:
- RWTexture2DArray
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e9ae4d4c7c47012b71a70916f5861975176b86e6612cb2a4fec3ea6c9c6e17cb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120095129"
---
# <a name="rwtexture2darray"></a>RWTexture2DArray

Ressource en lecture/écriture.



| Méthode                                                             | Description                   |
|--------------------------------------------------------------------|-------------------------------|
| [**GetDimensions**](sm5-object-rwtexture2darray-getdimensions.md) | Obtient les dimensions de ressource. |
| [**Load**](rwtexture2darray-load.md)                              | Lit les données de texture.           |
| [**Opérateur\[\]**](sm5-object-rwtexture2darray-operatorindex.md)  | Obtient une variable de ressource.     |



 

Vous pouvez préfixer les objets **RWTexture2DArray** avec la classe de stockage **globallycoherent**. Cette classe de stockage entraîne des barrières et des synchronisations de la mémoire pour vider les données sur l’ensemble du GPU, de telle sorte que les autres groupes puissent voir les écritures. Sans ce spécificateur, une barrière de mémoire ou une synchronisation vide un UAV uniquement dans le groupe actuel.

Un objet **RWTexture2DArray** requiert un type d’élément dans une instruction de déclaration pour l’objet. Par exemple, la déclaration suivante est correcte :


```
RWTexture2DArray<float> tex;
```



Étant donné qu’un objet **RWTexture2DArray** est un objet de type UAV, ses propriétés diffèrent d’un objet de type de vue de ressource (SRV) de nuanceur, tel qu’un objet [**Texture2DArray**](sm5-object-texture2darray.md) . Par exemple, vous pouvez lire et écrire dans un objet **RWTexture2DArray** , mais vous ne pouvez lire qu’à partir d’un objet **Texture2DArray** .

Un objet **RWTexture2DArray** ne peut pas utiliser les méthodes d’un objet [**Texture2DArray**](sm5-object-texture2darray.md) , comme [Sample](dx-graphics-hlsl-to-sample.md). Toutefois, étant donné que vous pouvez créer plusieurs types d’affichages pour la même ressource, vous pouvez déclarer plusieurs types de texture comme une seule texture dans plusieurs nuanceurs. Par exemple, vous pouvez déclarer et utiliser un objet **RWTexture2DArray** comme *Tex* dans un nuanceur de calcul, puis déclarer et utiliser un objet **Texture2DArray** comme *Tex* dans un nuanceur de pixels.

> [!Note]  
> Le runtime applique certains modèles d’utilisation quand vous créez plusieurs types d’affichages dans la même ressource. Par exemple, le runtime ne vous permet pas d’avoir à la fois un mappage UAV pour une ressource et un mappage SRV pour la même ressource active en même temps.

 

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

 

 




