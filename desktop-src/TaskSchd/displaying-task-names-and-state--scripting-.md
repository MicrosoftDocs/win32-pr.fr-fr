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
# <a name="displaying-task-names-and-states-scripting"></a>Affichage des noms et des États des tâches (script)

Cet exemple de script montre comment énumérer des tâches dans un dossier de tâches et afficher des valeurs de propriété à partir de chaque tâche.

La procédure suivante décrit comment afficher les noms de tâches et les États de toutes les tâches d’un dossier de tâches.

**Pour afficher les noms des tâches et l’état de toutes les tâches d’un dossier de tâches**

1.  Créez l’objet [**TaskService**](taskservice.md) .

    Cet objet vous permet de vous connecter au service Planificateur de tâches et d’accéder à un dossier de tâches spécifique.

2.  Récupérez un dossier de tâches qui contient les tâches pour lesquelles vous souhaitez obtenir des informations.

    Utilisez la méthode [**TaskService. GetFolder**](taskservice-getfolder.md) pour accéder au dossier.

3.  Obtient la collection de tâches à partir du dossier.

    Utilisez la méthode [**TaskFolder. GetTasks**](taskfolder-gettasks.md) pour récupérer la collection de tâches ([**RegisteredTaskCollection**](registeredtaskcollection.md)).

4.  Obtient le nombre de tâches dans la collection et énumère chaque tâche de la collection.

    Utilisez la collection [**RegisteredTaskCollection**](registeredtaskcollection.md) d’objets pour obtenir une instance d’objet [**RegisteredTask**](registeredtask.md) . Chaque instance contient une tâche dans la collection. Vous pouvez ensuite afficher les informations (valeurs de propriété) à partir de chaque tâche inscrite.

L’exemple VBScript suivant montre comment énumérer une collection de tâches inscrites dans le dossier racine de la tâche et afficher le nom et l’état de chaque tâche.


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



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation de l’Planificateur de tâches](using-the-task-scheduler.md)
</dt> </dl>

 

 




