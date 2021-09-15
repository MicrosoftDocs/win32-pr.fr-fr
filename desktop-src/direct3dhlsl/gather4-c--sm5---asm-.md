---
title: gather4_c (SM5-ASM)
description: Identique à gather4, sauf que cette Inserte effectue une comparaison des texels, similaire à l’exemple \_ c.
ms.assetid: 6265151A-36CE-4D31-B7B2-233CEEBDCF87
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 35414aa2cd4d9f0686ab7a5cc17b94caa960cec1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127526373"
---
# <a name="gather4_c-sm5---asm"></a>gather4 \_ c (SM5-ASM)

Identique à [**gather4**](gather4--sm5---asm-.md), sauf que cette Inserte effectue une comparaison des texels, similaire à l' [**exemple \_ c**](sample-c--sm4---asm-.md).



| gather4 \_ c \[ \_ aoffimmi (u, v) \] dest \[ . Mask \] , srcAddress \[ . Swizzle \] , srcResource \[ . Swizzle \] , srcSampler \[ . R \] , srcReferenceValue |
|-----------------------------------------------------------------------------------------------------------------------------------|



 



| Élément                                                                                                                                       | Description                                                                                     |
|--------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/>                                                                            | \[dans \] l’adresse du résultat de l’opération<br/>                                    |
| <span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*<br/>                             | \[dans \] un ensemble de coordonnées de texture.<br/>                                                 |
| <span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*<br/>                         | \[dans \] un registre de texture.<br/>                                                           |
| <span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*<br/>                             | \[dans \] un registre d’échantillonneur.<br/>                                                           |
| <span id="srcReferenceValue"></span><span id="srcreferencevalue"></span><span id="SRCREFERENCEVALUE"></span>*srcReferenceValue*<br/> | \[dans \] un registre avec un seul composant sélectionné, qui est utilisé dans la comparaison.<br/> |



 

## <a name="remarks"></a>Remarques

Consultez l' [**exemple \_ c**](sample-c--sm4---asm-.md) pour obtenir une description de la façon dont *srcReferenceValue* est comparé à chaque Texel extrait. Contrairement à l' **exemple \_ c**, **gather4 \_ c** retourne chaque résultat de comparaison, plutôt que de les filtrer.

Pour les TextureCube Corners, où trois texels réels et un quatrième doivent être synthétisés, la synthèse doit se produire après l’étape de comparaison. Cela signifie que le résultat de la comparaison renvoyée pour la Texel syntesized peut être 0, 0,33, 0,66 ou 1. Certaines implémentations ne peuvent retourner que 0 ou 1 pour le Texel synthétisé. Hormis cette liste de résultats possibles, la méthode permettant de synthétiser le Texel n’est pas spécifiée.

Pour les formats avec des composants float32, si la valeur extraite est normalisée, ou +-INF, elle est utilisée dans l’opération de comparaison non touchée. NaN est utilisé dans l’opération de comparaison comme NaN, mais la représentation exacte du bit de NaN peut être modifiée. Les dénormes sont vidées jusqu’à zéro dans la comparaison. Pour TextureCubes, une certaine synthèse du 4ème Texel manquant doit se produire au niveau des angles, de sorte que la notion de retour de bits inchangé pour le Texel synthétisé ne s’applique pas.

Les formats pris en charge pour *gather4 \_ c* sont les mêmes que ceux pris en charge pour l' *exemple \_ c*. Il s’agit de formats à un seul composant, donc. R sur *srcSampler*, plutôt qu’un Swizzle arbitraire. **gather4 \_ c** sur une ressource indépendante retourne 0.

Utilisez cette instruction pour le filtrage personnalisé des mappages d’ombres.

Cette instruction s’applique aux étapes suivantes du nuanceur :



| Sommet | Forme | Domain | Géométrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

## <a name="minimum-shader-model"></a>Modèle de nuanceur minimal

Cette instruction est prise en charge dans les modèles de nuanceur suivants :



| Modèle de nuanceur                                              | Pris en charge. |
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

 

 





