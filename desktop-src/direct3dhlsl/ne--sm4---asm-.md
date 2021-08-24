---
title: ne (SM4-ASM)
description: Comparaison non égale des points à virgule flottante vectorielle au niveau du composant.
ms.assetid: 5BED97D3-8FF6-4F1C-819B-DC8B4A4F2CCA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 116f6197c33ef3c040d6c02b7aa561e03cdcc694a2878b6f16554c053a8862db
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119457339"
---
# <a name="ne-sm4---asm"></a>ne (SM4-ASM)

Comparaison non égale des points à virgule flottante vectorielle au niveau du composant.



| Nou dest. \[ Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle \] , \[ - \] src1 \[ \_ ABS \] \[ . Swizzle\] |
|----------------------------------------------------------------------------------|



 



| Élément                                                            | Description                                            |
|-----------------------------------------------------------------|--------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[dans \] le résultat de l’opération.<br/>         |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[dans \] les composants à comparer à *src1*.<br/> |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[dans \] les composants à comparer à *src0*.<br/> |



 

## <a name="remarks"></a>Remarques

Cette instruction effectue la comparaison float (*src0* ! = *src1*) pour chaque composant et écrit le résultat dans *dest*.

Si la comparaison est true, 0xFFFFFFFF est retourné pour ce composant. Sinon, 0x0000000 est retourné.

Les dénormes sont vidées avant que la comparaison avec les registres source d’origine ne soit touchée.

+ 0 est égal à-0.

La comparaison avec NaN retourne la valeur true.

Cette instruction s’applique aux étapes suivantes du nuanceur :



| Nuanceur de sommets | Nuanceur de géométrie | Nuanceur de pixels |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

## <a name="minimum-shader-model"></a>Modèle de nuanceur minimal

Cette fonction est prise en charge dans les modèles de nuanceur suivants.



| Modèle de nuanceur                                              | Pris en charge |
|-----------------------------------------------------------|-----------|
| [Shader, modèle 5](d3d11-graphics-reference-sm5.md)        | oui       |
| [Modèle de nuanceur 4,1](dx-graphics-hlsl-sm4.md)              | oui       |
| [Nuanceur modèle 4](dx-graphics-hlsl-sm4.md)                | oui       |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | non        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | non        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | non        |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Assembly modèle 4 du nuanceur (DirectX HLSL)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





