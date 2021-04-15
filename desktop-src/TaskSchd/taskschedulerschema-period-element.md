---
title: Élément period
description: Spécifie la fréquence à laquelle la tâche doit être démarrée pendant la maintenance automatique.
ms.assetid: E4BE2466-3119-41F8-8238-4627C28B26E5
keywords:
- Point, élément Planificateur de tâches
topic_type:
- apiref
api_name:
- Period
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7a507a9b0a8f97d1ae4e6c8df654a45d67b77767
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466983"
---
# <a name="period-element"></a>Élément period

Spécifie la fréquence à laquelle la tâche doit être démarrée pendant la maintenance automatique.

Le format de cette chaîne est *PnYnMnDTnHnMnS*, où *NY* est le nombre d’années, nm est le nombre de mois, *ND* est le nombre de jours, *T* est le séparateur de date/heure, *NH* est le nombre d’heures, *nm* est le nombre de minutes et *NS* est le nombre de secondes (par exemple, « PT5M » spécifie 5 minutes et « P1M4DT2H5M » indique un mois, quatre jours, deux heures et cinq minutes). La valeur minimale est d’une minute. Pour plus d’informations sur le type de durée, consultez [XML Schema Part 2 : Datatypes Second Edition](https://www.w3.org/TR/xmlschema-2/#duration).

``` syntax
<xs:element name="Period"
    maxOccurs="1"
    minOccurs="1"
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
```

L’élément **period** est défini par le type complexe [**maintenanceSettingsType**](taskschedulerschema-maintenancesettingstype-complextype.md) .

## <a name="parent-element"></a>Élément parent



| Élément                                                                                                                          | Dérivé de                                                                               | Description                                                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [**MaintenanceSettings (maintenanceSettingsType)**](taskschedulerschema-maintenancesettings-maintenancesettingstype-element.md) | [**maintenanceSettingsType**](taskschedulerschema-maintenancesettingstype-complextype.md) | Spécifie les paramètres de tâche que le planificateur de tâches utilisera pour démarrer la tâche pendant la maintenance automatique.<br/> |



## <a name="remarks"></a>Notes

Pour la programmation en C++, ce paramètre inactif est spécifié à l’aide de la propriété [**IMaintenanceSettings ::P eriod**](/windows/desktop/api/Taskschd/nf-taskschd-imaintenancesettings-get_period) .

## <a name="examples"></a>Exemples

Le code XML suivant définit la tâche de maintenance avec une exigence de périodicité définie sur 5 jours.


```XML
<MaintenanceSettings>
    <Period>P5D</Period>
</MaintenanceSettings>
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 8 uniquement\]<br/>           |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2012 \[ uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Éléments de schéma Planificateur de tâches](task-scheduler-schema-elements.md)
</dt> <dt>

[Planificateur de tâches](task-scheduler-start-page.md)
</dt> </dl>

 

 





