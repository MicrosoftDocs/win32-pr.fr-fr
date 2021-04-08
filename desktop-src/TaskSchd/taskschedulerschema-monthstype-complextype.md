---
title: Type complexe monthsType
description: Définit les éléments enfants et les informations de séquencement pour les éléments months (monthlyDayOfWeekScheduleType) et months (monthlyScheduleType).
ms.assetid: f1faa67a-2f5f-4a00-a1df-2d44e218278b
keywords:
- Planificateur de tâches de type complexe monthsType
topic_type:
- apiref
api_name:
- monthsType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e6a19000073fd12e05aa915921850264979a0541
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740437"
---
# <a name="monthstype-complex-type"></a>Type complexe monthsType

Définit les éléments enfants et les informations de séquencement pour les éléments [**months (monthlyDayOfWeekScheduleType)**](taskschedulerschema-months-monthlydayofweekscheduletype-element.md) et [**months (monthlyScheduleType)**](taskschedulerschema-months-monthlyscheduletype-element.md) .

``` syntax
<xs:complexType name="monthsType">
    <xs:all>
        <xs:element name="January"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="February"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="March"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="April"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="May"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="June"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="July"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="August"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="September"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="October"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="November"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="December"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a>Éléments enfants



| Élément                                                               | Type | Description                                            |
|-----------------------------------------------------------------------|------|--------------------------------------------------------|
| [**Avril**](taskschedulerschema-april-monthstype-element.md)         | N/A  | Spécifie que la tâche s’exécute en avril. <br/>     |
| [**Août**](taskschedulerschema-august-monthstype-element.md)       | N/A  | Spécifie que la tâche s’exécute en août. <br/>    |
| [**Décembre**](taskschedulerschema-december-monthstype-element.md)   | N/A  | Spécifie que la tâche s’exécute en décembre. <br/>  |
| [**February**](taskschedulerschema-february-monthstype-element.md)   | N/A  | Spécifie que la tâche s’exécute en février. <br/>  |
| [**Janvier**](taskschedulerschema-january-monthstype-element.md)     | N/A  | Spécifie que la tâche s’exécute en janvier. <br/>   |
| [**Juillet**](taskschedulerschema-july-monthstype-element.md)           | N/A  | Spécifie que la tâche s’exécute en juillet. <br/>      |
| [**June**](taskschedulerschema-june-monthstype-element.md)           | N/A  | Spécifie que la tâche s’exécute en juin. <br/>      |
| [**Mars**](taskschedulerschema-march-monthstype-element.md)         | N/A  | Spécifie que la tâche s’exécute en mars. <br/>     |
| [**Mai**](taskschedulerschema-may-monthstype-element.md)             | N/A  | Spécifie que la tâche s’exécute en mai. <br/>       |
| [**Novembre**](taskschedulerschema-november-monthstype-element.md)   | N/A  | Spécifie que la tâche s’exécute en novembre. <br/>  |
| [**Octobre**](taskschedulerschema-october-monthstype-element.md)     | N/A  | Spécifie que la tâche s’exécute en octobre. <br/>   |
| [**Septembre**](taskschedulerschema-september-monthstype-element.md) | N/A  | Spécifie que la tâche s’exécute en septembre. <br/> |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Types complexes de schéma Planificateur de tâches](task-scheduler-schema-complex-types.md)
</dt> <dt>

[Planificateur de tâches](task-scheduler-start-page.md)
</dt> </dl>

 

 





