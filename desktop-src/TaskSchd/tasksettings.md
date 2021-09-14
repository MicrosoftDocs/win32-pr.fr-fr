---
title: Objet TaskSettings
description: Objet de script qui fournit les paramètres utilisés par le service de Planificateur de tâches pour effectuer la tâche.
ms.assetid: f2ba952b-7864-467d-8709-eb6995dd5df5
keywords:
- Objet TaskSettings Planificateur de tâches
- Planificateur de tâches d’objets TaskSettings, Description
topic_type:
- apiref
api_name:
- TaskSettings
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e7690ba59b4794f952ca3b381fc28247f0dfb4e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127008657"
---
# <a name="tasksettings-object"></a>Objet TaskSettings

Objet de script qui fournit les paramètres utilisés par le service de Planificateur de tâches pour effectuer la tâche.

## <a name="members"></a>Membres

L’objet **TaskSettings** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

L’objet **TaskSettings** a ces propriétés.



| Propriété                                                                                 | Type d’accès           | Description                                                                                                                                                                                                                                                                                                                                                                                                                  |
|:-----------------------------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AllowDemandStart**](tasksettings-allowdemandstart.md)<br/>                     | Lecture/écriture<br/> | Obtient ou définit une valeur booléenne qui indique que la tâche peut être démarrée à l’aide de la commande exécuter ou du menu contextuel.<br/>                                                                                                                                                                                                                                                                                     |
| [**AllowHardTerminate**](tasksettings-allowhardterminate.md)<br/>                 | Lecture/écriture<br/> | Obtient ou définit une valeur booléenne qui indique que la tâche peut être terminée à l’aide de [**TerminateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-terminateprocess).<br/>                                                                                                                                                                                                                                                                               |
| [**Compatibilité**](tasksettings-compatibility.md)<br/>                           | Lecture/écriture<br/> | Obtient ou définit une valeur entière qui indique quelle version de Planificateur de tâches une tâche est compatible.<br/>                                                                                                                                                                                                                                                                                                           |
| [**DeleteExpiredTaskAfter**](tasksettings-deleteexpiredtaskafter.md)<br/>         | Lecture/écriture<br/> | Obtient ou définit la durée d’attente de la Planificateur de tâches avant la suppression de la tâche après son expiration.<br/>                                                                                                                                                                                                                                                                                                      |
| [**DisallowStartIfOnBatteries**](tasksettings-disallowstartifonbatteries.md)<br/> | Lecture/écriture<br/> | Obtient ou définit une valeur booléenne qui indique que la tâche ne sera pas démarrée si l’ordinateur fonctionne sur batterie.<br/>                                                                                                                                                                                                                                                                                        |
| [**Activé**](tasksettings-enabled.md)<br/>                                       | Lecture/écriture<br/> | Obtient ou définit une valeur booléenne qui indique que la tâche est activée. La tâche ne peut être exécutée que lorsque ce paramètre a la valeur true.<br/>                                                                                                                                                                                                                                                                                   |
| [**ExecutionTimeLimit**](tasksettings-executiontimelimit.md)<br/>                 | Lecture/écriture<br/> | Obtient ou définit la durée autorisée pour terminer la tâche.<br/>                                                                                                                                                                                                                                                                                                                                                     |
| [**Hidden**](tasksettings-hidden.md)<br/>                                         | Lecture/écriture<br/> | Obtient ou définit une valeur booléenne qui indique que la tâche ne sera pas visible dans l’interface utilisateur. Toutefois, les administrateurs peuvent remplacer ce paramètre à l’aide d’un « commutateur maître » qui rend toutes les tâches visibles dans l’interface utilisateur.<br/>                                                                                                                                                                                           |
| [**IdleSettings**](tasksettings-idlesettings.md)<br/>                             | Lecture/écriture<br/> | Obtient ou définit les informations qui spécifient la façon dont le Planificateur de tâches exécute des tâches lorsque l’ordinateur est dans un état d’inactivité.<br/>                                                                                                                                                                                                                                                                                          |
| [**MultipleInstances**](tasksettings-multipleinstances.md)<br/>                   | Lecture/écriture<br/> | Obtient ou définit la stratégie qui définit la façon dont le Planificateur de tâches gère plusieurs instances de la tâche.<br/>                                                                                                                                                                                                                                                                                                            |
| [**NetworkSettings**](tasksettings-networksettings.md)<br/>                       | Lecture/écriture<br/> | Obtient ou définit l’objet paramètres réseau qui contient un identificateur et un nom de profil réseau. Si la propriété [**RunOnlyIfNetworkAvailable**](tasksettings-runonlyifnetworkavailable.md) de **TaskSettings** a la **valeur true** et qu’un propfile réseau est spécifié dans la propriété [**NetworkSettings**](tasksettings-networksettings.md) , la tâche s’exécute uniquement si le profil réseau spécifié est disponible.<br/> |
| [**Priorité**](tasksettings-priority.md)<br/>                                     | Lecture/écriture<br/> | Obtient ou définit le niveau de priorité de la tâche.<br/>                                                                                                                                                                                                                                                                                                                                                                      |
| [**RestartCount**](tasksettings-restartcount.md)<br/>                             | Lecture/écriture<br/> | Obtient ou définit le nombre de tentatives de redémarrage de la tâche par le Planificateur de tâches.<br/>                                                                                                                                                                                                                                                                                                                        |
| [**RestartInterval**](tasksettings-restartinterval.md)<br/>                       | Lecture/écriture<br/> | Obtient ou définit une valeur qui spécifie la durée pendant laquelle l’Planificateur de tâches tente de redémarrer la tâche.<br/>                                                                                                                                                                                                                                                                                                                 |
| [**RunOnlyIfIdle**](tasksettings-runonlyifidle.md)<br/>                           | Lecture/écriture<br/> | Obtient ou définit une valeur booléenne qui indique que le Planificateur de tâches exécutera la tâche uniquement si l’ordinateur est dans un état inactif.<br/>                                                                                                                                                                                                                                                                                   |
| [**RunOnlyIfNetworkAvailable**](tasksettings-runonlyifnetworkavailable.md)<br/>   | Lecture/écriture<br/> | Obtient ou définit une valeur booléenne qui indique que le Planificateur de tâches exécutera la tâche uniquement lorsqu’un réseau est disponible.<br/>                                                                                                                                                                                                                                                                                           |
| [**StartWhenAvailable**](tasksettings-startwhenavailable.md)<br/>                 | Lecture/écriture<br/> | Obtient ou définit une valeur booléenne qui indique que la Planificateur de tâches peut démarrer la tâche à tout moment une fois l’heure planifiée passée.<br/>                                                                                                                                                                                                                                                                           |
| [**StopIfGoingOnBatteries**](tasksettings-stopifgoingonbatteries.md)<br/>         | Lecture/écriture<br/> | Obtient ou définit une valeur booléenne qui indique que la tâche sera arrêtée si l’ordinateur commence à fonctionner sur batterie.<br/>                                                                                                                                                                                                                                                                                         |
| [**WakeToRun**](tasksettings-waketorun.md)<br/>                                   | Lecture/écriture<br/> | Obtient ou définit une valeur booléenne qui indique que le Planificateur de tâches met l’ordinateur en éveil lorsqu’il est temps d’exécuter la tâche.<br/>                                                                                                                                                                                                                                                                                       |
| [**XmlText**](tasksettings-xmltext.md)<br/>                                       | Lecture/écriture<br/> | Obtient ou définit une définition XML des paramètres de tâche.<br/>                                                                                                                                                                                                                                                                                                                                                    |



 

## <a name="remarks"></a>Notes

Par défaut, une tâche sera arrêtée 72 heures après son démarrage. Vous pouvez modifier ce paramètre en modifiant le paramètre [**ExecutionTimeLimit**](tasksettings-executiontimelimit.md) .

lors de la lecture ou de l’écriture de données XML pour une tâche, les paramètres de tâche sont définis dans l’élément [**Paramètres**](taskschedulerschema-settings-tasktype-element.md) du schéma Planificateur de tâches.

## <a name="examples"></a>Exemples

Pour plus d’informations et pour obtenir un exemple de code pour cet objet de script, consultez [exemple de déclenchement temporel (script)](time-trigger-example--scripting-.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                          |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                    |
| Bibliothèque de types<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Planificateur de tâches](task-scheduler-start-page.md)
</dt> <dt>

[**TaskDefinition**](taskdefinition.md)
</dt> <dt>

[**NetworkSettings**](networksettings.md)
</dt> <dt>

[**IdleSettings**](idlesettings.md)
</dt> </dl>

 

