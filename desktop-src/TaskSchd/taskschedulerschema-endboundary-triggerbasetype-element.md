---
title: Élément EndBoundary (triggerBaseType)
description: Spécifie la date et l’heure de désactivation du déclencheur. Le déclencheur ne peut pas démarrer la tâche une fois qu’elle est désactivée.
ms.assetid: 84731c0b-3fb8-44dd-be1a-67547add1f9e
keywords:
- Élément EndBoundary Planificateur de tâches
topic_type:
- apiref
api_name:
- EndBoundary
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8e26eb05b7b9fa15c0667fff7fd0d1eb85e61ed2daa90d6a238cbf9575f6c0e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120010739"
---
# <a name="endboundary-triggerbasetype-element"></a>Élément EndBoundary (triggerBaseType)

Spécifie la date et l’heure de désactivation du déclencheur. Le déclencheur ne peut pas démarrer la tâche une fois qu’elle est désactivée.

``` syntax
<xs:element name="EndBoundary"
    type="dateTime"
 />
```

L’élément **EndBoundary** est défini par le type complexe [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) .

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

Pour le développement de script, la limite de fin est spécifiée à l’aide de la propriété [**Trigger. EndBoundary**](trigger-endboundary.md) qui est héritée par tous les objets déclencheurs.

Pour le développement C++, la limite de fin est spécifiée à l’aide de la propriété [**ITrigger :: EndBoundary**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_endboundary) qui est héritée par les interfaces de déclencheur All.

## <a name="examples"></a>Exemples

Le code XML suivant définit un élément de déclencheur de démarrage qui définit une limite de fin du 1er janvier 2007:8:00 AM.


```XML
<BootTrigger>
    <StartBoundary>2005-01-01T08:00:00</StartBoundary>
    <EndBounadry>2007-01-01T08:00:00</EndBoundary>
    <Enabled>true</Enabled>
    <Repetition></Repetition>
    <ExecutionTimeLimit></ExecutionTimeLimit>
    <Delay><Delay>
 </BootTrigger>
```



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

 

 





