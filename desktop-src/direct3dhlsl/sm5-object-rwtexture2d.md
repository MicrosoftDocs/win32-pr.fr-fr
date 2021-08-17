---
title: RWTexture2D
description: Ressource en lecture/écriture. | RWTexture2D
ms.assetid: 19b383f1-c787-4c20-b77a-60ef9f212b9f
keywords:
- HLSL RWTexture2D
topic_type:
- apiref
api_name:
- RWTexture2D
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c015aaa8606f5d04386b7839584203c5672e4ac1bf031b89eb4c41ca69f7dd14
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118985929"
---
# <a name="rwtexture2d"></a>RWTexture2D

Ressource en lecture/écriture.



| Méthode                                                        | Description                   |
|---------------------------------------------------------------|-------------------------------|
| [**GetDimensions**](sm5-object-rwtexture2d-getdimensions.md) | Obtient les dimensions de ressource. |
| [**Load**](rwtexture2d-load.md)                              | Lit les données de texture.           |
| [**Opérateur\[\]**](sm5-object-rwtexture2d-operatorindex.md)  | Obtient une variable de ressource.     |



 

Vous pouvez préfixer les objets RWTexture2D avec la classe de stockage **globallycoherent**. Cette classe de stockage entraîne des barrières et des synchronisations de la mémoire pour vider les données sur l’ensemble du GPU, de telle sorte que les autres groupes puissent voir les écritures. Sans ce spécificateur, une barrière de mémoire ou une synchronisation vide uniquement un affichage d’accès non ordonné (UAV) dans le groupe actuel.

Un objet RWTexture2D requiert un type d’élément dans une instruction de déclaration pour l’objet. Par exemple, la déclaration suivante n’est pas correcte :


```
// The following declaration is incorrectly coded.
RWTexture2D myTexture;
```



La déclaration suivante est correcte :


```
// The following declaration is correctly coded.
RWTexture2D<float> tex;
```



Étant donné qu’un objet RWTexture2D est un objet de type UAV, ses propriétés diffèrent d’un objet de type de vue de ressource (SRV) de nuanceur, tel qu’un objet [Texture2D](sm5-object-texture2d.md) . Par exemple, vous pouvez lire et écrire dans un objet RWTexture2D, mais vous ne pouvez lire qu’à partir d’un objet Texture2D.

Un objet RWTexture2D ne peut pas utiliser les méthodes d’un objet [Texture2D](sm5-object-texture2d.md) , comme [Sample](dx-graphics-hlsl-to-sample.md). Toutefois, étant donné que vous pouvez créer plusieurs types d’affichages pour la même ressource, vous pouvez déclarer plusieurs types de texture comme une seule texture dans plusieurs nuanceurs. Par exemple, les extraits de code suivants montrent comment vous pouvez déclarer et utiliser un objet RWTexture2D comme *Tex* dans un nuanceur de calcul, puis déclarer et utiliser un objet Texture2D comme *Tex* dans un nuanceur de pixels.

> [!Note]  
> Le runtime applique certains modèles d’utilisation quand vous créez plusieurs types d’affichages dans la même ressource. Par exemple, le runtime ne vous permet pas d’avoir à la fois un mappage UAV pour une ressource et un mappage SRV pour la même ressource active en même temps.

 

Le code suivant concerne le nuanceur de calcul :


```
RWTexture2D<float> tex;
[numthreads(groupDim_x, groupDim_y, 1)]
void main(
    uint3 groupId : SV_GroupID,
    uint3 groupThreadId : SV_GroupThreadID,
    uint3 dispatchThreadId : SV_DispatchThreadID,
    uint groupIndex : SV_GroupIndex)
{
    tex [dispatchThreadId.xy] = <something>;
}
```



Le code suivant concerne le nuanceur de pixels :


```
struct PixelShaderInput
{
    float4 pos : SV_POSITION;
    float2 tex : TEXTURE;
};

Texture2D<float> tex;
float4 main(PixelShaderInput input) : SV_TARGET
{
    return tex.Sample(TextureSampler, input.tex);
}
```



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

 

 




