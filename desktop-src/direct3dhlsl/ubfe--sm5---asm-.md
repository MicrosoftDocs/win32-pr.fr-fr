---
title: ubfe (SM5-ASM)
description: À partir d’une plage de bits dans un nombre, décalez ces bits vers le LSB et définissez les bits restants sur 0.
ms.assetid: CC6BE378-2726-47A2-8E23-B8151521F72D
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43ebbe853ec1b53b452f32d79c9c2ec120e826b8
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "103841657"
---
# <a name="ubfe-sm5---asm"></a>ubfe (SM5-ASM)

À partir d’une plage de bits dans un nombre, décalez ces bits vers le LSB et définissez les bits restants sur 0.



| ubfe dest \[ . Mask \] , src0 \[ . Swizzle \] , src1 \[ . Swizzle \] , src2 \[ . Swizzle\] |
|--------------------------------------------------------------------------|



 



| Élément                                                            | Description                                                                    |
|-----------------------------------------------------------------|--------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[dans \] contient les résultats de l’instruction.<br/>                     |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[dans, \] LSB 5 bits fournissent la largeur de champ de bits (0-31).<br/>            |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[dans, \] LSB 5 bits de *src1* fournissent l’offset de champ de bits (0-31).<br/> |
| <span id="src2"></span><span id="SRC2"></span>*src2*<br/> | \[dans \] le nombre à décaler.<br/>                                         |



 

## <a name="remarks"></a>Notes

``` syntax
 
        Given width, offset:
                if( width == 0 )
                {
                    dest = 0
                }
                else if( width + offset < 32 )
                {
                    shl dest, src2, 32-(width+offset)
                    ushr dest, dest, 32-width
                }
                else
                {
                    ushr dest, src2, offset
                }
```

Utilisez cette instruction pour décompresser des entiers ou des indicateurs non signés.

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

 

 





