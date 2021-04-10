---
description: Dans le gestionnaire d’autorisations, une tâche est une action de haut niveau que les utilisateurs d’une application doivent effectuer.
ms.assetid: a266dde7-86f8-4537-99a5-be7142e765c6
title: Regroupement d’opérations en tâches dans un script
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: fb7fc1d4a84cd42dc0ae48af4fcbf02412b93337
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867830"
---
# <a name="grouping-operations-into-tasks-in-script"></a><span data-ttu-id="67ab2-103">Regroupement d’opérations en tâches dans un script</span><span class="sxs-lookup"><span data-stu-id="67ab2-103">Grouping Operations into Tasks in Script</span></span>

<span data-ttu-id="67ab2-104">Dans le gestionnaire d’autorisations, une tâche est une action de haut niveau que les utilisateurs d’une application doivent effectuer.</span><span class="sxs-lookup"><span data-stu-id="67ab2-104">In Authorization Manager, a task is a high-level action that users of an application need to complete.</span></span> <span data-ttu-id="67ab2-105">Les tâches sont constituées d’opérations, qui sont des fonctions de bas niveau et des méthodes de l’application.</span><span class="sxs-lookup"><span data-stu-id="67ab2-105">Tasks are made up of operations, which are low-level functions and methods of the application.</span></span> <span data-ttu-id="67ab2-106">Une tâche est ensuite affectée aux rôles qui doivent effectuer cette tâche.</span><span class="sxs-lookup"><span data-stu-id="67ab2-106">A task is then assigned to those roles that must perform that task.</span></span> <span data-ttu-id="67ab2-107">Une tâche est représentée par un objet [**IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) .</span><span class="sxs-lookup"><span data-stu-id="67ab2-107">A task is represented by an [**IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) object.</span></span> <span data-ttu-id="67ab2-108">Pour plus d’informations sur les opérations et les tâches, consultez [opérations et tâches](operations-and-tasks.md).</span><span class="sxs-lookup"><span data-stu-id="67ab2-108">For more information about operations and tasks, see [Operations and Tasks](operations-and-tasks.md).</span></span>

<span data-ttu-id="67ab2-109">L’exemple suivant montre comment regrouper des opérations pour créer une tâche.</span><span class="sxs-lookup"><span data-stu-id="67ab2-109">The following example shows how to group operations to create a task.</span></span> <span data-ttu-id="67ab2-110">L’exemple suppose qu’il existe un magasin de stratégies XML nommé MyStore.xml dans le répertoire racine du lecteur C, que ce magasin contient une application nommée Expense et que cette application contient des opérations définies dans la rubrique [définition d’opérations dans le script](defining-operations-in-script.md).</span><span class="sxs-lookup"><span data-stu-id="67ab2-110">The example assumes that there is an existing XML policy store named MyStore.xml in the root directory of drive C, that this store contains an application named Expense, and that this application contains operations defined in the topic [Defining Operations in Script](defining-operations-in-script.md).</span></span>


```VB
'  Create the AzAuthorizationStore object.
Dim AzManStore
Set AzManStore = CreateObject("AzRoles.AzAuthorizationStore")

'  Initialize the authorization store.
AzManStore.Initialize 2, "msxml://C:\MyStore.xml"

'  Create an application object in the store.
Dim expenseApp
Set expenseApp= AzManStore.OpenApplication("Expense")

'  Create a task object.
Dim Task1
Set Task1 = expenseApp.CreateTask("Submit Expense")

'  Add operations to the task.
Task1.AddOperation CStr("RetrieveForm")
Task1.AddOperation CStr("EnqueRequest")
Task1.AddOperation Cstr("UseFormControl")

'  Save the task to the store.
Task1.Submit
```



 

 



