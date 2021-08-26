---
title: dmul (SM5-ASM)
description: Multiplication à double précision au niveau du composant.
ms.assetid: 53AE27BE-2F4B-4C55-B496-D7122C00DC52
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 838b9e2b3ed24dd5a6025c230439ce0719922d88bac723b3aed759c5fa224d8d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120068379"
---
# <a name="dmul-sm5---asm"></a>dmul (SM5-ASM)

Multiplication à double précision au niveau du composant.



| dmul \[ \_ SAT \] dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle \] , \[ - \] src1 \[ \_ ABS \] \[ . Swizzle\] |
|---------------------------------------------------------------------------------------------|



 



| Élément                                                            | Description                                                                                        |
|-----------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[dans \] l’adresse du résultat de l’opération.<br/> *dest*  =  . *src0* \* *src1*<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[dans \] les composants à multiplier avec *src1*.<br/>                                          |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[dans \] les composants à multiplier avec *src0*.<br/>                                          |



 

## <a name="remarks"></a>Remarques

Les Swizzles valides pour les paramètres sources sont. XYZW,. Xyxy,. zwxy,. zwzw. Les masques de *dest* valides sont. XY,. ZW et. XYZW. Les mappages *src* suivants sont postérieurs à Swizzle :

-   *dest* est un double vec2 entre (x 32LSB, y 32MSB) et (z 32LSB, w 32MSB).
-   *src0* est un double vec2 entre (x 32LSB, y 32MSB) et (z 32LSB, w 32MSB).
-   *src1* est un double vec2 entre (x 32LSB, y 32MSB) et (z 32LSB, w 32MSB).

Le tableau suivant présente les résultats obtenus lors de l’exécution de l’instruction avec différentes classes de nombres, en supposant qu’aucun dépassement de capacité ou négatif ne se produit.

F signifie nombre fini-réel.



| **src0 src1->** | **-INF** | **-F** | **-1,0** | **-0** | **+0** | **+ 1,0** | **+ F** | **+ INF** | **NaN** |
|--------------------|----------|--------|----------|--------|--------|----------|--------|----------|---------|
| **-INF**           | +inf     | +inf   | +inf     | NaN    | NaN    | -inf     | -inf   | -inf     | NaN     |
| **-F**             | +inf     | + F     | -src0    | +0     | -0     | src0     | -F     | -inf     | NaN     |
| **-1.0 f**          | +inf     | -src1  | + 1,0     | +0     | -0     | -1.0     | -src1  | -inf     | NaN     |
| **-0**             | NaN      | +0     | +0       | +0     | -0     | -0       | -0     | NaN      | NaN     |
| **+0**             | NaN      | -0     | -0       | -0     | +0     | +0       | +0     | NaN      | NaN     |
| **+ 1,0**           | -inf     | src1   | -1.0     | -0     | +0     | +1       | src1   | +inf     | NaN     |
| **+ F**             | -inf     | -F     | -src0    | -0     | +0     | src0     | + F     | +inf     | NaN     |
| **+ INF**           | -inf     | -inf   | -inf     | NaN    | NaN    | +inf     | +inf   | +inf     | NaN     |
| **NaN**            | NaN      | NaN    | NaN      | NaN    | NaN    | NaN      | NaN    | NaN      | NaN     |



 

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

 

 





