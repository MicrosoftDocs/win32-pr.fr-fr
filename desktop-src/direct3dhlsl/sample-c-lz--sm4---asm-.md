---
title: sample_c_lz (SM4-ASM)
description: Effectue un filtre de comparaison. Cette instruction se comporte comme l’exemple \_ c, sauf que LOD est égal à 0 et que les dérivés sont ignorés.
ms.assetid: 5F11F091-AF2F-4293-88C7-824F11FE01E4
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24ec2889dd3ea4c86af51c8e36bf2e302c6ad4dd
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127291711"
---
# <a name="sample_c_lz-sm4---asm"></a>exemple \_ c \_ LZ (SM4-ASM)

Effectue un filtre de comparaison. Cette instruction se comporte comme l' [exemple \_ c](sample-c--sm4---asm-.md), sauf que LOD est égal à 0 et que les dérivés sont ignorés.



| exemple \_ c \_ LZ \[ \_ aoffimmi (u, v, w) \] dest \[ . Mask \] , srcAddress \[ . Swizzle \] , srcResource. r,//doit être. r Swizzle srcSampler, srcReferenceValue//composant unique sélectionné |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|



 



| Élément                                                                                                                                       | Description                                                                                                                |
|--------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/>                                                                            | \[dans \] l’adresse des résultats de l’opération.<br/>                                                             |
| <span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*<br/>                             | \[dans \] un ensemble de coordonnées de texture. Pour plus d’informations, consultez l' [exemple](sample--sm4---asm-.md) d’instruction.<br/> |
| <span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*<br/>                         | \[dans \] un registre de texture. Pour plus d’informations, consultez l' **exemple** d’instruction.<br/>                                 |
| <span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*<br/>                             | \[dans \] un registre d’échantillonneur. Pour plus d’informations, consultez l' **exemple** d’instruction.<br/>                                 |
| <span id="srcReferenceValue"></span><span id="srcreferencevalue"></span><span id="SRCREFERENCEVALUE"></span>*srcReferenceValue*<br/> | \[dans \] un registre avec un seul composant sélectionné, qui est utilisé dans la comparaison.<br/>                            |



 

## <a name="remarks"></a>Notes

La valeur « LZ » correspond au niveau zéro. Étant donné que les dérivés sont ignorés, cette instruction est disponible dans les nuanceurs autres que le nuanceur de pixels.

Si cette instruction est utilisée avec une texture mipmapped, LOD 0 est échantillonné, à moins que l’échantillonneur ait une pince LOD qui place le LOD ailleurs, ou s’il existe un décalage de LOD, ce qui ferait un décalage à partir de 0. Étant donné que les dérivés sont ignorés, le filtrage anisotrope se comporte comme un filtrage isotrope.

Dans les nuanceurs de pixels, cette instruction peut être utilisée à l’intérieur d’un contrôle de Flow variable lorsque les coordonnées de texture sont dérivées dans le nuanceur, contrairement à l' **exemple \_ c**.

L’extraction à partir d’un emplacement d’entrée auquel rien n’est lié retourne 0 pour tous les composants.

Cette instruction est disponible dans tous les nuanceurs, et pas seulement dans le nuanceur de pixels, à des fins de cohérence.



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

 

 





