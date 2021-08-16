---
title: Cut (SM4-ASM)
description: Instruction de nuanceur Geometry qui termine la topologie primitive actuelle (si des vertex ont été émis) et démarre une nouvelle topologie du type déclaré par le nuanceur Geometry.
ms.assetid: 9B28E33D-F518-4844-BE3F-BE61B5F08B4F
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34357c05cdd9506ec480d5021db5b330971de9fce7fd70ce9909658be9bb8c4d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117908823"
---
# <a name="cut-sm4---asm"></a>Cut (SM4-ASM)

Instruction de nuanceur Geometry qui termine la topologie primitive actuelle (si des vertex ont été émis) et démarre une nouvelle topologie du type déclaré par le nuanceur Geometry.



| cut |
|-----|



 

## <a name="remarks"></a>Remarques

Lors de l’exécution de **Cut** , la première chose qui se produit est que toute topologie précédemment émise par l’appel de nuanceur Geometry est terminée. Si le nombre de vertex non suffisant a été émis pour la topologie primitive précédente, ceux-ci sont ignorés. Étant donné que les seules topologies de sortie disponibles pour le nuanceur Geometry sont PointList, linestrip et TriangleStrip, il n’y a jamais de sommets restants lors de la **coupe**.

Une fois la topologie précédente terminée, le cas échéant, **Cut** provoque le début d’une nouvelle topologie, à l’aide de la topologie déclarée comme sortie du nuanceur Geometry.

## <a name="restrictions"></a>Restrictions

-   L’instruction **Cut** s’applique uniquement au nuanceur Geometry.
-   **Cut** peut apparaître un nombre quelconque de fois dans le nuanceur Geometry, y compris dans le contrôle de Flow.
-   Si le nuanceur Geometry se termine et que les vertex ont été émis, la topologie qu’ils génèrent est terminée, comme si une **coupe** avait été exécutée en tant que dernière instruction.
-   Si des flux ont été déclarés, le [ \_ flux](cut-stream---sm5---asm-.md) doit être utilisé à la place de **Cut**.

Cette instruction s’applique aux étapes suivantes du nuanceur :



| Nuanceur de sommets | Nuanceur de géométrie | Nuanceur de pixels |
|---------------|-----------------|--------------|
|               | x               |              |



 

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

 

 




