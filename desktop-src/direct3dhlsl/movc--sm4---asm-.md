---
title: MOVC (SM4-ASM)
description: Déplacement conditionnel au niveau du composant. | MOVC (SM4-ASM)
ms.assetid: B7F19DF5-282F-41D4-AE2D-6ACF61A42088
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81da36b39f60929bdfbac3b4a37c379189cf358ed4844e1a4cc899f867970065
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120095359"
---
# <a name="movc-sm4---asm"></a>MOVC (SM4-ASM)

Déplacement conditionnel au niveau du composant.



| MOVC \[ \_ SAT \] dest \[ . Mask \] , src0 \[ . Swizzle \] , \[ - \] src1 \[ \_ ABS \] \[ . Swizzle \] , \[ - \] src2 \[ \_ ABS \] \[ . Swizzle \] , |
|----------------------------------------------------------------------------------------------------------------|



 



| Élément                                                            | Description                                                                                                                    |
|-----------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[dans \] l’adresse du résultat de l’opération. <br/> Si *src0*, puis *dest*  =  *src1* else *dest*  =  *src2*<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[dans \] les composants sur lesquels tester la condition.<br/>                                                               |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[dans \] les composants à déplacer. <br/>                                                                                     |
| <span id="src2"></span><span id="SRC2"></span>*src2*<br/> | \[dans \] les composants à déplacer.<br/>                                                                                      |



 

## <a name="remarks"></a>Remarques

L’exemple suivant montre comment utiliser cette instruction.

``` syntax
                for each component in dest[.mask]
                    if the corresponding component in src0 (POS-swizzle)
                       has any bit set
                    {
                        copy this component (POS-swizzle) from src1 into dest
                    }
                    else
                    {
                        copy this component (POS-swizzle) from src2 into dest
                    }
                endfor
```

Les modificateurs sur *src1* et *src2*, à l’exception de Swizzle, supposent que les données sont à virgule flottante. L’absence de modificateurs déplace uniquement les données sans modifier les bits.

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

 

 





