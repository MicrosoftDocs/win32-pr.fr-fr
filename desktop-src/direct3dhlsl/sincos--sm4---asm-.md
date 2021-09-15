---
title: SinCos, (SM4-ASM)
description: Sin (thêta) et cos (thêta) du composant pour Theta en radians.
ms.assetid: 81FDEC8F-2C1C-4C60-A6DA-699C798F8316
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c03118ff9a1fc2d958eaa6eb1a550a6dbf672a2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127411231"
---
# <a name="sincos-sm4---asm"></a>SinCos, (SM4-ASM)

Sin (thêta) et cos (thêta) du composant pour Theta en radians.



| SinCos, \[ \_ SAT \] destSIN \[ . Mask \] , destCOS \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle\] |
|------------------------------------------------------------------------------------|



 



| Élément                                                                                               | Description                                                           |
|----------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <span id="destSIN"></span><span id="destsin"></span><span id="DESTSIN"></span>*destSIN*<br/> | \[dans \] l’adresse de Sin (*src0*), calculée par composant.<br/> |
| <span id="destCOS"></span><span id="destcos"></span><span id="DESTCOS"></span>*destCOS*<br/> | \[dans \] l’adresse cos (*src0*), calculée par composant.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/>                                    | \[dans \] les composants pour lesquels calculer des Sin et des COS.<br/>    |



 

## <a name="remarks"></a>Remarques

Si le résultat n’est pas nécessaire, vous pouvez spécifier *destSIN* et *destCOS* comme null au lieu de spécifier un registre.

Les valeurs Thêta peuvent être n’importe quelle valeur à virgule flottante IEEE 32 bits.

L’erreur absolue maximale est 0,0008 dans l’intervalle compris entre-100 \* pi et + 100 \* pi.

Le tableau suivant présente les résultats obtenus lors de l’exécution de l’instruction avec différentes classes de nombres.

F signifie nombre fini-réel.



| **src**     | **-INF** | **-F**       | **-dénorme** | **-0** | **+0** | **+ dénorme** | **+ F**       | **+ INF** | **NaN** |
|-------------|----------|--------------|-------------|--------|--------|-------------|--------------|----------|---------|
| **destSIN** | NaN      | \[-1 à + 1\] | -0          | -0     | +0     | +0          | \[-1 à + 1\] | NaN      | NaN     |
| **destCOS** | NaN      | \[-1 à + 1\] | +1          | +1     | +1     | +1          | \[-1 à + 1\] | NaN      | NaN     |



 

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

 

 





