---
title: else (SM4-ASM)
description: Démarre un bloc Else.
ms.assetid: CFF25E78-D986-4EC5-B542-B3396EFF88E1
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36f676a1a14f23923e8cebe44a0539a8ba5f382c010fc87a292e77afe1470c57
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118512159"
---
# <a name="else-sm4---asm"></a>else (SM4-ASM)

Démarre un bloc **else** .



| else |
|------|



 

## <a name="remarks"></a>Remarques

Le format de jeton contient le décalage de l’instruction [endif](endif--sm4---asm-.md) correspondante dans le nuanceur pour des raisons pratiques.

L’exemple suivant montre comment utiliser l’instruction **else** .

``` syntax
                if     // any of the various forms of if* statements
                   ...
                else   // (optional)
                   ...
                endif
```

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

 

 




