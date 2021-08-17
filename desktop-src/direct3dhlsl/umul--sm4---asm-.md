---
title: umul (SM4-ASM)
description: Multiplication d’entier non signé.
ms.assetid: C84AF349-32E6-40C4-9973-BCFA73EFBF0B
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ec63b3a95ffbdf1f71142c9fc508e21e718b44d988b725dad5d73775746871c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117721833"
---
# <a name="umul-sm4---asm"></a>umul (SM4-ASM)

Multiplication d’entier non signé.



| umul destHI \[ . Mask \] , destLO \[ . Mask \] , src0 \[ . Swizzle \] , src1 \[ . Swizzle\] |
|---------------------------------------------------------------------------|



 



| Élément                                                                                           | Description                                                      |
|------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <span id="destHI"></span><span id="desthi"></span><span id="DESTHI"></span>*destHI*<br/> | \[dans \] les 32 bits de poids fort du résultat, par composant.<br/> |
| <span id="destLO"></span><span id="destlo"></span><span id="DESTLO"></span>*destLO*<br/> | \[dans \] les 32 bits de poids faible du résultat, par composant.<br/>  |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/>                                | \[dans \] les composants par lesquels multiplier *src1*.<br/>    |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/>                                | \[dans \] les composants par lesquels multiplier *src0*.<br/>    |



 

## <a name="remarks"></a>Remarques

Cette instruction effectue une multiplication au niveau du composant des opérandes 32 bits non signés *src0* et *src1*, ce qui produit le résultat 64 bits complet par composant. Les 32 bits de poids faible par composant sont placés dans *destLO*. La haute 32 bits par composant est placée dans *destHI*.

Vous pouvez spécifier *destHI* ou *destLO* comme null au lieu de spécifier un registre si les 32 bits de poids fort ou faible du résultat de 64 bits ne sont pas nécessaires.

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

 

 





