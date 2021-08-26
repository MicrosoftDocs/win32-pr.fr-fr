---
title: UDIV (SM4-ASM)
description: Division d’entier non signé.
ms.assetid: 87C81418-0F74-4C67-9D4A-DA952EFD008E
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87b1320d0518034129efe2222a42aa2694df0422db524da0714377cb43a2b9a0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119948979"
---
# <a name="udiv-sm4---asm"></a>UDIV (SM4-ASM)

Division d’entier non signé.



| UDIV destQUOT \[ . Mask \] , destREM \[ . Mask \] , src0 \[ . Swizzle \] , src1 \[ . Swizzle\] |
|------------------------------------------------------------------------------|



 



| Élément                                                                                                   | Description                                                |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <span id="destQUOT"></span><span id="destquot"></span><span id="DESTQUOT"></span>*destQUOT*<br/> | \[dans \] l’adresse du quotient résultant.<br/>   |
| <span id="destREM"></span><span id="destrem"></span><span id="DESTREM"></span>*destREM*<br/>     | \[dans \] l’adresse du reste résultant.<br/>  |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/>                                        | \[dans \] les composants à diviser par *src1*.<br/>  |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/>                                        | \[dans \] les composants par abordé pour diviser *src0*.<br/> |



 

## <a name="remarks"></a>Remarques

Cette instruction effectue une division non signée au niveau du composant de l’opérande 32 bits *src0* par l’opérande 32 bits *src1*. Les résultats des divisions sont les quotients de 32 bits placés dans *destQUOT* et les restes de 32 bits placés dans *destREM*.

La division par zéro retourne 0xFFFFFFFF pour le quotient et le reste.

Vous pouvez spécifier *destQUOT* ou *destREM* comme null au lieu de spécifier un registre, si le quotient ou le reste ne sont pas nécessaires.

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

 

 





