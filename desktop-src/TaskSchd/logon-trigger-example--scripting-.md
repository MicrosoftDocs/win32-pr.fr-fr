---
title: Exemple de déclencheur LOGON (script)
description: Cet exemple de script montre comment créer une tâche qui est planifiée pour exécuter le bloc-notes lorsqu’un utilisateur ouvre une session.
ms.assetid: f25e105f-9439-4646-bdfd-609ee99a5d55
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 72a8c4b5d0d67b59160eb3ed0b13885ee7e0eb51
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104196550"
---
# <a name="logon-trigger-example-scripting"></a>Exemple de déclencheur LOGON (script)

Cet exemple de script montre comment créer une tâche qui est planifiée pour exécuter le bloc-notes lorsqu’un utilisateur ouvre une session. La tâche contient un déclencheur d’ouverture de session qui spécifie une limite de début pour le démarrage de la tâche et un identificateur d’utilisateur qui spécifie l’utilisateur. La tâche est inscrite à l’aide du groupe administrateurs comme contexte de sécurité pour l’exécution de la tâche.

La procédure suivante décrit comment planifier le démarrage d’un exécutable, tel que le bloc-notes, lorsqu’un utilisateur spécifié ouvre une session.

**Pour planifier le démarrage du bloc-notes quand un utilisateur ouvre une session**

1.  Créez un objet [**TaskService**](taskservice.md) . Cet objet vous permet de créer la tâche dans un dossier spécifié.
2.  Récupérez un dossier de tâches et créez une tâche. Utilisez la méthode [**TaskService. GetFolder**](taskservice-getfolder.md) pour récupérer le dossier dans lequel la tâche est stockée et la méthode [**TaskService. newtask**](taskservice-newtask.md) pour créer l’objet [**TaskDefinition**](taskdefinition.md) qui représente la tâche.
3.  Définissez des informations sur la tâche à l’aide de l’objet [**TaskDefinition**](taskdefinition.md) . Utilisez la propriété [**TaskDefinition. Settings**](taskdefinition-settings.md) pour définir les paramètres qui déterminent la façon dont le service Planificateur de tâches effectue la tâche et la propriété [**TaskDefinition. RegistrationInfo**](taskdefinition-registrationinfo.md) pour définir les informations qui décrivent la tâche.
4.  Créez un déclencheur de connexion à l’aide de la propriété [**TaskDefinition. Triggers**](taskdefinition-triggers.md) . Cette propriété permet d’accéder à l’objet [**TriggerCollection**](triggercollection.md) . Utilisez la méthode [**TriggerCollection. Create**](triggercollection-create.md) (en spécifiant le type de déclencheur que vous souhaitez créer) pour créer un déclencheur Logon. Lorsque vous créez le déclencheur, définissez les limites de début et de fin du déclencheur pour activer et désactiver le déclencheur. Vous devez définir la propriété [**userid**](/windows/desktop/api/taskschd/nf-taskschd-ilogontrigger-get_userid) pour le déclencheur afin que les actions de la tâche soient planifiées pour s’exécuter lorsque l’utilisateur spécifié se connecte après la limite de début.
5.  Créez une action à exécuter par la tâche à l’aide de la propriété [**TaskDefinition. actions**](taskdefinition-actions.md) . Cette propriété permet d’accéder à l’objet [**ActionCollection**](actioncollection.md) . Utilisez la méthode [**ActionCollection. Create**](actioncollection-create.md) pour spécifier le type d’action que vous souhaitez créer. Cet exemple utilise un objet [**ExecAction**](execaction.md) , qui représente une action qui démarre un exécutable.
6.  Inscrivez la tâche à l’aide de la méthode [**TaskFolder. RegisterTaskDefinition**](taskfolder-registertaskdefinition.md) . Cet exemple inscrit la tâche pour qu’elle utilise le groupe administrateurs comme contexte de sécurité pour l’exécution de la tâche.

L’exemple VBScript suivant montre comment planifier une tâche pour exécuter le bloc-notes lorsqu’un utilisateur ouvre une session.


```VB
'---------------------------------------------------------
' This sample schedules a task to start notepad.exe when a user logs on.
'---------------------------------------------------------

' A constant that specifies a logon trigger.
const TriggerTypeLogon = 9
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
regInfo.Description = "Task will execute Notepad when a " & _
    "specified user logs on."
regInfo.Author = "Author Name"

' Set the task setting info for the Task Scheduler by
' creating a TaskSettings object.
Dim settings
Set settings = taskDefinition.Settings
settings.StartWhenAvailable = True

'********************************************************
' Create a logon trigger.
Dim triggers
Set triggers = taskDefinition.Triggers

Dim trigger
Set trigger = triggers.Create(TriggerTypeLogon)

' Trigger variables that define when the trigger is active.
Dim startTime, endTime
startTime = "2006-05-02T10:49:02"
endTime = "2006-05-02T10:52:02"

WScript.Echo "startTime :" & startTime
WScript.Echo "endTime :" & endTime

trigger.StartBoundary = startTime
trigger.EndBoundary = endTime
trigger.ExecutionTimeLimit = "PT5M"    ' Five minutes
trigger.Id = "LogonTriggerId"
trigger.UserId = "DOMAIN\UserName"   ' Must be a valid user account   

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
    "Test Logon Trigger", taskDefinition, createOrUpdateTask, _
    "Builtin\Administrators", , 4)

WScript.Echo "Task submitted."
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation de l’Planificateur de tâches](using-the-task-scheduler.md)
</dt> </dl>

 

 




