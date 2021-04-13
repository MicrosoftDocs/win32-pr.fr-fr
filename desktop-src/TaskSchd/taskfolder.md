---
title: Objet TaskFolder
description: Objet de script qui fournit les méthodes utilisées pour inscrire (créer) des tâches dans le dossier, supprimer des tâches du dossier et créer ou supprimer des sous-dossiers du dossier.
ms.assetid: f6fd09ec-2777-4903-83b5-e3ac1aa472a0
keywords:
- Objet TaskFolder Planificateur de tâches
- Planificateur de tâches d’objets TaskFolder, Description
topic_type:
- apiref
api_name:
- TaskFolder
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1ccad9331cf3df12ea5752fdd7e5ac94bfbeba6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509122"
---
# <a name="taskfolder-object"></a>Objet TaskFolder

Objet de script qui fournit les méthodes utilisées pour inscrire (créer) des tâches dans le dossier, supprimer des tâches du dossier et créer ou supprimer des sous-dossiers du dossier.

## <a name="members"></a>Membres

L’objet **TaskFolder** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

L’objet **TaskFolder** a ces méthodes.



| Méthode                                                              | Description                                                                                                                                    |
|:--------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateFolder**](taskfolder-createfolder.md)                     | Crée un dossier pour les tâches associées.<br/>                                                                                                 |
| [**DeleteFolder**](taskfolder-deletefolder.md)                     | Supprime un sous-dossier du dossier parent.<br/>                                                                                         |
| [**DeleteTask**](taskfolder-deletetask.md)                         | Supprime une tâche du dossier.<br/>                                                                                                     |
| [**GetFolder ITaskService**](taskfolder-getfolder.md)                           | Obtient un dossier qui contient des tâches à un emplacement spécifié.<br/>                                                                          |
| [**GetFolders**](taskfolder-getfolders.md)                         | Obtient tous les sous-dossiers du dossier.<br/>                                                                                              |
| [**GetSecurityDescriptor**](taskfolder-getsecuritydescriptor.md)   | Obtient le descripteur de sécurité pour le dossier.<br/>                                                                                        |
| [**GetTask**](taskfolder-gettask.md)                               | Obtient une tâche à un emplacement spécifié dans un dossier.<br/>                                                                                    |
| [**GetTasks**](taskfolder-gettasks.md)                             | Obtient toutes les tâches dans le dossier.<br/>                                                                                                   |
| [**RegisterTask**](taskfolder-registertask.md)                     | Inscrit (crée) une nouvelle tâche dans le dossier à l’aide de XML pour définir la tâche.<br/>                                                          |
| [**RegisterTaskDefinition**](taskfolder-registertaskdefinition.md) | Inscrit (crée) une tâche à un emplacement spécifié à l’aide de l’interface [**ITaskDefinition**](/windows/desktop/api/taskschd/nn-taskschd-itaskdefinition) pour définir une tâche.<br/> |
| [**SetSecurityDescriptor**](taskfolder-setsecuritydescriptor.md)   | Définit le descripteur de sécurité pour le dossier.<br/>                                                                                        |



 

### <a name="properties"></a>Propriétés

L’objet **TaskFolder** a ces propriétés.



| Propriété                                   | Type d’accès          | Description                                                                        |
|:-------------------------------------------|:---------------------|:-----------------------------------------------------------------------------------|
| [**Nom**](taskfolder-name.md)<br/> | Lecture seule<br/> | Obtient le nom utilisé pour identifier le dossier qui contient une tâche.<br/> |
| [**D**](taskfolder-path.md)<br/> | Lecture seule<br/> | Obtient le chemin d’accès à l’emplacement où le dossier est stocké.<br/>                            |



 

## <a name="examples"></a>Exemples

Pour plus d’informations et pour obtenir un exemple de code pour cet objet de script, consultez [exemple de déclenchement temporel (script)](time-trigger-example--scripting-.md), [exemple de déclencheur d’événements (script)](https://www.bing.com/search?q=Event+Trigger+Example+(Scripting)), [exemple de déclencheur quotidien (script)](daily-trigger-example--scripting-.md), [exemple de déclencheur d’inscription (script)](registration-trigger-example--scripting-.md), exemple de déclencheur [hebdomadaire](weekly-trigger-example--scripting-.md)(script), exemple de [déclencheur de connexion (](logon-trigger-example--scripting-.md)script), exemple de [déclencheur de démarrage (script)](boot-trigger-example--scripting-.md)ou [affichage des noms de tâches et des États (script)](displaying-task-names-and-state--scripting-.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                          |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                    |
| Bibliothèque de types<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Objets Planificateur de tâches](task-scheduler-objects.md)
</dt> <dt>

[Planificateur de tâches](task-scheduler-start-page.md)
</dt> </dl>

 

 





