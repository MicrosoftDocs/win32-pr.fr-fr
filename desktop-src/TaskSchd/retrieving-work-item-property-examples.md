---
title: Récupération d’exemples de propriétés d’élément de travail
description: Pour récupérer les propriétés d’un élément de travail, appelez ITaskScheduler Activate pour récupérer l’interface de l’objet d’élément de travail, puis appelez la méthode appropriée pour récupérer la propriété de tâche qui vous intéresse.
ms.assetid: d9723dea-1a82-4993-b4d0-bc7d944e775f
keywords:
- récupération des propriétés de l’élément de travail Planificateur de tâches
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74a51c623301a4a3b53369713abe95ea1dafba80
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382230"
---
# <a name="retrieving-work-item-property-examples"></a><span data-ttu-id="0e861-104">Récupération d’exemples de propriétés d’élément de travail</span><span class="sxs-lookup"><span data-stu-id="0e861-104">Retrieving Work Item Property Examples</span></span>

<span data-ttu-id="0e861-105">Pour récupérer les propriétés d’un élément de travail, appelez [**ITaskScheduler :: Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) pour récupérer l’interface de l’objet d’élément de travail, puis appelez la méthode appropriée pour récupérer la propriété de tâche qui vous intéresse.</span><span class="sxs-lookup"><span data-stu-id="0e861-105">To retrieve the properties of a work item, call [**ITaskScheduler::Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) to retrieve the interface of the work item object, then call the appropriate method to retrieve the task property you are interested in.</span></span> <span data-ttu-id="0e861-106">Actuellement, les seuls éléments de travail valides sont les tâches.</span><span class="sxs-lookup"><span data-stu-id="0e861-106">Currently, the only valid work items are tasks.</span></span>

<span data-ttu-id="0e861-107">Les exemples de code listés en bas de cette page montrent comment récupérer les propriétés qui s’appliquent à tous les éléments de travail.</span><span class="sxs-lookup"><span data-stu-id="0e861-107">The code examples listed at the bottom of this page show how to retrieve the properties that apply to all work items.</span></span> <span data-ttu-id="0e861-108">Pour les autres propriétés qui sont propres aux tâches, consultez [définition d’exemples de propriétés de tâche](setting-task-property-examples.md).</span><span class="sxs-lookup"><span data-stu-id="0e861-108">For other properties that are unique to tasks, see [Setting Task Property Examples](setting-task-property-examples.md).</span></span>

> [!Note]  
> <span data-ttu-id="0e861-109">Dans l’exemple de code suivant, toutes les interfaces sont libérées après qu’elles ne sont plus nécessaires.</span><span class="sxs-lookup"><span data-stu-id="0e861-109">In the following code example, all interfaces are released after they are no longer needed.</span></span>

 

<span data-ttu-id="0e861-110">Notez que si vous récupérez une propriété de type chaîne (par exemple, un commentaire pour un élément de travail), vous devez appeler [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) pour libérer la mémoire allouée pour la chaîne retournée.</span><span class="sxs-lookup"><span data-stu-id="0e861-110">Note that if you are retrieving a string property (such as comment for a work item), you must call [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) to free the memory allocated for the returned string.</span></span>

<span data-ttu-id="0e861-111">La procédure suivante décrit comment récupérer une propriété de tâche.</span><span class="sxs-lookup"><span data-stu-id="0e861-111">The following procedure describes how to retrieve a task property.</span></span>

<span data-ttu-id="0e861-112">**Pour récupérer une propriété de tâche**</span><span class="sxs-lookup"><span data-stu-id="0e861-112">**To retrieve a task property**</span></span>

1.  <span data-ttu-id="0e861-113">Appelez [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) pour initialiser la bibliothèque com et [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) pour obtenir un objet planificateur de tâches.</span><span class="sxs-lookup"><span data-stu-id="0e861-113">Call [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) to initialize the COM library and [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) to get a Task Scheduler object.</span></span> <span data-ttu-id="0e861-114">(Ces exemples supposent que le service Planificateur de tâches est en cours d’exécution.)</span><span class="sxs-lookup"><span data-stu-id="0e861-114">(These examples assume that the Task Scheduler service is running.)</span></span>
2.  <span data-ttu-id="0e861-115">Appelez [**ITaskScheduler :: Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) pour récupérer l’interface [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) de l’objet Task.</span><span class="sxs-lookup"><span data-stu-id="0e861-115">Call [**ITaskScheduler::Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) to get the [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) interface of the task object.</span></span> <span data-ttu-id="0e861-116">(Notez que les tâches sont actuellement le seul type d’élément de travail valide.)</span><span class="sxs-lookup"><span data-stu-id="0e861-116">(Note that tasks are currently the only valid type of work item.)</span></span>
3.  <span data-ttu-id="0e861-117">Appelez la méthode appropriée pour récupérer la propriété qui vous intéresse.</span><span class="sxs-lookup"><span data-stu-id="0e861-117">Call the appropriate method to retrieve the property you are interested in.</span></span>
4.  <span data-ttu-id="0e861-118">Traitez la propriété en fonction des besoins.</span><span class="sxs-lookup"><span data-stu-id="0e861-118">Process the property as needed.</span></span> <span data-ttu-id="0e861-119">(Ces exemples impriment simplement la propriété à l’écran.)</span><span class="sxs-lookup"><span data-stu-id="0e861-119">(These examples simply print the property to the screen.)</span></span>
5.  <span data-ttu-id="0e861-120">Si la propriété retournée est une chaîne, appelez [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) pour libérer la mémoire allouée à la chaîne retournée.</span><span class="sxs-lookup"><span data-stu-id="0e861-120">If the returned property is a string, call [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) to free the memory allocated for the returned string.</span></span>



| <span data-ttu-id="0e861-121">Pour obtenir un exemple de code de</span><span class="sxs-lookup"><span data-stu-id="0e861-121">For a code example of</span></span>                                                                        | <span data-ttu-id="0e861-122">Consultez</span><span class="sxs-lookup"><span data-stu-id="0e861-122">See</span></span>                                                                                                                       |
|----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0e861-123">Récupération des informations de compte d’une tâche connue</span><span class="sxs-lookup"><span data-stu-id="0e861-123">Retrieving the account information of a known task</span></span>                                           | [<span data-ttu-id="0e861-124">Exemple de code C/C++ : récupération des informations de compte de tâche</span><span class="sxs-lookup"><span data-stu-id="0e861-124">C/C++ Code Example: Retrieving Task Account Information</span></span>](c-c-code-example-retrieving-task-account-information.md)       |
| <span data-ttu-id="0e861-125">Récupération de la chaîne de commentaire d’une tâche connue</span><span class="sxs-lookup"><span data-stu-id="0e861-125">Retrieving the comment string of a known task</span></span>                                                | [<span data-ttu-id="0e861-126">Exemple de code C/C++ : récupération d’un commentaire de tâche</span><span class="sxs-lookup"><span data-stu-id="0e861-126">C/C++ Code Example: Retrieving a Task Comment</span></span>](c-c-code-example-retrieving-a-task-comment.md)                           |
| <span data-ttu-id="0e861-127">Récupération du nom du créateur de la tâche et affichage à l’écran</span><span class="sxs-lookup"><span data-stu-id="0e861-127">Retrieving the name of the creator of the task and displaying it on the screen</span></span>               | [<span data-ttu-id="0e861-128">Exemple de code C/C++ : récupération du créateur de tâche</span><span class="sxs-lookup"><span data-stu-id="0e861-128">C/C++ Code Example: Retrieving the Task Creator</span></span>](c-c-code-example-retrieving-the-task-creator.md)                       |
| <span data-ttu-id="0e861-129">Récupération du dernier code de sortie retourné par une tâche connue</span><span class="sxs-lookup"><span data-stu-id="0e861-129">Retrieving the last exit code returned by a known task</span></span>                                       | [<span data-ttu-id="0e861-130">Exemple de code C/C++ : récupération du code de sortie de la tâche</span><span class="sxs-lookup"><span data-stu-id="0e861-130">C/C++ Code Example: Retrieving Task Exit Code</span></span>](c-c-code-example-retrieving-task-exit-code.md)                           |
| <span data-ttu-id="0e861-131">Récupération du temps d’inactivité de la tâche et affichage à l’écran</span><span class="sxs-lookup"><span data-stu-id="0e861-131">Retrieving the idle-wait time of the task and displaying it on the screen</span></span>                    | [<span data-ttu-id="0e861-132">Exemple de code C/C++ : récupération d’une tâche inactive-temps d’attente</span><span class="sxs-lookup"><span data-stu-id="0e861-132">C/C++ Code Example: Retrieving Task Idle-wait Time</span></span>](c-c-code-example-retrieving-task-idle-wait-time.md)                 |
| <span data-ttu-id="0e861-133">Récupération de l’heure de la dernière exécution de la tâche et affichage à l’écran</span><span class="sxs-lookup"><span data-stu-id="0e861-133">Retrieving the time the task was last run and displaying it on the screen</span></span>                    | [<span data-ttu-id="0e861-134">Exemple de code C/C++ : récupération de la tâche MostRecentRun temps</span><span class="sxs-lookup"><span data-stu-id="0e861-134">C/C++ Code Example: Retrieving the Task MostRecentRun Time</span></span>](c-c-code-example-retrieving-the-task-mostrecentrun-time.md) |
| <span data-ttu-id="0e861-135">Récupération la prochaine fois que la tâche est planifiée pour s’exécuter et afficher cette heure à l’écran</span><span class="sxs-lookup"><span data-stu-id="0e861-135">Retrieving the next time the task is scheduled to run and displaying that time on the screen</span></span> | [<span data-ttu-id="0e861-136">Exemple de code C/C++ : récupération de la tâche NextRun temps</span><span class="sxs-lookup"><span data-stu-id="0e861-136">C/C++ Code Example: Retrieving the Task NextRun Time</span></span>](c-c-code-example-retrieving-the-task-nextrun-time.md)             |
| <span data-ttu-id="0e861-137">Récupération des durées d’exécution de la tâche et affichage de celles-ci à l’écran</span><span class="sxs-lookup"><span data-stu-id="0e861-137">Retrieving the run times of the task and displaying them on the screen</span></span>                       | [<span data-ttu-id="0e861-138">Exemple de code C/C++ : récupération des durées d’exécution des tâches</span><span class="sxs-lookup"><span data-stu-id="0e861-138">C/C++ Code Example: Retrieving Task Run Times</span></span>](c-c-code-example-retrieving-task-run-times.md)                           |
| <span data-ttu-id="0e861-139">Récupération de l’état actuel de la tâche et affichage à l’écran</span><span class="sxs-lookup"><span data-stu-id="0e861-139">Retrieving the current status of the task and displaying it on the screen</span></span>                    | [<span data-ttu-id="0e861-140">Exemple de code C/C++ : récupération de l’état de la tâche</span><span class="sxs-lookup"><span data-stu-id="0e861-140">C/C++ Code Example: Retrieving Task Status</span></span>](c-c-code-example-retrieving-task-status.md)                                 |



 

## <a name="related-topics"></a><span data-ttu-id="0e861-141">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="0e861-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0e861-142">Exemples de Planificateur de tâches 1,0</span><span class="sxs-lookup"><span data-stu-id="0e861-142">Task Scheduler 1.0 Examples</span></span>](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 