---
title: sample_l (SM4-ASM)
description: Échantillonne des données à partir de l’élément/texture spécifié à l’aide de l’adresse spécifiée et du mode de filtrage identifié par l’échantillonneur donné. | sample_l (SM4-ASM)
ms.assetid: D285F63E-1026-45F1-9959-6F5AB2A27C95
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5acd83d81e4648cc9eae5f8e0166013dcca512a8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127012694"
---
# <a name="sample_l-sm4---asm"></a>exemple \_ l (SM4-ASM)

Échantillonne des données à partir de l’élément/texture spécifié à l’aide de l’adresse spécifiée et du mode de filtrage identifié par l’échantillonneur donné.



| exemple \_ l \[ \_ aoffimmi (u, v, w) \] dest \[ . Mask \] , srcAddress \[ . Swizzle \] , srcResource \[ . Swizzle \] , srcSampler, srcLOD. Sélectionner un \_ composant |
|-------------------------------------------------------------------------------------------------------------------------------------|



 



| Élément                                                                                                               | Description                                                                                                                |
|--------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/>                                                    | \[dans \] l’adresse des résultats de l’opération.<br/>                                                             |
| <span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*<br/>     | \[dans \] un ensemble de coordonnées de texture. Pour plus d’informations, consultez l' [exemple](sample--sm4---asm-.md) d’instruction.<br/> |
| <span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*<br/> | \[dans \] un registre de texture. Pour plus d’informations, consultez l' **exemple** d’instruction.<br/>                                 |
| <span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*<br/>     | \[dans \] un registre d’échantillonneur. Pour plus d’informations, consultez l' **exemple** d’instruction.<br/>                                 |
| <span id="srcLOD"></span><span id="srclod"></span><span id="SRCLOD"></span>*srcLOD*<br/>                     | \[dans \] le LOD.<br/>                                                                                                 |



 

## <a name="remarks"></a>Notes

Cette instruction est identique à [Sample](sample--sm4---asm-.md), sauf que LOD est fourni directement par l’application en tant que valeur scalaire, ce qui ne représente pas de anisotrope. Cette instruction est disponible dans toutes les étapes de nuanceur prodisponibles.

**Sample \_ l** échantillonne la texture à l’aide de *SRCLOD* pour être le LOD. Si la valeur LOD est <= 0, zero’th (mappage le plus grand) est choisi, avec le filtre loupe appliqué (le cas échéant, en fonction du mode de filtre). Étant donné que *srcLOD* est une valeur à virgule flottante, la valeur fractionnaire est utilisée pour interpoler entre deux niveaux MIP, si le filtre réduire est linéaire ou avec un filtrage anisotrope.

l' **exemple \_ l** ignore les dérivés d’adresse, de sorte que le comportement de filtrage est purement isotrope. Étant donné que les dérivés sont ignorés, le filtrage anisotrope se comporte comme un filtrage isotrope.

Les États de l’échantillonneur MIPLODBIAS et MAX/MINMIPLEVEL sont honorés.

Lorsqu’il est utilisé dans le nuanceur de pixels, l' **exemple \_ l** signifie que le choix de LOD est par pixel, sans effet des pixels voisins, par exemple dans le même horodatage 2x2.

L’extraction à partir d’un emplacement d’entrée auquel rien n’est lié retourne 0 pour tous les composants.

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

 

 





