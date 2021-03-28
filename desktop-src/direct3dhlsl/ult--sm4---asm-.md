---
title: ULT (SM4-ASM)
description: Comparaison des entiers non signés Vector au niveau du composant, inférieur à.
ms.assetid: DB10F654-4A98-4ED8-A3B4-CA9FE1DFE6CD
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 624c09d182e9ecfd4d1b603f6fd2c34b83d768ed
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104990740"
---
# <a name="ult-sm4---asm"></a>ULT (SM4-ASM)

Comparaison des entiers non signés Vector au niveau du composant, inférieur à.



| ULT dest \[ . Mask \] , src0 \[ . Swizzle \] , src1 \[ . Swizzle\] |
|-------------------------------------------------------|



 



| Élément                                                            | Description                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[dans \] l’adresse du résultat de l’opération.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[dans \] la valeur à comparer à *src1*.<br/>             |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[dans \] la valeur à comparer à *src1*.<br/>             |



 

## <a name="remarks"></a>Notes

Effectue une comparaison d’entiers non signés (*src0*  <  *src1*) pour chaque composant et écrit le résultat dans *dest*.

Si la comparaison est true, cette instruction retourne 0xFFFFFFFF pour ce composant. Sinon, elle retourne 0x0000000.

Cette instruction s’applique aux étapes suivantes du nuanceur :



| Nuanceur de sommets | Nuanceur de géométrie | Nuanceur de pixels |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

## <a name="minimum-shader-model"></a>Modèle de nuanceur minimal

Cette fonction est prise en charge dans les modèles de nuanceur suivants.



| Modèle de nuanceur                                              | Prise en charge |
|-----------------------------------------------------------|-----------|
| [Shader, modèle 5](d3d11-graphics-reference-sm5.md)        | Oui       |
| [Modèle de nuanceur 4,1](dx-graphics-hlsl-sm4.md)              | Oui       |
| [Nuanceur modèle 4](dx-graphics-hlsl-sm4.md)                | Oui       |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | non        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | non        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | non        |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Assembly modèle 4 du nuanceur (DirectX HLSL)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





