---
title: Dmax (SM5-ASM)
description: Valeur maximale à double précision au niveau du composant.
ms.assetid: 34ED8B34-2592-4BBB-BCF0-F2222E4D51D9
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b6846da6fbf3ad5d42be5131322e1214fc49fe2627b824775798e4527de3d24
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120068369"
---
# <a name="dmax-sm5---asm"></a>Dmax (SM5-ASM)

Valeur maximale à double précision au niveau du composant.



| Dmax \[ \_ SAT \] dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle \] , \[ - \] src1 \[ \_ ABS \] \[ . Swizzle\] |
|---------------------------------------------------------------------------------------------|



 



| Élément                                                            | Description                                                                                                                                                                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[dans \] l’adresse des résultats de l’opération.<br/> *dest*  =  . *src0*  >=  *src1* ? *src0* : *src1*<br/> >= est utilisé à la place de > afin que si min (x, y) = x, alors Max (x, y) = y. <br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[dans \] la valeur à comparer à *src1*.<br/>                                                                                                                                                           |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[dans \] la valeur à comparer à *src0*.<br/>                                                                                                                                                           |



 

## <a name="remarks"></a>Remarques

NaN a une gestion spéciale. Si un opérande source est NaN, l’autre opérande source est retourné. Le choix est effectué par composant. Si les deux sont NaN, toute représentation NaN est retournée.

Les Swizzles valides pour les paramètres sources sont. XYZW,. Xyxy,. zwxy,. zwzw. Les masques de *dest* valides sont. XY,. ZW et. XYZW. Les mappages *src* suivants sont postérieurs à Swizzle :

-   *dest* est un double vec2 entre (x 32LSB, y 32MSB) et (z 32LSB, w 32MSB).
-   *src0* est un double vec2 entre (x 32LSB, y 32MSB) et (z 32LSB, w 32MSB).
-   *src1* est un double vec2 entre (x 32LSB, y 32MSB) et (z 32LSB, w 32MSB).

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

 

 





