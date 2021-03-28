---
title: ftod (SM5-ASM)
description: Conversion au niveau du composant des données à virgule flottante simple précision en données à virgule flottante double précision.
ms.assetid: 95297556-41ED-4ED0-8F9A-16B7A440AF25
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6790735745805426d32aefcc5d5d771ade644e43
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104313705"
---
# <a name="ftod-sm5---asm"></a>ftod (SM5-ASM)

Conversion au niveau du composant des données à virgule flottante simple précision en données à virgule flottante double précision.



| ftod dest \[ . Mask \] , \[ - \] src \[ . Swizzle \] , |
|-------------------------------------------|



 



| Élément                                                            | Description                                          |
|-----------------------------------------------------------------|------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[dans \] l’adresse des données converties.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[dans \] les données à convertir.<br/>          |



 

## <a name="remarks"></a>Notes

Chaque composant de la source est converti à partir de la représentation à simple précision en représentation à double précision.

Les masques de *dest* valides sont. XY,. ZW et. XYZW. . XY reçoit le résultat de la première conversion, et. ZW reçoit le résultat de la deuxième conversion.

*dest* est un double vec2 entre (x 32LSB, y 32MSB) et (z 32LSB, w 32MSB).

*src* est un vec2 flottant sur x et y (ZW ignoré) (Swizzle).

Pour les conversions de type float32<->, les implémentations peuvent honorer des dénormes float32 ou peuvent les vider.

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

 

 





