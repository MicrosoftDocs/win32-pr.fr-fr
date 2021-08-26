---
title: Élément ExecutionTimeLimit (triggerBaseType)
description: Spécifie la durée maximale pendant laquelle la tâche peut être démarrée par le déclencheur.
ms.assetid: f78e7c7b-d069-4920-9435-020f6e081eff
keywords:
- Élément ExecutionTimeLimit Planificateur de tâches
topic_type:
- apiref
api_name:
- ExecutionTimeLimit
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6e958c6a2b873bb78e66645ce2a2ae8100e2acbc
ms.sourcegitcommit: 0dec0044816af3f2b2e6403659e1cf11138c90cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/13/2021
ms.locfileid: "121812526"
---
# <a name="executiontimelimit-triggerbasetype-element"></a>Élément ExecutionTimeLimit (triggerBaseType)

Durée maximale pendant laquelle la tâche lancée par le déclencheur est autorisée à s’exécuter. Le format de cette chaîne est PnYnMnDTnHnMnS, où nY est le nombre d’années, nM est le nombre de mois, nD le nombre de jours, 't’est le séparateur de date/heure, nH est le nombre d’heures, nM est le nombre de minutes et nS est le nombre de secondes (par exemple, PT5M spécifie 5 minutes et P1M4DT2H5M spécifie un mois, quatre jours, deux heures et cinq minutes). Pour plus d’informations sur le type de durée, consultez <https://go.microsoft.com/fwlink/p/?linkid=106886> .

``` syntax
<xs:element name="ExecutionTimeLimit"
    type="duration"
 />
```

L’élément **ExecutionTimeLimit** est défini par le type complexe [**triggerBaseType**](taskschedulerschema-boottriggertype-complextype.md) .

## <a name="parent-element"></a>Élément parent



| Élément                                                                                     | Dérivé de                                                                               | Description                                                                                  |
|---------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [**BootTrigger**](taskschedulerschema-boottrigger-triggergroup-element.md)                 | [**bootTriggerType**](taskschedulerschema-boottriggertype-complextype.md)                 | Spécifie un déclencheur qui démarre une tâche au démarrage du système.<br/>                 |
| [**CalendarTrigger**](taskschedulerschema-calendartrigger-triggergroup-element.md)         | [**calendarTriggerType**](taskschedulerschema-calendartriggertype-complextype.md)         | Spécifie un déclencheur quotidien, hebdomadaire, mensuel ou un jour de la semaine (DOW) mensuel.<br/>   |
| [**EventTrigger**](taskschedulerschema-eventtrigger-triggergroup-element.md)               | [**eventTriggerType**](taskschedulerschema-eventtriggertype-complextype.md)               | Spécifie un déclencheur qui démarre une tâche lorsqu’un événement système se produit.<br/>                |
| [**IdleTrigger**](taskschedulerschema-idletrigger-triggergroup-element.md)                 | [**idleTriggerType**](taskschedulerschema-idletriggertype-complextype.md)                 | Spécifie un déclencheur qui démarre une tâche lorsque l’ordinateur passe en état d’inactivité.<br/> |
| [**LogonTrigger**](taskschedulerschema-logontrigger-triggergroup-element.md)               | [**logonTriggerType**](taskschedulerschema-logontriggertype-complextype.md)               | Spécifie un déclencheur qui démarre une tâche lorsqu’un utilisateur ouvre une session.<br/>                       |
| [**RegistrationTrigger**](taskschedulerschema-registrationtrigger-triggergroup-element.md) | [**registrationTriggerType**](taskschedulerschema-registrationtriggertype-complextype.md) | Spécifie un déclencheur qui démarre une tâche lorsque la tâche est inscrite.<br/>               |
| [**TimeTrigger**](taskschedulerschema-timetrigger-triggergroup-element.md)                 | [**timeTriggerType**](taskschedulerschema-timetriggertype-complextype.md)                 | Spécifie un déclencheur qui démarre une tâche lorsque le déclencheur est activé.<br/>             |



## <a name="remarks"></a>Remarques

Pour le développement de scripts, la limite de durée d’exécution est spécifiée à l’aide de la propriété [**Trigger.ExecutionTimeLimit**](trigger-executiontimelimit.md) qui est héritée par tous les objets déclencheurs.

Pour le développement C++, le délai d’exécution est spécifié à l’aide de la propriété [**ITrigger :: ExecutionTimeLimit**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_executiontimelimit) qui est héritée par les interfaces de déclencheur All.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Éléments de schéma Planificateur de tâches](task-scheduler-schema-elements.md)
</dt> <dt>

[Planificateur de tâches](task-scheduler-start-page.md)
</dt> </dl>

 

 





