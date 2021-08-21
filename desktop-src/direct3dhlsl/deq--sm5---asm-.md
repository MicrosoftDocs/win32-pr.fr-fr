---
title: DEQ (SM5-ASM)
description: Comparaison d’égalité double précision au niveau du composant.
ms.assetid: 99806989-D3A0-43F4-832A-5F1BD9C59A11
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5781c0b7d757e8bf72b81da54a4d6a8fe7467a40fa2509abdf093e27eb119ddc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119950549"
---
# <a name="deq-sm5---asm"></a>DEQ (SM5-ASM)

Comparaison d’égalité double précision au niveau du composant.



| DEQ \[ \_ SAT \] dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle \] , \[ - \] src1 \[ \_ ABS \] \[ . Swizzle\] |
|--------------------------------------------------------------------------------------------|



 



| Élément                                                            | Description                                                    |
|-----------------------------------------------------------------|----------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[dans \] l’adresse des résultats de l’opération.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[dans \] les composants à comparer à *src1*.<br/>         |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[dans \] les composants à comparer à *src0*.<br/>         |



 

## <a name="remarks"></a>Remarques

Cette instruction effectue la comparaison à virgule flottante double précision (*src0*  ==  *src1*) pour chaque composant et écrit le résultat dans *dest*.

Si la comparaison est true, 32-bit 0xFFFFFFFF est retourné pour ce composant. Sinon 32-bit 0x00000000 est retourné.

La comparaison avec NaN retourne false.

Les masques de *dest* valides sont un ou deux composants. C’est-à-dire :. x,. y,. z,. w,. XY,. XZ,. xw,. YZ,. YW,. ZW le premier composant *dest* dans le masque reçoit le résultat 32 bits pour la première comparaison double. Le deuxième composant dans le masque, s’il est présent, reçoit le résultat 32 bits pour la deuxième comparaison double.

Les Swizzles valides pour les paramètres sources sont. XYZW,. Xyxy,. zwxy,. zwzw. Les mappages *src* suivants sont postérieurs à Swizzle :

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

 

 





