---
title: Valeur absolue
description: Prend la valeur absolue d’un opérande source utilisé dans une opération arithmétique.
ms.assetid: FD2ACE91-0AF6-43E8-80C5-849488E39BEF
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 27ceefa2c4b4ee2eb890b0692a33266e89a18cfb
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104313741"
---
# <a name="absolute-value"></a>Valeur absolue

Prend la valeur absolue d’un opérande source utilisé dans une opération arithmétique.



| \_absolue |
|-------|



 

Ce modificateur est utilisé pour les instructions à virgule flottante simple et double précision uniquement. Le modificateur **\_ ABS** force le signe du ou des nombres sur l’opérande source positif, y compris sur les valeurs INF.

L’application d' **\_ ABS** sur Nan préserve Nan, bien que le modèle binaire Nan particulier qui résulte n’est pas défini.

Quand \_ ABS est combiné avec le modificateur de [négation](negate.md) , la combinaison force le signe à être négatif, comme si le modificateur **\_ ABS** était appliqué en premier, puis la **négation**.

## <a name="minimum-shader-model"></a>Modèle de nuanceur minimal

Ce modificateur est pris en charge dans les modèles de nuanceur suivants.



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

[Modificateurs d’instruction](instruction-modifiers.md)
</dt> </dl>

 

 




