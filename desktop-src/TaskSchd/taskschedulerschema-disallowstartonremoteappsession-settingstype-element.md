---
title: Élément DisallowStartOnRemoteAppSession (settingsType)
description: Spécifie que la tâche ne sera pas démarrée si elle est déclenchée pour s’exécuter dans une session à distance intégrée à des applications locales (RAIL).
ms.assetid: 8323d8d9-fb6a-4876-9967-cc2344c77de3
keywords:
- Élément DisallowStartOnRemoteAppSession Planificateur de tâches
topic_type:
- apiref
api_name:
- DisallowStartOnRemoteAppSession
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d2f7834ecd57fa10aaaabfa21945f1e908834d535d50f94b4dd21e6ca45c0a62
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120010799"
---
# <a name="disallowstartonremoteappsession-settingstype-element"></a>Élément DisallowStartOnRemoteAppSession (settingsType)

Spécifie que la tâche ne sera pas démarrée si elle est déclenchée pour s’exécuter dans une session à distance intégrée à des applications locales (RAIL).

``` syntax
<xs:element name="DisallowStartOnRemoteAppSession"
    type="boolean"
    default="false"
    minOccurs="0"
 />
```

L’élément **DisallowStartOnRemoteAppSession** est défini par le type complexe [**settingsType**](taskschedulerschema-settingstype-complextype.md) .

## <a name="parent-element"></a>Élément parent



| Élément                                                           | Dérivé de                                                         | Description                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**Paramètres**](taskschedulerschema-settings-tasktype-element.md) | [**settingsType**](taskschedulerschema-settingstype-complextype.md) | Contient les paramètres que le Planificateur de tâches utilise pour effectuer la tâche.<br/> |



## <a name="remarks"></a>Remarques

La valeur par défaut de cet élément est false.

Pour le développement C++, ces informations sont accessibles par le biais de la propriété [**ITaskSettings2 ::D isallowstartonremoteappsession**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings2-get_disallowstartonremoteappsession) .

## <a name="examples"></a>Exemples

Le code XML suivant définit un élément Settings qui n’autorise pas la tâche à démarrer si la tâche est déclenchée pour s’exécuter dans une session de RAIL.


```XML
<Settings>
    <DisallowStartOnRemoteAppSession>true</DisallowStartOnRemoteAppSession>
</Settings>
        
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 uniquement\]<br/>              |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 R2, \[ applications de bureau uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Éléments de schéma Planificateur de tâches](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





