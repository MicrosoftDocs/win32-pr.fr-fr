---
title: DMin (SM5-ASM)
description: Valeur minimale à double précision au niveau du composant.
ms.assetid: 77331B4D-C4B5-49B2-BB6A-77BD5050B575
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e199b01c68acca6609123425438f309af872fb4
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104030586"
---
# <a name="dmin-sm5---asm"></a>DMin (SM5-ASM)

Valeur minimale à double précision au niveau du composant.



| Dmin \[ \_ SAT \] dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle \] , \[ - \] src1 \[ \_ ABS \] \[ . Swizzle\] |
|---------------------------------------------------------------------------------------------|



 



| Élément                                                            | Description                                                                                                                                                                                                  |
|-----------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[dans \] l’adresse des résultats de l’opération.<br/> *dest*  =  . *src0*  <  *src1* ? *src0* : *src1*<br/> < est utilisé à la place de <= de sorte que si min (x, y) = x, Max (x, y) = y. <br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[dans \] les composants à comparer à *src1*.<br/>                                                                                                                                                     |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[dans \] les composants à comparer à *src0*.<br/>                                                                                                                                                     |



 

## <a name="remarks"></a>Notes

NaN a une gestion spéciale. Si un opérande source est NaN, l’autre opérande source est retourné. Le choix est effectué par composant. Si les deux sont NaN, toute représentation NaN est retournée.

Les Swizzles valides pour les paramètres sources sont. XYZW,. Xyxy,. zwxy,. zwzw. Les masques de *dest* valides sont. XY,. ZW et. XYZW. Les mappages *src* suivants sont postérieurs à Swizzle :

-   *dest* est un double vec2 entre (x 32LSB, y 32MSB) et (z 32LSB, w 32MSB).
-   *src0* est un double vec2 entre (x 32LSB, y 32MSB) et (z 32LSB, w 32MSB).
-   *src1* est un double vec2 entre (x 32LSB, y 32MSB) et (z 32LSB, w 32MSB).

Cette instruction s’applique aux étapes suivantes du nuanceur :



| Sommet | Forme | Domain | Géométrie | Pixel | Compute |
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

 

 





