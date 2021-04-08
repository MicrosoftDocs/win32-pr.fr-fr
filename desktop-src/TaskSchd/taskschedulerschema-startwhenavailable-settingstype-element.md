---
title: Élément StartWhenAvailable (settingsType)
description: Spécifie que les Planificateur de tâches peuvent démarrer la tâche à tout moment une fois l’heure planifiée passée.
ms.assetid: 1d65fd51-3a94-4083-8e38-2a652383656a
keywords:
- Élément StartWhenAvailable Planificateur de tâches
topic_type:
- apiref
api_name:
- StartWhenAvailable
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d86f6f6e75457d08e10ef40d728eaf3e3b00aa7d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941822"
---
# <a name="startwhenavailable-settingstype-element"></a>Élément StartWhenAvailable (settingsType)

Spécifie que les Planificateur de tâches peuvent démarrer la tâche à tout moment une fois l’heure planifiée passée.

``` syntax
<xs:element name="StartWhenAvailable"
    type="boolean"
    default="false"
    minOccurs="0"
 />
```

L’élément **StartWhenAvailable** est défini par le type complexe [**settingsType**](taskschedulerschema-settingstype-complextype.md) .

## <a name="parent-element"></a>Élément parent



| Élément                                                           | Dérivé de                                                         | Description                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**Paramètres**](taskschedulerschema-settings-tasktype-element.md) | [**settingsType**](taskschedulerschema-settingstype-complextype.md) | Contient les paramètres que le Planificateur de tâches utilise pour effectuer la tâche.<br/> |



## <a name="remarks"></a>Notes

Cette propriété s’applique uniquement aux tâches chronométrées.

Pour le développement C++, consultez la [**propriété StartWhenAvailable de ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_startwhenavailable).

Pour le développement de scripts, consultez [**TaskSettings. StartWhenAvailable**](tasksettings-startwhenavailable.md).

## <a name="examples"></a>Exemples

Le code XML suivant définit un élément Settings qui permet au Planificateur de tâches de démarrer la tâche lorsqu’elle est disponible.


```XML
<Settings>
    <StartWhenAvailable>true</StartWhenAvailable>
</Settings>
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Éléments de schéma Planificateur de tâches](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





