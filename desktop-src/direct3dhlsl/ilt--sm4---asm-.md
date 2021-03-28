---
title: ILT (SM4-ASM)
description: Comparaison des entiers vectoriels au niveau du composant inférieur à.
ms.assetid: 5F06E568-6234-4778-8169-D8352FAB5297
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e2c2e5e47272412bb483e4782e9a6c35e971293c
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104313633"
---
# <a name="ilt-sm4---asm"></a>ILT (SM4-ASM)

Comparaison des entiers vectoriels au niveau du composant inférieur à.



| ILT dest \[ . Mask \] , src0 \[ . Swizzle \] , src1 \[ . Swizzle\] |
|-------------------------------------------------------|



 



| Élément                                                            | Description                                       |
|-----------------------------------------------------------------|---------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | Résultat de l'opération.<br/>           |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[dans \] la valeur à comparer à *src1*.<br/> |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[dans \] la valeur à comparer à *src0*.<br/> |



 

## <a name="remarks"></a>Notes

Effectue une comparaison d’entiers *(src0*  <  *src1*) pour chaque composant et écrit le résultat dans *dest*.

Si la comparaison est true, 0xFFFFFFFF est retourné pour ce composant. Sinon, 0x0000000 est retourné.

Cette instruction s’applique aux étapes suivantes du nuanceur :



| Nuanceur de sommets | Nuanceur de géométrie | Nuanceur de pixels |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

## <a name="minimum-shader-model"></a>Modèle de nuanceur minimal



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

 

 





