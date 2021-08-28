---
title: ISHR (SM4-ASM)
description: Décalage arithmétique vers la droite (extension de signe). | ISHR (SM4-ASM)
ms.assetid: AFE46BBA-A6B2-4691-A3F4-A4141F1578DB
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d2ec191320561b05ba736b7da5630fb50a610e739d0e74f9def3eaa10bb4e17
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118511134"
---
# <a name="ishr-sm4---asm"></a>ISHR (SM4-ASM)

Décalage arithmétique vers la droite (extension de signe).



| ISHR dest \[ . Mask \] , src0 \[ . Swizzle \] , src1. Select, \_ composant |
|--------------------------------------------------------------|



 



| Élément                                                            | Description                                             |
|-----------------------------------------------------------------|---------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[dans \] contient le résultat de l’opération.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[dans \] contient la valeur à décaler.<br/>     |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[dans \] contient le nombre de décalages.<br/>            |



 

## <a name="remarks"></a>Remarques

Cette instruction effectue un décalage arithmétique au niveau du composant de chaque valeur 32 bits dans *src0* avec un nombre de bits entier non signé fourni par LSB 5 bits (plage 0-31) dans *src1. Sélectionnez le \_ composant*, en répliquant la valeur de bit 31. Le résultat 32 bits par composant est placé dans *dest*. Le nombre est une valeur scalaire appliquée à tous les composants.

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

 

 





