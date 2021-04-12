---
title: Exemple de déclencheur d’inscription (script)
description: Cet exemple de script montre comment créer une tâche qui est planifiée pour exécuter le bloc-notes lorsqu’une tâche est inscrite.
ms.assetid: 956b3a21-7d36-4d06-be84-690884ba653a
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: bce6271927e74e31f25b3ac86783b35899bbd862
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311419"
---
# <a name="registration-trigger-example-scripting"></a><span data-ttu-id="8d1f9-103">Exemple de déclencheur d’inscription (script)</span><span class="sxs-lookup"><span data-stu-id="8d1f9-103">Registration Trigger Example (Scripting)</span></span>

<span data-ttu-id="8d1f9-104">Cet exemple de script montre comment créer une tâche qui est planifiée pour exécuter le bloc-notes lorsqu’une tâche est inscrite.</span><span class="sxs-lookup"><span data-stu-id="8d1f9-104">This scripting example shows how to create a task that is scheduled to execute Notepad when a task is registered.</span></span> <span data-ttu-id="8d1f9-105">La tâche contient un déclencheur d’inscription qui spécifie une limite de début et une limite de fin pour la tâche.</span><span class="sxs-lookup"><span data-stu-id="8d1f9-105">The task contains a registration trigger that specifies a start boundary and an end boundary for the task.</span></span> <span data-ttu-id="8d1f9-106">La limite de début spécifie le moment où le déclencheur est activé.</span><span class="sxs-lookup"><span data-stu-id="8d1f9-106">The start boundary specifies when the trigger is activated.</span></span> <span data-ttu-id="8d1f9-107">La tâche contient également une action qui spécifie la tâche d’exécution du bloc-notes.</span><span class="sxs-lookup"><span data-stu-id="8d1f9-107">The task also contains an action that specifies the task to execute Notepad.</span></span>

> [!Note]  
> <span data-ttu-id="8d1f9-108">Quand une tâche avec un déclencheur d’inscription est mise à jour, la tâche s’exécute une fois la mise à jour effectuée.</span><span class="sxs-lookup"><span data-stu-id="8d1f9-108">When a task with a registration trigger is updated, the task will execute after the update occurs.</span></span>

 

<span data-ttu-id="8d1f9-109">La procédure suivante décrit comment planifier le démarrage d’un exécutable, tel que le bloc-notes, lorsqu’une tâche est inscrite.</span><span class="sxs-lookup"><span data-stu-id="8d1f9-109">The following procedure describes how to schedule an executable such as Notepad to start when a task is registered.</span></span>

<span data-ttu-id="8d1f9-110">**Pour planifier le démarrage du bloc-notes quand une tâche est inscrite**</span><span class="sxs-lookup"><span data-stu-id="8d1f9-110">**To schedule Notepad to start when a task is registered**</span></span>

1.  <span data-ttu-id="8d1f9-111">Créez un objet [**TaskService**](taskservice.md) .</span><span class="sxs-lookup"><span data-stu-id="8d1f9-111">Create a [**TaskService**](taskservice.md) object.</span></span> <span data-ttu-id="8d1f9-112">Cet objet vous permet de créer la tâche dans un dossier spécifié.</span><span class="sxs-lookup"><span data-stu-id="8d1f9-112">This object allows you to create the task in a specified folder.</span></span>
2.  <span data-ttu-id="8d1f9-113">Récupérez un dossier de tâches et créez une tâche.</span><span class="sxs-lookup"><span data-stu-id="8d1f9-113">Get a task folder and create a task.</span></span> <span data-ttu-id="8d1f9-114">Utilisez la méthode [**TaskService. GetFolder**](taskservice-getfolder.md) pour récupérer le dossier dans lequel la tâche est stockée et la méthode [**TaskService. newtask**](taskservice-newtask.md) pour créer l’objet [**TaskDefinition**](taskdefinition.md) qui représente la tâche.</span><span class="sxs-lookup"><span data-stu-id="8d1f9-114">Use the [**TaskService.GetFolder**](taskservice-getfolder.md) method to get the folder where the task is stored and the [**TaskService.NewTask**](taskservice-newtask.md) method to create the [**TaskDefinition**](taskdefinition.md) object that represents the task.</span></span>
3.  <span data-ttu-id="8d1f9-115">Définissez des informations sur la tâche à l’aide de l’objet [**TaskDefinition**](taskdefinition.md) .</span><span class="sxs-lookup"><span data-stu-id="8d1f9-115">Define information about the task using the [**TaskDefinition**](taskdefinition.md) object.</span></span> <span data-ttu-id="8d1f9-116">Utilisez la propriété [**TaskDefinition. Settings**](taskdefinition-settings.md) pour définir les paramètres qui déterminent la façon dont le service Planificateur de tâches effectue la tâche et la propriété [**TaskDefinition. RegistrationInfo**](taskdefinition-registrationinfo.md) pour définir les informations qui décrivent la tâche.</span><span class="sxs-lookup"><span data-stu-id="8d1f9-116">Use the [**TaskDefinition.Settings**](taskdefinition-settings.md) property to define the settings that determine how the Task Scheduler service performs the task and the [**TaskDefinition.RegistrationInfo**](taskdefinition-registrationinfo.md) property to define the information that describes the task.</span></span>
4.  <span data-ttu-id="8d1f9-117">Créez un déclencheur d’inscription à l’aide de la propriété [**TaskDefinition. Triggers**](taskdefinition-triggers.md) .</span><span class="sxs-lookup"><span data-stu-id="8d1f9-117">Create a registration trigger using the [**TaskDefinition.Triggers**](taskdefinition-triggers.md) property.</span></span> <span data-ttu-id="8d1f9-118">Cette propriété permet d’accéder à l’objet [**TriggerCollection**](triggercollection.md) .</span><span class="sxs-lookup"><span data-stu-id="8d1f9-118">This property provides access to the [**TriggerCollection**](triggercollection.md) object.</span></span> <span data-ttu-id="8d1f9-119">Utilisez la méthode [**TriggerCollection. Create**](triggercollection-create.md) (en spécifiant le type de déclencheur que vous souhaitez créer) pour créer un déclencheur d’inscription.</span><span class="sxs-lookup"><span data-stu-id="8d1f9-119">Use the [**TriggerCollection.Create**](triggercollection-create.md) method (specifying the type of trigger that you want to create) to create a registration trigger.</span></span>
5.  <span data-ttu-id="8d1f9-120">Créez une action à exécuter par la tâche à l’aide de la propriété [**TaskDefinition. actions**](taskdefinition-actions.md) .</span><span class="sxs-lookup"><span data-stu-id="8d1f9-120">Create an action for the task to execute by using the [**TaskDefinition.Actions**](taskdefinition-actions.md) property.</span></span> <span data-ttu-id="8d1f9-121">Cette propriété permet d’accéder à l’objet [**ActionCollection**](actioncollection.md) .</span><span class="sxs-lookup"><span data-stu-id="8d1f9-121">This property provides access to the [**ActionCollection**](actioncollection.md) object.</span></span> <span data-ttu-id="8d1f9-122">Utilisez la méthode [**ActionCollection. Create**](actioncollection-create.md) pour spécifier le type d’action que vous souhaitez créer.</span><span class="sxs-lookup"><span data-stu-id="8d1f9-122">Use the [**ActionCollection.Create**](actioncollection-create.md) method to specify the type of action that you want to create.</span></span> <span data-ttu-id="8d1f9-123">Cet exemple utilise un objet [**ExecAction**](execaction.md) , qui représente une action qui démarre un exécutable.</span><span class="sxs-lookup"><span data-stu-id="8d1f9-123">This example uses an [**ExecAction**](execaction.md) object, which represents an action that starts an executable.</span></span>
6.  <span data-ttu-id="8d1f9-124">Inscrivez la tâche à l’aide de la méthode [**TaskFolder. RegisterTaskDefinition**](taskfolder-registertaskdefinition.md) .</span><span class="sxs-lookup"><span data-stu-id="8d1f9-124">Register the task using the [**TaskFolder.RegisterTaskDefinition**](taskfolder-registertaskdefinition.md) method.</span></span>

<span data-ttu-id="8d1f9-125">L’exemple VBScript suivant montre comment créer une tâche qui planifie l’exécution du bloc-notes quand la tâche est inscrite.</span><span class="sxs-lookup"><span data-stu-id="8d1f9-125">The following VBScript example shows how to create a task that schedules Notepad to execute when the task is registered.</span></span>


```VB
'---------------------------------------------------------
' This sample schedules a task to start notepad.exe when
' the task is registered.
'---------------------------------------------------------

' A constant that specifies a registration trigger.
const TriggerTypeRegistration = 7
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
regInfo.Description = "Start Notepad when the task is registered."
regInfo.Author = "Author Name"

' Set the task setting info for the Task Scheduler by
' creating a TaskSettings object.
Dim settings
Set settings = taskDefinition.Settings
settings.StartWhenAvailable = True

'********************************************************
' Create a registration trigger.
Dim triggers
Set triggers = taskDefinition.Triggers

Dim trigger
Set trigger = triggers.Create(TriggerTypeRegistration)

trigger.ExecutionTimeLimit = "PT5M"    'Five minutes
trigger.Id = "RegistrationTriggerId"   

'***********************************************************
' Create the action for the task to execute.

' Add an action to the task. The action executes Notepad.
Dim Action
Set Action = taskDefinition.Actions.Create( ActionTypeExecutable )
Action.Path = "C:\Windows\System32\notepad.exe"

WScript.Echo "Task definition created. About to submit the task..."

'***********************************************************
' Register (create) the task.

call rootFolder.RegisterTaskDefinition( _
    "Test Registration Trigger", taskDefinition, 6, , , 3)

WScript.Echo "Task submitted."

```



## <a name="related-topics"></a><span data-ttu-id="8d1f9-126">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="8d1f9-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8d1f9-127">Utilisation de l’Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="8d1f9-127">Using the Task Scheduler</span></span>](using-the-task-scheduler.md)
</dt> </dl>

 

 




