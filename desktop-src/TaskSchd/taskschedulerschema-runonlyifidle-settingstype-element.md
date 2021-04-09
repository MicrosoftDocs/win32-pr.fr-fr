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
ms.openlocfilehash: 3c57663d763926d68e5a552ebaf66edff2172e7e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104033121"
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



## <a name="remarks"></a>Notes

Pour le développement C++, consultez la [**propriété RunOnlyIfIdle de ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_runonlyifidle).

Pour le développement de scripts, consultez [**TaskSettings. RunOnlyIfIdle**](tasksettings-runonlyifidle.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Éléments de schéma Planificateur de tâches](task-scheduler-schema-elements.md)
</dt> <dt>

[Planificateur de tâches](task-scheduler-start-page.md)
</dt> </dl>

 

 





