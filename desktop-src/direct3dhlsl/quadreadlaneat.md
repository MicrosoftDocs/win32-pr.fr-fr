---
title: QuadReadLaneAt fonction)
description: Retourne la valeur source spécifiée à partir du Lane identifié par l’ID Lane dans le quad actuel.
ms.assetid: 5CD7EE4C-E64E-46A3-ABDC-1BF65D0F96BE
keywords:
- QuadReadLaneAt fonction HLSL
topic_type:
- apiref
api_name:
- QuadReadLaneAt
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a6c06fc1118496c0f87b39ea73dfa9a515d2f2f684eb7258979c7c93dfc4eea1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118088645"
---
# <a name="quadreadlaneat-function"></a>QuadReadLaneAt fonction)

Retourne la valeur source spécifiée à partir du Lane identifié par l’ID Lane dans le quad actuel.

## <a name="syntax"></a>Syntaxe


``` syntax
<type> QuadReadLaneAt(
   <type> sourceValue,
   uint   quadLaneID  
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*sourceValue* 
</dt> <dd>

Type demandé.

</dd> <dt>

*quadLaneID* 
</dt> <dd>

ID Lane ; Il s’agit d’une valeur comprise entre 0 et 3.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Valeur source spécifiée. Le résultat de cette fonction est uniforme sur le quadruple. Si le couloir source est inactif, les résultats ne sont pas définis.

## <a name="remarks"></a>Remarques

Pour plus d’informations sur les Quad, reportez-vous à [vue d’ensemble du Shader Model 6](hlsl-shader-model-6-0-features-for-direct3d-12.md).

Cette fonction est prise en charge à partir du nuanceur modèle 6,0 uniquement dans les nuanceurs de pixels et de calcul.



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Shader, modèle 6](shader-model-6-0.md)
</dt> </dl>

 

 




