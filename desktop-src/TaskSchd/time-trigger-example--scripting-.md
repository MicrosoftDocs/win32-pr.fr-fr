---
title: Exemple de déclencheur de temps (script)
description: Cet exemple de script montre comment créer une tâche qui exécute le bloc-notes à un moment donné.
ms.assetid: 8511ffcd-166f-4c63-9cd2-ead53dde9ed8
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 77cbf9eab12f5ca027fbb6c48ade37a9f57d9beb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106511621"
---
# <a name="time-trigger-example-scripting"></a><span data-ttu-id="5f737-103">Exemple de déclencheur de temps (script)</span><span class="sxs-lookup"><span data-stu-id="5f737-103">Time Trigger Example (Scripting)</span></span>

<span data-ttu-id="5f737-104">Cet exemple de script montre comment créer une tâche qui exécute le bloc-notes à un moment donné.</span><span class="sxs-lookup"><span data-stu-id="5f737-104">This scripting example shows how to create a task that runs Notepad at a specific time.</span></span> <span data-ttu-id="5f737-105">La tâche contient un déclencheur basé sur l’heure qui spécifie une limite de début pour activer la tâche, une action exécutable qui exécute le bloc-notes et une limite de fin qui désactive la tâche.</span><span class="sxs-lookup"><span data-stu-id="5f737-105">The task contains a time-based trigger that specifies a start boundary to activate the task, an executable action that runs Notepad, and an end boundary that deactivates the task.</span></span>

<span data-ttu-id="5f737-106">La procédure suivante décrit comment planifier une tâche pour démarrer un exécutable à un moment donné.</span><span class="sxs-lookup"><span data-stu-id="5f737-106">The following procedure describes how to schedule a task to start an executable at a specific time.</span></span>

<span data-ttu-id="5f737-107">**Pour planifier le démarrage du bloc-notes à un moment donné**</span><span class="sxs-lookup"><span data-stu-id="5f737-107">**To Schedule Notepad to start at a Specific Time**</span></span>

1.  <span data-ttu-id="5f737-108">Créez un objet [**TaskService**](taskservice.md) .</span><span class="sxs-lookup"><span data-stu-id="5f737-108">Create a [**TaskService**](taskservice.md) object.</span></span> <span data-ttu-id="5f737-109">Cet objet vous permet de créer la tâche dans un dossier spécifié.</span><span class="sxs-lookup"><span data-stu-id="5f737-109">This object allows you to create the task in a specified folder.</span></span>
2.  <span data-ttu-id="5f737-110">Récupérez un dossier de tâches et créez une tâche.</span><span class="sxs-lookup"><span data-stu-id="5f737-110">Get a task folder and create a task.</span></span> <span data-ttu-id="5f737-111">Utilisez la méthode [**TaskService. GetFolder**](taskservice-getfolder.md) pour récupérer le dossier dans lequel la tâche est stockée et la méthode [**TaskService. newtask**](taskservice-newtask.md) pour créer l’objet [**TaskDefinition**](taskdefinition.md) qui représente la tâche.</span><span class="sxs-lookup"><span data-stu-id="5f737-111">Use the [**TaskService.GetFolder**](taskservice-getfolder.md) method to get the folder where the task is stored and the [**TaskService.NewTask**](taskservice-newtask.md) method to create the [**TaskDefinition**](taskdefinition.md) object that represents the task.</span></span>
3.  <span data-ttu-id="5f737-112">Définissez des informations sur la tâche à l’aide de l’objet [**TaskDefinition**](taskdefinition.md) .</span><span class="sxs-lookup"><span data-stu-id="5f737-112">Define information about the task using the [**TaskDefinition**](taskdefinition.md) object.</span></span> <span data-ttu-id="5f737-113">Utilisez la propriété [**TaskDefinition. Settings**](taskdefinition-settings.md) pour définir les paramètres qui déterminent la façon dont le service Planificateur de tâches effectue la tâche et la propriété [**TaskDefinition. RegistrationInfo**](taskdefinition-registrationinfo.md) pour définir les informations qui décrivent la tâche.</span><span class="sxs-lookup"><span data-stu-id="5f737-113">Use the [**TaskDefinition.Settings**](taskdefinition-settings.md) property to define the settings that determine how the Task Scheduler service performs the task and the [**TaskDefinition.RegistrationInfo**](taskdefinition-registrationinfo.md) property to define the information that describes the task.</span></span>
4.  <span data-ttu-id="5f737-114">Créez un déclencheur basé sur l’heure à l’aide de la propriété [**TaskDefinition. Triggers**](taskdefinition-triggers.md) .</span><span class="sxs-lookup"><span data-stu-id="5f737-114">Create a time-based trigger using the [**TaskDefinition.Triggers**](taskdefinition-triggers.md) property.</span></span> <span data-ttu-id="5f737-115">Cette propriété permet d’accéder à l’objet [**TriggerCollection**](triggercollection.md) .</span><span class="sxs-lookup"><span data-stu-id="5f737-115">This property provides access to the [**TriggerCollection**](triggercollection.md) object.</span></span> <span data-ttu-id="5f737-116">Utilisez la méthode [**TriggerCollection. Create**](triggercollection-create.md) (en spécifiant le type de déclencheur que vous souhaitez créer) pour créer un déclencheur basé sur l’heure.</span><span class="sxs-lookup"><span data-stu-id="5f737-116">Use the [**TriggerCollection.Create**](triggercollection-create.md) method (specifying the type of trigger you want to create) to create a time-based trigger.</span></span> <span data-ttu-id="5f737-117">Lorsque vous créez le déclencheur, définissez les limites de début et de fin du déclencheur pour activer et désactiver le déclencheur.</span><span class="sxs-lookup"><span data-stu-id="5f737-117">As you create the trigger, set the start boundary and end boundary of the trigger to activate and deactivate the trigger.</span></span> <span data-ttu-id="5f737-118">La limite de début spécifie le moment où l’action de la tâche sera exécutée.</span><span class="sxs-lookup"><span data-stu-id="5f737-118">The start boundary specifies when the task's action will be performed.</span></span>
5.  <span data-ttu-id="5f737-119">Créez une action à exécuter par la tâche à l’aide de la propriété [**TaskDefinition. actions**](taskdefinition-actions.md) .</span><span class="sxs-lookup"><span data-stu-id="5f737-119">Create an action for the task to execute by using the [**TaskDefinition.Actions**](taskdefinition-actions.md) property.</span></span> <span data-ttu-id="5f737-120">Cette propriété permet d’accéder à l’objet [**ActionCollection**](actioncollection.md) .</span><span class="sxs-lookup"><span data-stu-id="5f737-120">This property provides access to the [**ActionCollection**](actioncollection.md) object.</span></span> <span data-ttu-id="5f737-121">Utilisez la méthode [**ActionCollection. Create**](actioncollection-create.md) pour spécifier le type d’action que vous souhaitez créer.</span><span class="sxs-lookup"><span data-stu-id="5f737-121">Use the [**ActionCollection.Create**](actioncollection-create.md) method to specify the type of action you want to create.</span></span> <span data-ttu-id="5f737-122">Cet exemple utilise un objet [**ExecAction**](execaction.md) , qui représente une action qui exécute une opération de ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="5f737-122">This example uses an [**ExecAction**](execaction.md) object, which represents an action that executes a command-line operation.</span></span>
6.  <span data-ttu-id="5f737-123">Inscrivez la tâche à l’aide de la méthode [**TaskFolder. RegisterTaskDefinition**](taskfolder-registertaskdefinition.md) .</span><span class="sxs-lookup"><span data-stu-id="5f737-123">Register the task using the [**TaskFolder.RegisterTaskDefinition**](taskfolder-registertaskdefinition.md) method.</span></span> <span data-ttu-id="5f737-124">Pour cet exemple, la tâche démarre le bloc-notes à l’heure actuelle plus 30 secondes.</span><span class="sxs-lookup"><span data-stu-id="5f737-124">For this example the task will start Notepad at the current time plus 30 seconds.</span></span>

<span data-ttu-id="5f737-125">L’exemple VBScript suivant montre comment planifier une tâche pour exécuter le bloc-notes 30 secondes après l’inscription de la tâche.</span><span class="sxs-lookup"><span data-stu-id="5f737-125">The following VBScript example shows how to schedule a task to execute Notepad 30 seconds after the task is registered.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="5f737-126">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="5f737-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5f737-127">Utilisation de l’Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="5f737-127">Using the Task Scheduler</span></span>](using-the-task-scheduler.md)
</dt> </dl>

 

 




