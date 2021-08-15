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
ms.openlocfilehash: a3680ba3c29dc0d258a48aa16ae7923e3761eda30f198384fecfbf238e2933cb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119991029"
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



## <a name="remarks"></a>Remarques

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
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Éléments de schéma Planificateur de tâches](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





