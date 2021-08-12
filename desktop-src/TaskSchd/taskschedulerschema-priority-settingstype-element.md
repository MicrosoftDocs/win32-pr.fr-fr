---
title: Élément Priority (settingsType)
description: Spécifie le niveau de priorité de la tâche.
ms.assetid: 4885fffa-b7d9-4f5e-b6e8-6f18b01c2427
keywords:
- Élément Priority Planificateur de tâches
topic_type:
- apiref
api_name:
- Priority
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 11b71c88f63e7a3beb3c1c9ec8e1f3253bcd05a567ec5cd077f62175561ce2c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118611891"
---
# <a name="priority-settingstype-element"></a>Élément Priority (settingsType)

Spécifie le niveau de priorité de la tâche.

``` syntax
<xs:element name="Priority"
    type="priorityType"
    default="7"
    minOccurs="0"
 />
```

L’élément **Priority** est défini par le type complexe [**settingsType**](taskschedulerschema-settingstype-complextype.md) .

## <a name="parent-element"></a>Élément parent



| Élément                                                           | Dérivé de                                                         | Description                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**Paramètres**](taskschedulerschema-settings-tasktype-element.md) | [**settingsType**](taskschedulerschema-settingstype-complextype.md) | Contient les paramètres que le Planificateur de tâches utilise pour effectuer la tâche.<br/> |



## <a name="remarks"></a>Remarques

Le niveau de priorité 0 est la priorité la plus élevée et le niveau de priorité 10 est la priorité la plus basse. La valeur par défaut est 7. Les valeurs minimales et maximales sont définies par le type simple [**priorityType**](taskschedulerschema-prioritytype-simpletype.md) . Les niveaux de priorité 7 et 8 sont utilisés pour les tâches en arrière-plan, et les niveaux de priorité 4, 5 et 6 sont utilisés pour les tâches interactives.

L’action de la tâche est démarrée dans un processus avec une priorité basée sur une valeur de classe de priorité. Une valeur de niveau de priorité (priorité de thread) est utilisée pour les actions de la tâche du gestionnaire COM, de la boîte de message et de l’e-mail. Pour plus d’informations sur la classe de priorité et les valeurs de niveau de priorité, consultez [planification des priorités](/windows/desktop/ProcThread/scheduling-priorities). Le tableau suivant répertorie les valeurs possibles pour l’élément **Priority** , ainsi que la classe de priorité correspondante et les valeurs de niveau de priorité.



| Priorité de la tâche | Classe de priorité                 | Niveau de priorité                   |
|---------------|--------------------------------|----------------------------------|
| 0             | \_classe de priorité en temps réel \_      | temps de priorité des THREADs \_ \_ \_ critique |
| 1             | \_classe de priorité élevée \_          | priorité de THREAD la \_ \_ plus élevée        |
| 2             | classe de priorité supérieure à la \_ normale \_ \_ | priorité de THREAD supérieure à la \_ \_ \_ normale  |
| 3             | classe de priorité supérieure à la \_ normale \_ \_ | priorité de THREAD supérieure à la \_ \_ \_ normale  |
| 4             | \_classe de priorité normale \_        | priorité de THREAD \_ \_ normale         |
| 5             | \_classe de priorité normale \_        | priorité de THREAD \_ \_ normale         |
| 6             | \_classe de priorité normale \_        | priorité de THREAD \_ \_ normale         |
| 7             | classe de priorité inférieure à la \_ normale \_ \_ | priorité de THREAD inférieure à la \_ \_ \_ normale  |
| 8             | classe de priorité inférieure à la \_ normale \_ \_ | priorité de THREAD inférieure à la \_ \_ \_ normale  |
| 9             | \_classe de priorité Idle \_          | priorité de THREAD la \_ \_ plus basse         |
| 10            | \_classe de priorité Idle \_          | priorité de THREAD \_ \_ inactive           |



 

Pour le développement C++, consultez la [**propriété Priority de ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_priority).

Pour le développement de scripts, consultez [**TaskSettings. Priority**](tasksettings-priority.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Éléments de schéma Planificateur de tâches](task-scheduler-schema-elements.md)
</dt> </dl>

 

