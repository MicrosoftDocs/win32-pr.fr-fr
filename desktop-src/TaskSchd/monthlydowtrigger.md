---
title: Objet MonthlyDOWTrigger
description: Objet de script qui représente un déclencheur qui démarre une tâche sur une planification mensuelle de jour de semaine.
ms.assetid: 18607189-295f-4f7d-bf72-f0ac8d5067cf
keywords:
- Planificateur de tâches du déclencheur DOW mensuel, objet
- Objet MonthlyDOWTrigger Planificateur de tâches
- Planificateur de tâches d’objets MonthlyDOWTrigger, Description
topic_type:
- apiref
api_name:
- MonthlyDOWTrigger
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b7e43925c6ebe27933a39fe5e25f37ffe6cf72e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127120626"
---
# <a name="monthlydowtrigger-object"></a>Objet MonthlyDOWTrigger

Objet de script qui représente un déclencheur qui démarre une tâche sur une planification mensuelle de jour de semaine. Par exemple, la tâche commence à chaque jeudi, du 1er mai au octobre.

## <a name="members"></a>Membres

L’objet **MonthlyDOWTrigger** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

L’objet **MonthlyDOWTrigger** a ces propriétés.



| Propriété                                                                          | Type d’accès           | Description                                                                                                                                                                                 |
|:----------------------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DaysOfWeek**](monthlydowtrigger-daysofweek.md)<br/>                     | Lecture/écriture<br/> | Obtient ou définit les jours de la semaine pendant lesquels la tâche est exécutée.<br/>                                                                                                                    |
| [**Activé**](trigger-enabled.md)<br/>                                     | Lecture/écriture<br/> | Héritée de l’objet [**déclencheur**](trigger.md) . Obtient ou définit une valeur booléenne qui indique si le déclencheur est activé.<br/>                                                |
| [EndBoundary](trigger-endboundary.md)<br/>                                 | Lecture/écriture<br/> | Héritée de l’objet [**déclencheur**](trigger.md) . Obtient ou définit la date et l’heure de désactivation du déclencheur. Le déclencheur ne peut pas démarrer la tâche une fois qu’elle est désactivée.<br/> |
| [**ExecutionTimeLimit**](trigger-executiontimelimit.md)<br/>               | Lecture/écriture<br/> | Héritée de l’objet [**déclencheur**](trigger.md) . Obtient ou définit la durée maximale pendant laquelle la tâche lancée par ce déclencheur est autorisée à s’exécuter.<br/>                          |
| [**Identifi**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_id)<br/>                                              | Lecture/écriture<br/> | Héritée de l’objet [**déclencheur**](trigger.md) . Obtient ou définit l’identificateur pour le déclencheur.<br/>                                                                               |
| [**MonthsOfYear**](monthlydowtrigger-monthsofyear.md)<br/>                 | Lecture/écriture<br/> | Obtient ou définit les mois de l’année pendant laquelle la tâche s’exécute.<br/>                                                                                                                  |
| [**RandomDelay**](monthlydowtrigger-randomdelay.md)<br/>                   | Lecture/écriture<br/> | Obtient ou définit un délai qui est ajouté de manière aléatoire à l’heure de début du déclencheur.<br/>                                                                                               |
| [**Répétition**](trigger-repetition.md)<br/>                               | Lecture/écriture<br/> | Héritée de l’objet [**déclencheur**](trigger.md) . Obtient ou définit la fréquence d’exécution de la tâche et la durée de répétition du modèle de répétition après le démarrage de la tâche.<br/>          |
| [**RunOnLastWeekOfMonth**](monthlydowtrigger-runonlastweekofmonth.md)<br/> | Lecture/écriture<br/> | Obtient ou définit une valeur booléenne qui indique que la tâche s’exécute à la dernière semaine du mois.<br/>                                                                                    |
| [**StartBoundary**](trigger-startboundary.md)<br/>                         | Lecture/écriture<br/> | Héritée de l’objet [**déclencheur**](trigger.md) . Obtient ou définit la date et l’heure d’activation du déclencheur.<br/>                                                              |
| [**Entrer**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_type)<br/>                                          | Lecture seule<br/>  | Héritée de l’objet [**déclencheur**](trigger.md) . Obtient le type du déclencheur.<br/>                                                                                              |
| [**WeeksOfMonth**](monthlydowtrigger-weeksofmonth.md)<br/>                 | Lecture/écriture<br/> | Obtient ou définit les semaines du mois pendant lequel la tâche s’exécute.<br/>                                                                                                                  |



 

## <a name="remarks"></a>Notes

L’heure de début de la tâche est définie par la propriété [**StartBoundary**](trigger-startboundary.md) .

Lors de la lecture ou de l’écriture de données XML pour une tâche, un déclencheur de jour de semaine mensuel est spécifié à l’aide de l’élément [**ScheduleByMonthDayOfWeek**](taskschedulerschema-schedulebymonthdayofweek-calendartriggertype-element.md) du schéma planificateur de tâches.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                          |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                    |
| Bibliothèque de types<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Déclencheur**](trigger.md)
</dt> <dt>

[Objets Planificateur de tâches](task-scheduler-objects.md)
</dt> <dt>

[Planificateur de tâches](task-scheduler-start-page.md)
</dt> <dt>

[**TriggerCollection**](triggercollection.md)
</dt> <dt>

[**TriggerCollection. Create**](triggercollection-create.md)
</dt> </dl>

 

 





