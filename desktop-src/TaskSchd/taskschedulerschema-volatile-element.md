---
title: Volatile (élément)
description: indique si la tâche est automatiquement désactivée à chaque démarrage de Windows.
ms.assetid: E0298876-2A96-401D-B857-69758AF980E5
keywords:
- Planificateur de tâches d’élément volatile
topic_type:
- apiref
api_name:
- Volatile
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 496e95fe98ecb2890d19bde0b99e171ab20b045a47bf69840dd78f501bfbc309
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119872099"
---
# <a name="volatile-element"></a>Volatile (élément)

indique si la tâche est automatiquement désactivée à chaque démarrage de Windows.

``` syntax
<xs:element name="Volatile"
    type="xsd:boolean"
    maxOccurs="1"
    minOccurs="0"
    default="false"
 />
```

L’élément **volatile** est défini par le type complexe [**settingsType**](taskschedulerschema-settingstype-complextype.md) .

## <a name="parent-element"></a>Élément parent



| Élément                                                           | Dérivé de | Description                                                                        |
|-------------------------------------------------------------------|--------------|------------------------------------------------------------------------------------|
| [**Paramètres**](taskschedulerschema-settings-tasktype-element.md) |              | Contient les paramètres que le Planificateur de tâches utilise pour effectuer la tâche.<br/> |



## <a name="remarks"></a>Remarques

Pour la programmation en C++, ce paramètre inactif est spécifié à l’aide de la propriété [**ITaskSettings3 :: volatile**](/windows/desktop/api/Taskschd/nf-taskschd-itasksettings3-get_volatile) .

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

 

 





