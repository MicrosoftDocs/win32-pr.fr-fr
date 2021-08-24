---
title: WaveIsFirstLane fonction)
description: Retourne true uniquement pour la voie active dans l’onde actuelle avec l’index le plus petit.
ms.assetid: 5D90F713-08C7-4BD4-867B-2E7CA3A85E87
keywords:
- WaveIsFirstLane fonction HLSL
topic_type:
- apiref
api_name:
- WaveIsFirstLane
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d909d4269db61980325c48b5858d910955512f701fb09adbcb91f5e078fa3b33
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119852709"
---
# <a name="waveisfirstlane-function"></a>WaveIsFirstLane fonction)

Retourne true uniquement pour la voie active dans l’onde actuelle avec l’index le plus petit.

## <a name="syntax"></a>Syntaxe


``` syntax
bool WaveIsFirstLane(void);
```



## <a name="parameters"></a>Paramètres

Cette fonction n’a pas de paramètres.

## <a name="return-value"></a>Valeur retournée

True uniquement pour la voie active dans l’onde actuelle avec l’index le plus petit.

## <a name="remarks"></a>Remarques

Cette fonction peut être utilisée pour identifier les opérations qui doivent être exécutées une seule fois par vague.

Cette fonction est prise en charge à partir du Shader Model 6,0 dans toutes les étapes du nuanceur. 



 

## <a name="examples"></a>Exemples

``` syntax
 if ( WaveIsFirstLane() )
{
    . . . // once per-wave code
}
```

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Vue d’ensemble du modèle de nuanceur 6](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[Shader, modèle 6](shader-model-6-0.md)
</dt> </dl>

 

 




