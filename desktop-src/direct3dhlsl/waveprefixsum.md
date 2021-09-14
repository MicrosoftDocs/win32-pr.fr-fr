---
title: Fonction WavePrefixSum
description: Retourne la somme de toutes les valeurs des couloirs actifs avec des index plus petits que celui-ci.
ms.assetid: F51B90AB-3E85-4521-8A2C-7C16A4ECB1F9
keywords:
- WavePrefixSum fonction HLSL
topic_type:
- apiref
api_name:
- WavePrefixSum
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b133aa37b522156df73914eef66c4d3695a70ed7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126854769"
---
# <a name="waveprefixsum-function"></a>Fonction WavePrefixSum

Retourne la somme de toutes les valeurs des couloirs actifs avec des index plus petits que celui-ci.

## <a name="syntax"></a>Syntaxe

``` syntax
<type> WavePrefixSum(
   <type> value
);
```

## <a name="parameters"></a>Paramètres

*value* 

Valeur à additionner.

## <a name="return-value"></a>Valeur de retour

Somme des valeurs.

## <a name="remarks"></a>Notes

L’ordre des opérations sur cette routine ne peut pas être garanti. Ainsi, en fait, \[ l' \] indicateur précis est ignoré dans celui-ci.

Une somme suffixée peut être calculée en ajoutant la somme du préfixe à la valeur de la voie actuelle.

Notez que la voie active avec l’index le plus bas reçoit toujours 0 pour sa somme de préfixe.

Cette fonction est prise en charge à partir du Shader Model 6,0 dans toutes les étapes du nuanceur. 

## <a name="examples"></a>Exemples

```hlsl
uint numToSum = 2;
uint prefixSum = WavePrefixSum( numToSum );
```

Sur un ordinateur doté d’une taille d’onde de 8, et de tous les couloirs actifs, à l’exception des couloirs 0 et 4, les valeurs suivantes sont retournées à partir de WavePrefixSum.

| index Lane | status   | prefixSum     | 
|------------|----------|---------------|
| 0          | inactive | n/a           |
| 1          | active   | = 0           |
| 2          | active   | = 0 + 2         |
| 3          | active   | = 0 + 2 + 2       |
| 4          | inactive | n/a           |
| 5          | active   | = 0 + 2 + 2 + 2     |
| 6          | active   | = 0 + 2 + 2 + 2 + 2   |
| 7          | active   | = 0 + 2 + 2 + 2 + 2 + 2 |

## <a name="see-also"></a>Voir aussi

[Vue d’ensemble du modèle de nuanceur 6](hlsl-shader-model-6-0-features-for-direct3d-12.md)

[Shader, modèle 6](shader-model-6-0.md)
