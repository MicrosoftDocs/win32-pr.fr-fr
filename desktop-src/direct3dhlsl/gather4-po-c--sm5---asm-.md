---
title: gather4_po_c (SM5-ASM)
description: Se comporte comme gather4 \_ po, sauf que effectue une comparaison sur les texels, comme dans l’exemple \_ c.
ms.assetid: B128EEF3-3440-4F00-9792-20FB1AE075E9
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36b07dcad08b4d117a453a3c97e461e6b9b4cab6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127297138"
---
# <a name="gather4_po_c-sm5---asm"></a>gather4 \_ po \_ c (SM5-ASM)

Se comporte comme [**gather4 \_ po**](gather4-po--sm5---asm-.md), sauf que effectue une comparaison sur les texels, comme dans l' [**exemple \_ c**](sample-c--sm4---asm-.md).



| gather4 \_ po \_ c dest \[ . Mask \] , srcAddress \[ . Swizzle \] , srcOffset \[ . Swizzle \] , srcResource \[ . Swizzle \] , srcSampler \[ . R \] , srcReferenceValue |
|-------------------------------------------------------------------------------------------------------------------------------------------|



 



| Élément                                                                                                                                       | Description                                                   |
|--------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/>                                                                            | \[dans \] l’adresse du résultat de l’opération.<br/> |
| <span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*<br/>                             | \[dans \] un ensemble de coordonnées de texture.<br/>               |
| <span id="srcOffset"></span><span id="srcoffset"></span><span id="SRCOFFSET"></span>*srcOffset*<br/>                                 | \[dans \] le décalage.<br/>                                 |
| <span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*<br/>                         | \[dans \] un registre de texture.<br/>                         |
| <span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*<br/>                             | \[dans \] un registre d’échantillonneur.<br/>                         |
| <span id="srcReferenceValue"></span><span id="srcreferencevalue"></span><span id="SRCREFERENCEVALUE"></span>*srcReferenceValue*<br/> | \[dans \] un seul composant sélectionné.<br/>                  |



 

## <a name="remarks"></a>Notes

Consultez l' [**exemple \_ c**](sample-c--sm4---asm-.md) pour plus d’informations sur la façon dont *srcReferenceValue* est comparé à chaque Texel extrait. Contrairement à l' **exemple \_ c**, *gather4 \_ po \_ c* retourne chaque résultat de comparaison, plutôt que de les filtrer.

Cette instruction, par exemple **gather4 \_ po**, fonctionne uniquement avec les textures 2D. Contrairement à [**gather4 \_ c**](gather4-c--sm5---asm-.md), qui fonctionne également avec TextureCubes.

Pour les formats avec des composants float32, si la valeur extraite est normalisée, ou +-INF, elle est utilisée dans l’opération de comparaison non touchée. NaN est utilisé dans l’opération de comparaison comme NaN, mais la représentation exacte du bit de NaN peut être modifiée. Les dénormes sont vidées jusqu’à zéro dans la comparaison. Pour TextureCubes, une certaine synthèse du 4ème Texel manquant doit se produire au niveau des angles, de sorte que la notion de retour de bits inchangé pour le Texel synthétisé ne s’applique pas.

Les formats pris en charge pour **gather4 \_ po \_ c** sont les mêmes que ceux pris en charge pour l' **exemple \_ c**. Il s’agit de formats à un seul composant, donc. R sur srcSampler, plutôt qu’un Swizzle arbitraire.

**gather4 \_ po \_ c** sur une ressource indépendante retourne 0.

Utilisez cette méthode pour le filtrage de table fictive.

Cette instruction s’applique aux étapes suivantes du nuanceur :



| Sommet | Forme | Domain | Géométrie | Pixel | Calcul |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

## <a name="minimum-shader-model"></a>Modèle de nuanceur minimal

Cette instruction est prise en charge dans les modèles de nuanceur suivants :



| Modèle de nuanceur                                              | Prise en charge |
|-----------------------------------------------------------|-----------|
| [Shader, modèle 5](d3d11-graphics-reference-sm5.md)        | Oui       |
| [Modèle de nuanceur 4,1](dx-graphics-hlsl-sm4.md)              | non        |
| [Nuanceur modèle 4](dx-graphics-hlsl-sm4.md)                | non        |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | non        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | non        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | non        |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Assembly modèle 5 du nuanceur (DirectX HLSL)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





