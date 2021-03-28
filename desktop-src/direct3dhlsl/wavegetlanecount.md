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
ms.openlocfilehash: 0bfdb3ce2dfde84b070fee57e7fc587a71d5f948
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/04/2020
ms.locfileid: "104383284"
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

## <a name="remarks"></a>Notes

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

 

 




