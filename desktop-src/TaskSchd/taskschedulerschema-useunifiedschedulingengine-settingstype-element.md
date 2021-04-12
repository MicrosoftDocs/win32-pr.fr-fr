---
title: Élément UseUnifiedSchedulingEngine (settingsType)
description: Spécifie que le moteur de planification unifiée sera utilisé pour exécuter cette tâche.
ms.assetid: 93436f14-1caf-4ec8-bf74-a198b7dcb27c
keywords:
- Élément UseUnifiedSchedulingEngine Planificateur de tâches
topic_type:
- apiref
api_name:
- UseUnifiedSchedulingEngine
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a00798a46df3dfbb351dd8705b264192c38daff6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032644"
---
# <a name="useunifiedschedulingengine-settingstype-element"></a>Élément UseUnifiedSchedulingEngine (settingsType)

Spécifie que le moteur de planification unifiée sera utilisé pour exécuter cette tâche.

``` syntax
<xs:element name="UseUnifiedSchedulingEngine"
    type="boolean"
    default="false"
    minOccurs="0"
 />
```

L’élément **UseUnifiedSchedulingEngine** est défini par le type complexe [**settingsType**](taskschedulerschema-settingstype-complextype.md) .

## <a name="parent-element"></a>Élément parent



| Élément                                                           | Dérivé de                                                         | Description                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**Paramètres**](taskschedulerschema-settings-tasktype-element.md) | [**settingsType**](taskschedulerschema-settingstype-complextype.md) | Contient les paramètres que le Planificateur de tâches utilise pour effectuer la tâche.<br/> |



## <a name="remarks"></a>Notes

La valeur par défaut de cet élément est false.

Pour le développement C++, ces informations sont accessibles par le biais de la propriété [**ITaskSettings2 :: UseUnifiedSchedulingEngine**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings2-get_useunifiedschedulingengine) .

## <a name="examples"></a>Exemples

Le code XML suivant définit un élément Settings qui spécifie que le moteur de planification unifié sera utilisé pour exécuter cette tâche.


```XML
<Settings>
    <UseUnifiedSchedulingEngine>true</UseUnifiedSchedulingEngine>
</Settings>
        
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 7 uniquement\]<br/>              |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 R2 \[ uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Éléments de schéma Planificateur de tâches](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





