---
title: Élément WakeToRun (settingsType)
description: Spécifie que Planificateur de tâches met l’ordinateur en éveil lorsqu’il est temps d’exécuter la tâche.
ms.assetid: 5fb53016-5778-463d-bb32-3c1da2de6fc2
keywords:
- Élément WakeToRun Planificateur de tâches
topic_type:
- apiref
api_name:
- WakeToRun
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 23eeaa06073fa9259c1a48137cf3676baa402d39
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106518115"
---
# <a name="waketorun-settingstype-element"></a>Élément WakeToRun (settingsType)

Spécifie que Planificateur de tâches met l’ordinateur en éveil lorsqu’il est temps d’exécuter la tâche.

``` syntax
<xs:element name="WakeToRun"
    type="boolean"
 />
```

L’élément **WakeToRun** est défini par le type complexe [**settingsType**](taskschedulerschema-settingstype-complextype.md) .

## <a name="parent-element"></a>Élément parent



| Élément                                                           | Dérivé de                                                         | Description                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**Paramètres**](taskschedulerschema-settings-tasktype-element.md) | [**settingsType**](taskschedulerschema-settingstype-complextype.md) | Contient les paramètres que le Planificateur de tâches utilise pour effectuer la tâche.<br/> |



## <a name="remarks"></a>Notes

Lorsque le service Planificateur de tâches sort de l’ordinateur pour exécuter une tâche, l’écran peut rester inactif même si l’ordinateur n’est plus en mode veille ou veille prolongée. L’écran s’active lorsque Windows Vista détecte qu’un utilisateur a retourné pour utiliser l’ordinateur.

Pour le développement C++, consultez la [**propriété WakeToRun de ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_waketorun).

Pour le développement de scripts, consultez [**TaskSettings. WakeToRun**](tasksettings-waketorun.md).

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

 

 





