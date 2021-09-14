---
title: Exemple de déclencheur de temps (script)
description: cet exemple de script montre comment créer une tâche qui s’exécute Bloc-notes à un moment donné.
ms.assetid: 8511ffcd-166f-4c63-9cd2-ead53dde9ed8
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 77cbf9eab12f5ca027fbb6c48ade37a9f57d9beb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127233028"
---
# <a name="time-trigger-example-scripting"></a>Exemple de déclencheur de temps (script)

cet exemple de script montre comment créer une tâche qui s’exécute Bloc-notes à un moment donné. la tâche contient un déclencheur basé sur l’heure qui spécifie une limite de début pour activer la tâche, une action exécutable qui exécute Bloc-notes et une limite de fin qui désactive la tâche.

La procédure suivante décrit comment planifier une tâche pour démarrer un exécutable à un moment donné.

**pour planifier le démarrage de Bloc-notes à une heure spécifique**

1.  Créez un objet [**TaskService**](taskservice.md) . Cet objet vous permet de créer la tâche dans un dossier spécifié.
2.  Récupérez un dossier de tâches et créez une tâche. Utilisez la méthode [**TaskService. GetFolder**](taskservice-getfolder.md) pour récupérer le dossier dans lequel la tâche est stockée et la méthode [**TaskService. newtask**](taskservice-newtask.md) pour créer l’objet [**TaskDefinition**](taskdefinition.md) qui représente la tâche.
3.  Définissez des informations sur la tâche à l’aide de l’objet [**TaskDefinition**](taskdefinition.md) . utilisez la propriété [**TaskDefinition. Paramètres**](taskdefinition-settings.md) pour définir les paramètres qui déterminent la façon dont le service de Planificateur de tâches effectue la tâche et la propriété [**TaskDefinition. RegistrationInfo**](taskdefinition-registrationinfo.md) pour définir les informations qui décrivent la tâche.
4.  Créez un déclencheur basé sur l’heure à l’aide de la propriété [**TaskDefinition. Triggers**](taskdefinition-triggers.md) . Cette propriété permet d’accéder à l’objet [**TriggerCollection**](triggercollection.md) . Utilisez la méthode [**TriggerCollection. Create**](triggercollection-create.md) (en spécifiant le type de déclencheur que vous souhaitez créer) pour créer un déclencheur basé sur l’heure. Lorsque vous créez le déclencheur, définissez les limites de début et de fin du déclencheur pour activer et désactiver le déclencheur. La limite de début spécifie le moment où l’action de la tâche sera exécutée.
5.  Créez une action à exécuter par la tâche à l’aide de la propriété [**TaskDefinition. actions**](taskdefinition-actions.md) . Cette propriété permet d’accéder à l’objet [**ActionCollection**](actioncollection.md) . Utilisez la méthode [**ActionCollection. Create**](actioncollection-create.md) pour spécifier le type d’action que vous souhaitez créer. Cet exemple utilise un objet [**ExecAction**](execaction.md) , qui représente une action qui exécute une opération de ligne de commande.
6.  Inscrivez la tâche à l’aide de la méthode [**TaskFolder. RegisterTaskDefinition**](taskfolder-registertaskdefinition.md) . pour cet exemple, la tâche démarre Bloc-notes à l’heure actuelle plus 30 secondes.

l’exemple VBScript suivant montre comment planifier l’exécution d’une tâche Bloc-notes 30 secondes après l’inscription de la tâche.


```VB
'------------------------------------------------------------------
' This sample schedules a task to start notepad.exe 30 seconds
' from the time the task is registered.
'------------------------------------------------------------------

' A constant that specifies a time-based trigger.
const TriggerTypeTime = 1
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
regInfo.Description = "Start notepad at a certain time"
regInfo.Author = "Author Name"

'********************************************************
' Set the principal for the task
Dim principal
Set principal = taskDefinition.Principal

' Set the logon type to interactive logon
principal.LogonType = 3


' Set the task setting info for the Task Scheduler by
' creating a TaskSettings object.
Dim settings
Set settings = taskDefinition.Settings
settings.Enabled = True
settings.StartWhenAvailable = True
settings.Hidden = False

'********************************************************
' Create a time-based trigger.
Dim triggers
Set triggers = taskDefinition.Triggers

Dim trigger
Set trigger = triggers.Create(TriggerTypeTime)

' Trigger variables that define when the trigger is active.
Dim startTime, endTime

Dim time
time = DateAdd("s", 30, Now)  'start time = 30 seconds from now
startTime = XmlTime(time)

time = DateAdd("n", 5, Now) 'end time = 5 minutes from now
endTime = XmlTime(time)

WScript.Echo "startTime :" & startTime
WScript.Echo "endTime :" & endTime

trigger.StartBoundary = startTime
trigger.EndBoundary = endTime
trigger.ExecutionTimeLimit = "PT5M"    'Five minutes
trigger.Id = "TimeTriggerId"
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
    "Test TimeTrigger", taskDefinition, 6, , , 3)

WScript.Echo "Task submitted."



'------------------------------------------------------------------
' Used to get the time for the trigger 
' startBoundary and endBoundary.
' Return the time in the correct format: 
' YYYY-MM-DDTHH:MM:SS. 
'------------------------------------------------------------------
Function XmlTime(t)
    Dim cSecond, cMinute, CHour, cDay, cMonth, cYear
    Dim tTime, tDate

    cSecond = "0" & Second(t)
    cMinute = "0" & Minute(t)
    cHour = "0" & Hour(t)
    cDay = "0" & Day(t)
    cMonth = "0" & Month(t)
    cYear = Year(t)

    tTime = Right(cHour, 2) & ":" & Right(cMinute, 2) & _
        ":" & Right(cSecond, 2)
    tDate = cYear & "-" & Right(cMonth, 2) & "-" & Right(cDay, 2)
    XmlTime = tDate & "T" & tTime 
End Function

```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation de l’Planificateur de tâches](using-the-task-scheduler.md)
</dt> </dl>

 

 




