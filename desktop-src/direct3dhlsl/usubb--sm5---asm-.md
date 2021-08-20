---
title: usubb (SM5-ASM)
description: Entier non signé soustrait avec emprunt.
ms.assetid: 6D42E3CA-5A37-4194-AB42-7A2337C5AB9D
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7c2f70f39729f5245f7044945e9d3b233ec4f0893be27c5143f5c55989693b9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117721823"
---
# <a name="usubb-sm5---asm"></a>usubb (SM5-ASM)

Entier non signé soustrait avec emprunt.



| usubb dest0 \[ . Mask \] , dest1 \[ . Mask \] , src0 \[ . Swizzle \] , src1 \[ . Swizzle\] |
|--------------------------------------------------------------------------|



 



| Élément                                                               | Description                                                                                       |
|--------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span id="dest0"></span><span id="DEST0"></span>*dest0*<br/> | \[dans \] contient les résultats LSAB de l’instruction.<br/>                                   |
| <span id="dest1"></span><span id="DEST1"></span>*dest1*<br/> | \[dans \] le composant correspondant de *dest0* qui spécifie si un emprunt a été produit.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/>    | \[dans \] la valeur à partir de laquelle soustraire.<br/>                                               |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/>    | \[dans \] le montant à soustraire de *src0*.<br/>                                             |



 

## <a name="remarks"></a>Remarques

Cette instruction effectue une soustraction non signée au niveau du composant des opérandes 32 bits *src1* à partir de *src0*, en plaçant la partie LSB du résultat 32 bits dans *dest0*.

Le composant correspondant dans *dest1* est écrit avec 1 si un emprunt est produit, 0 dans le cas contraire.

*dest1* peut avoir la valeur null si le emprunt n’est pas nécessaire.

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

 

 





