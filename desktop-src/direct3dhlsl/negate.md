---
title: Negate
description: Retourne le signe de la valeur d’un opérande source utilisé dans une opération arithmétique.
ms.assetid: 83ef3f61-7b0b-4033-8f7b-5345b205c441
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: cc2637a76b52b28eefcfb3637cc8b2d406c02c06
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104030568"
---
# <a name="negate"></a>Negate

Retourne le signe de la valeur d’un opérande source utilisé dans une opération arithmétique.



| \-  |
|-----|



 

Pour les instructions et les points à virgule flottante simple et double précision, le modificateur de négation retourne le signe du ou des nombres dans l’opérande source, y compris sur les valeurs INF. L’application de l' **inverse** sur Nan préserve Nan, bien que le modèle binaire Nan particulier qui résulte n’est pas défini.

Pour les instructions entières, le modificateur de **négation** prend le complément à 2 du ou des nombres dans l’opérande source.

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

 

 




