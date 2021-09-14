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
ms.openlocfilehash: 8a8d93bcabd0e121c44f4a7212d11491624a08d0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126857338"
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



## <a name="remarks"></a>Notes

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



## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Éléments de schéma Planificateur de tâches](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





