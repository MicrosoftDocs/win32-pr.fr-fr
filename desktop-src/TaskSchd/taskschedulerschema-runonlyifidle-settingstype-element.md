---
title: Élément RunOnlyIfIdle (settingsType)
description: Spécifie que la tâche est exécutée uniquement lorsque l’ordinateur est dans un état d’inactivité.
ms.assetid: 2ef3dd19-4d5c-4399-89b8-d737be4ef85e
keywords:
- Élément RunOnlyIfIdle Planificateur de tâches
topic_type:
- apiref
api_name:
- RunOnlyIfIdle
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a623ac6b6ede3f3920ae792bdfb87b7678bdb3047d7bff44f373371fd4cd5c41
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120099919"
---
# <a name="runonlyifidle-settingstype-element"></a>Élément RunOnlyIfIdle (settingsType)

Spécifie que la tâche est exécutée uniquement lorsque l’ordinateur est dans un état d’inactivité.

``` syntax
<xs:element name="RunOnlyIfIdle"
    type="boolean"
 />
```

L’élément **RunOnlyIfIdle** est défini par le type complexe [**settingsType**](taskschedulerschema-settingstype-complextype.md) .

## <a name="parent-element"></a>Élément parent



| Élément                                                           | Dérivé de                                                         | Description                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**Paramètres**](taskschedulerschema-settings-tasktype-element.md) | [**settingsType**](taskschedulerschema-settingstype-complextype.md) | Contient les paramètres que le Planificateur de tâches utilise pour effectuer la tâche.<br/> |



## <a name="remarks"></a>Remarques

Pour le développement C++, consultez la [**propriété RunOnlyIfIdle de ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_runonlyifidle).

Pour le développement de scripts, consultez [**TaskSettings. RunOnlyIfIdle**](tasksettings-runonlyifidle.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Éléments de schéma Planificateur de tâches](task-scheduler-schema-elements.md)
</dt> <dt>

[Planificateur de tâches](task-scheduler-start-page.md)
</dt> </dl>

 

 





