---
title: Groupe triggerGroup
description: Définit le groupe de déclencheurs.
ms.assetid: e07e6999-d982-405b-adfd-2976707b999f
keywords:
- triggerGroup Planificateur de tâches
topic_type:
- apiref
api_name:
- triggerGroup
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ce0203cd9515808891f93223dd7b3ebaf2642103
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126920248"
---
# <a name="triggergroup-group"></a>Groupe triggerGroup

Définit le groupe de déclencheurs.

``` syntax
<xs:group name="triggerGroup">
    <xs:choice>
        <xs:element name="BootTrigger"
            type="bootTriggerType"
            minOccurs="0"
         />
        <xs:element name="RegistrationTrigger"
            type="registrationTriggerType"
            minOccurs="0"
         />
        <xs:element name="IdleTrigger"
            type="idleTriggerType"
            minOccurs="0"
         />
        <xs:element name="TimeTrigger"
            type="timeTriggerType"
            minOccurs="0"
         />
        <xs:element name="EventTrigger"
            type="eventTriggerType"
            minOccurs="0"
         />
        <xs:element name="LogonTrigger"
            type="logonTriggerType"
            minOccurs="0"
         />
        <xs:element name="SessionStateChangeTrigger"
            type="sessionStateChangeTriggerType"
            minOccurs="0"
         />
        <xs:element name="CalendarTrigger"
            type="calendarTriggerType"
            minOccurs="0"
         />
    </xs:choice>
</xs:group>
```

## <a name="child-elements"></a>Éléments enfants



| Élément                                                                                                 | Type                                                                                                   | Description                                                                                                       |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| [**BootTrigger**](taskschedulerschema-boottrigger-triggergroup-element.md)                             | [**bootTriggerType**](taskschedulerschema-boottriggertype-complextype.md)                             | Déclencheur qui démarre une tâche lors du démarrage du système.<br/>                                                |
| [**CalendarTrigger**](taskschedulerschema-calendartrigger-triggergroup-element.md)                     | [**calendarTriggerType**](taskschedulerschema-calendartriggertype-complextype.md)                     | Déclencheur qui démarre une tâche en fonction d’une planification quotidienne, hebdomadaire, mensuelle ou mensuelle (DOW).<br/> |
| [**EventTrigger**](taskschedulerschema-eventtrigger-triggergroup-element.md)                           | [**eventTriggerType**](taskschedulerschema-eventtriggertype-complextype.md)                           | Déclencheur qui démarre une tâche lorsqu’un événement système se produit.<br/>                                               |
| [**IdleTrigger**](taskschedulerschema-idletrigger-triggergroup-element.md)                             | [**idleTriggerType**](taskschedulerschema-idletriggertype-complextype.md)                             | Déclencheur qui démarre une tâche lorsque l’ordinateur passe en état d’inactivité.<br/>                                |
| [**LogonTrigger**](taskschedulerschema-logontrigger-triggergroup-element.md)                           | [**logonTriggerType**](taskschedulerschema-logontriggertype-complextype.md)                           | Déclencheur qui démarre une tâche lorsqu’un utilisateur ouvre une session.<br/>                                                      |
| [**RegistrationTrigger**](taskschedulerschema-registrationtrigger-triggergroup-element.md)             | [**registrationTriggerType**](taskschedulerschema-registrationtriggertype-complextype.md)             | Déclencheur qui démarre une tâche lorsque la tâche est inscrite.<br/>                                              |
| [**SessionStateChangeTrigger**](taskschedulerschema-sessionstatechangetrigger-triggergroup-element.md) | [**sessionStateChangeTriggerType**](taskschedulerschema-sessionstatechangetriggertype-complextype.md) | Déclencheur qui démarre une tâche quand une session de Terminal Server change d’État.<br/>                             |
| [**TimeTrigger**](taskschedulerschema-timetrigger-triggergroup-element.md)                             | [**timeTriggerType**](taskschedulerschema-timetriggertype-complextype.md)                             | Déclencheur qui démarre une tâche lorsque le déclencheur est activé.<br/>                                            |



## <a name="remarks"></a>Notes

Lors de la lecture ou de l’écriture de code XML, les éléments définis par ce groupe sont les éléments enfants de l’élément [**triggers**](taskschedulerschema-triggers-tasktype-element.md) .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Planificateur de tâches](task-scheduler-start-page.md)
</dt> </dl>

 

 





