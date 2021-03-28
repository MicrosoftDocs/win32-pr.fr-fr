---
title: RWTexture1DArray
description: Ressource en lecture/écriture. | RWTexture1DArray
ms.assetid: 214c7e7d-4e74-4f4f-bf78-98e9df0b3a0e
keywords:
- HLSL RWTexture1DArray
topic_type:
- apiref
api_name:
- RWTexture1DArray
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2e7f6841cb1f15b12c9755da2a9fae50e42ed333
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "103953667"
---
# <a name="rwtexture1darray"></a>RWTexture1DArray

Ressource en lecture/écriture.



| Méthode                                                             | Description                   |
|--------------------------------------------------------------------|-------------------------------|
| [**GetDimensions**](sm5-object-rwtexture1darray-getdimensions.md) | Obtient les dimensions de ressource. |
| [**Load**](rwtexture1darray-load.md)                              | Lit les données de texture.           |
| [**Opérateur\[\]**](sm5-object-rwtexture1darray-operatorindex.md)  | Obtient une variable de ressource.     |



 

Vous pouvez préfixer les objets **RWTexture1DArray** avec la classe de stockage **globallycoherent**. Cette classe de stockage entraîne des barrières et des synchronisations de la mémoire pour vider les données sur l’ensemble du GPU, de telle sorte que les autres groupes puissent voir les écritures. Sans ce spécificateur, une barrière de mémoire ou une synchronisation vide un UAV uniquement dans le groupe actuel.

Un objet **RWTexture1DArray** requiert un type d’élément dans une instruction de déclaration pour l’objet. Par exemple, la déclaration suivante est correcte :


```
RWTexture1DArray<float> tex;
```



Étant donné qu’un objet **RWTexture1DArray** est un objet de type UAV, ses propriétés diffèrent d’un objet de type de vue de ressource (SRV) de nuanceur, tel qu’un objet [**Texture1DArray**](sm5-object-texture1darray.md) . Par exemple, vous pouvez lire et écrire dans un objet **RWTexture1DArray** , mais vous ne pouvez lire qu’à partir d’un objet **Texture1DArray** .

Un objet **RWTexture1DArray** ne peut pas utiliser les méthodes d’un objet [**Texture1DArray**](sm5-object-texture1darray.md) , comme [Sample](dx-graphics-hlsl-to-sample.md). Toutefois, étant donné que vous pouvez créer plusieurs types d’affichages pour la même ressource, vous pouvez déclarer plusieurs types de texture comme une seule texture dans plusieurs nuanceurs. Par exemple, vous pouvez déclarer et utiliser un objet **RWTexture1DArray** comme *Tex* dans un nuanceur de calcul, puis déclarer et utiliser un objet **Texture1DArray** comme *Tex* dans un nuanceur de pixels.

> [!Note]  
> Le runtime applique certains modèles d’utilisation quand vous créez plusieurs types d’affichages dans la même ressource. Par exemple, le runtime ne vous permet pas d’avoir à la fois un mappage UAV pour une ressource et un mappage SRV pour la même ressource active en même temps.

 

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

 

 




