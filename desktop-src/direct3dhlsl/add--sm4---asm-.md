---
title: Add (SM4-ASM)
description: Ajout de 2 vecteurs au niveau du composant.
ms.assetid: 405A513C-B2DD-43B9-A86D-1D173B084C51
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79a6a0fbec409f7184c0af3b305603fcf468ef867234e8b6791bff0d1d527ad3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118795398"
---
# <a name="add-sm4---asm"></a>Add (SM4-ASM)

Ajout de 2 vecteurs au niveau du composant.



| Ajoutez \[ \_ SAT \] dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle \] , \[ - \] src1 \[ \_ ABS \] \[ . Swizzle\] |
|--------------------------------------------------------------------------------------------|



 



| Élément                                                            | Description                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[dans \] l’adresse du résultat de l’opération.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[dans \] le vecteur à ajouter à *src1*.<br/>                |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[dans \] le vecteur à ajouter à *src0*.<br/>                |



 

## <a name="remarks"></a>Remarques

Le tableau suivant présente les résultats obtenus lors de l’exécution de l’instruction avec différentes classes de nombres, en supposant qu’aucun dépassement de capacité ou négatif ne se produit. F signifie nombre réel fini.



| **src0 src1->** | **-INF** | **-F**     | **-dénorme** | **-0** | **+0** | **dénorme** | **+ F**     | **+ INF** | **NaN** |
|--------------------|----------|------------|-------------|--------|--------|------------|------------|----------|---------|
| **-INF**           | -inf     | -inf       | -inf        | -inf   | -inf   | -inf       | -inf       | NaN      | NaN     |
| **-F**             | -inf     | -F         | src0        | src0   | src0   | src0       | +-F ou +-0 | +inf     | NaN     |
| **-dénorme**        | -inf     | src1       | -0          | -0     | +0     | +0         | src1       | +inf     | NaN     |
| **-0**             | -inf     | src1       | -0          | -0     | +0     | +0         | src1       | +inf     | NaN     |
| **+0**             | i-INF    | src1       | +0          | +0     | +0     | +0         | src1       | +inf     | NaN     |
| **+ dénorme**        | -inf     | src1       | +0          | +0     | +0     | +0         | src1       | +inf     | NaN     |
| **+ F**             | -inf     | +-F ou +-0 | src0        | src0   | src0   | src0       | + F         | +inf     | NaN     |
| **+ INF**           | NaN      | +inf       | +inf        | +inf   | +inf   | +inf       | +inf       | +inf     | NaN     |
| **NaN**            | NaN      | NaN        | NaN         | NaN    | NaN    | NaN        | NaN        | NaN      | NaN     |



 

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

 

 





