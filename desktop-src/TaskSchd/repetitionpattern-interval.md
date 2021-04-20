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
ms.openlocfilehash: c1e81920fffe5c9fd58dd36a028b924f54ebe6dd
ms.sourcegitcommit: b3a9abea47dea7374eac0f9a95a652ac6977fb2e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/20/2021
ms.locfileid: "107734174"
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
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                          |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                    |
| Bibliothèque de types<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Planificateur de tâches](task-scheduler-start-page.md)
</dt> </dl>

 

 





