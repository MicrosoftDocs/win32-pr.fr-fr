---
title: objet TimeTrigger (Windows. applicationmodel. background. h)
description: Objet de script qui représente un déclencheur qui démarre une tâche à une date et une heure spécifiques.
ms.assetid: 3c277827-8e70-42e7-a849-773ecc997a93
keywords:
- Planificateur de tâches de déclencheur d’heure, objet
- Objet TimeTrigger Planificateur de tâches
- Planificateur de tâches d’objets TimeTrigger, Description
topic_type:
- apiref
api_name:
- TimeTrigger
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40f0fb6f5eaff5101f3cc1f5c4aeb2245335e4f65b27d2fafb364df2d05618ec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119771979"
---
# <a name="timetrigger-object"></a>Objet TimeTrigger

Objet de script qui représente un déclencheur qui démarre une tâche à une date et une heure spécifiques.

## <a name="members"></a>Membres

L’objet **timetrigger** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

L’objet **timetrigger** a ces propriétés.



| Propriété                                                            | Type d’accès           | Description                                                                                                                                                                      |
|:--------------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**activé**](trigger-enabled.md)<br/>                       | Lecture/écriture<br/> | Héritée du [**déclencheur**](trigger.md). Obtient ou définit une valeur booléenne qui indique si le déclencheur est activé.<br/>                                                |
| [**EndBoundary**](trigger-endboundary.md)<br/>               | Lecture/écriture<br/> | Héritée du [**déclencheur**](trigger.md). Obtient ou définit la date et l’heure de désactivation du déclencheur. Le déclencheur ne peut pas démarrer la tâche une fois qu’elle est désactivée.<br/> |
| [**ExecutionTimeLimit**](trigger-executiontimelimit.md)<br/> | Lecture/écriture<br/> | Héritée du [**déclencheur**](trigger.md). Obtient ou définit la durée maximale pendant laquelle la tâche lancée par le déclencheur est autorisée à s’exécuter.<br/>                           |
| [**Identifi**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_id)<br/>                                | Lecture/écriture<br/> | Héritée du [**déclencheur**](trigger.md). Obtient ou définit l’identificateur pour le déclencheur.<br/>                                                                               |
| [**RandomDelay**](dailytrigger-randomdelay.md)<br/>          | Lecture/écriture<br/> | Obtient ou définit un délai qui est ajouté de manière aléatoire à l’heure de début du déclencheur.<br/>                                                                                    |
| [**Répétition**](trigger-repetition.md)<br/>                 | Lecture/écriture<br/> | Héritée du [**déclencheur**](trigger.md). Obtient ou définit la fréquence d’exécution de la tâche et la durée de répétition du modèle de répétition après le démarrage de la tâche.<br/>          |
| [**StartBoundary**](trigger-startboundary.md)<br/>           | Lecture/écriture<br/> | Héritée du [**déclencheur**](trigger.md). Obtient ou définit la date et l’heure d’activation du déclencheur. Cet élément est obligatoire.<br/>                                    |
| [**Type**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_type)<br/>                            | Lecture seule<br/>  | Héritée du [**déclencheur**](trigger.md). Obtient le type du déclencheur.<br/>                                                                                              |



 

## <a name="remarks"></a>Remarques

L’élément [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) est un élément requis pour les déclencheurs de temps et de calendrier ([**timetrigger**](taskschedulerschema-timetrigger-triggergroup-element.md) et [**CalendarTrigger**](taskschedulerschema-calendartrigger-triggergroup-element.md)).

Lors de la lecture ou de l’écriture de données XML pour une tâche, un déclencheur inactif est spécifié à l’aide de l’élément [**timetrigger**](taskschedulerschema-timetrigger-triggergroup-element.md) du schéma planificateur de tâches.

## <a name="examples"></a>Exemples

Pour plus d’informations et pour obtenir un exemple de code pour cet objet de script, consultez [exemple de déclenchement temporel (script)](time-trigger-example--scripting-.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                                                   |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                                             |
| En-tête<br/>                   | <dl> <dt>Windows. applicationmodel. background. h</dt> </dl> |
| Bibliothèque de types<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl>                          |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl>                          |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Déclencheur**](trigger.md)
</dt> <dt>

[**TriggerCollection**](triggercollection.md)
</dt> <dt>

[**TriggerCollection. Create**](triggercollection-create.md)
</dt> </dl>

 

 





