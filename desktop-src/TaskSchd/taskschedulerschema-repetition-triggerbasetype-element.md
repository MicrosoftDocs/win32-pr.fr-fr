---
title: Élément de répétition (triggerBaseType)
description: Spécifie la fréquence d’exécution de la tâche et la durée de répétition du modèle de répétition après le démarrage de la tâche.
ms.assetid: d43c7f9a-3a7b-44a9-901b-9ad18c027b1b
keywords:
- Planificateur de tâches d’élément à répétition
topic_type:
- apiref
api_name:
- Repetition
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: dfcce3e008a9959ca279f64c83a898eb2239d007d8fc32dfb5da5942395055bd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119959539"
---
# <a name="repetition-triggerbasetype-element"></a>Élément de répétition (triggerBaseType)

Spécifie la fréquence d’exécution de la tâche et la durée de répétition du modèle de répétition après le démarrage de la tâche.

``` syntax
<xs:element name="Repetition"
    type="repetitionType"
 />
```

L’élément à **répétition** est défini par le type complexe [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) .

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



## <a name="child-elements"></a>Éléments enfants



| Élément                                                                                   | Type     | Description                                                                                                         |
|-------------------------------------------------------------------------------------------|----------|---------------------------------------------------------------------------------------------------------------------|
| [**Macauley**](taskschedulerschema-duration-repetitiontype-element.md)                   | duration | Spécifie la durée de répétition du modèle.<br/>                                                              |
| [**Intervalle**](taskschedulerschema-interval-repetitiontype-element.md)                   | duration | Spécifie la durée entre chaque redémarrage de la tâche.<br/>                                           |
| [**StopAtDurationEnd**](taskschedulerschema-stopatdurationend-repetitiontype-element.md) | boolean  | Spécifie qu’une instance en cours d’exécution de la tâche est arrêtée à la fin de la durée du modèle de répétition.<br/> |



## <a name="remarks"></a>Remarques

Si vous spécifiez une durée de répétition pour une tâche, vous devez également spécifier l’intervalle de répétition.

Si vous enregistrez une tâche qui contient un déclencheur avec un intervalle de répétition égal à une minute et une durée de répétition égale à quatre minutes, la tâche est lancée cinq fois. Les cinq répétitions peuvent être définies par le modèle suivant.

1.  Une tâche commence au début de la première minute.
2.  La tâche suivante démarre à la fin de la première minute.
3.  La tâche suivante démarre à la fin de la seconde minute.
4.  La tâche suivante démarre à la fin de la troisième minute.
5.  La tâche suivante démarre à la fin de la quatrième minute.

**Windows Server 2003, Windows XP et Windows 2000 :** Si vous enregistrez une tâche qui contient un déclencheur avec un intervalle de répétition égal à une minute et une durée de répétition égale à quatre minutes, la tâche est lancée quatre fois.

**Windows Vista, Windows 7, Windows Server 2008, Windows 8 et Windows Server 2012 :** En règle générale, la définition de la durée de répétition sur un multiple exact de l’intervalle produit les nombres décrits ci-dessus. Toutefois, dans certaines conditions de charge élevée, il est possible que le délai d’expiration soit écoulé avant que TaskScheduler puisse lancer l’intervalle de tâche final.

Pour le développement de scripts, le modèle de répétition est spécifié à l’aide de la propriété [**déclencheur.**](trigger-repetition.md) reformation qui est héritée par tous les objets déclencheurs.

Pour le développement C++, le modèle de répétition est spécifié à l’aide de la propriété [**ITRigger :: rerépétition**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_repetition) qui est héritée par toutes les interfaces de déclencheur.

## <a name="examples"></a>Exemples

Le code XML suivant définit un élément de déclencheur de démarrage qui spécifie un modèle de répétition pour un déclencheur.


```XML
<BootTrigger>
    <StartBoundary>2005-01-01T08:00:00</StartBoundary>
    <EndBounadry>2007-01-01T08:00:00</EndBoundary>
    <Enabled>true</Enabled>
    <Repetition>
        <Interval></Interval>
        <Duration></Duration>
        <StopAtDurationEnd>true</StopAtDirationEnd>
    </Repetition>
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

 

 





