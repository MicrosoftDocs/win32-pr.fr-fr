---
title: dcl_tessellator_partitioning (SM5-ASM)
description: Déclarez le partitionnement du paveur dans une section de déclaration de nuanceur de coque.
ms.assetid: 6EA00C6B-A0DE-4CE4-8B52-1337CA92CA5E
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae40873db4042e568ae637634e75db6f4746985a316bf9c1e092e6b0925b51b2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120068499"
---
# <a name="dcl_tessellator_partitioning-sm5---asm"></a>\_ \_ partitionnement de du paveur DCL (SM5-ASM)

Déclarez le partitionnement du paveur dans une section de déclaration de nuanceur de coque.



| \_partitionnement de du paveur DCL \_ {entier de partitionnement \_ \| partitionnement \_ pow2 \|partitionnement de \_ fractions \_ impair \| partitionnement \_ fractionnaire \_ pair} |
|---------------------------------------------------------------------------------------------------------------------------------------------|



 



| Élément                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            | Description                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------|
| <span id="partitioning_integer__________________________________partitioning_pow2_partitioning_fractional_odd__________________________________partitioning_fractional_even"></span><span id="PARTITIONING_INTEGER__________________________________PARTITIONING_POW2_PARTITIONING_FRACTIONAL_ODD__________________________________PARTITIONING_FRACTIONAL_EVEN"></span>*partitionnement des nombres entiers partitionnement pow2 partitionnement du partitionnement impair fractionnement \_ \| \_ \| \_ \_ \| \_ fractionnaire \_ même*<br/> | \[dans \] le partitionnement du paveur.<br/> |



 

## <a name="remarks"></a>Remarques

Du point de vue matériel, \_ pow2 se comporte comme un \_ entier. C’est à l’auteur du nuanceur HLSL et/ou compilercode d’arrondir les TessFactors aux puissances de 2.

Cette instruction s’applique aux étapes suivantes du nuanceur :



| Sommet | Forme                 | Domaine | Géométrie | Pixel | Calcul |
|--------|----------------------|--------|----------|-------|---------|
|        | Section déclarations |        |          |       |         |



 

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

 

 





