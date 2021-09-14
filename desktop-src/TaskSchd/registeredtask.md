---
title: Objet RegisteredTask
description: Objet de script qui fournit les méthodes utilisées pour exécuter immédiatement la tâche, récupérez les instances en cours d’exécution de la tâche, récupérez ou définissez les informations d’identification utilisées pour enregistrer la tâche et les propriétés qui décrivent la tâche.
ms.assetid: d280f22b-4dd1-44df-be12-286fb1c029a3
keywords:
- Objet RegisteredTask Planificateur de tâches
- Planificateur de tâches d’objets RegisteredTask, Description
topic_type:
- apiref
api_name:
- RegisteredTask
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7ce300375e5122a7b63266c0cd21cdddf34606b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127122894"
---
# <a name="registeredtask-object"></a>Objet RegisteredTask

Objet de script qui fournit les méthodes utilisées pour exécuter immédiatement la tâche, récupérez les instances en cours d’exécution de la tâche, récupérez ou définissez les informations d’identification utilisées pour enregistrer la tâche et les propriétés qui décrivent la tâche.

## <a name="members"></a>Membres

L’objet **RegisteredTask** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

L’objet **RegisteredTask** a ces méthodes.



| Méthode                                                                | Description                                                                                     |
|:----------------------------------------------------------------------|:------------------------------------------------------------------------------------------------|
| [**GetInstances**](registeredtask-getinstances.md)                   | Retourne toutes les instances de la tâche inscrite en cours d’exécution.<br/>             |
| [**GetRunTimes**](/windows/desktop/api/taskschd/nf-taskschd-iregisteredtask-getruntimes)                    | Obtient le nombre de fois que la tâche inscrite est planifiée pour s’exécuter pendant une période spécifiée.<br/> |
| [**GetSecurityDescriptor**](registeredtask-getsecuritydescriptor.md) | Obtient le descripteur de sécurité utilisé comme informations d’identification pour la tâche inscrite.<br/>    |
| [**Exécuter**](registeredtask-run.md)                                     | Exécute la tâche inscrite immédiatement.<br/>                                                |
| [**RunEx**](registeredtask-runex.md)                                 | Exécute la tâche inscrite immédiatement à l’aide des indicateurs spécifiés et d’un identificateur de session.<br/> |
| [**SetSecurityDescriptor**](registeredtask-setsecuritydescriptor.md) | Définit le descripteur de sécurité utilisé comme informations d’identification pour la tâche inscrite.<br/>    |
| [**Arrêter**](registeredtask-stop.md)                                   | Arrête immédiatement la tâche inscrite.<br/>                                               |



 

### <a name="properties"></a>Propriétés

L’objet **RegisteredTask** a ces propriétés.



| Propriété                                                                   | Type d’accès           | Description                                                                               |
|:---------------------------------------------------------------------------|:----------------------|:------------------------------------------------------------------------------------------|
| [**Définition**](registeredtask-definition.md)<br/>                 | Lecture seule<br/>  | Obtient la définition de la tâche.<br/>                                               |
| [**Activé**](registeredtask-enabled.md)<br/>                       | Lecture/écriture<br/> | Obtient ou définit une valeur booléenne qui indique si la tâche inscrite est activée.<br/>  |
| [**LastRunTime**](registeredtask-lastruntime.md)<br/>               | Lecture seule<br/>  | Obtient l’heure de la dernière exécution de la tâche inscrite.<br/>                                |
| [**LastTaskResult**](registeredtask-lasttaskresult.md)<br/>         | Lecture seule<br/>  | Obtient les résultats qui ont été retournés lors de la dernière exécution de la tâche inscrite.<br/> |
| [**Nom**](registeredtask-name.md)<br/>                             | Lecture seule<br/>  | Obtient le nom de la tâche inscrite.<br/>                                          |
| [**NextRunTime**](registeredtask-nextruntime.md)<br/>               | Lecture seule<br/>  | Obtient l’heure à laquelle la tâche inscrite est planifiée pour s’exécuter.<br/>               |
| [**NumberOfMissedRuns**](registeredtask-numberofmissedruns.md)<br/> | Lecture seule<br/>  | Obtient le nombre de fois où la tâche inscrite a manqué une exécution planifiée.<br/>       |
| [**Chemin d’accès**](registeredtask-path.md)<br/>                             | Lecture seule<br/>  | Obtient le chemin d’accès à l’emplacement où la tâche inscrite est stockée.<br/>                          |
| [**State**](registeredtask-state.md)<br/>                           | Lecture seule<br/>  | Obtient l’état opérationnel de la tâche inscrite.<br/>                             |
| [**LANGAGE**](registeredtask-xml.md)<br/>                               | Lecture seule<br/>  | Obtient les informations d’inscription au format XML pour la tâche inscrite.<br/>       |



 

## <a name="examples"></a>Exemples

Pour plus d’informations et pour obtenir un exemple de code pour cet objet de script, consultez [exemple de déclenchement temporel (script)](time-trigger-example--scripting-.md) et [affichage des noms et des États des tâches (script)](displaying-task-names-and-state--scripting-.md).

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                          |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                    |
| Bibliothèque de types<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

 





