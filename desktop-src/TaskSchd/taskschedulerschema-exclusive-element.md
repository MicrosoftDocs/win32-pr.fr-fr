---
title: Élément exclusive
description: Indique si le planificateur de tâches doit démarrer la tâche pendant la maintenance automatique en mode exclusif.
ms.assetid: F690FD8F-BCCB-456D-92E3-25A262D6DCF1
keywords:
- Planificateur de tâches d’élément exclusif
topic_type:
- apiref
api_name:
- Exclusive
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: aab796abfdcad67a348b6d42186732d402bbe8eeeb359ac772588fe809dbf73c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119991329"
---
# <a name="exclusive-element"></a>Élément exclusive

Indique si le planificateur de tâches doit démarrer la tâche pendant la maintenance automatique en mode exclusif.

L’exclusivité est garantie uniquement entre les autres tâches de maintenance et n’accorde aucune priorité de classement de la tâche. Si l’exclusivité n’est pas spécifiée, la tâche est démarrée en parallèle avec d’autres tâches de maintenance.

``` syntax
<xs:element name="Exclusive"
    type="xsd:boolean"
    maxOccurs="1"
    minOccurs="0"
 />
```

L’élément **exclusive** est défini par le type complexe [**maintenanceSettingsType**](taskschedulerschema-maintenancesettingstype-complextype.md) .

## <a name="parent-element"></a>Élément parent



| Élément                                                                                                                          | Dérivé de                                                                               | Description                                                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [**MaintenanceSettings (maintenanceSettingsType)**](taskschedulerschema-maintenancesettings-maintenancesettingstype-element.md) | [**maintenanceSettingsType**](taskschedulerschema-maintenancesettingstype-complextype.md) | Spécifie les paramètres de tâche que le planificateur de tâches utilisera pour démarrer la tâche pendant la maintenance automatique.<br/> |



## <a name="remarks"></a>Remarques

Pour la programmation en C++, ce paramètre inactif est spécifié à l’aide de la propriété [**IMaintenanceSettings :: exclusive**](/windows/desktop/api/Taskschd/nf-taskschd-imaintenancesettings-get_exclusive) .

## <a name="examples"></a>Exemples

Le code XML suivant définit des tâches de maintenance avec des exigences d’échéance définies sur 15 jours.


```XML
<MaintenanceSettings>
    <Period>P5D</Period>
    <Deadline>P15D</Deadline>
    <Exclusive>true</Exclusive>
</MaintenanceSettings>
```



## <a name="requirements"></a>Configuration requise



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

 

 





