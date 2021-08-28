---
title: Élément DisallowStartIfOnBatteries (settingsType)
description: Spécifie que la tâche ne sera pas démarrée si l’ordinateur fonctionne sur batterie.
ms.assetid: 48c0fd32-4441-4628-8090-c736f2945b4d
keywords:
- Élément DisallowStartIfOnBatteries Planificateur de tâches
topic_type:
- apiref
api_name:
- DisallowStartIfOnBatteries
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: efd78b3e868c41431521b4c584a4044b9086362cf55d86466eb38ed75fcee148
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120100039"
---
# <a name="disallowstartifonbatteries-settingstype-element"></a>Élément DisallowStartIfOnBatteries (settingsType)

Spécifie que la tâche ne sera pas démarrée si l’ordinateur fonctionne sur batterie.

``` syntax
<xs:element name="DisallowStartIfOnBatteries"
    type="boolean"
 />
```

L’élément **DisallowStartIfOnBatteries** est défini par le type complexe [**settingsType**](taskschedulerschema-settingstype-complextype.md) .

## <a name="parent-element"></a>Élément parent



| Élément                                                           | Dérivé de                                                         | Description                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**Paramètres**](taskschedulerschema-settings-tasktype-element.md) | [**settingsType**](taskschedulerschema-settingstype-complextype.md) | Contient les paramètres que le Planificateur de tâches utilise pour effectuer la tâche.<br/> |



## <a name="remarks"></a>Remarques

Le paramètre par défaut de cet élément est true.

Pour le développement de script, ces informations sont accessibles via la propriété [**TaskSettings. DisallowStartIfOnBatteries**](tasksettings-disallowstartifonbatteries.md) .

Pour le développement C++, ces informations sont accessibles par le biais de la propriété [**ITaskSettings ::D isallowstartifonbatteries**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_disallowstartifonbatteries) .

## <a name="examples"></a>Exemples

Le code XML suivant définit un élément Settings qui ne permet pas à la tâche de s’exécuter si l’ordinateur s’exécute sur des batteries.


```XML
<Settings>
    <DisallowStartIfOnBatteries>true</DisallowStartIfOnBatteries>
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

 

 





