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
# <a name="daily-trigger-example-scripting"></a><span data-ttu-id="a6592-103">Exemple de déclencheur quotidien (script)</span><span class="sxs-lookup"><span data-stu-id="a6592-103">Daily Trigger Example (Scripting)</span></span>

<span data-ttu-id="a6592-104">Cet exemple de script montre comment créer une tâche qui exécute le bloc-notes à 8:00 AM tous les jours.</span><span class="sxs-lookup"><span data-stu-id="a6592-104">This scripting example shows how to create a task that runs Notepad at 8:00 AM every day.</span></span> <span data-ttu-id="a6592-105">La tâche contient un déclencheur quotidien qui spécifie une limite de départ pour activer le déclencheur et spécifier l’heure d’exécution de la tâche, un intervalle de déclencheur pour spécifier que la tâche s’exécute tous les jours et une limite de fin pour désactiver le déclencheur.</span><span class="sxs-lookup"><span data-stu-id="a6592-105">The task contains a daily trigger that specifies a start boundary to activate the trigger and to specify the time of day that the task runs, a trigger interval to specify that the task runs every day, and an end boundary to deactivates the trigger.</span></span> <span data-ttu-id="a6592-106">L’exemple montre également comment définir un modèle de répétition pour le déclencheur afin de répéter la tâche.</span><span class="sxs-lookup"><span data-stu-id="a6592-106">The example also shows how to set a repetition pattern for the trigger to repeat the task.</span></span> <span data-ttu-id="a6592-107">La tâche contient également une action exécutable qui exécute le bloc-notes.</span><span class="sxs-lookup"><span data-stu-id="a6592-107">The task also contains an executable action that runs Notepad.</span></span>

<span data-ttu-id="a6592-108">La procédure suivante décrit comment planifier une tâche pour démarrer un exécutable à 8:00 AM tous les jours.</span><span class="sxs-lookup"><span data-stu-id="a6592-108">The following procedure describes how to schedule a task to start an executable at 8:00 AM every day.</span></span> <span data-ttu-id="a6592-109">(Ces étapes correspondent aux commentaires de code inclus dans l’exemple de code.)</span><span class="sxs-lookup"><span data-stu-id="a6592-109">(These steps correspond to the code comments included in the example code.)</span></span>

<span data-ttu-id="a6592-110">**Pour planifier le démarrage du bloc-notes à 8:00 AM tous les jours**</span><span class="sxs-lookup"><span data-stu-id="a6592-110">**To schedule Notepad to start at 8:00 AM every day**</span></span>

1.  <span data-ttu-id="a6592-111">Créez un objet [**TaskService**](taskservice.md) .</span><span class="sxs-lookup"><span data-stu-id="a6592-111">Create a [**TaskService**](taskservice.md) object.</span></span> <span data-ttu-id="a6592-112">Cet objet vous permet de créer la tâche dans un dossier spécifié.</span><span class="sxs-lookup"><span data-stu-id="a6592-112">This object allows you to create the task in a specified folder.</span></span>
2.  <span data-ttu-id="a6592-113">Récupérez un dossier de tâches et créez une tâche.</span><span class="sxs-lookup"><span data-stu-id="a6592-113">Get a task folder and create a task.</span></span> <span data-ttu-id="a6592-114">Utilisez la méthode [**TaskService. GetFolder**](taskservice-getfolder.md) pour récupérer le dossier dans lequel la tâche est stockée et la méthode [**TaskService. newtask**](taskservice-newtask.md) pour créer l’objet [**TaskDefinition**](taskdefinition.md) qui représente la tâche.</span><span class="sxs-lookup"><span data-stu-id="a6592-114">Use the [**TaskService.GetFolder**](taskservice-getfolder.md) method to get the folder where the task is stored and the [**TaskService.NewTask**](taskservice-newtask.md) method to create the [**TaskDefinition**](taskdefinition.md) object that represents the task.</span></span>
3.  <span data-ttu-id="a6592-115">Définissez des informations sur la tâche à l’aide de l’objet [**TaskDefinition**](taskdefinition.md) .</span><span class="sxs-lookup"><span data-stu-id="a6592-115">Define information about the task using the [**TaskDefinition**](taskdefinition.md) object.</span></span> <span data-ttu-id="a6592-116">Utilisez la propriété [**TaskDefinition. Settings**](taskdefinition-settings.md) pour définir les paramètres qui déterminent la façon dont le service Planificateur de tâches effectue la tâche et la propriété [**TaskDefinition. RegistrationInfo**](taskdefinition-registrationinfo.md) pour définir les informations qui décrivent la tâche.</span><span class="sxs-lookup"><span data-stu-id="a6592-116">Use the [**TaskDefinition.Settings**](taskdefinition-settings.md) property to define the settings that determine how the Task Scheduler service performs the task and the [**TaskDefinition.RegistrationInfo**](taskdefinition-registrationinfo.md) property to define the information that describes the task.</span></span>
4.  <span data-ttu-id="a6592-117">Créez un déclencheur quotidien à l’aide de la propriété [**TaskDefinition. Triggers**](taskdefinition-triggers.md) .</span><span class="sxs-lookup"><span data-stu-id="a6592-117">Create a daily trigger using the [**TaskDefinition.Triggers**](taskdefinition-triggers.md) property.</span></span> <span data-ttu-id="a6592-118">Cette propriété permet d’accéder à l’objet [**TriggerCollection**](triggercollection.md) utilisé pour créer le déclencheur.</span><span class="sxs-lookup"><span data-stu-id="a6592-118">This property provides access to the [**TriggerCollection**](triggercollection.md) object that is used to create the trigger.</span></span> <span data-ttu-id="a6592-119">Utilisez la méthode [**TriggerCollection. Create**](triggercollection-create.md) (en spécifiant le type de déclencheur que vous souhaitez créer) pour créer un déclencheur quotidien.</span><span class="sxs-lookup"><span data-stu-id="a6592-119">Use the [**TriggerCollection.Create**](triggercollection-create.md) method (specifying the type of trigger you want to create) to create a daily trigger.</span></span> <span data-ttu-id="a6592-120">Lorsque vous créez le déclencheur, définissez la limite de démarrage pour activer le déclencheur et spécifier l’heure d’exécution de la tâche, l’intervalle entre les jours et la limite de fin pour désactiver le déclencheur.</span><span class="sxs-lookup"><span data-stu-id="a6592-120">As you create the trigger, set the start boundary to activate the trigger and specify the time of day that the task runs, the interval between the days, and the end boundary to deactivate the trigger.</span></span> <span data-ttu-id="a6592-121">L’exemple ci-dessous montre comment définir un modèle de répétition pour le déclencheur afin de répéter la tâche.</span><span class="sxs-lookup"><span data-stu-id="a6592-121">The example below shows how to set a repetition pattern for the trigger to repeat the task.</span></span>
5.  <span data-ttu-id="a6592-122">Créez une action à exécuter par la tâche à l’aide de la propriété [**TaskDefinition. actions**](taskdefinition-actions.md) .</span><span class="sxs-lookup"><span data-stu-id="a6592-122">Create an action for the task to execute by using the [**TaskDefinition.Actions**](taskdefinition-actions.md) property.</span></span> <span data-ttu-id="a6592-123">Cette propriété permet d’accéder à l’objet [**ActionCollection**](actioncollection.md) utilisé pour créer l’action.</span><span class="sxs-lookup"><span data-stu-id="a6592-123">This property provides access to the [**ActionCollection**](actioncollection.md) object used to create the action.</span></span> <span data-ttu-id="a6592-124">Utilisez la méthode [**ActionCollection. Create**](actioncollection-create.md) pour spécifier le type d’action que vous souhaitez créer.</span><span class="sxs-lookup"><span data-stu-id="a6592-124">Use the [**ActionCollection.Create**](actioncollection-create.md) method to specify the type of action you want to create.</span></span> <span data-ttu-id="a6592-125">Cet exemple utilise un objet [**ExecAction**](execaction.md) , qui représente une action qui exécute une opération de ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="a6592-125">This example uses an [**ExecAction**](execaction.md) object, which represents an action that executes a command-line operation.</span></span>
6.  <span data-ttu-id="a6592-126">Inscrivez la tâche à l’aide de la méthode [**TaskFolder. RegisterTaskDefinition**](taskfolder-registertaskdefinition.md) .</span><span class="sxs-lookup"><span data-stu-id="a6592-126">Register the task using the [**TaskFolder.RegisterTaskDefinition**](taskfolder-registertaskdefinition.md) method.</span></span> <span data-ttu-id="a6592-127">Pour cet exemple, la tâche démarre le bloc-notes à 8:00 AM tous les jours.</span><span class="sxs-lookup"><span data-stu-id="a6592-127">For this example the task will start Notepad at 8:00 AM every day.</span></span>

<span data-ttu-id="a6592-128">L’exemple VBScript suivant montre comment planifier une tâche pour exécuter le bloc-notes tous les jours à 8:00 AM.</span><span class="sxs-lookup"><span data-stu-id="a6592-128">The following VBScript example shows how to schedule a task to execute Notepad every day at 8:00 AM.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="a6592-129">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a6592-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a6592-130">Utilisation de l’Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="a6592-130">Using the Task Scheduler</span></span>](using-the-task-scheduler.md)
</dt> </dl>

 

 




