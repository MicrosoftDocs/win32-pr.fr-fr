---
title: ILT (SM4-ASM)
description: Comparaison des entiers vectoriels au niveau du composant inférieur à.
ms.assetid: 5F06E568-6234-4778-8169-D8352FAB5297
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b8d70e2c71ad0e503e7119abc2b28e76819053d843b0091d15bfd2045d5351d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119119453"
---
# <a name="ilt-sm4---asm"></a>ILT (SM4-ASM)

Comparaison des entiers vectoriels au niveau du composant inférieur à.



| ILT dest \[ . Mask \] , src0 \[ . Swizzle \] , src1 \[ . Swizzle\] |
|-------------------------------------------------------|



 



| Élément                                                            | Description                                       |
|-----------------------------------------------------------------|---------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | Résultat de l'opération.<br/>           |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[dans \] la valeur à comparer à *src1*.<br/> |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[dans \] la valeur à comparer à *src0*.<br/> |



 

## <a name="remarks"></a>Remarques

Effectue une comparaison d’entiers *(src0*  <  *src1*) pour chaque composant et écrit le résultat dans *dest*.

Si la comparaison est true, 0xFFFFFFFF est retourné pour ce composant. Sinon, 0x0000000 est retourné.

Cette instruction s’applique aux étapes suivantes du nuanceur :



| Nuanceur de sommets | Nuanceur de géométrie | Nuanceur de pixels |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

## <a name="minimum-shader-model"></a>Modèle de nuanceur minimal



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

 

 





