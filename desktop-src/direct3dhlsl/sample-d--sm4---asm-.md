---
title: sample_d (SM4-ASM)
description: Échantillonne des données à partir de l’élément/texture spécifié à l’aide de l’adresse spécifiée et du mode de filtrage identifié par l’échantillonneur donné. | sample_d (SM4-ASM)
ms.assetid: 9CF57C4A-C0D1-4D57-A5EE-62BBBB291438
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: abe2d3ad310c18ff2bb10e101c95e0267d534fed
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104992041"
---
# <a name="sample_d-sm4---asm"></a>exemple \_ d (SM4-ASM)

Échantillonne des données à partir de l’élément/texture spécifié à l’aide de l’adresse spécifiée et du mode de filtrage identifié par l’échantillonneur donné.



| ssample \_ d \[ \_ aoffimmi (u, v, w) \] dest \[ . Mask \] , srcAddress \[ . Swizzle \] , srcResource \[ . Swizzle \] , srcSampler, srcXDerivatives \[ . Swizzle \] , srcYDerivatives \[ . Swizzle\] |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|



 



| Élément                                                                                                                               | Description                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/>                                                                    | \[dans \] l’adresse des résultats de l’opération.<br/>                                                                  |
| <span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*<br/>                     | \[dans \] un ensemble de coordonnées de texture. Pour plus d’informations, consultez l' [exemple](sample--sm4---asm-.md) d’instruction.<br/>      |
| <span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*<br/>                 | \[dans \] un registre de texture. Pour plus d’informations, consultez l' **exemple** d’instruction.<br/>                                      |
| <span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*<br/>                     | \[dans \] un registre d’échantillonneur. Pour plus d’informations, consultez l' **exemple** d’instruction.<br/>                                      |
| <span id="srcXDerivatives"></span><span id="srcxderivatives"></span><span id="SRCXDERIVATIVES"></span>*srcXDerivatives*<br/> | \[dans \] les dérivés de l’adresse source sur l’axe x. Pour plus d’informations, consultez la section **Notes** .<br/> |
| <span id="srcYDerivatives"></span><span id="srcyderivatives"></span><span id="SRCYDERIVATIVES"></span>*srcYDerivatives*<br/> | \[dans \] les dérivés de l’adresse source de l’axe y. Pour plus d’informations, consultez la section **Notes** .<br/> |



 

## <a name="remarks"></a>Notes

Cette instruction se comporte comme l' [exemple](sample--sm4---asm-.md) d’instruction, sauf que les dérivés de l’adresse source sur la direction x et de l’axe y sont fournis par des paramètres supplémentaires, *srcXDerivatives* et *srcYDerivatives*, respectivement. Ces dérivés se trouvent dans l’espace de coordonnées de texture normalisé.

Les composants r, g et b de *srcXDerivatives* (pos-Swizzle) fournissent du/DX, DV/DX et DW/DX. Le composant « a » (POS-Swizzle) est ignoré.

Les composants r, g et b de *srcYDerivatives* (pos-Swizzle) fournissent du/dy, DV/dy et DW/dy. Le composant « a » (POS-Swizzle) est ignoré.

Contrairement à l' **exemple** d’instruction, qui est autorisé à partager un calcul de LOD unique sur un tampon 2x2, l' **échantillon \_ d** doit calculer la valeur de LOD entièrement indépendamment, par pixel lorsqu’il est utilisé dans le nuanceur de pixels.

Si les entrées dérivées de l' **exemple \_ d** proviennent d’instructions de calcul dérivées dans le nuanceur de pixels et que les valeurs incluent INF/Nan, le comportement de l' **exemple \_ d** peut ne pas correspondre à l' **exemple** d’instruction, qui calcule implicitement la dérivée. Les valeurs INF/NaN peuvent affecter différemment le calcul de LOD.

L’extraction à partir d’un emplacement d’entrée auquel rien n’est lié retourne 0 pour tous les composants.

### <a name="restrictions"></a>Restrictions

-   l' **exemple \_ d** hérite des mêmes restrictions que l' **exemple** d’instruction, ainsi qu’une restriction supplémentaire ci-dessous pour ses paramètres supplémentaires.
-   *srcXDerivatives* et *srcYDerivatives* doivent être des registres Temp (r \# /x \# ), constantBuffer (CB \# ), Input (v \# ) ou une ou plusieurs valeurs immédiates.

Cette instruction s’applique aux étapes suivantes du nuanceur :



| Nuanceur de sommets | Nuanceur de géométrie | Nuanceur de pixels |
|---------------|-----------------|--------------|
| X             | X               | x            |



 

## <a name="minimum-shader-model"></a>Modèle de nuanceur minimal

Cette fonction est prise en charge dans les modèles de nuanceur suivants.



| Modèle de nuanceur                                              | Prise en charge |
|-----------------------------------------------------------|-----------|
| [Shader, modèle 5](d3d11-graphics-reference-sm5.md)        | Oui       |
| [Modèle de nuanceur 4,1](dx-graphics-hlsl-sm4.md)              | Oui       |
| [Nuanceur modèle 4](dx-graphics-hlsl-sm4.md)                | Oui       |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | non        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | non        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | non        |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Assembly modèle 4 du nuanceur (DirectX HLSL)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





