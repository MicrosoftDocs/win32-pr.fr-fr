---
title: Exemple de déclencheur de démarrage (script)
description: Cet exemple de script montre comment créer une tâche qui est planifiée pour exécuter le bloc-notes lors du démarrage du système.
ms.assetid: 73ae9cc4-ef89-4390-ac05-8a773f45fa46
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 72b7735c607dfc39b848532a70e4d24b1a14d346
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029223"
---
# <a name="boot-trigger-example-scripting"></a><span data-ttu-id="56f4a-103">Exemple de déclencheur de démarrage (script)</span><span class="sxs-lookup"><span data-stu-id="56f4a-103">Boot Trigger Example (Scripting)</span></span>

<span data-ttu-id="56f4a-104">Cet exemple de script montre comment créer une tâche qui est planifiée pour exécuter le bloc-notes lors du démarrage du système.</span><span class="sxs-lookup"><span data-stu-id="56f4a-104">This scripting example shows how to create a task that is scheduled to execute Notepad when the system is booted.</span></span> <span data-ttu-id="56f4a-105">La tâche contient un déclencheur de démarrage qui spécifie une limite de début et le délai de démarrage de la tâche après le démarrage du système.</span><span class="sxs-lookup"><span data-stu-id="56f4a-105">The task contains a boot trigger that specifies a start boundary and delay time for the task to start after the system is booted.</span></span> <span data-ttu-id="56f4a-106">La tâche contient également une action qui spécifie la tâche d’exécution du bloc-notes.</span><span class="sxs-lookup"><span data-stu-id="56f4a-106">The task also contains an action that specifies the task to execute Notepad.</span></span> <span data-ttu-id="56f4a-107">La tâche est inscrite en utilisant le compte de service local comme contexte de sécurité pour exécuter la tâche.</span><span class="sxs-lookup"><span data-stu-id="56f4a-107">The task is registered using the Local Service account as a security context to run the task.</span></span>

<span data-ttu-id="56f4a-108">La procédure suivante décrit comment planifier le démarrage d’un exécutable, tel que le bloc-notes, lors du démarrage du système.</span><span class="sxs-lookup"><span data-stu-id="56f4a-108">The following procedure describes how to schedule an executable such as Notepad to start when the system is booted.</span></span>

<span data-ttu-id="56f4a-109">**Pour planifier le démarrage du bloc-notes lors du démarrage du système**</span><span class="sxs-lookup"><span data-stu-id="56f4a-109">**To schedule Notepad to start when the system is booted**</span></span>

1.  <span data-ttu-id="56f4a-110">Créez un objet [**TaskService**](taskservice.md) .</span><span class="sxs-lookup"><span data-stu-id="56f4a-110">Create a [**TaskService**](taskservice.md) object.</span></span> <span data-ttu-id="56f4a-111">Cet objet vous permet de créer la tâche dans un dossier spécifié.</span><span class="sxs-lookup"><span data-stu-id="56f4a-111">This object allows you to create the task in a specified folder.</span></span>
2.  <span data-ttu-id="56f4a-112">Récupérez un dossier de tâches et créez une tâche.</span><span class="sxs-lookup"><span data-stu-id="56f4a-112">Get a task folder and create a task.</span></span> <span data-ttu-id="56f4a-113">Utilisez la méthode [**TaskService. GetFolder**](taskservice-getfolder.md) pour récupérer le dossier dans lequel la tâche est stockée et la méthode [**TaskService. newtask**](taskservice-newtask.md) pour créer l’objet [**TaskDefinition**](taskdefinition.md) qui représente la tâche.</span><span class="sxs-lookup"><span data-stu-id="56f4a-113">Use the [**TaskService.GetFolder**](taskservice-getfolder.md) method to get the folder where the task is stored and the [**TaskService.NewTask**](taskservice-newtask.md) method to create the [**TaskDefinition**](taskdefinition.md) object that represents the task.</span></span>
3.  <span data-ttu-id="56f4a-114">Définissez des informations sur la tâche à l’aide de l’objet [**TaskDefinition**](taskdefinition.md) .</span><span class="sxs-lookup"><span data-stu-id="56f4a-114">Define information about the task using the [**TaskDefinition**](taskdefinition.md) object.</span></span> <span data-ttu-id="56f4a-115">Utilisez la propriété [**TaskDefinition. Settings**](taskdefinition-settings.md) pour définir les paramètres qui déterminent la façon dont le service Planificateur de tâches effectue la tâche et la propriété [**TaskDefinition. RegistrationInfo**](taskdefinition-registrationinfo.md) pour définir les informations qui décrivent la tâche.</span><span class="sxs-lookup"><span data-stu-id="56f4a-115">Use the [**TaskDefinition.Settings**](taskdefinition-settings.md) property to define the settings that determine how the Task Scheduler service performs the task and the [**TaskDefinition.RegistrationInfo**](taskdefinition-registrationinfo.md) property to define the information that describes the task.</span></span>
4.  <span data-ttu-id="56f4a-116">Créez un déclencheur de connexion à l’aide de la propriété [**TaskDefinition. Triggers**](taskdefinition-triggers.md) .</span><span class="sxs-lookup"><span data-stu-id="56f4a-116">Create a logon trigger using the [**TaskDefinition.Triggers**](taskdefinition-triggers.md) property.</span></span> <span data-ttu-id="56f4a-117">Cette propriété permet d’accéder à l’objet [**TriggerCollection**](triggercollection.md) .</span><span class="sxs-lookup"><span data-stu-id="56f4a-117">This property provides access to the [**TriggerCollection**](triggercollection.md) object.</span></span> <span data-ttu-id="56f4a-118">Utilisez la méthode [**TriggerCollection. Create**](triggercollection-create.md) (en spécifiant le type de déclencheur que vous souhaitez créer) pour créer un déclencheur de démarrage.</span><span class="sxs-lookup"><span data-stu-id="56f4a-118">Use the [**TriggerCollection.Create**](triggercollection-create.md) method (specifying the type of trigger that you want to create) to create a boot trigger.</span></span> <span data-ttu-id="56f4a-119">Au fur et à mesure que vous créez le déclencheur, définissez les propriétés [**StartBoundary**](trigger-startboundary.md) et [**EndBoundary**](trigger-endboundary.md) du déclencheur pour activer et désactiver le déclencheur.</span><span class="sxs-lookup"><span data-stu-id="56f4a-119">As you create the trigger, set the [**StartBoundary**](trigger-startboundary.md) and [**EndBoundary**](trigger-endboundary.md) properties of the trigger to activate and deactivate the trigger.</span></span> <span data-ttu-id="56f4a-120">Vous pouvez également spécifier une valeur pour la propriété [**delay**](boottrigger-delay.md) du déclencheur de démarrage.</span><span class="sxs-lookup"><span data-stu-id="56f4a-120">You can also specify a value for the [**Delay**](boottrigger-delay.md) property of the boot trigger.</span></span>
5.  <span data-ttu-id="56f4a-121">Créez une action à exécuter par la tâche à l’aide de la propriété [**TaskDefinition. actions**](taskdefinition-actions.md) .</span><span class="sxs-lookup"><span data-stu-id="56f4a-121">Create an action for the task to execute by using the [**TaskDefinition.Actions**](taskdefinition-actions.md) property.</span></span> <span data-ttu-id="56f4a-122">Cette propriété permet d’accéder à l’objet [**ActionCollection**](actioncollection.md) .</span><span class="sxs-lookup"><span data-stu-id="56f4a-122">This property provides access to the [**ActionCollection**](actioncollection.md) object.</span></span> <span data-ttu-id="56f4a-123">Utilisez la méthode [**ActionCollection. Create**](actioncollection-create.md) pour spécifier le type d’action que vous souhaitez créer.</span><span class="sxs-lookup"><span data-stu-id="56f4a-123">Use the [**ActionCollection.Create**](actioncollection-create.md) method to specify the type of action that you want to create.</span></span> <span data-ttu-id="56f4a-124">Cet exemple utilise un objet [**ExecAction**](execaction.md) , qui représente une action qui démarre un exécutable.</span><span class="sxs-lookup"><span data-stu-id="56f4a-124">This example uses an [**ExecAction**](execaction.md) object, which represents an action that starts an executable.</span></span>
6.  <span data-ttu-id="56f4a-125">Inscrivez la tâche à l’aide de la méthode [**TaskFolder. RegisterTaskDefinition**](taskfolder-registertaskdefinition.md) .</span><span class="sxs-lookup"><span data-stu-id="56f4a-125">Register the task using the [**TaskFolder.RegisterTaskDefinition**](taskfolder-registertaskdefinition.md) method.</span></span> <span data-ttu-id="56f4a-126">La tâche est inscrite en utilisant le compte de service local comme contexte de sécurité pour exécuter la tâche.</span><span class="sxs-lookup"><span data-stu-id="56f4a-126">The task is registered using the Local Service account as a security context to run the task.</span></span>

<span data-ttu-id="56f4a-127">L’exemple VBScript suivant montre comment planifier une tâche pour exécuter le bloc-notes 30 secondes après le démarrage du système.</span><span class="sxs-lookup"><span data-stu-id="56f4a-127">The following VBScript example shows how to schedule a task to execute Notepad 30 seconds after the system is booted.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="56f4a-128">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="56f4a-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="56f4a-129">Utilisation de l’Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="56f4a-129">Using the Task Scheduler</span></span>](using-the-task-scheduler.md)
</dt> </dl>

 

 




