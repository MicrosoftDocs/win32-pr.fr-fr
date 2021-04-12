---
title: Objet IdleSettings
description: Objet de script qui spécifie la façon dont le Planificateur de tâches exécute des tâches lorsque l’ordinateur est dans une condition d’inactivité.
ms.assetid: d303596a-0a84-4056-9f7a-5a9512852002
keywords:
- Objet IdleSettings Planificateur de tâches
- Planificateur de tâches d’objets IdleSettings, Description
topic_type:
- apiref
api_name:
- IdleSettings
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 819ff226386f30483de96fac6213b35d7dd51a52
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384367"
---
# <a name="idlesettings-object"></a>Objet IdleSettings

Objet de script qui spécifie la façon dont le Planificateur de tâches exécute des tâches lorsque l’ordinateur est dans une condition d’inactivité. Pour plus d’informations sur les conditions d’inactivité, consultez conditions d’inactivité de la [tâche](task-idle-conditions.md).

## <a name="members"></a>Membres

L’objet **IdleSettings** possède les types de membres suivants :

- [Propriétés](#properties)

### <a name="properties"></a>Propriétés

L’objet **IdleSettings** a ces propriétés.

> [!NOTE]
> Les paramètres *IdleDuration* et *WaitTimeout* sont déconseillés. Elles sont toujours présentes dans l’interface utilisateur Planificateur de tâches et leurs méthodes d’interface peuvent toujours retourner des valeurs valides, mais elles ne sont plus utilisées.

| Propriété                                                       | Type d’accès           | Description                                                                                                                                                     |
|:---------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**RestartOnIdle**](idlesettings-restartonidle.md)<br/> | Lecture/écriture<br/> | Obtient ou définit une valeur booléenne qui indique si la tâche est redémarrée lorsque l’ordinateur entre dans une condition d’inactivité plusieurs fois.<br/>            |
| [**StopOnIdleEnd**](idlesettings-stoponidleend.md)<br/> | Lecture/écriture<br/> | Obtient ou définit une valeur booléenne qui indique que le Planificateur de tâches met fin à la tâche si la condition d’inactivité se termine avant la fin de la tâche.<br/> |
| **Déconseillé**: [ **IdleDuration**](idlesettings-idleduration.md)<br/>   | Lecture/écriture<br/> | Obtient ou définit une valeur qui indique la durée pendant laquelle l’ordinateur doit être dans un état inactif avant que la tâche soit exécutée.<br/>                            |
| **Déconseillé**: [ **WaitTimeout**](idlesettings-waittimeout.md)<br/>     | Lecture/écriture<br/> | Obtient ou définit une valeur qui indique la durée pendant laquelle le Planificateur de tâches attendra qu’une condition d’inactivité se produise.<br/>                             |

## <a name="remarks"></a>Notes

Lors de la lecture ou de l’écriture de données XML pour une tâche, ce paramètre est spécifié dans l’élément [**IdleSettings**](taskschedulerschema-idlesettings-settingstype-element.md) du schéma planificateur de tâches.

Si une tâche est déclenchée par un déclencheur inactif, la propriété [**IdleSettings. WaitTimeout**](idlesettings-waittimeout.md) est ignorée.

> [!NOTE]
> *IdleSettings. IdleDuration* et *IdleSettings. WaitTimeout* sont déconseillés.

## <a name="requirements"></a>Configuration requise

| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                          |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                    |
| Bibliothèque de types<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |

## <a name="see-also"></a>Voir aussi

[Objets Planificateur de tâches](task-scheduler-objects.md)

[Planificateur de tâches](task-scheduler-start-page.md)
