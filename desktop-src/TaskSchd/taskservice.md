---
title: Objet TaskService
description: Pour les scripts, fournit l’accès au service Planificateur de tâches pour la gestion des tâches inscrites.
ms.assetid: 6ddd43dc-d027-4792-a53b-07fe4d4a3576
keywords:
- Objet TaskService Planificateur de tâches
- Planificateur de tâches d’objets TaskService, Description
topic_type:
- apiref
api_name:
- TaskService
- HighestVersion
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 74f20840a5580d0188354ca6b65ab3ce5b7402d57ea7346462d2f990ecfe34cf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119658649"
---
# <a name="taskservice-object"></a>Objet TaskService

Pour les scripts, fournit l’accès au service Planificateur de tâches pour la gestion des tâches inscrites.

la méthode [**TaskService. Connecter**](taskservice-connect.md) doit être appelée avant d’appeler l’une des autres méthodes **TaskService** .

## <a name="members"></a>Membres

L’objet **TaskService** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

L’objet **TaskService** a ces méthodes.



| Méthode                                                 | Description                                                                                                                                                                                                          |
|:-------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Connecter**](taskservice-connect.md)                 | Établit une connexion à un ordinateur distant et associe tous les appels suivants à cette interface avec une session à distance.<br/>                                                                                                 |
| [**GetFolder ITaskService**](taskservice-getfolder.md)             | Obtient le chemin d’accès à un dossier de tâches inscrites.<br/>                                                                                                                                                            |
| [**GetRunningTasks**](taskservice-getrunningtasks.md) | Obtient une collection de tâches en cours d’exécution.<br/>                                                                                                                                                                       |
| [**NewTask**](taskservice-newtask.md)                 | Retourne un objet de définition de tâche vide à remplir avec des paramètres et des propriétés, puis inscrit à l’aide de la méthode [**TaskFolder. RegisterTaskDefinition**](taskfolder-registertaskdefinition.md) .<br/> |



 

### <a name="properties"></a>Propriétés

L’objet **TaskService** a ces propriétés.



| Propriété                                                          | Description                                                                                                                 |
|:------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------|
| [**Connecté**](taskservice-connected.md)<br/>             | Obtient une valeur booléenne qui indique si vous êtes connecté au service Planificateur de tâches.<br/>                          |
| [**ConnectedDomain**](taskservice-connecteddomain.md)<br/> | Obtient le nom du domaine auquel l’ordinateur [**TargetServer**](taskservice-targetserver.md) est connecté.<br/> |
| [**ConnectedUser**](taskservice-connecteduser.md)<br/>     | Obtient le nom de l’utilisateur connecté au service Planificateur de tâches.<br/>                                       |
| HighestVersion<br/>                                         | Obtient la version la plus récente de Planificateur de tâches qu’un ordinateur prend en charge.<br/>                                             |
| [**TargetServer**](taskservice-targetserver.md)<br/>       | Obtient le nom de l’ordinateur qui exécute le service Planificateur de tâches auquel l’utilisateur est connecté.<br/>          |



 

## <a name="examples"></a>Exemples

Pour plus d’informations et pour obtenir un exemple de code pour cet objet de script, consultez [exemple de déclenchement temporel (script)](time-trigger-example--scripting-.md), [exemple de déclencheur d’événements (script)](https://www.bing.com/search?q=Event+Trigger+Example+(Scripting)), [exemple de déclencheur quotidien (script)](daily-trigger-example--scripting-.md), [exemple de déclencheur d’inscription (script)](registration-trigger-example--scripting-.md), exemple de déclencheur [hebdomadaire](weekly-trigger-example--scripting-.md)(script), exemple de [déclencheur de connexion (](logon-trigger-example--scripting-.md)script), exemple de [déclencheur de démarrage (script)](boot-trigger-example--scripting-.md)ou [affichage des noms de tâches et des États (script)](displaying-task-names-and-state--scripting-.md).

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
</dt> </dl>

 

 





