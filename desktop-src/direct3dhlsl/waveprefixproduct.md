---
title: Fonction WavePrefixProduct
description: Retourne le produit de toutes les valeurs des couloirs actifs dans cette vague avec des index inférieurs à ce couloir.
ms.assetid: 3A5B271D-EF45-4511-9086-A9AD0D215D9A
keywords:
- WavePrefixProduct fonction HLSL
topic_type:
- apiref
api_name:
- WavePrefixProduct
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d073d72590951ddbbbb74274d4cd237e0a138c4f
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/04/2020
ms.locfileid: "104383283"
---
# <a name="waveprefixproduct-function"></a>Fonction WavePrefixProduct

Retourne le produit de toutes les valeurs des couloirs actifs dans cette vague avec des index inférieurs à ce couloir.

## <a name="syntax"></a>Syntaxe

``` syntax
<type> WavePrefixProduct(
   <type> value
);
```

## <a name="parameters"></a>Paramètres

*value* 

Valeur à multiplier.

## <a name="return-value"></a>Valeur retournée

Produit de toutes les valeurs.

## <a name="remarks"></a>Notes

L’ordre des opérations sur cette routine ne peut pas être garanti. Ainsi, en fait, \[ l' \] indicateur précis est ignoré dans celui-ci.

Un produit postfix peut être calculé en multipliant le préfixe produit par la valeur de la voie actuelle.

Notez que la voie active avec l’index le plus bas reçoit toujours 1 pour son préfixe Product.

Cette fonction est prise en charge à partir du Shader Model 6,0 dans toutes les étapes du nuanceur. 

## <a name="examples"></a>Exemples

```hlsl
uint numToMultiply = 2;
uint prefixProduct = WavePrefixProduct( numToMultiply );
```

Sur un ordinateur doté d’une taille d’onde de 8, et de tous les couloirs actifs, à l’exception des couloirs 0 et 4, les valeurs suivantes sont retournées à partir de WavePrefixProduct.

| index Lane | status   | prefixProduct | 
|------------|----------|---------------|
| 0          | inactive | n/a           |
| 1          | active   | = 1           |
| 2          | active   | = 1 \* 2        |
| 3          | active   | = 1 \* 2 \* 2     |
| 4          | inactive | n/a           |
| 5          | active   | = 1 \* 2 \* 2 2 \*       |
| 6          | active   | = 1 \* 2 \* 2 \* 2 \* 2    |
| 7          | active   | = 1 \* 2 \* 2 \* 2 \* 2 \* 2 |

## <a name="see-also"></a>Voir aussi

[Vue d’ensemble du modèle de nuanceur 6](hlsl-shader-model-6-0-features-for-direct3d-12.md)

[Shader, modèle 6](shader-model-6-0.md)
