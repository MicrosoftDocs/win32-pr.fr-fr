---
title: WaveActiveAllEqual fonction)
description: Retourne la valeur true si l’expression est la même pour chaque voie active de l’onde actuelle (et donc uniforme sur celle-ci).
ms.assetid: E0A051A8-0ADD-4EC7-8D9A-8820CED9DA9D
keywords:
- WaveActiveAllEqual fonction HLSL
topic_type:
- apiref
api_name:
- WaveActiveAllEqual
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 34745e428fcd4453ce7274fc2a5accc6185f5b10
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/04/2020
ms.locfileid: "103734797"
---
# <a name="waveactiveallequal-function"></a>WaveActiveAllEqual fonction)

Retourne la valeur true si l’expression est la même pour chaque voie active de l’onde actuelle (et donc uniforme sur celle-ci).

## <a name="syntax"></a>Syntaxe


``` syntax
bool WaveActiveAllEqual(
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

True si l’expression est la même pour chaque voie active de l’onde actuelle.

## <a name="remarks"></a>Notes

Cette fonction est prise en charge à partir du Shader Model 6,0 dans toutes les étapes du nuanceur. 



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Vue d’ensemble du modèle de nuanceur 6](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[Shader, modèle 6](shader-model-6-0.md)
</dt> </dl>

 

 




