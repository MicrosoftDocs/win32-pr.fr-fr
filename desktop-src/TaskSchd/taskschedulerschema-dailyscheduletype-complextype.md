---
title: Type complexe dailyScheduleType
description: Définit les éléments enfants et les informations de séquencement pour l’élément ScheduleByDay.
ms.assetid: e0b1b09f-d72a-4a85-9059-4a917bc0104a
keywords:
- Planificateur de tâches de type complexe dailyScheduleType
topic_type:
- apiref
api_name:
- dailyScheduleType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5982ab7e72a79dc909a4e91fafe363ca4703639d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127011045"
---
# <a name="dailyscheduletype-complex-type"></a>Type complexe dailyScheduleType

Définit les éléments enfants et les informations de séquencement pour l’élément [**ScheduleByDay**](taskschedulerschema-schedulebyday-calendartriggertype-element.md) .

``` syntax
<xs:complexType name="dailyScheduleType">
    <xs:all>
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
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a>Éléments enfants



| Élément                                                                            | Type | Description                                                          |
|------------------------------------------------------------------------------------|------|----------------------------------------------------------------------|
| [**DaysInterval**](taskschedulerschema-daysinterval-dailyscheduletype-element.md) |      | Spécifie l’intervalle entre les jours de la planification. <br/> |



## <a name="requirements"></a>Spécifications



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

 

 





