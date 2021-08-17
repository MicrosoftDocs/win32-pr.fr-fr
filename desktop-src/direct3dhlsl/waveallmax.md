---
title: WaveActiveMax fonction)
description: Retourne la valeur maximale de l’expression sur tous les couloirs actifs de l’onde actuelle et la réplique sur tous les couloirs actifs.
ms.assetid: 19101C56-2618-4F34-8725-DF92198ABDA4
keywords:
- WaveActiveMax fonction HLSL
topic_type:
- apiref
api_name:
- WaveActiveMax
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8c85936ca28aabe0365fd912b4d764739b0ab15765241a243ad67143dacd0d7d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119484199"
---
# <a name="waveactivemax-function"></a>WaveActiveMax fonction)

Retourne la valeur maximale de l’expression sur tous les couloirs actifs de l’onde actuelle et la réplique sur tous les couloirs actifs.

## <a name="syntax"></a>Syntaxe

``` syntax
<type> WaveActiveMax(
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

Valeur maximale.

## <a name="remarks"></a>Remarques

L’ordre des opérations n’est pas défini.

Cette fonction est prise en charge à partir du Shader Model 6,0 dans toutes les étapes du nuanceur. 



 

## <a name="examples"></a>Exemples

``` syntax
 float3 maxPos = WaveActiveMax( myPoint.position );
    BoundingBox.max = max( maxPos, BoundingBox.max );
```

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Vue d’ensemble du modèle de nuanceur 6](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[Shader, modèle 6](shader-model-6-0.md)
</dt> </dl>

 

 




