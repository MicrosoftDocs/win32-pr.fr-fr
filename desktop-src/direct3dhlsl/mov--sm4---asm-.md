---
title: MOV (SM4-ASM)
description: Déplacement au niveau du composant. | MOV (SM4-ASM)
ms.assetid: A8865237-59D3-4332-9F09-157E10C4FFC6
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 247e3838841d63c3cadf2e075fd088b534bf56ea19b8869b7cffe91e9f75e6c5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120095369"
---
# <a name="mov-sm4---asm"></a>MOV (SM4-ASM)

Déplacement au niveau du composant.



| Instruction : MOV \[ \_ SAT \] dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle\] |
|-------------------------------------------------------------------------|



 



| Élément                                                            | Description                                                                              |
|-----------------------------------------------------------------|------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[dans \] l’adresse du résultat de l’opération.<br/> *dest*  =  . *src0*<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[dans \] les composants à déplacer.<br/>                                                |



 

## <a name="remarks"></a>Remarques

Les modificateurs, autres que Swizzle, supposent que les données sont à virgule flottante. L’absence de modificateurs déplace uniquement les données sans modifier les bits.

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

 

 





