---
title: Objet WeeklyTrigger
description: Objet de script qui représente un déclencheur qui démarre une tâche basée sur une planification hebdomadaire.
ms.assetid: a000d7a8-0239-440f-b49b-7f0c55b01e8e
keywords:
- déclencheur hebdomadaire Planificateur de tâches, objet
- Objet WeeklyTrigger Planificateur de tâches
- Planificateur de tâches d’objets WeeklyTrigger, Description
topic_type:
- apiref
api_name:
- WeeklyTrigger
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58dec9172d38b53f779f44a048b39bc709dbd54f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743852"
---
# <a name="weeklytrigger-object"></a>Objet WeeklyTrigger

Objet de script qui représente un déclencheur qui démarre une tâche basée sur une planification hebdomadaire. Par exemple, la tâche commence à 8:00 h 00. à un jour spécifique de la semaine chaque semaine ou chaque semaine.

## <a name="members"></a>Membres

L’objet **WeeklyTrigger** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

L’objet **WeeklyTrigger** a ces propriétés.



| Propriété                                                            | Type d’accès           | Description                                                                                                                                                                                 |
|:--------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DaysOfWeek**](weeklytrigger-daysofweek.md)<br/>           | Lecture/écriture<br/> | Obtient ou définit les jours de la semaine où la tâche est exécutée.<br/>                                                                                                                        |
| [**Enabled**](trigger-enabled.md)<br/>                       | Lecture/écriture<br/> | Héritée de l’objet [**déclencheur**](trigger.md) . Obtient ou définit une valeur booléenne qui indique si le déclencheur est activé.<br/>                                                |
| [**EndBoundary**](trigger-endboundary.md)<br/>               | Lecture/écriture<br/> | Héritée de l’objet [**déclencheur**](trigger.md) . Obtient ou définit la date et l’heure de désactivation du déclencheur. Le déclencheur ne peut pas démarrer la tâche une fois qu’elle est désactivée.<br/> |
| [**ExecutionTimeLimit**](trigger-executiontimelimit.md)<br/> | Lecture/écriture<br/> | Héritée de l’objet [**déclencheur**](trigger.md) . Obtient ou définit la durée maximale pendant laquelle la tâche lancée par le déclencheur est autorisée à s’exécuter.<br/>                           |
| [**Identifi**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_id)<br/>                                | Lecture/écriture<br/> | Héritée de l’objet [**déclencheur**](trigger.md) . Obtient ou définit l’identificateur pour le déclencheur.<br/>                                                                               |
| [**RandomDelay**](weeklytrigger-randomdelay.md)<br/>         | Lecture/écriture<br/> | Obtient ou définit un délai qui est ajouté de manière aléatoire à l’heure de début du déclencheur.<br/>                                                                                               |
| [**Répétition**](trigger-repetition.md)<br/>                 | Lecture/écriture<br/> | Héritée de l’objet [**déclencheur**](trigger.md) . Obtient ou définit la fréquence d’exécution de la tâche et la durée de répétition du modèle de répétition après le démarrage de la tâche.<br/>          |
| [**StartBoundary**](trigger-startboundary.md)<br/>           | Lecture/écriture<br/> | Héritée de l’objet [**déclencheur**](trigger.md) . Obtient ou définit la date et l’heure d’activation du déclencheur.<br/>                                                              |
| [**Entrer**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_type)<br/>                            | Lecture seule<br/>  | Héritée de l’objet [**déclencheur**](trigger.md) . Obtient le type du déclencheur.<br/>                                                                                              |
| [**WeeksInterval**](weeklytrigger-weeksinterval.md)<br/>     | Lecture/écriture<br/> | Obtient ou définit l’intervalle entre les semaines de la planification.<br/>                                                                                                                     |



 

## <a name="remarks"></a>Notes

L’heure de début de la tâche est définie par la propriété [**StartBoundary**](trigger-startboundary.md) .

Lors de la lecture ou de l’écriture de vos propres données XML pour une tâche, un déclencheur hebdomadaire est spécifié à l’aide de l’élément [**ScheduleByWeek**](taskschedulerschema-schedulebyweek-calendartriggertype-element.md) du schéma planificateur de tâches.

## <a name="examples"></a>Exemples

Pour plus d’informations et pour obtenir un exemple de code pour cet objet de script, consultez [exemple de déclencheur hebdomadaire (script)](weekly-trigger-example--scripting-.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                          |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                    |
| Bibliothèque de types<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Stead**](trigger.md)
</dt> <dt>

[**TriggerCollection**](triggercollection.md)
</dt> <dt>

[**TriggerCollection. Create**](triggercollection-create.md)
</dt> </dl>

 

 





