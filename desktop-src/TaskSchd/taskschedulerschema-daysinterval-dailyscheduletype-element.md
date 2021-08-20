---
title: Élément DaysInterval (dailyScheduleType)
description: Spécifie l’intervalle entre les jours de la planification.
ms.assetid: 495ea1c0-37eb-4b12-8241-bfc6489e33ed
keywords:
- Élément DaysInterval Planificateur de tâches
topic_type:
- apiref
api_name:
- DaysInterval
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e35df4f102801f7d52faeb384f9a1113e00abbf034026d19b5b7b6e7b4c90ed7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119621099"
---
# <a name="daysinterval-dailyscheduletype-element"></a>Élément DaysInterval (dailyScheduleType)

Spécifie l’intervalle entre les jours de la planification.

``` syntax
<xs:element name="DaysInterval"
    minOccurs="0"
>
    <xs:simpleType>
        <xs:restriction
            base="unsignedInt"
        >
            <xs:minInclusive
                value="1"
             />
            <xs:maxInclusive
                value="365"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

L’élément est défini par le type complexe [**dailyScheduleType**](taskschedulerschema-dailyscheduletype-complextype.md) .

## <a name="parent-element"></a>Élément parent



| Élément                                                                                | Dérivé de                                                                   | Description                            |
|----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|----------------------------------------|
| [**ScheduleByDay**](taskschedulerschema-schedulebyday-calendartriggertype-element.md) | [**dailyScheduleType**](taskschedulerschema-dailyscheduletype-complextype.md) | Spécifie une planification quotidienne.<br/> |



## <a name="remarks"></a>Remarques

Pour le développement de script, l’intervalle de jours pour un déclencheur quotidien est spécifié par la propriété [**DailyTrigger. DaysInterval**](dailytrigger-daysinterval.md) .

Pour le développement C++, l’intervalle de jours pour un déclencheur quotidien est spécifié par la propriété [**IDailyTrigger ::D aysinterval**](/windows/desktop/api/taskschd/nf-taskschd-idailytrigger-get_daysinterval) .

## <a name="examples"></a>Exemples

Le code XML suivant définit un déclencheur de calendrier quotidien qui démarre la tâche tous les jours.


```XML
<CalendarTrigger>
    <StartBoundary>2005-01-01T00:00:00</StartBoundary>
    <EndBounadry>2007-01-01T00:00:00</EndBoundary>
    <ScheduleByDay>
        <DaysInterval>1</DaysInterval>
    </ScheduleByDay>
</CalendarTrigger>
```



Pour obtenir un exemple complet du code XML d’une tâche qui spécifie une planification quotidienne, consultez [exemple de déclencheur quotidien (XML)](daily-trigger-example--xml-.md).

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

 

 





