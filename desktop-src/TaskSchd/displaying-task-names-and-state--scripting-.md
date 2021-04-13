---
title: Affichage des noms et des États des tâches (script)
description: Cet exemple de script montre comment énumérer des tâches dans un dossier de tâches et afficher des valeurs de propriété à partir de chaque tâche.
ms.assetid: 2a84a752-fbf3-4041-8b0a-304f89a49354
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e7a8f22977f8cfd2d40b3c37a1cc8d7bcb5259e1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104380099"
---
# <a name="displaying-task-names-and-states-scripting"></a><span data-ttu-id="562d4-103">Affichage des noms et des États des tâches (script)</span><span class="sxs-lookup"><span data-stu-id="562d4-103">Displaying Task Names and States (Scripting)</span></span>

<span data-ttu-id="562d4-104">Cet exemple de script montre comment énumérer des tâches dans un dossier de tâches et afficher des valeurs de propriété à partir de chaque tâche.</span><span class="sxs-lookup"><span data-stu-id="562d4-104">This scripting example shows how to enumerate tasks in a task folder and display property values from each task.</span></span>

<span data-ttu-id="562d4-105">La procédure suivante décrit comment afficher les noms de tâches et les États de toutes les tâches d’un dossier de tâches.</span><span class="sxs-lookup"><span data-stu-id="562d4-105">The following procedure describes how to display task names and states for all the tasks in a task folder.</span></span>

<span data-ttu-id="562d4-106">**Pour afficher les noms des tâches et l’état de toutes les tâches d’un dossier de tâches**</span><span class="sxs-lookup"><span data-stu-id="562d4-106">**To display task names and state for all the tasks in a task folder**</span></span>

1.  <span data-ttu-id="562d4-107">Créez l’objet [**TaskService**](taskservice.md) .</span><span class="sxs-lookup"><span data-stu-id="562d4-107">Create the [**TaskService**](taskservice.md) object.</span></span>

    <span data-ttu-id="562d4-108">Cet objet vous permet de vous connecter au service Planificateur de tâches et d’accéder à un dossier de tâches spécifique.</span><span class="sxs-lookup"><span data-stu-id="562d4-108">This object allows you to connect to the Task Scheduler service and access a specific task folder.</span></span>

2.  <span data-ttu-id="562d4-109">Récupérez un dossier de tâches qui contient les tâches pour lesquelles vous souhaitez obtenir des informations.</span><span class="sxs-lookup"><span data-stu-id="562d4-109">Get a task folder that holds the tasks you want information about.</span></span>

    <span data-ttu-id="562d4-110">Utilisez la méthode [**TaskService. GetFolder**](taskservice-getfolder.md) pour accéder au dossier.</span><span class="sxs-lookup"><span data-stu-id="562d4-110">Use the [**TaskService.GetFolder**](taskservice-getfolder.md) method to get the folder.</span></span>

3.  <span data-ttu-id="562d4-111">Obtient la collection de tâches à partir du dossier.</span><span class="sxs-lookup"><span data-stu-id="562d4-111">Get the collection of tasks from the folder.</span></span>

    <span data-ttu-id="562d4-112">Utilisez la méthode [**TaskFolder. GetTasks**](taskfolder-gettasks.md) pour récupérer la collection de tâches ([**RegisteredTaskCollection**](registeredtaskcollection.md)).</span><span class="sxs-lookup"><span data-stu-id="562d4-112">Use the [**TaskFolder.GetTasks**](taskfolder-gettasks.md) method to get the collection of tasks ([**RegisteredTaskCollection**](registeredtaskcollection.md)).</span></span>

4.  <span data-ttu-id="562d4-113">Obtient le nombre de tâches dans la collection et énumère chaque tâche de la collection.</span><span class="sxs-lookup"><span data-stu-id="562d4-113">Get the number of tasks in the collection and enumerate through each task in the collection.</span></span>

    <span data-ttu-id="562d4-114">Utilisez la collection [**RegisteredTaskCollection**](registeredtaskcollection.md) d’objets pour obtenir une instance d’objet [**RegisteredTask**](registeredtask.md) .</span><span class="sxs-lookup"><span data-stu-id="562d4-114">Use the [**RegisteredTaskCollection**](registeredtaskcollection.md) collection of objects to get a [**RegisteredTask**](registeredtask.md) object instance.</span></span> <span data-ttu-id="562d4-115">Chaque instance contient une tâche dans la collection.</span><span class="sxs-lookup"><span data-stu-id="562d4-115">Each instance will contain a task in the collection.</span></span> <span data-ttu-id="562d4-116">Vous pouvez ensuite afficher les informations (valeurs de propriété) à partir de chaque tâche inscrite.</span><span class="sxs-lookup"><span data-stu-id="562d4-116">You can then display the information (property values) from each registered task.</span></span>

<span data-ttu-id="562d4-117">L’exemple VBScript suivant montre comment énumérer une collection de tâches inscrites dans le dossier racine de la tâche et afficher le nom et l’état de chaque tâche.</span><span class="sxs-lookup"><span data-stu-id="562d4-117">The following VBScript example shows how to enumerate through a collection of registered tasks in the root task folder and display the name and state for each task.</span></span>


```VB
'---------------------------------------------------------
' This sample enumerates through the tasks on the local computer and
' displays their name and state.
'---------------------------------------------------------


' Create the TaskService object.
Set service = CreateObject("Schedule.Service")
call service.Connect()

' Get the task folder that contains the tasks. 
Dim rootFolder
Set rootFolder = service.GetFolder("\")
 
Dim taskCollection
Set taskCollection = rootFolder.GetTasks(0)

Dim numberOfTasks
numberOfTasks = taskCollection.Count

If numberOfTasks = 0 Then 
    Wscript.Echo "No tasks are registered."
Else
    WScript.Echo "Number of tasks registered: " & numberOfTasks
    
    Dim registeredTask
    For Each registeredTask In taskCollection
        WScript.Echo "Task Name: " & registeredTask.Name
    
        Dim taskState 
        Select Case registeredTask.State 
            Case "0"
                taskState = "Unknown"
            Case "1"
                taskState = "Disabled"
            Case "2"
                taskState = "Queued"
            Case "3"
                taskState = "Ready"
            Case "4"
                taskState = "Running"
        End Select

        WScript.Echo "    Task State: " & taskState
    Next
End If

```



## <a name="related-topics"></a><span data-ttu-id="562d4-118">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="562d4-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="562d4-119">Utilisation de l’Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="562d4-119">Using the Task Scheduler</span></span>](using-the-task-scheduler.md)
</dt> </dl>

 

 




