---
title: cas (SM4-ASM)
description: Étiquette dans une instruction switch.
ms.assetid: 456BB918-327E-4E15-8D38-F53850CAF666
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0278b8492575b1ef54fd64fc24b031fdec6cfb21
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127295663"
---
# <a name="case-sm4---asm"></a>cas (SM4-ASM)

Étiquette dans une instruction switch.



| cas \[ 32-bit immédiat\] |
|---------------------------|



 

## <a name="remarks"></a>Notes

Étant donné que la chute des **cas** n’est valide que si aucun code n’est ajouté, plusieurs **cas** (y compris la [valeur par défaut](default--sm4---asm-.md)) peuvent partager le même bloc de code.

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

 

 




