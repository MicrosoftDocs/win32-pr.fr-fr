---
title: Objet MonthlyTrigger
description: Objet de script qui représente un déclencheur qui démarre une tâche basée sur une planification mensuelle.
ms.assetid: d73715cb-a52e-4daf-930f-e94fbe28881e
keywords:
- Planificateur de tâches de déclencheur mensuel, objet
- Objet MonthlyTrigger Planificateur de tâches
- Planificateur de tâches d’objets MonthlyTrigger, Description
topic_type:
- apiref
api_name:
- MonthlyTrigger
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 078ecf023bd66fb0ad92b87f6dcc16978166fd7c6b3bbfce6d9b971f19b87be9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117760066"
---
# <a name="monthlytrigger-object"></a>Objet MonthlyTrigger

Objet de script qui représente un déclencheur qui démarre une tâche basée sur une planification mensuelle. Par exemple, la tâche démarre sur des jours spécifiques de mois spécifiques.

## <a name="members"></a>Membres

L’objet **MonthlyTrigger** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

L’objet **MonthlyTrigger** a ces propriétés.



| Propriété                                                                     | Type d’accès           | Description                                                                                                                                                                                 |
|:-----------------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DaysOfMonth**](monthlytrigger-daysofmonth.md)<br/>                 | Lecture/écriture<br/> | Obtient ou définit les jours du mois pendant lesquels la tâche s’exécute.<br/>                                                                                                                   |
| [**Activé**](trigger-enabled.md)<br/>                                | Lecture/écriture<br/> | Héritée de l’objet [**déclencheur**](trigger.md) . Obtient ou définit une valeur booléenne qui indique si le déclencheur est activé.<br/>                                                |
| [EndBoundary](trigger-endboundary.md)<br/>                            | Lecture/écriture<br/> | Héritée de l’objet [**déclencheur**](trigger.md) . Obtient ou définit la date et l’heure de désactivation du déclencheur. Le déclencheur ne peut pas démarrer la tâche une fois qu’elle est désactivée.<br/> |
| [**ExecutionTimeLimit**](trigger-executiontimelimit.md)<br/>          | Lecture/écriture<br/> | Héritée de l’objet [**déclencheur**](trigger.md) . Obtient ou définit la durée maximale pendant laquelle la tâche lancée par le déclencheur est autorisée à s’exécuter.<br/>                           |
| [**Identifi**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_id)<br/>                                         | Lecture/écriture<br/> | Héritée de l’objet [**déclencheur**](trigger.md) . Obtient ou définit l’identificateur pour le déclencheur.<br/>                                                                               |
| [**MonthsOfYear**](monthlytrigger-monthsofyear.md)<br/>               | Lecture/écriture<br/> | Obtient ou définit les mois de l’année pendant laquelle la tâche s’exécute.<br/>                                                                                                                  |
| [**RandomDelay**](monthlytrigger-randomdelay.md)<br/>                 | Lecture/écriture<br/> | Obtient ou définit un délai qui est ajouté de manière aléatoire à l’heure de début du déclencheur.<br/>                                                                                               |
| [**Répétition**](trigger-repetition.md)<br/>                          | Lecture/écriture<br/> | Héritée de l’objet [**déclencheur**](trigger.md) . Obtient ou définit la fréquence d’exécution de la tâche et la durée de répétition du modèle de répétition après le démarrage de la tâche.<br/>          |
| [**RunOnLastDayOfMonth**](monthlytrigger-runonlastdayofmonth.md)<br/> | Lecture/écriture<br/> | Obtient ou définit une valeur booléenne qui indique que la tâche s’exécute le dernier jour du mois.<br/>                                                                                     |
| [**StartBoundary**](trigger-startboundary.md)<br/>                    | Lecture/écriture<br/> | Héritée de l’objet [**déclencheur**](trigger.md) . Obtient ou définit la date et l’heure d’activation du déclencheur.<br/>                                                              |
| [**Type**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_type)<br/>                                     | Lecture seule<br/>  | Héritée de l’objet [**déclencheur**](trigger.md) . Obtient le type du déclencheur.<br/>                                                                                              |



 

## <a name="remarks"></a>Remarques

L’heure de début de la tâche est définie par la propriété [**StartBoundary**](trigger-startboundary.md) .

Lors de la lecture ou de l’écriture de votre propre XML pour une tâche, un déclencheur mensuel est spécifié à l’aide de l’élément [**ScheduleByMonth**](taskschedulerschema-schedulebymonth-calendartriggertype-element.md) du schéma planificateur de tâches.

## <a name="requirements"></a>Configuration requise



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

 

 





