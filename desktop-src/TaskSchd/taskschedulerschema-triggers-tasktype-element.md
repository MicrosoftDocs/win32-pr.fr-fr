---
title: Élément Triggers (taskType)
description: Spécifie les déclencheurs qui démarrent la tâche.
ms.assetid: 4bf8e85e-3742-433d-821f-736fb2ff7139
keywords:
- Déclenche l’élément Planificateur de tâches
topic_type:
- apiref
api_name:
- Triggers
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d067c9e315006c55e07e972e5616525750d8a383d7ed8294f7d39a6acf32caff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118610883"
---
# <a name="triggers-tasktype-element"></a>Élément Triggers (taskType)

Spécifie les déclencheurs qui démarrent la tâche.

``` syntax
<xs:element name="Triggers"
    type="triggersType"
 />
```

L’élément **triggers** est défini par le type complexe [**triggersType**](taskschedulerschema-triggerstype-complextype.md) .

## <a name="parent-element"></a>Élément parent



| Élément                                          | Dérivé de                                                 | Description                                                                  |
|--------------------------------------------------|--------------------------------------------------------------|------------------------------------------------------------------------------|
| [**Tâche**](taskschedulerschema-task-element.md) | [**taskType**](taskschedulerschema-tasktype-complextype.md) | Définit la tâche qui est effectuée par le service Planificateur de tâches.<br/> |



## <a name="child-elements"></a>Éléments enfants



| Élément                                                                                     | Type                                                                                       | Description                                                                                  |
|---------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [**BootTrigger**](taskschedulerschema-boottrigger-triggergroup-element.md)                 | [**bootTriggerType**](taskschedulerschema-boottriggertype-complextype.md)                 | Spécifie un déclencheur qui démarre une tâche au démarrage du système.<br/>                 |
| [**CalendarTrigger**](taskschedulerschema-calendartrigger-triggergroup-element.md)         | [**calendarTriggerType**](taskschedulerschema-calendartriggertype-complextype.md)         | Spécifie un déclencheur quotidien, hebdomadaire, mensuel ou un jour de la semaine (DOW) mensuel.<br/>   |
| [**EventTrigger**](taskschedulerschema-eventtrigger-triggergroup-element.md)               | [**eventTriggerType**](taskschedulerschema-eventtriggertype-complextype.md)               | Spécifie un déclencheur qui démarre une tâche lorsqu’un événement système se produit.<br/>                |
| [**IdleTrigger**](taskschedulerschema-idletrigger-triggergroup-element.md)                 | [**idleTriggerType**](taskschedulerschema-idletriggertype-complextype.md)                 | Spécifie un déclencheur qui démarre une tâche lorsque l’ordinateur passe en état d’inactivité.<br/> |
| [**LogonTrigger**](taskschedulerschema-logontrigger-triggergroup-element.md)               | [**logonTriggerType**](taskschedulerschema-logontriggertype-complextype.md)               | Spécifie un déclencheur qui démarre une tâche lorsqu’un utilisateur ouvre une session.<br/>                       |
| [**RegistrationTrigger**](taskschedulerschema-registrationtrigger-triggergroup-element.md) | [**registrationTriggerType**](taskschedulerschema-registrationtriggertype-complextype.md) | Spécifie un déclencheur qui démarre une tâche lorsque la tâche est inscrite.<br/>               |
| [**TimeTrigger**](taskschedulerschema-timetrigger-triggergroup-element.md)                 | [**timeTriggerType**](taskschedulerschema-timetriggertype-complextype.md)                 | Spécifie un déclencheur qui démarre une tâche lorsque le déclencheur est activé.<br/>             |



## <a name="remarks"></a>Remarques

Les éléments enfants listés ci-dessus peuvent être ajoutés dans n’importe quel ordre.

Pour le développement C++, les déclencheurs d’une tâche sont spécifiés à l’aide [**de la propriété triggers de ITaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_triggers).

Pour le développement de scripts, les déclencheurs d’une tâche sont spécifiés à l’aide de la propriété [**TaskDefinition. Triggers**](taskdefinition-triggers.md) .

## <a name="examples"></a>Exemples

Pour obtenir un exemple complet du code XML d’une tâche qui spécifie un déclencheur, consultez [exemple de déclencheur temporel (XML)](time-trigger-example--xml-.md).

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

 

 





