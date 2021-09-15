---
title: Arê (SM5-ASM)
description: Comparaison de type supérieur ou égal à double précision au niveau du composant.
ms.assetid: 2E769077-E861-4EFA-817F-7D1AE998746C
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 508354affbabe1ebab70be31ab45f0e7f80d0765
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127524705"
---
# <a name="dge-sm5---asm"></a>Arê (SM5-ASM)

Comparaison de type supérieur ou égal à double précision au niveau du composant.



| Arê \[ \_ SAT \] dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle \] , \[ - \] src1 \[ \_ ABS \] \[ . Swizzle\] |
|--------------------------------------------------------------------------------------------|



 



| Élément                                                            | Description                                                    |
|-----------------------------------------------------------------|----------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[dans \] l’adresse des résultats de l’opération.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | Composants à comparer à *src1*.<br/>                |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | Composants à comparer à *src0*.<br/>                |



 

## <a name="remarks"></a>Notes

Cette instruction effectue la comparaison à virgule flottante double précision (*src0*  >=  *src1*) pour chaque composant et écrit le résultat dans *dest*.

Si la comparaison est true, 32-bit 0xFFFFFFFF est retourné pour ce composant. Sinon 32-bit 0x00000000 est retourné.

La comparaison avec NaN retourne false.

Les masques de *dest* valides sont un ou deux composants. C’est-à-dire :. x,. y,. z,. w,. XY,. XZ,. xw,. YZ,. YW,. ZW le premier composant *dest* dans le masque reçoit le résultat 32 bits pour la première comparaison double. Le deuxième composant dans le masque, s’il est présent, reçoit le résultat 32 bits pour la deuxième comparaison double.

Les Swizzles valides pour les paramètres sources sont. XYZW,. Xyxy,. zwxy,. zwzw. Les mappages *src* suivants sont postérieurs à Swizzle :

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

 

 





