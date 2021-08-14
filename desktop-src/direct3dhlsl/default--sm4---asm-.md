---
title: par défaut (SM4-ASM)
description: Étiquette facultative dans une instruction switch.
ms.assetid: DB10F654-4A98-4ED8-A3B4-CA9FE1DFE6CD
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d54c3bbe83bd2499bdc2d50a30153bbc8b66e6ee53c29125b6a66416e419aa1a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118792675"
---
# <a name="default-sm4---asm"></a>par défaut (SM4-ASM)

Étiquette facultative dans une instruction [switch](switch--sm4---asm-.md) .



| default |
|---------|



 

## <a name="remarks"></a>Remarques

Cette instruction fonctionne comme **par défaut** dans C. la chute est valide uniquement si aucun code n’est ajouté. par conséquent, plusieurs cas (y compris la **valeur par défaut**) peuvent partager le même bloc de code.

Une seule instruction **par défaut** est autorisée dans une construction de **commutateur** .

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

 

 




