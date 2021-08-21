---
title: Objet DailyTrigger
description: Objet de script qui représente un déclencheur qui démarre une tâche basée sur une planification quotidienne.
ms.assetid: f03f53a0-0060-4793-96c1-b47a96852579
keywords:
- Planificateur de tâches de déclencheur quotidien, objet
- Objet DailyTrigger Planificateur de tâches
- Planificateur de tâches d’objets DailyTrigger, Description
topic_type:
- apiref
api_name:
- DailyTrigger
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7b330906b309bbd672fcb9c333bc254fb02ee668549764d7dc1375f6ac405a3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119060177"
---
# <a name="dailytrigger-object"></a>Objet DailyTrigger

Objet de script qui représente un déclencheur qui démarre une tâche basée sur une planification quotidienne.

## <a name="members"></a>Membres

L’objet **DailyTrigger** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

L’objet **DailyTrigger** a ces propriétés.



| Propriété                                                            | Type d’accès           | Description                                                                                                                                                                                 |
|:--------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DaysInterval**](dailytrigger-daysinterval.md)<br/>        | Lecture/écriture<br/> | Obtient ou définit l’intervalle entre les jours de la planification.<br/>                                                                                                                      |
| [**Activé**](trigger-enabled.md)<br/>                       | Lecture/écriture<br/> | Héritée de l’objet [**déclencheur**](trigger.md) . Obtient ou définit une valeur booléenne qui indique si le déclencheur est activé.<br/>                                                |
| [**EndBoundary**](trigger-endboundary.md)<br/>               | Lecture/écriture<br/> | Héritée de l’objet [**déclencheur**](trigger.md) . Obtient ou définit la date et l’heure de désactivation du déclencheur. Le déclencheur ne peut pas démarrer la tâche une fois qu’elle est désactivée.<br/> |
| [**ExecutionTimeLimit**](trigger-executiontimelimit.md)<br/> | Lecture/écriture<br/> | Héritée de l’objet [**déclencheur**](trigger.md) . Obtient ou définit la durée maximale pendant laquelle la tâche lancée par le déclencheur est autorisée à s’exécuter.<br/>                           |
| [**Identifi**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_id)<br/>                                | Lecture/écriture<br/> | Héritée de l’objet [**déclencheur**](trigger.md) . Obtient ou définit l’identificateur pour le déclencheur.<br/>                                                                               |
| [**RandomDelay**](dailytrigger-randomdelay.md)<br/>          | Lecture/écriture<br/> | Obtient ou définit un délai qui est ajouté de manière aléatoire à l’heure de début du déclencheur.<br/>                                                                                               |
| [**Répétition**](trigger-repetition.md)<br/>                 | Lecture/écriture<br/> | Héritée de l’objet [**déclencheur**](trigger.md) . Obtient ou définit la fréquence d’exécution de la tâche et la durée de répétition du modèle de répétition après le démarrage de la tâche.<br/>          |
| [**StartBoundary**](trigger-startboundary.md)<br/>           | Lecture/écriture<br/> | Héritée de l’objet [**déclencheur**](trigger.md) . Obtient ou définit la date et l’heure d’activation du déclencheur.<br/>                                                              |
| [**Type**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_type)<br/>                            | Lecture seule<br/>  | Héritée de l’objet [**déclencheur**](trigger.md) . Obtient le type du déclencheur.<br/>                                                                                              |



 

## <a name="remarks"></a>Remarques

L’heure de début de la tâche est définie par la propriété [**StartBoundary**](trigger-startboundary.md) .

Un intervalle de 1 produit une planification quotidienne. Un intervalle de 2 produit une planification tous les jours, et ainsi de suite.

Lors de la lecture ou de l’écriture de vos propres données XML pour une tâche, un déclencheur quotidien est spécifié à l’aide de l’élément [**ScheduleByDay**](taskschedulerschema-schedulebyday-calendartriggertype-element.md) du schéma planificateur de tâches.

## <a name="examples"></a>Exemples

Pour plus d’informations et pour obtenir un exemple de code pour cet objet de script, consultez [exemple de déclencheur quotidien (script)](daily-trigger-example--scripting-.md).

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

[**TriggerCollection**](triggercollection.md)
</dt> <dt>

[**TriggerCollection. Create**](triggercollection-create.md)
</dt> </dl>

 

 





