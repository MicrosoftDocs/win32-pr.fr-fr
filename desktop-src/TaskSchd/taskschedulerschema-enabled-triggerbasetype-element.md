---
title: Élément Enabled (triggerBaseType)
description: Spécifie que le déclencheur est activé.
ms.assetid: 14c98f40-0ec5-4dc1-978e-b02c08ee2384
keywords:
- Élément activé Planificateur de tâches
topic_type:
- apiref
api_name:
- Enabled
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 42b495ba1af5f3b9b99034b0d6ca9d02040460c4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104033253"
---
# <a name="enabled-triggerbasetype-element"></a>Élément Enabled (triggerBaseType)

Spécifie que le déclencheur est activé.

``` syntax
<xs:element name="Enabled"
    type="boolean"
 />
```

L’élément **activé** est défini par le type complexe [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) .

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



## <a name="remarks"></a>Notes

Pour le développement de script, ces informations sont accessibles par le biais de la propriété [**déclencheur. Enabled**](trigger-enabled.md) qui est héritée par tous les objets déclencheurs.

Pour le développement C++, ces informations sont accessibles via la propriété [**ITrigger :: Enabled**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_enabled) qui est héritée par les interfaces de déclencheur All.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Éléments de schéma Planificateur de tâches](task-scheduler-schema-elements.md)
</dt> <dt>

[Planificateur de tâches](task-scheduler-start-page.md)
</dt> </dl>

 

 





