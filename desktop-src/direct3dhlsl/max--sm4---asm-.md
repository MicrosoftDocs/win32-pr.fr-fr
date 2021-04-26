---
title: Max (SM4-ASM)
description: Nombre maximal de virgule flottante au niveau du composant.
ms.assetid: 005468AA-577E-441F-ACD5-37A691E62CDD
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f64d88c581828f2563f6d5d8a6c57de6400f9bbf
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994726"
---
# <a name="max-sm4---asm"></a>Max (SM4-ASM)

Nombre maximal de virgule flottante au niveau du composant.



| Max \[ \_ SAT \] dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle \] , \[ - \] src1 \[ \_ ABS \] \[ . Swizzle \] , |
|---------------------------------------------------------------------------------------------|



 



| Élément                                                            | Description                                                                                               |
|-----------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[dans \] le résultat de l’opération. <br/> *dest*  =  . *src0*  >=  *src1* ? *src0* : *src1*<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[dans \] les composants à comparer à *src1*.<br/>                                                    |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[dans \] les composants à comparer à *src0*.<br/>                                                    |



 

## <a name="remarks"></a>Remarques

>= est utilisé à la place de > afin que si min (x, y) = x, alors Max (x, y) = y.

NaN a une gestion spéciale. Si un opérande source est NaN, l’autre opérande source est retourné et le choix est effectué par composant. Si les deux sont NaN, toute représentation NaN est retournée.

Les dénormes sont vidées avec le signe préservé avant la comparaison. Toutefois, le résultat écrit dans *dest* peut ou non être vidé.

Le tableau suivant présente les résultats obtenus lors de l’exécution de l’instruction avec différentes classes de nombres, en supposant qu’aucun dépassement de capacité ou négatif ne se produit. F signifie nombre réel fini.



| **src0 src1->** | **-INF** | **F**        | **+ INF** | **NaN** |
|--------------------|----------|--------------|----------|---------|
| **-INF**           | -inf     | src1         | +inf     | -inf    |
| **F**              | src0     | src0 ou src1 | +inf     | src0    |
| **+ INF**           | +inf     | +inf         | +inf     | +inf    |
| **NaN**            | -inf     | src1         | +inf     | NaN     |



 

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

 

 





