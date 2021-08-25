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
ms.openlocfilehash: 12d16f9f06685a427a8f3e7c4f2356dff0bc6415e50379ba752a4bc3a3fec8e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119872059"
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



## <a name="remarks"></a>Remarques

Lorsque le service Planificateur de tâches sort de l’ordinateur pour exécuter une tâche, l’écran peut rester inactif même si l’ordinateur n’est plus en mode veille ou veille prolongée. l’écran s’active quand Windows Vista détecte qu’un utilisateur est revenu à utiliser l’ordinateur.

Pour le développement C++, consultez la [**propriété WakeToRun de ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_waketorun).

Pour le développement de scripts, consultez [**TaskSettings. WakeToRun**](tasksettings-waketorun.md).

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

 

 





