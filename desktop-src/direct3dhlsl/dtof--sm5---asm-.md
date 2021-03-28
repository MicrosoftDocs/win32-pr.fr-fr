---
title: dtof (SM5-ASM)
description: Conversion au niveau du composant des données à virgule flottante double précision en données à virgule flottante simple précision.
ms.assetid: 1D2EF05C-06EF-44F0-AA0F-22D3057FF43E
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a66e72cf4c2cb1ac49adc492a586b4cbb9eef3b4
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104313627"
---
# <a name="dtof-sm5---asm"></a>dtof (SM5-ASM)

Conversion au niveau du composant des données à virgule flottante double précision en données à virgule flottante simple précision.



| dtof dest \[ . Mask \] , \[ - \] src \[ . Swizzle \] , |
|-------------------------------------------|



 



| Élément                                                            | Description                                          |
|-----------------------------------------------------------------|------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[dans \] l’adresse des données converties.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[dans \] les données à convertir.<br/>          |



 

## <a name="remarks"></a>Notes

Chaque composant de la source est converti à partir de la représentation à double précision en une représentation à simple précision à l’aide de l’arrondi à la valeur la plus proche.

Le Swizzles valide pour le paramètre source est. XYZW,. Xyxy,. zwxy,. zwzw.

Les masques de *dest* valides sont un ou deux composants. C’est-à-dire :. x,. y,. z,. w,. XY,. XZ,. xw,. YZ,. YW,. ZW le résultat de la première conversion est dirigé vers le premier composant du masque, et le résultat du deuxième composant est placé dans le deuxième composant du masque, s’il est présent.

les composants *dest* sont float32.

*src* est un double vec2 entre (x 32LSB, y 32MSB) et (z 32LSB, w 32MSB) poster Swizzle.

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

 

 





