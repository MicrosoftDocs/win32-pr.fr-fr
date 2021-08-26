---
title: DP2 (SM4-ASM)
description: vecteur à deux dimensions-produit des composants RG, POS-Swizzle.
ms.assetid: E35F6A8B-6D8E-4660-B0F3-95B76BC19229
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 65e50c791fc5c994cf6e8da56cabf64a257244519b8ee0d0d50137926bffef91
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120024639"
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



 

## <a name="remarks"></a>Remarques

Résultat scalaire répliqué sur les composants dans le masque d’écriture.

Cette instruction s’applique aux étapes suivantes du nuanceur :



| Nuanceur de sommets | Nuanceur de géométrie | Nuanceur de pixels |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

## <a name="minimum-shader-model"></a>Modèle de nuanceur minimal

Cette fonction est prise en charge dans les modèles de nuanceur suivants.



| Modèle de nuanceur                                              | Pris en charge |
|-----------------------------------------------------------|-----------|
| [Shader, modèle 5](d3d11-graphics-reference-sm5.md)        | oui       |
| [Modèle de nuanceur 4,1](dx-graphics-hlsl-sm4.md)              | oui       |
| [Nuanceur modèle 4](dx-graphics-hlsl-sm4.md)                | oui       |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | non        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | non        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | non        |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Assembly modèle 4 du nuanceur (DirectX HLSL)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





