---
title: bfrev (SM5-ASM)
description: Inversez un nombre de 32 bits.
ms.assetid: 24F8209A-093E-4737-BF50-12F228024E9D
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87263a4ab2a4db54c25944905c36d81a4773e2f4eec40336b35fda03111dc3dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119983539"
---
# <a name="bfrev-sm5---asm"></a>bfrev (SM5-ASM)

Inversez un nombre de 32 bits.



| bfrev dest \[ . Mask \] , src0 \[ . Swizzle\] |
|---------------------------------------|



 



| Élément                                                            | Description                                                  |
|-----------------------------------------------------------------|--------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[dans \] l’adresse de *src0* avec bits inversé.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[dans \] le nombre 32 bits à inverser.<br/>              |



 

## <a name="remarks"></a>Remarques

Par exemple, pour 0x12345678 sinon, le résultat est 0x1e6a2c48.

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

 

 





