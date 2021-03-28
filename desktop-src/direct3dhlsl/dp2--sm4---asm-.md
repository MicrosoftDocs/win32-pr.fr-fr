---
title: DP2 (SM4-ASM)
description: vecteur à deux dimensions-produit des composants RG, POS-Swizzle.
ms.assetid: E35F6A8B-6D8E-4660-B0F3-95B76BC19229
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4073def6cb315dc0268d1ce8e3f28039b9b2a69
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104381146"
---
# <a name="dp2-sm4---asm"></a>DP2 (SM4-ASM)

vecteur à deux dimensions-produit des composants RG, POS-Swizzle.



| DP2 \[ \_ SAT \] dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle \] , \[ - \] src1 \[ \_ ABS \] \[ . Swizzle\] |
|--------------------------------------------------------------------------------------------|



 



| Élément                                                            | Description                                                                                                                    |
|-----------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[dans \] l’adresse du résultat de l’opération. <br/> *dest*  =  . *src0. r* \* *src1. r*  +  *src0. g* \* *src1. g*<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[dans \] les composants de l’opération.<br/>                                                                             |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[dans \] les composants de l’opération.<br/>                                                                             |



 

## <a name="remarks"></a>Notes

Résultat scalaire répliqué sur les composants dans le masque d’écriture.

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

 

 





