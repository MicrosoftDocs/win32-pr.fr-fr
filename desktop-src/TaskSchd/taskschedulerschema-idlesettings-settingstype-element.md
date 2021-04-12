---
title: Élément IdleSettings (settingsType)
description: Spécifie comment l’Planificateur de tâches effectue des tâches lorsque l’ordinateur est dans un état d’inactivité.
ms.assetid: 23d57417-95a9-42e3-904c-7f0859fcda7c
keywords:
- Élément IdleSettings Planificateur de tâches
topic_type:
- apiref
api_name:
- IdleSettings
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5ae8b7953f31d7e9c6f01387d3136f01d8ab697a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105220"
---
# <a name="idlesettings-settingstype-element"></a>Élément IdleSettings (settingsType)

Spécifie comment l’Planificateur de tâches effectue des tâches lorsque l’ordinateur est dans un état d’inactivité. Pour plus d’informations sur les conditions d’inactivité, consultez conditions d’inactivité de la [tâche](task-idle-conditions.md).

``` syntax
<xs:element name="IdleSettings"
    type="idleSettingsType"
    minOccurs="0"
 />
```

L’élément **IdleSettings** est défini par le type complexe [**settingsType**](taskschedulerschema-settingstype-complextype.md) .

## <a name="parent-element"></a>Élément parent

| Élément                                                           | Dérivé de                                                         | Description                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**Paramètres**](taskschedulerschema-settings-tasktype-element.md) | [**settingsType**](taskschedulerschema-settingstype-complextype.md) | Contient les paramètres que le Planificateur de tâches utilise pour effectuer la tâche.<br/> |

## <a name="child-elements"></a>Éléments enfants

> [!NOTE]
> Les paramètres *Duration* et *WaitTimeout* sont déconseillés. Elles sont toujours présentes dans l’interface utilisateur Planificateur de tâches et leurs méthodes d’interface peuvent toujours retourner des valeurs valides, mais elles ne sont plus utilisées.

| Élément                                                                                  | Type     | Description                                                                                                              |
|------------------------------------------------------------------------------------------|----------|--------------------------------------------------------------------------------------------------------------------------|
| [**RestartOnIdle**](taskschedulerschema-restartonidle-idlesettingstype-element.md)      | boolean  | Spécifie si la tâche est redémarrée lorsque l’ordinateur entre dans une condition d’inactivité plusieurs fois.<br/>       |
| [**StopOnIdleEnd**](taskschedulerschema-terminateonidleend-idlesettingstype-element.md) | boolean  | Spécifie que l’Planificateur de tâches arrêtera la tâche si la condition d’inactivité se termine avant la fin de la tâche.<br/> |
| **Déconseillé**: [ **durée**](taskschedulerschema-duration-idlesettingstype-element.md)                | duration | Spécifie la durée pendant laquelle l’ordinateur doit être dans un état inactif avant que la tâche ne soit exécutée.<br/>                              |
| **Déconseillé**: [ **WaitTimeout**](taskschedulerschema-waittimeout-idlesettingstype-element.md)          | duration | Spécifie la durée pendant laquelle le Planificateur de tâches attendra qu’une condition d’inactivité se produise.<br/>                |

## <a name="remarks"></a>Notes

Pour le développement de scripts, les paramètres inactifs sont spécifiés à l’aide de la propriété [**TaskSettings. IdleSettings**](tasksettings-idlesettings.md) .

Pour le développement C++, les paramètres inactifs sont spécifiés à l’aide de la propriété [**ITaskSettings :: IdleSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_idlesettings) .

## <a name="examples"></a>Exemples

Le code XML suivant définit un élément Settings qui permet à Planificateur de tâches d’attendre 24 heures pour une condition d’inactivité, puis autorise uniquement 10 minutes {IdleDuration) à lancer la tâche.

```XML
<Settings>
    <IdleSettings>
        <StopOnIdleEnd>false</StopOnIdleEnd>
        <RestartOnIdle>false</RestartOnIdle> 
        <!-- WaitTimeout and Duration have been deprecated -->
        <Duration>PT5M</Duration>
        <WaitTimeout>PT24H</WaitTimeout>
    </IdleSettings>       
</Settings>
```

## <a name="requirements"></a>Configuration requise

| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/> |

## <a name="see-also"></a>Voir aussi

[Éléments de schéma Planificateur de tâches](task-scheduler-schema-elements.md)

[Planificateur de tâches](task-scheduler-start-page.md)
