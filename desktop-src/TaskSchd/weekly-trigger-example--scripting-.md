---
title: Exemple de déclencheur hebdomadaire (script)
description: Cet exemple de script montre comment créer une tâche qui exécute le bloc-notes à 8 00 AM le lundi de chaque semaine.
ms.assetid: 68ef73b0-3780-480e-90fe-940b6e8a5340
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4d9cf627591250c341008ba3a5129c4cc10cad6b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104379764"
---
# <a name="weekly-trigger-example-scripting"></a><span data-ttu-id="40b9a-103">Exemple de déclencheur hebdomadaire (script)</span><span class="sxs-lookup"><span data-stu-id="40b9a-103">Weekly Trigger Example (Scripting)</span></span>

<span data-ttu-id="40b9a-104">Cet exemple de script montre comment créer une tâche qui exécute le bloc-notes à 8:00 AM le lundi de chaque semaine.</span><span class="sxs-lookup"><span data-stu-id="40b9a-104">This scripting example shows how to create a task that runs Notepad at 8:00 AM on Monday of every week.</span></span> <span data-ttu-id="40b9a-105">La tâche contient un déclencheur quotidien qui spécifie le moment d’exécution de la tâche et une action exécutable qui exécute le bloc-notes.</span><span class="sxs-lookup"><span data-stu-id="40b9a-105">The task contains a daily trigger that specifies when the task runs and an executable action that runs Notepad.</span></span>

<span data-ttu-id="40b9a-106">La procédure suivante décrit comment planifier une tâche pour démarrer un exécutable à 8:00 AM le lundi de chaque semaine.</span><span class="sxs-lookup"><span data-stu-id="40b9a-106">The following procedure describes how to schedule a task to start an executable at 8:00 AM on Monday of every week.</span></span>

<span data-ttu-id="40b9a-107">**Pour planifier le démarrage du bloc-notes à 8:00 AM le lundi de chaque semaine**</span><span class="sxs-lookup"><span data-stu-id="40b9a-107">**To schedule Notepad to start at 8:00 AM on Monday of every week**</span></span>

1.  <span data-ttu-id="40b9a-108">Créez un objet [**TaskService**](taskservice.md) .</span><span class="sxs-lookup"><span data-stu-id="40b9a-108">Create a [**TaskService**](taskservice.md) object.</span></span> <span data-ttu-id="40b9a-109">Cet objet vous permet de créer la tâche dans un dossier spécifié.</span><span class="sxs-lookup"><span data-stu-id="40b9a-109">This object allows you to create the task in a specified folder.</span></span>
2.  <span data-ttu-id="40b9a-110">Récupérez un dossier de tâches et créez une tâche.</span><span class="sxs-lookup"><span data-stu-id="40b9a-110">Get a task folder and create a task.</span></span> <span data-ttu-id="40b9a-111">Utilisez la méthode [**TaskService. GetFolder**](taskservice-getfolder.md) pour récupérer le dossier dans lequel la tâche est stockée et la méthode [**TaskService. newtask**](taskservice-newtask.md) pour créer l’objet [**TaskDefinition**](taskdefinition.md) qui représente la tâche.</span><span class="sxs-lookup"><span data-stu-id="40b9a-111">Use the [**TaskService.GetFolder**](taskservice-getfolder.md) method to get the folder where the task is stored and the [**TaskService.NewTask**](taskservice-newtask.md) method to create the [**TaskDefinition**](taskdefinition.md) object that represents the task.</span></span>
3.  <span data-ttu-id="40b9a-112">Définissez des informations sur la tâche à l’aide de l’objet [**TaskDefinition**](taskdefinition.md) .</span><span class="sxs-lookup"><span data-stu-id="40b9a-112">Define information about the task using the [**TaskDefinition**](taskdefinition.md) object.</span></span> <span data-ttu-id="40b9a-113">Utilisez la propriété [**TaskDefinition. Settings**](taskdefinition-settings.md) pour définir les paramètres qui déterminent la façon dont le service Planificateur de tâches effectue la tâche et la propriété [**TaskDefinition. RegistrationInfo**](taskdefinition-registrationinfo.md) pour définir les informations qui décrivent la tâche.</span><span class="sxs-lookup"><span data-stu-id="40b9a-113">Use the [**TaskDefinition.Settings**](taskdefinition-settings.md) property to define the settings that determine how the Task Scheduler service performs the task and the [**TaskDefinition.RegistrationInfo**](taskdefinition-registrationinfo.md) property to define the information that describes the task.</span></span>
4.  <span data-ttu-id="40b9a-114">Créez un déclencheur hebdomadaire à l’aide de la propriété [**TaskDefinition. Triggers**](taskdefinition-triggers.md) .</span><span class="sxs-lookup"><span data-stu-id="40b9a-114">Create a weekly trigger using the [**TaskDefinition.Triggers**](taskdefinition-triggers.md) property.</span></span> <span data-ttu-id="40b9a-115">Cette propriété permet d’accéder à l’objet [**TriggerCollection**](triggercollection.md) utilisé pour créer le déclencheur.</span><span class="sxs-lookup"><span data-stu-id="40b9a-115">This property provides access to the [**TriggerCollection**](triggercollection.md) object that is used to create the trigger.</span></span>

    <span data-ttu-id="40b9a-116">Utilisez la méthode [**TriggerCollection. Create**](triggercollection-create.md) (en spécifiant le type de déclencheur que vous souhaitez créer) pour créer un déclencheur hebdomadaire.</span><span class="sxs-lookup"><span data-stu-id="40b9a-116">Use the [**TriggerCollection.Create**](triggercollection-create.md) method (specifying the type of trigger you want to create) to create a weekly trigger.</span></span>

    <span data-ttu-id="40b9a-117">Définissez la propriété [**WeeklyTrigger. StartBoundary**](trigger-startboundary.md) pour spécifier à quel moment le déclencheur est activé et l’heure de la journée à laquelle la tâche est exécutée.</span><span class="sxs-lookup"><span data-stu-id="40b9a-117">Set the [**WeeklyTrigger.StartBoundary**](trigger-startboundary.md) property to specify when the trigger is activated and the time of the day when the task is run.</span></span> <span data-ttu-id="40b9a-118">Dans cet exemple, le déclencheur est activé le 1er janvier 2005 et la tâche s’exécute à 8:00 AM.</span><span class="sxs-lookup"><span data-stu-id="40b9a-118">In this example the trigger is activated on January 1, 2005 and the task runs at 8:00 AM.</span></span>

    <span data-ttu-id="40b9a-119">Définissez la propriété [**WeeklyTrigger. EndBoundary**](trigger-endboundary.md)pour spécifier le moment où le déclencheur est désactivé.</span><span class="sxs-lookup"><span data-stu-id="40b9a-119">Set the [**WeeklyTrigger.EndBoundary**](trigger-endboundary.md)property to specify when the trigger is deactivated.</span></span> <span data-ttu-id="40b9a-120">Dans cet exemple, le déclencheur est désactivé le 1er janvier 2015.</span><span class="sxs-lookup"><span data-stu-id="40b9a-120">In this example the trigger is deactivated on January 1, 2015.</span></span>

    <span data-ttu-id="40b9a-121">Définissez la propriété [**WeeklyTrigger. DaysOfWeek**](weeklytrigger-daysofweek.md) pour spécifier les jours de la semaine où la tâche est exécutée.</span><span class="sxs-lookup"><span data-stu-id="40b9a-121">Set the [**WeeklyTrigger.DaysOfWeek**](weeklytrigger-daysofweek.md) property to specify the days of the week on which the task runs.</span></span> <span data-ttu-id="40b9a-122">Dans cet exemple, la tâche est exécutée le lundi.</span><span class="sxs-lookup"><span data-stu-id="40b9a-122">In this example the task is run on Monday.</span></span>

    <span data-ttu-id="40b9a-123">Définissez la propriété [**WeeklyTrigger. WeeksInterval**](weeklytrigger-weeksinterval.md)pour spécifier l’intervalle entre les semaines de la planification.</span><span class="sxs-lookup"><span data-stu-id="40b9a-123">Set the [**WeeklyTrigger.WeeksInterval**](weeklytrigger-weeksinterval.md)property to specify the interval between the weeks in the schedule.</span></span> <span data-ttu-id="40b9a-124">Dans cet exemple, la tâche s’exécute toutes les semaines.</span><span class="sxs-lookup"><span data-stu-id="40b9a-124">In this example the task runs every week.</span></span>

5.  <span data-ttu-id="40b9a-125">Créez une action à exécuter par la tâche à l’aide de la propriété [**TaskDefinition. actions**](taskdefinition-actions.md) .</span><span class="sxs-lookup"><span data-stu-id="40b9a-125">Create an action for the task to execute by using the [**TaskDefinition.Actions**](taskdefinition-actions.md) property.</span></span> <span data-ttu-id="40b9a-126">Cette propriété permet d’accéder à l’objet [**ActionCollection**](actioncollection.md) utilisé pour créer l’action.</span><span class="sxs-lookup"><span data-stu-id="40b9a-126">This property provides access to the [**ActionCollection**](actioncollection.md) object used to create the action.</span></span> <span data-ttu-id="40b9a-127">Utilisez la méthode [**ActionCollection. Create**](actioncollection-create.md) pour spécifier le type d’action que vous souhaitez créer.</span><span class="sxs-lookup"><span data-stu-id="40b9a-127">Use the [**ActionCollection.Create**](actioncollection-create.md) method to specify the type of action you want to create.</span></span> <span data-ttu-id="40b9a-128">Cet exemple utilise un objet [**ExecAction**](execaction.md) , qui représente une action qui exécute une opération de ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="40b9a-128">This example uses an [**ExecAction**](execaction.md) object, which represents an action that executes a command-line operation.</span></span>
6.  <span data-ttu-id="40b9a-129">Inscrivez la tâche à l’aide de la méthode [**TaskFolder. RegisterTaskDefinition**](taskfolder-registertaskdefinition.md) .</span><span class="sxs-lookup"><span data-stu-id="40b9a-129">Register the task using the [**TaskFolder.RegisterTaskDefinition**](taskfolder-registertaskdefinition.md) method.</span></span> <span data-ttu-id="40b9a-130">Pour cet exemple, la tâche démarre le bloc-notes à 8:00 AM le lundi de chaque semaine.</span><span class="sxs-lookup"><span data-stu-id="40b9a-130">For this example the task will start Notepad at 8:00 AM on Monday of every week.</span></span>

<span data-ttu-id="40b9a-131">L’exemple VBScript suivant montre comment planifier une tâche pour exécuter le bloc-notes tous les jours à 8:00 AM.</span><span class="sxs-lookup"><span data-stu-id="40b9a-131">The following VBScript example shows how to schedule a task to execute Notepad every day at 8:00 AM.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="40b9a-132">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="40b9a-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="40b9a-133">Utilisation de l’Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="40b9a-133">Using the Task Scheduler</span></span>](using-the-task-scheduler.md)
</dt> </dl>

 

 




