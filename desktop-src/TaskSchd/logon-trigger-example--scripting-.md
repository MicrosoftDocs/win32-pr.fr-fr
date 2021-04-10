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
# <a name="logon-trigger-example-scripting"></a><span data-ttu-id="33f57-103">Exemple de déclencheur LOGON (script)</span><span class="sxs-lookup"><span data-stu-id="33f57-103">Logon Trigger Example (Scripting)</span></span>

<span data-ttu-id="33f57-104">Cet exemple de script montre comment créer une tâche qui est planifiée pour exécuter le bloc-notes lorsqu’un utilisateur ouvre une session.</span><span class="sxs-lookup"><span data-stu-id="33f57-104">This scripting example shows how to create a task that is scheduled to execute Notepad when a user logs on.</span></span> <span data-ttu-id="33f57-105">La tâche contient un déclencheur d’ouverture de session qui spécifie une limite de début pour le démarrage de la tâche et un identificateur d’utilisateur qui spécifie l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="33f57-105">The task contains a logon trigger that specifies a start boundary for the task to start and a user identifier that specifies the user.</span></span> <span data-ttu-id="33f57-106">La tâche est inscrite à l’aide du groupe administrateurs comme contexte de sécurité pour l’exécution de la tâche.</span><span class="sxs-lookup"><span data-stu-id="33f57-106">The task is registered using the Administrators group as a security context to run the task.</span></span>

<span data-ttu-id="33f57-107">La procédure suivante décrit comment planifier le démarrage d’un exécutable, tel que le bloc-notes, lorsqu’un utilisateur spécifié ouvre une session.</span><span class="sxs-lookup"><span data-stu-id="33f57-107">The following procedure describes how to schedule an executable such as Notepad to start when a specified user logs on.</span></span>

<span data-ttu-id="33f57-108">**Pour planifier le démarrage du bloc-notes quand un utilisateur ouvre une session**</span><span class="sxs-lookup"><span data-stu-id="33f57-108">**To schedule Notepad to start when a user logs on**</span></span>

1.  <span data-ttu-id="33f57-109">Créez un objet [**TaskService**](taskservice.md) .</span><span class="sxs-lookup"><span data-stu-id="33f57-109">Create a [**TaskService**](taskservice.md) object.</span></span> <span data-ttu-id="33f57-110">Cet objet vous permet de créer la tâche dans un dossier spécifié.</span><span class="sxs-lookup"><span data-stu-id="33f57-110">This object allows you to create the task in a specified folder.</span></span>
2.  <span data-ttu-id="33f57-111">Récupérez un dossier de tâches et créez une tâche.</span><span class="sxs-lookup"><span data-stu-id="33f57-111">Get a task folder and create a task.</span></span> <span data-ttu-id="33f57-112">Utilisez la méthode [**TaskService. GetFolder**](taskservice-getfolder.md) pour récupérer le dossier dans lequel la tâche est stockée et la méthode [**TaskService. newtask**](taskservice-newtask.md) pour créer l’objet [**TaskDefinition**](taskdefinition.md) qui représente la tâche.</span><span class="sxs-lookup"><span data-stu-id="33f57-112">Use the [**TaskService.GetFolder**](taskservice-getfolder.md) method to get the folder where the task is stored and the [**TaskService.NewTask**](taskservice-newtask.md) method to create the [**TaskDefinition**](taskdefinition.md) object that represents the task.</span></span>
3.  <span data-ttu-id="33f57-113">Définissez des informations sur la tâche à l’aide de l’objet [**TaskDefinition**](taskdefinition.md) .</span><span class="sxs-lookup"><span data-stu-id="33f57-113">Define information about the task using the [**TaskDefinition**](taskdefinition.md) object.</span></span> <span data-ttu-id="33f57-114">Utilisez la propriété [**TaskDefinition. Settings**](taskdefinition-settings.md) pour définir les paramètres qui déterminent la façon dont le service Planificateur de tâches effectue la tâche et la propriété [**TaskDefinition. RegistrationInfo**](taskdefinition-registrationinfo.md) pour définir les informations qui décrivent la tâche.</span><span class="sxs-lookup"><span data-stu-id="33f57-114">Use the [**TaskDefinition.Settings**](taskdefinition-settings.md) property to define the settings that determine how the Task Scheduler service performs the task and the [**TaskDefinition.RegistrationInfo**](taskdefinition-registrationinfo.md) property to define the information that describes the task.</span></span>
4.  <span data-ttu-id="33f57-115">Créez un déclencheur de connexion à l’aide de la propriété [**TaskDefinition. Triggers**](taskdefinition-triggers.md) .</span><span class="sxs-lookup"><span data-stu-id="33f57-115">Create a logon trigger using the [**TaskDefinition.Triggers**](taskdefinition-triggers.md) property.</span></span> <span data-ttu-id="33f57-116">Cette propriété permet d’accéder à l’objet [**TriggerCollection**](triggercollection.md) .</span><span class="sxs-lookup"><span data-stu-id="33f57-116">This property provides access to the [**TriggerCollection**](triggercollection.md) object.</span></span> <span data-ttu-id="33f57-117">Utilisez la méthode [**TriggerCollection. Create**](triggercollection-create.md) (en spécifiant le type de déclencheur que vous souhaitez créer) pour créer un déclencheur Logon.</span><span class="sxs-lookup"><span data-stu-id="33f57-117">Use the [**TriggerCollection.Create**](triggercollection-create.md) method (specifying the type of trigger that you want to create) to create a logon trigger.</span></span> <span data-ttu-id="33f57-118">Lorsque vous créez le déclencheur, définissez les limites de début et de fin du déclencheur pour activer et désactiver le déclencheur.</span><span class="sxs-lookup"><span data-stu-id="33f57-118">As you create the trigger, set the start boundary and end boundary of the trigger to activate and deactivate the trigger.</span></span> <span data-ttu-id="33f57-119">Vous devez définir la propriété [**userid**](/windows/desktop/api/taskschd/nf-taskschd-ilogontrigger-get_userid) pour le déclencheur afin que les actions de la tâche soient planifiées pour s’exécuter lorsque l’utilisateur spécifié se connecte après la limite de début.</span><span class="sxs-lookup"><span data-stu-id="33f57-119">You must set the [**UserId**](/windows/desktop/api/taskschd/nf-taskschd-ilogontrigger-get_userid) property for the trigger so that the task's actions will be scheduled to execute when the specified user logs on after the start boundary.</span></span>
5.  <span data-ttu-id="33f57-120">Créez une action à exécuter par la tâche à l’aide de la propriété [**TaskDefinition. actions**](taskdefinition-actions.md) .</span><span class="sxs-lookup"><span data-stu-id="33f57-120">Create an action for the task to execute by using the [**TaskDefinition.Actions**](taskdefinition-actions.md) property.</span></span> <span data-ttu-id="33f57-121">Cette propriété permet d’accéder à l’objet [**ActionCollection**](actioncollection.md) .</span><span class="sxs-lookup"><span data-stu-id="33f57-121">This property provides access to the [**ActionCollection**](actioncollection.md) object.</span></span> <span data-ttu-id="33f57-122">Utilisez la méthode [**ActionCollection. Create**](actioncollection-create.md) pour spécifier le type d’action que vous souhaitez créer.</span><span class="sxs-lookup"><span data-stu-id="33f57-122">Use the [**ActionCollection.Create**](actioncollection-create.md) method to specify the type of action that you want to create.</span></span> <span data-ttu-id="33f57-123">Cet exemple utilise un objet [**ExecAction**](execaction.md) , qui représente une action qui démarre un exécutable.</span><span class="sxs-lookup"><span data-stu-id="33f57-123">This example uses an [**ExecAction**](execaction.md) object, which represents an action that starts an executable.</span></span>
6.  <span data-ttu-id="33f57-124">Inscrivez la tâche à l’aide de la méthode [**TaskFolder. RegisterTaskDefinition**](taskfolder-registertaskdefinition.md) .</span><span class="sxs-lookup"><span data-stu-id="33f57-124">Register the task using the [**TaskFolder.RegisterTaskDefinition**](taskfolder-registertaskdefinition.md) method.</span></span> <span data-ttu-id="33f57-125">Cet exemple inscrit la tâche pour qu’elle utilise le groupe administrateurs comme contexte de sécurité pour l’exécution de la tâche.</span><span class="sxs-lookup"><span data-stu-id="33f57-125">This example registers the task so that it uses the Administrators group as a security context to run the task.</span></span>

<span data-ttu-id="33f57-126">L’exemple VBScript suivant montre comment planifier une tâche pour exécuter le bloc-notes lorsqu’un utilisateur ouvre une session.</span><span class="sxs-lookup"><span data-stu-id="33f57-126">The following VBScript example shows how to schedule a task to execute Notepad when a user logs on.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="33f57-127">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="33f57-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="33f57-128">Utilisation de l’Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="33f57-128">Using the Task Scheduler</span></span>](using-the-task-scheduler.md)
</dt> </dl>

 

 




