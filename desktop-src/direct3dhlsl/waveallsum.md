---
title: WaveActiveSum fonction)
description: Additionne la valeur de l’expression sur tous les couloirs actifs de l’onde actuelle et la réplique sur tous les couloirs de l’onde actuelle.
ms.assetid: 94CEF4AA-D6DE-4B00-9743-F491F255FE3D
keywords:
- WaveActiveSum fonction HLSL
topic_type:
- apiref
api_name:
- WaveActiveSum
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 403768b875ed9462b79fb5d0abeee9539189597591f3a3b20f5a3b9662995542
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119742259"
---
# <a name="waveactivesum-function"></a>WaveActiveSum fonction)

Additionne la valeur de l’expression sur tous les couloirs actifs de l’onde actuelle et la réplique sur tous les couloirs de l’onde actuelle.

## <a name="syntax"></a>Syntaxe

``` syntax
<type> WaveActiveSum(
   <type> expr
);
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*expr* 
</dt> <dd>

Expression à évaluer.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Valeur de la somme.

## <a name="remarks"></a>Remarques

L’ordre des opérations n’est pas défini.

Cette fonction est prise en charge à partir du Shader Model 6,0 dans toutes les étapes du nuanceur. 



 

## <a name="examples"></a>Exemples

``` syntax
float3 total = WaveActiveSum( position ); // sum positions in wave
float3 center = total/count;           // compute average of these positions
```

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Vue d’ensemble du modèle de nuanceur 6](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[Shader, modèle 6](shader-model-6-0.md)
</dt> </dl>

 

 




