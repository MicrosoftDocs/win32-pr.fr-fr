---
title: XOR (SM4-ASM)
description: XOR au niveau du bit.
ms.assetid: 6B949653-6DDA-402B-8ABE-B93858B68470
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7a998bd1e95793f463d7f234b464a542bed4fc0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126918063"
---
# <a name="xor-sm4---asm"></a>XOR (SM4-ASM)

XOR au niveau du bit.



| XOR dest \[ . Mask \] , src0 \[ . Swizzle \] , src1 \[ . Swizzle\] |
|-------------------------------------------------------|



 



| Élément                                                            | Description                                          |
|-----------------------------------------------------------------|------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[dans \] le résultat de l’opération.<br/>       |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[dans \] les composants à XOR avec *src1*.<br/> |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[dans \] les composants à XOR avec *src0*.<br/> |



 

## <a name="remarks"></a>Notes

Cette instruction effectue un XOR logique au niveau du composant de chaque paire de valeurs 32 bits à partir de *src0* et *src1*. les résultats 32 bits sont placés dans *dest*.

Cette instruction s’applique aux étapes suivantes du nuanceur :



| Nuanceur de sommets | Nuanceur de géométrie | Nuanceur de pixels |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

## <a name="minimum-shader-model"></a>Modèle de nuanceur minimal

Cette fonction est prise en charge dans les modèles de nuanceur suivants.



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

 

 





