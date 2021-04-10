---
title: Élément RunOnlyIfNetworkAvailable (settingsType)
description: Spécifie que le Planificateur de tâches exécutera la tâche uniquement lorsqu’un réseau est disponible.
ms.assetid: b7b804d3-b31a-4d70-9ba5-805a285e278e
keywords:
- Élément RunOnlyIfNetworkAvailable Planificateur de tâches
topic_type:
- apiref
api_name:
- RunOnlyIfNetworkAvailable
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7ff1e7c838c142e30b75eb4abb935c0de352d9f7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942619"
---
# <a name="runonlyifnetworkavailable-settingstype-element"></a>Élément RunOnlyIfNetworkAvailable (settingsType)

Spécifie que le Planificateur de tâches exécutera la tâche uniquement lorsqu’un réseau est disponible.

``` syntax
<xs:element name="RunOnlyIfNetworkAvailable"
    type="boolean"
    default="false"
    minOccurs="0"
 />
```

L’élément **RunOnlyIfNetworkAvailable** est défini par le type complexe [**settingsType**](taskschedulerschema-settingstype-complextype.md) .

## <a name="parent-element"></a>Élément parent



| Élément                                                           | Dérivé de                                                         | Description                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**Paramètres**](taskschedulerschema-settings-tasktype-element.md) | [**settingsType**](taskschedulerschema-settingstype-complextype.md) | Contient les paramètres que le Planificateur de tâches utilise pour effectuer la tâche.<br/> |



## <a name="remarks"></a>Notes

Pour le développement C++, consultez la [**propriété RunOnlyIfNetworkAvailable de ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_runonlyifnetworkavailable).

Pour le développement de scripts, consultez [**TaskSettings. RunOnlyIfNetworkAvailable**](tasksettings-runonlyifnetworkavailable.md).

## <a name="examples"></a>Exemples

Le code XML suivant définit un élément Settings qui permet à la tâche de démarrer uniquement si un réseau est disponible.


```XML
<Settings>
    <RunOnlyIfNetworkAvailable>true</RunOnlyIfNetworkAvailable>
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

 

 





