---
title: Saturation (référence HLSL)
description: Attache le résultat d’une opération arithmétique à virgule flottante simple ou double précision à \ 0.0 f... 1.0 f \ plage.
ms.assetid: ce3e79c7-c3e6-4a2c-910a-2cd568aece50
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 25e771bd53dbb8a4b0d2eaf8162675cd556c071344b249562defe4a06e715f5a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118790742"
---
# <a name="saturate-hlsl-reference"></a>Saturation (référence HLSL)

Attache le résultat d’une opération arithmétique à virgule flottante simple ou double précision à \[ 0.0 f... plage f 1.0 \] .



| \_sot |
|-------|



 

Le modificateur de résultat d’instruction **saturé** effectue l’opération suivante sur les valeurs de résultat à partir d’une opération arithmétique à virgule flottante qui \_ lui est appliquée :

`min(1.0f, max(0.0f, value))`

où min () et Max () dans l’expression ci-dessus se comportent de la façon dont [min](min--sm4---asm-.md), [Max](max--sm4---asm-.md), [DMin](dmin--sm5---asm-.md)ou [DMax](dmax--sm5---asm-.md) fonctionnent.

`_sat(NaN)` retourne 0, en fonction des règles min et max.

## <a name="minimum-shader-model"></a>Modèle de nuanceur minimal

Ce modificateur est pris en charge dans les modèles de nuanceur suivants.



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

[Modificateurs d’instruction](instruction-modifiers.md)
</dt> </dl>

 

 




