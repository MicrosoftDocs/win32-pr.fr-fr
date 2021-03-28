---
title: BFI (SM5-ASM)
description: En fonction d’une plage de bits du LSB d’un nombre, placez ce nombre de bits dans un autre nombre à tout décalage.
ms.assetid: BA84C882-A141-4AD2-8FD9-C60F1483FC65
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a14f8b9f6ef126ec3c6a31bf330dfd89cf0770c4
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104030594"
---
# <a name="bfi-sm5---asm"></a>BFI (SM5-ASM)

En fonction d’une plage de bits du LSB d’un nombre, placez ce nombre de bits dans un autre nombre à tout décalage.



| BFI dest \[ . Mask \] , src0 \[ . Swizzle \] , src1 \[ . Swizzle \] , src2 \[ . Swizzle \] , src3 \[ . Swizzle\] |
|-------------------------------------------------------------------------------------------|



 



| Élément                                                            | Description                                                         |
|-----------------------------------------------------------------|---------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[dans \] l’adresse des résultats.<br/>                       |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[dans \] la largeur de champ de champ à prendre de *src2*.<br/>           |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[dans \] l’offset de champ de bits pour le remplacement de bits dans *src3*.<br/> |
| <span id="src2"></span><span id="SRC2"></span>*src2*<br/> | \[dans \] le numéro à partir duquel les bits sont extraits. <br/>              |
| <span id="src3"></span><span id="SRC3"></span>*src3*<br/> | \[dans \] le nombre avec bits à remplacer.<br/>              |



 

## <a name="remarks"></a>Notes

Les LSB 5 bits de *src0* fournissent la largeur de champ de bits (0-31) à prendre de *src2*.

Les LSB 5 bits de *src1* fournissent l’offset de champ de bits (0-31) pour commencer à remplacer des bits dans le nombre lu à partir de *src3*.

``` syntax
Given width, offset:
                bitmask = (((1 << width)-1) << offset) & 0xffffffff
                dest = ((src2 << offset) & bitmask) | (src3 & ~bitmask)
```

Cette instruction est utilisée pour compresser des entiers ou des indicateurs.

Cette instruction s’applique aux étapes suivantes du nuanceur :



| Sommet | Forme | Domain | Géométrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

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

 

 





