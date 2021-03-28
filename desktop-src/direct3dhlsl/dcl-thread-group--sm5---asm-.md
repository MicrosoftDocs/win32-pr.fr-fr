---
title: dcl_thread_group (SM5-ASM)
description: Déclarez la taille du groupe de threads.
ms.assetid: CB8192C4-100D-49B6-94E7-6CD3AEC28149
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8141c80e82f1dfd1ae5a4d360d04fac32ba5221
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104030608"
---
# <a name="dcl_thread_group-sm5---asm"></a>\_groupe de threads DCL \_ (SM5-ASM)

Déclarez la taille du groupe de threads.



| \_groupe de threads DCL \_ x, y, z |
|----------------------------|



 



| Élément                                                   | Description                                                        |
|--------------------------------------------------------|--------------------------------------------------------------------|
| <span id="x"></span><span id="X"></span>*x*<br/> | \[dans \] un entier usigned 32 bits. 1 <= x <= 1024 <br/> |
| <span id="y"></span><span id="Y"></span>*y*<br/> | \[dans \] un entier usigned 32 bits. 1 <= y <= 1024<br/>  |
| <span id="z"></span><span id="Z"></span>*Lettre*<br/> | \[dans \] un entier usigned 32 bits. 1 <= z <= 64<br/>    |



 

## <a name="remarks"></a>Notes

x \* y \* z <= 1024

Cette déclaration de groupe de threads doit apparaître une fois dans un nuanceur de calcul.

Cette instruction s’applique aux étapes suivantes du nuanceur :



| Sommet | Forme | Domain | Géométrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          |       | X       |



 

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

 

 





