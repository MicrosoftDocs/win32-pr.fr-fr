---
title: Élément échéance
description: Spécifie quand le planificateur de tâches doit démarrer la tâche pendant la maintenance automatique d’urgence, s’il n’a pas pu se terminer au cours d’une maintenance automatique normale.
ms.assetid: 34E33FAE-888E-4E82-83B8-059FB4A64B52
keywords:
- Élément échéance Planificateur de tâches
topic_type:
- apiref
api_name:
- Deadline
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3e12524971e8b713d4d17817a8a7c7602017bd68
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740829"
---
# <a name="deadline-element"></a>Élément échéance

Spécifie quand le planificateur de tâches doit démarrer la tâche pendant la maintenance automatique d’urgence, s’il n’a pas pu se terminer au cours d’une maintenance automatique normale.

Le format de cette chaîne est *PnYnMnDTnHnMnS*, où *NY* est le nombre d’années, nm est le nombre de mois, *ND* est le nombre de jours, *T* est le séparateur de date/heure, *NH* est le nombre d’heures, *nm* est le nombre de minutes et *NS* est le nombre de secondes (par exemple, « PT5M » spécifie 5 minutes et « P1M4DT2H5M » indique un mois, quatre jours, deux heures et cinq minutes). La valeur minimale est d’une minute. Pour plus d’informations sur le type de durée, consultez [XML Schema Part 2 : Datatypes Second Edition](https://www.w3.org/TR/xmlschema-2/#duration). L’échéance minimale qu’une tâche peut utiliser est de 1 jour. La valeur de l’élément **échéance** doit être supérieure à la valeur de l’élément [**period**](taskschedulerschema-period-element.md) . Si l’échéance n’est pas spécifiée, la tâche ne sera pas démarrée pendant la maintenance automatique d’urgence.

``` syntax
<xs:element name="Deadline"
    maxOccurs="1"
    minOccurs="0"
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

L’élément **échéance** est défini par le type complexe [**maintenanceSettingsType**](taskschedulerschema-maintenancesettingstype-complextype.md) .

## <a name="parent-element"></a>Élément parent



| Élément                                                                                                                          | Dérivé de                                                                               | Description                                                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [**MaintenanceSettings (maintenanceSettingsType)**](taskschedulerschema-maintenancesettings-maintenancesettingstype-element.md) | [**maintenanceSettingsType**](taskschedulerschema-maintenancesettingstype-complextype.md) | Spécifie les paramètres de tâche que le planificateur de tâches utilisera pour démarrer la tâche pendant la maintenance automatique.<br/> |



## <a name="remarks"></a>Notes

Pour la programmation en C++, ce paramètre inactif est spécifié à l’aide de la propriété [**IMaintenanceSettings ::D échéanc**](/windows/desktop/api/Taskschd/nf-taskschd-imaintenancesettings-get_deadline) .

## <a name="examples"></a>Exemples

Le code XML suivant définit un calendrier de mois qui exécute la tâche en mars.


```XML
<MaintenanceSettings>
    <Period>P5D</Period>
    <Deadline>P15D</Deadline>
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

 

 





