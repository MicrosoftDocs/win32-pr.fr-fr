---
title: WaveActiveCountBits fonction)
description: Compte le nombre de variables booléennes qui ont la valeur true sur tous les couloirs actifs de l’onde actuelle, et réplique le résultat sur tous les couloirs de l’onde.
ms.assetid: 053E100C-7E09-4F9D-9F38-9D5E208A38CE
keywords:
- WaveActiveCountBits fonction HLSL
topic_type:
- apiref
api_name:
- WaveActiveCountBits
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4e1642cbd5cbdef162511185e9d2c05e849d78486b82e8219623286f33e39223
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118504934"
---
# <a name="waveactivecountbits-function"></a>WaveActiveCountBits fonction)

Compte le nombre de variables booléennes qui ont la valeur true sur tous les couloirs actifs de l’onde actuelle, et réplique le résultat sur tous les couloirs de l’onde.

## <a name="syntax"></a>Syntaxe


``` syntax
uint WaveActiveCountBits(
   bool bBit
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*bBit* 
</dt> <dd>

Variables booléennes à évaluer. La fourniture d’une valeur booléenne True explicite retourne le nombre de couloirs actifs.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Nombre dont la valeur est true sur tous les couloirs actifs de l’onde actuelle.

## <a name="remarks"></a>Remarques

Cette fonction est prise en charge à partir du Shader Model 6,0 dans toutes les étapes du nuanceur. 



 

## <a name="examples"></a>Exemples

Cela peut être implémenté plus efficacement qu’un WaveActiveSum complet, comme décrit dans l’exemple suivant :

``` syntax
result = WaveActiveCountBits( WaveActiveBallot( bBit ) );
```

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Vue d’ensemble du modèle de nuanceur 6](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[Shader, modèle 6](shader-model-6-0.md)
</dt> </dl>

 

 




