---
title: dmovc (SM5-ASM)
description: Déplacement conditionnel au niveau du composant. | dmovc (SM5-ASM)
ms.assetid: E376FE08-E251-4BE5-9F15-99B3B67A29C8
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc0ed15d81a91d8a93ce99eda3fa17b91900e0045301f1c5b5d1f56e4448954a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118792380"
---
# <a name="dmovc-sm5---asm"></a>dmovc (SM5-ASM)

Déplacement conditionnel au niveau du composant.



| dmovc \[ \_ SAT \] dest \[ . Mask \] , src0 \[ . Swizzle \] , \[ - \] src1 \[ \_ ABS \] \[ . Swizzle \] , \[ - \] src2 \[ \_ ABS \] \[ . Swizzle \] , |
|-----------------------------------------------------------------------------------------------------------------|



 



| Élément                                                            | Description                                                                                              |
|-----------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[dans \] la destination de déplacement.<br/> Si *src0*, puis *dest*  =  *src1* else *dest*  =  *src2*.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[dans \] les composants pour tester la condition.<br/>                                          |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[dans \] les composants à déplacer si la condition a la valeur true.<br/>                                       |
| <span id="src2"></span><span id="SRC2"></span>*src2*<br/> | \[dans \] les composants à déplacer si la condition est false.<br/>                                      |



 

## <a name="remarks"></a>Remarques

L’exemple suivant montre comment utiliser cette instruction.

``` syntax
                if(the dest mask contains .xy)
                {
                    if(the first 32-bit component of src0, post-swizzle, 
                       has any bit set)
                    {
                        copy the first double from src1 (post swizzle)
                        into dest.xy
                    }
                    else
                    {
                        copy the first double from src2 (post swizzle)
                        into dest.xy
                    }
                }
                if(the dest mask contains .zw)
                {
                    if(the second 32-bit component of src0, post-swizzle, 
                       has any bit set)
                    {
                        copy the second double from src1 (post swizzle)
                        into dest.zw
                    }
                    else
                    {
                        copy the second double from src2 (post swizzle)
                        into dest.zw
                    }
                }
```

Les masques valides pour dest sont. XY,. ZW,. XYZW.

Le Swizzles valide pour *src0* est n’importe quoi. Les deux premiers composants Swizzle sont utilisés pour faciliteront son identification les valeurs de condition de 2 32 bits.

Le Swizzles valide pour *src1* et *src2* contenant des doubles sont. XYZW,. Xyxy,. zwxy,. zwzw. sont. XY,. ZW et. XYZW.

Les mappages *src* ci-dessous sont postérieurs à Swizzle :

-   *dest* est un double vec2 entre (x 32LSB, y 32MSB) et (z 32LSB, w 32MSB).
-   *src0* est un vec2 de composant/32 bits sur x et y (ZW ignoré).
-   *src1* est un double vec2 entre (x 32LSB, y 32MSB) et (z 32LSB, w 32MSB).
-   *src2* est un double vec2 entre (x 32LSB, y 32MSB) et (z 32LSB, w 32MSB).

Les modificateurs sur *src1* et *src2*, à l’exception de Swizzle, supposent que les données sont de type double. L’absence de modificateurs déplace les données sans modifier les bits.

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

 

 





