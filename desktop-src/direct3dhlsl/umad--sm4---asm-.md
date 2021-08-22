---
title: UMAD (SM4-ASM)
description: Entier non signé multiplier et ajouter.
ms.assetid: C0BE31CA-E01D-42C0-A660-E63727CE344F
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b6a6c649a61c78eebee249b9fec5c032a07a8a0761a3d23d6e45da573be122c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119405989"
---
# <a name="umad-sm4---asm"></a>UMAD (SM4-ASM)

Entier non signé multiplier et ajouter.



| UMAD dest \[ . Mask \] , src0 \[ . Swizzle \] , src1 \[ . Swizzle \] , src2 \[ . Swizzle\] |
|--------------------------------------------------------------------------|



 



| Élément                                                            | Description                                                             |
|-----------------------------------------------------------------|-------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[dans \] l’adresse du résultat de l’opération.<br/>           |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[dans \] la valeur à multiplier avec *src1*.<br/>                    |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[dans \] la valeur à multiplier avec *src1*.<br/>                     |
| <span id="src2"></span><span id="SRC2"></span>*src2*<br/> | \[\]valeur à ajouter au produit de *src0* et *src1*.<br/> |



 

## <a name="remarks"></a>Remarques

[Umul](umul--sm4---asm-.md) des opérandes 32 bits *src0* et *src1* non signés, en conservant les 32 bits de poids faible, par composant, du résultat. Cette instruction effectue ensuite un [IAdd](iadd--sm4---asm-.md) de *src2*, en produisant le résultat à faible bit de 32 bits (par composant). Les résultats 32 bits sont placés dans *dest*.

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

 

 





