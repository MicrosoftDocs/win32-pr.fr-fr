---
title: Exemple de déclencheur de démarrage (script)
description: cet exemple de script montre comment créer une tâche qui est planifiée pour s’exécuter Bloc-notes lorsque le système est démarré.
ms.assetid: 73ae9cc4-ef89-4390-ac05-8a773f45fa46
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ff02bef70b4003c4e7b6e9aff03e2d615f24d7e15707cddcae3a4637ff2b11f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119002517"
---
# <a name="boot-trigger-example-scripting"></a>Exemple de déclencheur de démarrage (script)

cet exemple de script montre comment créer une tâche qui est planifiée pour s’exécuter Bloc-notes lorsque le système est démarré. La tâche contient un déclencheur de démarrage qui spécifie une limite de début et le délai de démarrage de la tâche après le démarrage du système. la tâche contient également une action qui spécifie la tâche à exécuter Bloc-notes. La tâche est inscrite en utilisant le compte de service local comme contexte de sécurité pour exécuter la tâche.

la procédure suivante décrit comment planifier l’exécution d’un fichier exécutable tel que Bloc-notes au démarrage du système.

**pour planifier le démarrage de Bloc-notes lors du démarrage du système**

1.  Créez un objet [**TaskService**](taskservice.md) . Cet objet vous permet de créer la tâche dans un dossier spécifié.
2.  Récupérez un dossier de tâches et créez une tâche. Utilisez la méthode [**TaskService. GetFolder**](taskservice-getfolder.md) pour récupérer le dossier dans lequel la tâche est stockée et la méthode [**TaskService. newtask**](taskservice-newtask.md) pour créer l’objet [**TaskDefinition**](taskdefinition.md) qui représente la tâche.
3.  Définissez des informations sur la tâche à l’aide de l’objet [**TaskDefinition**](taskdefinition.md) . utilisez la propriété [**TaskDefinition. Paramètres**](taskdefinition-settings.md) pour définir les paramètres qui déterminent la façon dont le service de Planificateur de tâches effectue la tâche et la propriété [**TaskDefinition. RegistrationInfo**](taskdefinition-registrationinfo.md) pour définir les informations qui décrivent la tâche.
4.  Créez un déclencheur de connexion à l’aide de la propriété [**TaskDefinition. Triggers**](taskdefinition-triggers.md) . Cette propriété permet d’accéder à l’objet [**TriggerCollection**](triggercollection.md) . Utilisez la méthode [**TriggerCollection. Create**](triggercollection-create.md) (en spécifiant le type de déclencheur que vous souhaitez créer) pour créer un déclencheur de démarrage. Au fur et à mesure que vous créez le déclencheur, définissez les propriétés [**StartBoundary**](trigger-startboundary.md) et [**EndBoundary**](trigger-endboundary.md) du déclencheur pour activer et désactiver le déclencheur. Vous pouvez également spécifier une valeur pour la propriété [**delay**](boottrigger-delay.md) du déclencheur de démarrage.
5.  Créez une action à exécuter par la tâche à l’aide de la propriété [**TaskDefinition. actions**](taskdefinition-actions.md) . Cette propriété permet d’accéder à l’objet [**ActionCollection**](actioncollection.md) . Utilisez la méthode [**ActionCollection. Create**](actioncollection-create.md) pour spécifier le type d’action que vous souhaitez créer. Cet exemple utilise un objet [**ExecAction**](execaction.md) , qui représente une action qui démarre un exécutable.
6.  Inscrivez la tâche à l’aide de la méthode [**TaskFolder. RegisterTaskDefinition**](taskfolder-registertaskdefinition.md) . La tâche est inscrite en utilisant le compte de service local comme contexte de sécurité pour exécuter la tâche.

l’exemple VBScript suivant montre comment planifier l’exécution d’une tâche Bloc-notes 30 secondes après le démarrage du système.


```VB
'---------------------------------------------------------
' This sample schedules a task to start notepad.exe 30 seconds after
' the system is booted.
'---------------------------------------------------------

' A constant that specifies a boot trigger.
const TriggerTypeBoot = 8
' A constant that specifies an executable action.
const ActionTypeExecutable = 0   

'********************************************************
' Create the TaskService object.
Set service = CreateObject("Schedule.Service")
call service.Connect()

'********************************************************
' Get a folder to create a task definition in. 
Dim rootFolder
Set rootFolder = service.GetFolder("\")

' The taskDefinition variable is the TaskDefinition object.
Dim taskDefinition
' The flags parameter is 0 because it is not supported.
Set taskDefinition = service.NewTask(0) 

'********************************************************
' Define information about the task.

' Set the registration info for the task by 
' creating the RegistrationInfo object.
Dim regInfo
Set regInfo = taskDefinition.RegistrationInfo
regInfo.Description = "Task will execute Notepad when " & _
    "the computer is booted."
regInfo.Author = "Author Name"

' Set the task setting info for the Task Scheduler by
' creating a TaskSettings object.
Dim settings
Set settings = taskDefinition.Settings
settings.StartWhenAvailable = True

'********************************************************
' Create a boot trigger.
Dim triggers
Set triggers = taskDefinition.Triggers

Dim trigger
Set trigger = triggers.Create(TriggerTypeBoot)

' Trigger variables that define when the trigger is active.
Dim startTime, endTime
startTime = "2006-05-02T10:49:02"
endTime = "2006-05-02T10:52:02"

WScript.Echo "startTime :" & startTime
WScript.Echo "endTime :" & endTime

trigger.StartBoundary = startTime
trigger.EndBoundary = endTime
trigger.ExecutionTimeLimit = "PT5M"    ' Five minutes
trigger.Id = "BootTriggerId"
trigger.Delay = "PT30S"                ' 30 Seconds   

'***********************************************************
' Create the action for the task to execute.

' Add an action to the task. The action executes notepad.
Dim Action
Set Action = taskDefinition.Actions.Create( ActionTypeExecutable )
Action.Path = "C:\Windows\System32\notepad.exe"

WScript.Echo "Task definition created. About to submit the task..."

'***********************************************************
' Register (create) the task.
const createOrUpdateTask = 6
call rootFolder.RegisterTaskDefinition( _
    "Test Boot Trigger", taskDefinition, createOrUpdateTask, _
    "Local Service", , 5)

WScript.Echo "Task submitted."
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation de l’Planificateur de tâches](using-the-task-scheduler.md)
</dt> </dl>

 

 




