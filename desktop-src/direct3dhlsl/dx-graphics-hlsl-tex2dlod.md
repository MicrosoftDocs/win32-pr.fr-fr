---
title: tex2Dlod
description: Échantillonne une texture 2D avec des mipmaps. Le LOD mipmap est spécifié dans t.w.
ms.assetid: 689eff39-f6ac-4c25-8b92-ca68707ae8ad
keywords:
- HLSL tex2Dlod
topic_type:
- apiref
api_name:
- tex2Dlod
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f63a922fe86dc10d984369a1a872f84089b4db34
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127012727"
---
# <a name="tex2dlod"></a>tex2Dlod

Échantillonne une texture 2D avec des mipmaps. Le LOD mipmap est spécifié dans t.w.



| RET tex2Dlod (s, t) |
|--------------------|



 

## <a name="parameters"></a>Paramètres



| Élément                                                   | Description                               |
|--------------------------------------------------------|-------------------------------------------|
| <span id="s"></span><span id="S"></span>*x*<br/> | \[dans \] l’état de l’échantillonneur.<br/>      |
| <span id="t"></span><span id="T"></span>*t*<br/> | \[dans \] la coordonnée de texture.<br/> |



 

## <a name="return-value"></a>Valeur renvoyée

Valeur des données de texture.

## <a name="type-description"></a>Description du type



| Nom | Entrée/Sortie | [**Type de modèle**](dx-graphics-hlsl-intrinsic-functions.md)                       | [**Type de composant**](dx-graphics-hlsl-intrinsic-functions.md) | Taille |
|------|--------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| s    | in     | [**object**](dx-graphics-hlsl-intrinsic-functions.md) | [sampler2D](dx-graphics-hlsl-sampler.md)                      | 1    |
| t    | in     | [**graphiques**](dx-graphics-hlsl-intrinsic-functions.md) | [**dissocié**](/windows/desktop/WinProg/windows-data-types)                        | 4    |
| Av  | out    | [**graphiques**](dx-graphics-hlsl-intrinsic-functions.md) | [**dissocié**](/windows/desktop/WinProg/windows-data-types)                        | 4    |



 

## <a name="minimum-shader-model"></a>Modèle de nuanceur minimal

Cette fonction est prise en charge dans les modèles de nuanceur suivants.



| Modèle de nuanceur                                                                       | Prise en charge |
|------------------------------------------------------------------------------------|-----------|
| [Nuancier modèle 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) et modèles de nuanceur plus élevés | Oui       |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md)                          | non        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)                          | non        |



 

## <a name="remarks"></a>Notes

À partir de Direct3D 10, vous pouvez utiliser la nouvelle syntaxe HLSL pour accéder aux textures et autres ressources. Vous pouvez remplacer les fonctions de recherche de texture de style intrinsèque, telles que **tex2Dlod**, par un style plus orienté objet. Dans ce style orienté objet, les textures sont dissociées des échantillonneurs et ont des méthodes de chargement et d’échantillonnage.

Pour échantillonner une texture 2D, au lieu d’utiliser **tex2Dlod** comme dans ce code :


```
sampler S;
...
color = tex2Dlod(S, Location);
```



Utilisez la méthode [SampleLevel](dx-graphics-hlsl-to-samplelevel.md) d’un [**objet texture**](dx-graphics-hlsl-to-type.md) comme dans ce code :


```
Texture2D MyTexture;
SamplerState MySampler;
...
color = MyTexture.SampleLevel(MySampler, Location, LOD);
```



Pour utiliser les fonctions de recherche de texture de style intrinsèque, telles que **tex2Dlod**, avec le [nuanceur modèle 4](dx-graphics-hlsl-sm4.md) et versions ultérieures, utilisez [**D3DCOMPILE \_ activer la \_ \_ compatibilité descendante**](d3dcompile-constants.md) pour la compilation. Toutefois, si vous souhaitez cibler le modèle de nuanceur 4 et les versions ultérieures (même [ \* \_ 4 \_ 0 \_ niveau \_ 9 \_ \* ](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro)) avec un code de style orienté objet plus récent, migrez vers la syntaxe HLSL la plus récente.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Fonctions intrinsèques (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

