---
title: WaveGetLaneCount fonction)
description: Retourne le nombre de couloirs dans une vague sur cette architecture.
ms.assetid: 04059B5E-0F62-4623-84AD-E41FF7166B34
keywords:
- WaveGetLaneCount fonction HLSL
topic_type:
- apiref
api_name:
- WaveGetLaneCount
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6a177e50ee3c4c9c715ea109faaed72c24e174e4e942059a4dee0dcd0de91a9e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118504737"
---
# <a name="wavegetlanecount-function"></a>WaveGetLaneCount fonction)

Retourne le nombre de couloirs dans une vague sur cette architecture.

## <a name="syntax"></a>Syntaxe

``` syntax
uint WaveGetLaneCount(void);
```

## <a name="parameters"></a>Paramètres

Cette fonction n’a pas de paramètres.

## <a name="return-value"></a>Valeur retournée

Le résultat sera compris entre 4 et 128, et comprend toutes les vagues : les pistes active, inactive et/ou d’assistance. Le résultat retourné par cette fonction peut varier considérablement en fonction de l’implémentation du pilote.

## <a name="remarks"></a>Remarques

Cette fonction est prise en charge à partir du Shader Model 6,0 dans toutes les étapes du nuanceur. 



 

## <a name="examples"></a>Exemples

``` syntax
 uint laneCount = WaveGetLaneCount();    // number of lanes in wave
```

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Vue d’ensemble du modèle de nuanceur 6](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[Shader, modèle 6](shader-model-6-0.md)
</dt> </dl>

 

 




