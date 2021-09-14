---
title: Type complexe daysOfWeekType
description: Définit les éléments enfants et les informations de séquencement pour les éléments DaysOfWeek (weeklyScheduleType) et DaysOfWeek (monthlyDayOfWeekScheduleType).
ms.assetid: b3315582-af7a-4d4c-8f6f-61de12a85f46
keywords:
- Planificateur de tâches de type complexe daysOfWeekType
topic_type:
- apiref
api_name:
- daysOfWeekType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0b4a1b5e6aeaa77c0bdfe12b1d5b68fde018f236
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127013420"
---
# <a name="daysofweektype-complex-type"></a>Type complexe daysOfWeekType

Définit les éléments enfants et les informations de séquencement pour les éléments [**DaysOfWeek (weeklyScheduleType)**](taskschedulerschema-daysofweek-weeklyscheduletype-element.md) et [**DaysOfWeek (monthlyDayOfWeekScheduleType)**](taskschedulerschema-daysofweek-monthlydayofweekscheduletype-element.md) .

``` syntax
<xs:complexType name="daysOfWeekType">
    <xs:all>
        <xs:element name="Monday"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="Tuesday"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="Wednesday"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="Thursday"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="Friday"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="Saturday"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="Sunday"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a>Éléments enfants



| Élément                                                                   | Type | Description                         |
|---------------------------------------------------------------------------|------|-------------------------------------|
| [**Vendredi**](taskschedulerschema-friday-daysofweektype-element.md)       | N/A  | La tâche est exécutée le vendredi. <br/>    |
| [**Lundi**](taskschedulerschema-monday-daysofweektype-element.md)       | N/A  | La tâche est exécutée le lundi.<br/>     |
| [**Samedi**](taskschedulerschema-saturday-daysofweektype-element.md)   | N/A  | La tâche est exécutée le samedi. <br/>  |
| [**Dimanche**](taskschedulerschema-sunday-daysofweektype-element.md)       | N/A  | La tâche est exécutée le dimanche. <br/>    |
| [**Thursday**](taskschedulerschema-thursday-daysofweektype-element.md)   | N/A  | Tâche exécutée le jeudi <br/>   |
| [**Mardi**](taskschedulerschema-tuesday-daysofweektype-element.md)     | N/A  | La tâche est exécutée le mardi. <br/>   |
| [**Mercredi**](taskschedulerschema-wednesday-daysofweektype-element.md) | N/A  | La tâche est exécutée le mercredi. <br/> |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Types complexes de schéma Planificateur de tâches](task-scheduler-schema-complex-types.md)
</dt> <dt>

[Planificateur de tâches](task-scheduler-start-page.md)
</dt> </dl>

 

 





