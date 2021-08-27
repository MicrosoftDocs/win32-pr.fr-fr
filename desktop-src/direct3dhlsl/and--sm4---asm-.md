---
title: et (SM4-ASM)
description: Opérateur AND au niveau du bit.
ms.assetid: 403DA289-E2CF-4736-8882-4131F884F777
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2b23d473522c2a796201a0edfc3a4b0ec9f047f9e00f359f3879fd80cfc699e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120068549"
---
# <a name="and-sm4---asm"></a>et (SM4-ASM)

And **au niveau du** bit.



| et dest \[ . Mask \] , src0 \[ . Swizzle \] , src1 \[ . Swizzle\] |
|-------------------------------------------------------|



 



| Élément                                                            | Description                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[dans \] l’adresse du résultat de l’opération.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[dans \] la valeur 32 bits vers **et** avec *src1*.<br/>    |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[dans \] la valeur 32 bits vers **et** avec *src0*.<br/>    |



 

## <a name="remarks"></a>Remarques

**And** logique au niveau du composant de chaque paire de valeurs 32 bits à partir de *src0* et *src1*. Les résultats 32 bits sont placés dans *dest*.

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

 

 





