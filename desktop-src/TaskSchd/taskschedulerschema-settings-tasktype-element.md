---
title: élément Paramètres (taskType)
description: Spécifie les paramètres utilisés par le Planificateur de tâches pour effectuer la tâche.
ms.assetid: 72d2929a-0dd2-44cd-be7b-72eca23a5e14
keywords:
- élément Paramètres Planificateur de tâches
topic_type:
- apiref
api_name:
- Settings
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ea754aa883f9c80c4a436357cc159c588bde375aaa66a229b358723b74b9e070
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119002237"
---
# <a name="settings-tasktype-element"></a>élément Paramètres (taskType)

Spécifie les paramètres utilisés par le Planificateur de tâches pour effectuer la tâche.

``` syntax
<xs:element name="Settings"
    type="settingsType"
    minOccurs="0"
 />
```

l’élément **Paramètres** est défini par le type complexe [**taskType**](taskschedulerschema-tasktype-complextype.md) .

## <a name="parent-element"></a>Élément parent



| Élément                                          | Dérivé de                                                 | Description                                                                    |
|--------------------------------------------------|--------------------------------------------------------------|--------------------------------------------------------------------------------|
| [**Tâche**](taskschedulerschema-task-element.md) | [**taskType**](taskschedulerschema-tasktype-complextype.md) | Spécifie la tâche qui est effectuée par le service Planificateur de tâches.<br/> |



## <a name="child-elements"></a>Éléments enfants



| Élément                                                                                                          | Type                                                                                              | Description                                                                                                          |
|------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [**AllowHardTerminate**](taskschedulerschema-allowhardterminate-settingstype-element.md)                        | boolean                                                                                           | Spécifie que la tâche peut être terminée à l’aide de TerminateProcess.<br/>                                         |
| [**AllowStartOnDemand**](taskschedulerschema-allowstartondemand-settingstype-element.md)                        | boolean                                                                                           | Spécifie que la tâche peut être démarrée à l’aide de la commande exécuter ou du menu contextuel.<br/>                  |
| [**DeleteExpiredTaskAfter**](taskschedulerschema-deleteexpiredtaskafter-settingstype-element.md)                | duration                                                                                          | Spécifie la durée d’attente de la Planificateur de tâches avant la suppression de la tâche après son expiration.<br/> |
| [**DisallowStartIfOnBatteries**](taskschedulerschema-disallowstartifonbatteries-settingstype-element.md)        | boolean                                                                                           | Spécifie que la tâche ne sera pas démarrée si l’ordinateur fonctionne sur batterie.<br/>                      |
| [**Activé**](taskschedulerschema-enabled-settingstype-element.md)                                              | boolean                                                                                           | Spécifie que la tâche est activée. La tâche ne peut être exécutée que lorsque ce paramètre a la valeur true.<br/>             |
| [**ExecutionTimeLimit**](taskschedulerschema-executiontimelimit-settingstype-element.md)                        | duration                                                                                          | Durée d’exécution de la tâche.<br/>                                                              |
| [**Masquer**](taskschedulerschema-hidden-settingstype-element.md)                                                | boolean                                                                                           | Spécifie que la tâche ne sera pas visible dans l’interface utilisateur par défaut.<br/>                                         |
| [**IdleSettings**](taskschedulerschema-idlesettings-settingstype-element.md)                                    | [**idleSettingsType**](taskschedulerschema-idlesettingstype-complextype.md)                      | Spécifie comment l’Planificateur de tâches effectue des tâches lorsque l’ordinateur est dans un état d’inactivité.<br/>                    |
| [**MaintenanceSettings**](taskschedulerschema-maintenancesettings-maintenancesettingstype-element.md)           | [**maintenanceSettingsType**](taskschedulerschema-maintenancesettingstype-complextype.md)        | Spécifie comment l’Planificateur de tâches effectue des tâches pendant la maintenance automatique.<br/>                             |
| [**MultipleInstancesPolicy**](taskschedulerschema-multipleinstancespolicy-settingstype-element.md)              | [**multipleInstancesPolicyType**](taskschedulerschema-multipleinstancespolicytype-simpletype.md) | Spécifie la stratégie qui définit la façon dont le Planificateur de tâches gère plusieurs instances de la tâche.<br/>       |
| [**Priorité**](taskschedulerschema-priority-settingstype-element.md)                                            | [**priorityType**](taskschedulerschema-prioritytype-simpletype.md)                               | Spécifie le niveau de priorité de la tâche.<br/>                                                                |
| [**RestartOnFailure**](taskschedulerschema-restartonfailure-settingstype-element.md)                            | [**restartType**](taskschedulerschema-restarttype-complextype.md)                                | Spécifie que l’Planificateur de tâches tentera de redémarrer la tâche si elle échoue pour une raison quelconque.<br/>      |
| [**RunOnlyIfIdle**](taskschedulerschema-runonlyifidle-settingstype-element.md)                                  | boolean                                                                                           | Spécifie que la tâche est exécutée uniquement lorsque l’ordinateur est dans un état d’inactivité.<br/>                                |
| [**RunOnlyIfNetworkAvailable**](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md)          | boolean                                                                                           | Spécifie que le Planificateur de tâches exécutera la tâche uniquement lorsqu’un réseau est disponible.<br/>                     |
| [**StartWhenAvailable**](taskschedulerschema-startwhenavailable-settingstype-element.md)                        | boolean                                                                                           | Spécifie que les Planificateur de tâches peuvent démarrer la tâche à tout moment une fois l’heure planifiée passée.<br/>     |
| [**StopIfGoingOnBatteries (settingsType)**](taskschedulerschema-stopifgoingonbatteries-settingstype-element.md) | boolean                                                                                           | Spécifie que la tâche sera arrêtée si l’ordinateur va sur des batteries.<br/>                          |
| [**Volatile**](taskschedulerschema-volatile-element.md)                                                         | boolean                                                                                           | spécifie si la tâche est automatiquement désactivée par Planificateur de tâches au démarrage de Windows.<br/>                     |
| [**WakeToRun (settingsType)**](taskschedulerschema-waketorun-settingstype-element.md)                           | boolean                                                                                           | Spécifie que Planificateur de tâches met l’ordinateur en éveil lorsqu’il est temps d’exécuter la tâche.<br/>                     |



## <a name="remarks"></a>Remarques

Vous pouvez sélectionner un ou plusieurs des éléments enfants référencés ci-dessus.

pour le développement C++, les informations d’inscription d’une tâche sont spécifiées à l’aide de la [**propriété Paramètres de ITaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_settings).

pour le développement de scripts, les informations d’inscription d’une tâche sont spécifiées à l’aide de la propriété [**TaskDefinition. Paramètres**](taskdefinition-settings.md) .

## <a name="examples"></a>Exemples

L’exemple de code XML suivant définit un élément Settings qui permet un arrêt forcé de la tâche.


```XML
<task>
    <Settings>
        <AllowHardTerminate>true</AllowHardTerminate>
        <AllowStartOnDemand>true</AllowStartOnDemand>
    </Settings>
</task>
```



Pour plus d’informations et pour obtenir un exemple complet du code XML permettant de définir des paramètres de tâche, consultez [exemple de déclenchement de temps (XML)](time-trigger-example--xml-.md).

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

 

 





