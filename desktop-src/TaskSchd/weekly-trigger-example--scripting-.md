---
title: Exemple de déclencheur hebdomadaire (script)
description: cet exemple de script montre comment créer une tâche qui s’exécute Bloc-notes à 8 00 AM le lundi de chaque semaine.
ms.assetid: 68ef73b0-3780-480e-90fe-940b6e8a5340
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4d9cf627591250c341008ba3a5129c4cc10cad6b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127414647"
---
# <a name="weekly-trigger-example-scripting"></a>Exemple de déclencheur hebdomadaire (script)

cet exemple de script montre comment créer une tâche qui s’exécute Bloc-notes à 8:00 AM le lundi de chaque semaine. la tâche contient un déclencheur quotidien qui spécifie le moment d’exécution de la tâche et une action exécutable qui s’exécute Bloc-notes.

La procédure suivante décrit comment planifier une tâche pour démarrer un exécutable à 8:00 AM le lundi de chaque semaine.

**pour planifier le démarrage de la Bloc-notes à 8:00 AM le lundi de chaque semaine**

1.  Créez un objet [**TaskService**](taskservice.md) . Cet objet vous permet de créer la tâche dans un dossier spécifié.
2.  Récupérez un dossier de tâches et créez une tâche. Utilisez la méthode [**TaskService. GetFolder**](taskservice-getfolder.md) pour récupérer le dossier dans lequel la tâche est stockée et la méthode [**TaskService. newtask**](taskservice-newtask.md) pour créer l’objet [**TaskDefinition**](taskdefinition.md) qui représente la tâche.
3.  Définissez des informations sur la tâche à l’aide de l’objet [**TaskDefinition**](taskdefinition.md) . utilisez la propriété [**TaskDefinition. Paramètres**](taskdefinition-settings.md) pour définir les paramètres qui déterminent la façon dont le service de Planificateur de tâches effectue la tâche et la propriété [**TaskDefinition. RegistrationInfo**](taskdefinition-registrationinfo.md) pour définir les informations qui décrivent la tâche.
4.  Créez un déclencheur hebdomadaire à l’aide de la propriété [**TaskDefinition. Triggers**](taskdefinition-triggers.md) . Cette propriété permet d’accéder à l’objet [**TriggerCollection**](triggercollection.md) utilisé pour créer le déclencheur.

    Utilisez la méthode [**TriggerCollection. Create**](triggercollection-create.md) (en spécifiant le type de déclencheur que vous souhaitez créer) pour créer un déclencheur hebdomadaire.

    Définissez la propriété [**WeeklyTrigger. StartBoundary**](trigger-startboundary.md) pour spécifier à quel moment le déclencheur est activé et l’heure de la journée à laquelle la tâche est exécutée. Dans cet exemple, le déclencheur est activé le 1er janvier 2005 et la tâche s’exécute à 8:00 AM.

    Définissez la propriété [**WeeklyTrigger. EndBoundary**](trigger-endboundary.md)pour spécifier le moment où le déclencheur est désactivé. Dans cet exemple, le déclencheur est désactivé le 1er janvier 2015.

    Définissez la propriété [**WeeklyTrigger. DaysOfWeek**](weeklytrigger-daysofweek.md) pour spécifier les jours de la semaine où la tâche est exécutée. Dans cet exemple, la tâche est exécutée le lundi.

    Définissez la propriété [**WeeklyTrigger. WeeksInterval**](weeklytrigger-weeksinterval.md)pour spécifier l’intervalle entre les semaines de la planification. Dans cet exemple, la tâche s’exécute toutes les semaines.

5.  Créez une action à exécuter par la tâche à l’aide de la propriété [**TaskDefinition. actions**](taskdefinition-actions.md) . Cette propriété permet d’accéder à l’objet [**ActionCollection**](actioncollection.md) utilisé pour créer l’action. Utilisez la méthode [**ActionCollection. Create**](actioncollection-create.md) pour spécifier le type d’action que vous souhaitez créer. Cet exemple utilise un objet [**ExecAction**](execaction.md) , qui représente une action qui exécute une opération de ligne de commande.
6.  Inscrivez la tâche à l’aide de la méthode [**TaskFolder. RegisterTaskDefinition**](taskfolder-registertaskdefinition.md) . pour cet exemple, la tâche démarre Bloc-notes à 8:00 AM le lundi de chaque semaine.

l’exemple VBScript suivant montre comment planifier l’exécution d’une tâche Bloc-notes tous les jours à 8:00 AM.


```VB
'------------------------------------------------------------------
' This sample schedules a task to start on a weekly basis.
'------------------------------------------------------------------

' A constant that specifies a weekly trigger.
const TriggerTypeWeekly = 3
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
regInfo.Description = "Start Notepad weekly."
regInfo.Author = "Administrator"

' Set the task setting info for the Task Scheduler by
' creating a TaskSettings object.
Dim settings
Set settings = taskDefinition.Settings
settings.Enabled = True
settings.StartWhenAvailable = True
settings.Hidden = False

'********************************************************
' Create a weekly trigger. Note that the start boundary 
' specifies the time of day that the task starts, the 
' day-of-week specfies on what day of the week the task 
' runs, and the interval specifies what weeks the task runs.
Dim triggers
Set triggers = taskDefinition.Triggers

Dim trigger
Set trigger = triggers.Create(TriggerTypeWeekly)

' Trigger variables that define when the trigger is active 
' and the time of day that the task is run. The format of 
' this tims is YYYY-MM-DDTHH:MM:SS
Dim startTime, endTime

Dim time
startTime = "2006-05-02T08:00:00"  'Task runs at 8:00 AM
endTime = "2015-05-02T08:00:00"

WScript.Echo "startTime :" & startTime
WScript.Echo "endTime :" & endTime

trigger.StartBoundary = startTime
trigger.EndBoundary = endTime
trigger.DaysOfWeek = 1
trigger.WeeksInterval = 1    'Task runs every week.
trigger.Id = "WeeklyTriggerId"
trigger.Enabled = True

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
    "Test Weekly Trigger", taskDefinition, 6, , , 3)

WScript.Echo "Task submitted."

```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation de l’Planificateur de tâches](using-the-task-scheduler.md)
</dt> </dl>

 

 




