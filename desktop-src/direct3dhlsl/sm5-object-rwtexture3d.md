---
title: RWTexture3D
description: Ressource en lecture/écriture. | RWTexture3D
ms.assetid: 4d02810e-4f3c-4b20-b057-0ff27d6732b5
keywords:
- HLSL RWTexture3D
topic_type:
- apiref
api_name:
- RWTexture3D
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9b89ed7ff724eabef9fc2b2757c6ac0e5272c69e
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104322045"
---
# <a name="rwtexture3d"></a>RWTexture3D

Ressource en lecture/écriture.



| Méthode                                                        | Description                   |
|---------------------------------------------------------------|-------------------------------|
| [**GetDimensions**](sm5-object-rwtexture3d-getdimensions.md) | Obtient les dimensions de ressource. |
| [**Load**](rwtexture3d-load.md)                              | Lit les données de texture.           |
| [**Opérateur\[\]**](sm5-object-rwtexture3d-operatorindex.md)  | Obtient une variable de ressource.     |



 

Vous pouvez préfixer les objets **RWTexture3D** avec la classe de stockage **globallycoherent**. Cette classe de stockage entraîne des barrières et des synchronisations de la mémoire pour vider les données sur l’ensemble du GPU, de telle sorte que les autres groupes puissent voir les écritures. Sans ce spécificateur, une barrière de mémoire ou une synchronisation vide un UAV uniquement dans le groupe actuel.

Un objet **RWTexture3D** requiert un type d’élément dans une instruction de déclaration pour l’objet. Par exemple, la déclaration suivante est correcte :


```
RWTexture3D<float> tex;
```



Étant donné qu’un objet **RWTexture3D** est un objet de type UAV, ses propriétés diffèrent d’un objet de type de vue de ressource (SRV) de nuanceur, tel qu’un objet [**Texture3D**](sm5-object-texture3d.md) . Par exemple, vous pouvez lire et écrire dans un objet **RWTexture3D** , mais vous ne pouvez lire qu’à partir d’un objet **Texture3D** .

Un objet **RWTexture3D** ne peut pas utiliser les méthodes d’un objet [**Texture3D**](sm5-object-texture3d.md) , comme [Sample](dx-graphics-hlsl-to-sample.md). Toutefois, étant donné que vous pouvez créer plusieurs types d’affichages pour la même ressource, vous pouvez déclarer plusieurs types de texture comme une seule texture dans plusieurs nuanceurs. Par exemple, vous pouvez déclarer et utiliser un objet **RWTexture3D** comme *Tex* dans un nuanceur de calcul, puis déclarer et utiliser un objet **Texture3D** comme *Tex* dans un nuanceur de pixels.

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

 

 




