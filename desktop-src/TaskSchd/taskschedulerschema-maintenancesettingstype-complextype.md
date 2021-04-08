---
title: Type complexe maintenanceSettingsType
description: Définit les éléments enfants et les informations de séquencement pour l’élément MaintenanceSettings.
ms.assetid: CA4C452E-CA25-4E2D-B5E2-ED64C59AB3AD
keywords:
- Planificateur de tâches de type complexe maintenanceSettingsType
topic_type:
- apiref
api_name:
- maintenanceSettingsType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7f261e84fe2af1239cce1bbd377e991ede6e8506
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742764"
---
# <a name="maintenancesettingstype-complex-type"></a>Type complexe maintenanceSettingsType

Définit les éléments enfants et les informations de séquencement pour l’élément [**MaintenanceSettings**](taskschedulerschema-maintenancesettings-maintenancesettingstype-element.md) .

``` syntax
<xs:complexType name="maintenanceSettingsType">
    <xs:all>
        <xs:element name="Period"
            minOccurs="1"
            maxOccurs="1"
        >
            <xs:simpleType>
                <xs:restriction
                    base="duration"
                >
                    <xs:minInclusive
                        value="P1D"
                     />
                </xs:restriction>
            </xs:simpleType>
        </xs:element>
        <xs:element name="Deadline"
            minOccurs="1"
            maxOccurs="1"
        >
            <xs:simpleType>
                <xs:restriction
                    base="duration"
                >
                    <xs:minInclusive
                        value="P1D"
                     />
                </xs:restriction>
            </xs:simpleType>
        </xs:element>
        <xs:element name="Exclusive"
            type="boolean"
            maxOccurs="1"
            minOccurs="1"
         />
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a>Éléments enfants



| Élément                                                                        | Type    | Description                                                                                                                                                                                    |
|--------------------------------------------------------------------------------|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Échéance**](taskschedulerschema-daysinterval-dailyscheduletype-element.md) |         | Spécifie la durée après laquelle le planificateur de tâches tente de démarrer la tâche pendant la maintenance automatique d’urgence, si elle n’a pas pu se terminer pendant une maintenance régulière.<br/> |
| **Exclusif**                                                                  | boolean | Si la valeur est true, la tâche est démarrée en mode exclusif parmi les autres tâches de maintenance.<br/>                                                                                                 |
| [**Heures**](taskschedulerschema-daysinterval-dailyscheduletype-element.md)   |         | Spécifie la fréquence à laquelle la tâche doit être démarrée pendant la maintenance automatique.<br/>                                                                                                      |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 8 uniquement\]<br/>           |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2012 \[ uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Types complexes de schéma Planificateur de tâches](task-scheduler-schema-complex-types.md)
</dt> <dt>

[Planificateur de tâches](task-scheduler-start-page.md)
</dt> </dl>

 

 





