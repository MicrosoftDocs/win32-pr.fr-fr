---
title: Type complexe daysOfMonthType
description: Définit l’élément enfant et les informations de séquencement pour l’élément DaysOfMonth (monthlyScheduleType).
ms.assetid: 8258c090-c836-497e-8e5b-db4782277822
keywords:
- Planificateur de tâches de type complexe daysOfMonthType
topic_type:
- apiref
api_name:
- daysOfMonthType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a32f2d0b3084e5146e53370d1771018a5d27a025f5ea419a61d8c39804d5611a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120010849"
---
# <a name="daysofmonthtype-complex-type"></a>Type complexe daysOfMonthType

Définit l’élément enfant et les informations de séquencement pour l’élément [**DaysOfMonth (monthlyScheduleType)**](taskschedulerschema-daysofmonth-monthlyscheduletype-element.md) .

``` syntax
<xs:complexType name="daysOfMonthType">
    <xs:sequence>
        <xs:element name="Day"
            type="dayOfMonthType"
            minOccurs="0"
            maxOccurs="32"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a>Éléments enfants



| Élément                                                        | Type                                                                    | Description                                                          |
|----------------------------------------------------------------|-------------------------------------------------------------------------|----------------------------------------------------------------------|
| [**Jour**](taskschedulerschema-day-daysofmonthtype-element.md) | [**dayOfMonthType**](taskschedulerschema-dayofmonthtype-simpletype.md) | Spécifie un jour du mois pendant lequel la tâche s’exécute. <br/> |



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

 

 





