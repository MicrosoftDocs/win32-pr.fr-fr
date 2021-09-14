---
title: Élément MaintenanceSettings (maintenanceSettingsType)
description: Spécifie comment l’Planificateur de tâches effectue des tâches pendant la maintenance automatique.
ms.assetid: 6A204980-851D-4487-A6CC-01BE262A517A
keywords:
- Élément MaintenanceSettings Planificateur de tâches
topic_type:
- apiref
api_name:
- MaintenanceSettings
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ca68876d8742ea04faa972d2ea7fd5f4b2071ffc
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127228707"
---
# <a name="maintenancesettings-maintenancesettingstype-element"></a>Élément MaintenanceSettings (maintenanceSettingsType)

Spécifie comment l’Planificateur de tâches effectue des tâches pendant la maintenance automatique.

``` syntax
<xs:element name="MaintenanceSettings"
    type="maintenanceSettingsType"
    minOccurs="0"
 />
```

L’élément **MaintenanceSettings** est défini par le type complexe [**maintenanceSettingsType**](taskschedulerschema-maintenancesettingstype-complextype.md) .

## <a name="parent-element"></a>Élément parent



| Élément                                                           | Dérivé de                                                         | Description                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**Paramètres**](taskschedulerschema-settings-tasktype-element.md) | [**settingsType**](taskschedulerschema-settingstype-complextype.md) | Contient les paramètres que le Planificateur de tâches utilise pour effectuer la tâche.<br/> |



## <a name="child-elements"></a>Éléments enfants



| Élément                                                    | Type    | Description                                                                                                                                                                                     |
|------------------------------------------------------------|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Échéance**](taskschedulerschema-deadline-element.md)   |         | Spécifie la durée après laquelle le planificateur de tâches tente de démarrer la tâche pendant la maintenance automatique d’urgence, si elle n’a pas pu se terminer pendant une maintenance régulière. <br/> |
| [**Exclusif**](taskschedulerschema-exclusive-element.md) | boolean | Si la valeur est true, la tâche est démarrée en mode exclusif parmi les autres tâches de maintenance. <br/>                                                                                                 |
| [**Période**](taskschedulerschema-period-element.md)       |         | Spécifie la fréquence à laquelle la tâche doit être démarrée pendant la maintenance automatique. <br/>                                                                                                      |



## <a name="remarks"></a>Notes

Pour la programmation en C++, ce paramètre inactif est spécifié à l’aide de la propriété [**ITaskSettings3 :: MaintenanceSettings**](/windows/desktop/api/Taskschd/nf-taskschd-itasksettings3-get_maintenancesettings) .

## <a name="examples"></a>Exemples

Le code XML suivant définit un élément Settings qui indique à Planificateur de tâches d’exécuter la tâche une fois par période de 5 jours au cours d’une maintenance automatique normale et, en cas d’échec pendant 15 jours, de démarrer la tâche pendant la maintenance automatique d’urgence.


```XML
<Settings>
    <MaintenanceSettings>
        <Period>P5D</Period>
        <Deadline>P15D</Deadline>
    </MaintenanceSettings>       
</Settings>
```



## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8 \[ applications de bureau uniquement\]<br/>           |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[ applications de bureau uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Éléments de schéma Planificateur de tâches](task-scheduler-schema-elements.md)
</dt> <dt>

[Planificateur de tâches](task-scheduler-start-page.md)
</dt> </dl>

 

 





