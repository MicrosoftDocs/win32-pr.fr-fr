---
title: RepetitionPattern. Interval, propriété
description: Pour les scripts, obtient ou définit la durée entre chaque redémarrage de la tâche.
ms.assetid: c48bd304-21f3-435e-99f5-3b2da0078bb8
keywords:
- Planificateur de tâches de la propriété Interval
- Planificateur de tâches de la propriété Interval, objet RepetitionPattern
- Objet RepetitionPattern Planificateur de tâches, propriété Interval
topic_type:
- apiref
api_name:
- RepetitionPattern.Interval
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc6efcaa56d2c251b5e044c87091bc646c21f8691aa384ad522b6062014fd496
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120072619"
---
# <a name="repetitionpatterninterval-property"></a>RepetitionPattern. Interval, propriété

Pour les scripts, obtient ou définit la durée entre chaque redémarrage de la tâche.

## <a name="syntax"></a>Syntaxe


```VB
RepetitionPattern.Interval As String
```



## <a name="property-value"></a>Valeur de la propriété

Intervalle de temps entre chaque redémarrage de la tâche. Le format de cette chaîne est `P<days>DT<hours>H<minutes>M<seconds>S` (par exemple, « PT5M » est de 5 minutes, « PT1H » est 1 heure et « PT20M » est 20 minutes). La durée maximale autorisée est de 31 jours, et la durée minimale autorisée est de 1 minute.

## <a name="remarks"></a>Remarques

Si vous spécifiez une durée de répétition pour une tâche, vous devez également spécifier l’intervalle de répétition.

Lors de la lecture ou de l’écriture de données XML pour une tâche, l’intervalle de répétition est spécifié dans l’élément [**Interval**](taskschedulerschema-interval-repetitiontype-element.md) du schéma planificateur de tâches.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                          |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                    |
| Bibliothèque de types<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Planificateur de tâches](task-scheduler-start-page.md)
</dt> </dl>

 

 





