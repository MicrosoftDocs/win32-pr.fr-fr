---
title: Exemple de déclencheur quotidien (script)
description: Cet exemple de script montre comment créer une tâche qui exécute le bloc-notes à 8 00 AM tous les jours.
ms.assetid: a13bd54d-b45a-46e5-8281-d080f50f6bef
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3399934786e1cd0f95ca020c92027ccafafa5272
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839846"
---
# <a name="daily-trigger-example-scripting"></a>Exemple de déclencheur quotidien (script)

Cet exemple de script montre comment créer une tâche qui exécute le bloc-notes à 8:00 AM tous les jours. La tâche contient un déclencheur quotidien qui spécifie une limite de départ pour activer le déclencheur et spécifier l’heure d’exécution de la tâche, un intervalle de déclencheur pour spécifier que la tâche s’exécute tous les jours et une limite de fin pour désactiver le déclencheur. L’exemple montre également comment définir un modèle de répétition pour le déclencheur afin de répéter la tâche. La tâche contient également une action exécutable qui exécute le bloc-notes.

La procédure suivante décrit comment planifier une tâche pour démarrer un exécutable à 8:00 AM tous les jours. (Ces étapes correspondent aux commentaires de code inclus dans l’exemple de code.)

**Pour planifier le démarrage du bloc-notes à 8:00 AM tous les jours**

1.  Créez un objet [**TaskService**](taskservice.md) . Cet objet vous permet de créer la tâche dans un dossier spécifié.
2.  Récupérez un dossier de tâches et créez une tâche. Utilisez la méthode [**TaskService. GetFolder**](taskservice-getfolder.md) pour récupérer le dossier dans lequel la tâche est stockée et la méthode [**TaskService. newtask**](taskservice-newtask.md) pour créer l’objet [**TaskDefinition**](taskdefinition.md) qui représente la tâche.
3.  Définissez des informations sur la tâche à l’aide de l’objet [**TaskDefinition**](taskdefinition.md) . Utilisez la propriété [**TaskDefinition. Settings**](taskdefinition-settings.md) pour définir les paramètres qui déterminent la façon dont le service Planificateur de tâches effectue la tâche et la propriété [**TaskDefinition. RegistrationInfo**](taskdefinition-registrationinfo.md) pour définir les informations qui décrivent la tâche.
4.  Créez un déclencheur quotidien à l’aide de la propriété [**TaskDefinition. Triggers**](taskdefinition-triggers.md) . Cette propriété permet d’accéder à l’objet [**TriggerCollection**](triggercollection.md) utilisé pour créer le déclencheur. Utilisez la méthode [**TriggerCollection. Create**](triggercollection-create.md) (en spécifiant le type de déclencheur que vous souhaitez créer) pour créer un déclencheur quotidien. Lorsque vous créez le déclencheur, définissez la limite de démarrage pour activer le déclencheur et spécifier l’heure d’exécution de la tâche, l’intervalle entre les jours et la limite de fin pour désactiver le déclencheur. L’exemple ci-dessous montre comment définir un modèle de répétition pour le déclencheur afin de répéter la tâche.
5.  Créez une action à exécuter par la tâche à l’aide de la propriété [**TaskDefinition. actions**](taskdefinition-actions.md) . Cette propriété permet d’accéder à l’objet [**ActionCollection**](actioncollection.md) utilisé pour créer l’action. Utilisez la méthode [**ActionCollection. Create**](actioncollection-create.md) pour spécifier le type d’action que vous souhaitez créer. Cet exemple utilise un objet [**ExecAction**](execaction.md) , qui représente une action qui exécute une opération de ligne de commande.
6.  Inscrivez la tâche à l’aide de la méthode [**TaskFolder. RegisterTaskDefinition**](taskfolder-registertaskdefinition.md) . Pour cet exemple, la tâche démarre le bloc-notes à 8:00 AM tous les jours.

L’exemple VBScript suivant montre comment planifier une tâche pour exécuter le bloc-notes tous les jours à 8:00 AM.


```VB
'------------------------------------------------------------------
' This sample schedules a task to start on a daily basis.
'------------------------------------------------------------------

' A constant that specifies a daily trigger.
const TriggerTypeDaily = 2
' A constant that specifies an executable action.
const ActionTypeExec = 0

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
regInfo.Description = "Start notepad at 8:00AM daily"
regInfo.Author = "Administrator"

' Set the task setting info for the Task Scheduler by
' creating a TaskSettings object.
Dim settings
Set settings = taskDefinition.Settings
settings.Enabled = True
settings.StartWhenAvailable = True
settings.Hidden = False

'********************************************************
' Create a daily trigger. Note that the start boundary 
' specifies the time of day that the task starts and the 
' interval specifies what days the task is run.
Dim triggers
Set triggers = taskDefinition.Triggers

Dim trigger
Set trigger = triggers.Create(TriggerTypeDaily)

' Trigger variables that define when the trigger is active 
' and the time of day that the task is run. The format of 
' this time is YYYY-MM-DDTHH:MM:SS
Dim startTime, endTime

Dim time
startTime = "2006-05-02T08:00:00"  'Task runs at 8:00 AM
endTime = "2015-05-02T08:00:00"

WScript.Echo "startTime :" & startTime
WScript.Echo "endTime :" & endTime

trigger.StartBoundary = startTime
trigger.EndBoundary = endTime
trigger.DaysInterval = 1    'Task runs every day.
trigger.Id = "DailyTriggerId"
trigger.Enabled = True

' Set the task repetition pattern for the task.
' This will repeat the task 5 times.
Dim repetitionPattern
Set repetitionPattern = trigger.Repetition
repetitionPattern.Duration = "PT4M"
repetitionPattern.Interval = "PT1M"

'***********************************************************
' Create the action for the task to execute.

' Add an action to the task to run notepad.exe.
Dim Action
Set Action = taskDefinition.Actions.Create( ActionTypeExec )
Action.Path = "C:\Windows\System32\notepad.exe"

WScript.Echo "Task definition created. About to submit the task..."

'***********************************************************
' Register (create) the task.

call rootFolder.RegisterTaskDefinition( _
    "Test Daily Trigger", taskDefinition, 6, , , 3)

WScript.Echo "Task submitted."

```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation de l’Planificateur de tâches](using-the-task-scheduler.md)
</dt> </dl>

 

 




