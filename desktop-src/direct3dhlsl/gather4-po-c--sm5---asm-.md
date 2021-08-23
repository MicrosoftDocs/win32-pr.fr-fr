---
title: gather4_po_c (SM5-ASM)
description: Se comporte comme gather4 \_ po, sauf que effectue une comparaison sur les texels, comme dans l’exemple \_ c.
ms.assetid: B128EEF3-3440-4F00-9792-20FB1AE075E9
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 83342aed97663c027b0915f612b13b288192d937d29d364257004cfc8966aec9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119743869"
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



 

## <a name="remarks"></a>Remarques

Consultez l' [**exemple \_ c**](sample-c--sm4---asm-.md) pour plus d’informations sur la façon dont *srcReferenceValue* est comparé à chaque Texel extrait. Contrairement à l' **exemple \_ c**, *gather4 \_ po \_ c* retourne chaque résultat de comparaison, plutôt que de les filtrer.

Cette instruction, par exemple **gather4 \_ po**, fonctionne uniquement avec les textures 2D. Contrairement à [**gather4 \_ c**](gather4-c--sm5---asm-.md), qui fonctionne également avec TextureCubes.

Pour les formats avec des composants float32, si la valeur extraite est normalisée, ou +-INF, elle est utilisée dans l’opération de comparaison non touchée. NaN est utilisé dans l’opération de comparaison comme NaN, mais la représentation exacte du bit de NaN peut être modifiée. Les dénormes sont vidées jusqu’à zéro dans la comparaison. Pour TextureCubes, une certaine synthèse du 4ème Texel manquant doit se produire au niveau des angles, de sorte que la notion de retour de bits inchangé pour le Texel synthétisé ne s’applique pas.

Les formats pris en charge pour **gather4 \_ po \_ c** sont les mêmes que ceux pris en charge pour l' **exemple \_ c**. Il s’agit de formats à un seul composant, donc. R sur srcSampler, plutôt qu’un Swizzle arbitraire.

**gather4 \_ po \_ c** sur une ressource indépendante retourne 0.

Utilisez cette méthode pour le filtrage de table fictive.

Cette instruction s’applique aux étapes suivantes du nuanceur :



| Sommet | Forme | Domaine | Géométrie | Pixel | Calcul |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

## <a name="minimum-shader-model"></a>Modèle de nuanceur minimal

Cette instruction est prise en charge dans les modèles de nuanceur suivants :



| Modèle de nuanceur                                              | Pris en charge |
|-----------------------------------------------------------|-----------|
| [Shader, modèle 5](d3d11-graphics-reference-sm5.md)        | oui       |
| [Modèle de nuanceur 4,1](dx-graphics-hlsl-sm4.md)              | non        |
| [Nuanceur modèle 4](dx-graphics-hlsl-sm4.md)                | non        |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | non        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | non        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | non        |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Assembly modèle 5 du nuanceur (DirectX HLSL)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





