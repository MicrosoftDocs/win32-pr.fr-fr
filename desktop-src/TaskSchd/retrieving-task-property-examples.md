---
title: Récupération d’exemples de propriétés de tâche
description: Pour récupérer les propriétés d’une tâche, appelez ITaskScheduler Activate pour récupérer l’interface de l’objet de tâche, puis appelez la méthode ITask appropriée pour récupérer la propriété de tâche qui vous intéresse.
ms.assetid: 9ec9d836-c735-4a32-96b1-3dbd0a31b22a
keywords:
- récupération des propriétés de la tâche Planificateur de tâches
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e2b42bc8044171834b6d99e97c41e3f5c7048ff
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104316049"
---
# <a name="retrieving-task-property-examples"></a><span data-ttu-id="bc580-104">Récupération d’exemples de propriétés de tâche</span><span class="sxs-lookup"><span data-stu-id="bc580-104">Retrieving Task Property Examples</span></span>

<span data-ttu-id="bc580-105">Pour récupérer les propriétés d’une tâche, appelez [**ITaskScheduler :: Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) pour obtenir la récupération de l’interface de l’objet de tâche, puis appelez la méthode [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) appropriée pour récupérer la propriété de tâche qui vous intéresse.</span><span class="sxs-lookup"><span data-stu-id="bc580-105">To retrieve the properties of a task, call [**ITaskScheduler::Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) to get retrieve the interface of the task object, then call the appropriate [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) method to retrieve the task property that you are interested in.</span></span> <span data-ttu-id="bc580-106">Les exemples de code figurant en bas de la page montrent comment récupérer les différentes propriétés des tâches.</span><span class="sxs-lookup"><span data-stu-id="bc580-106">The code examples listed at the bottom of the page show how to retrieve the different task properties.</span></span>

<span data-ttu-id="bc580-107">Les exemples de code répertoriés en bas de la page montrent comment récupérer les propriétés qui sont propres aux objets de tâche.</span><span class="sxs-lookup"><span data-stu-id="bc580-107">The code examples listed at the bottom of the page show how to retrieve the properties that are unique to task objects.</span></span> <span data-ttu-id="bc580-108">Pour les autres propriétés d' [*élément de travail*](w.md) qui s’appliquent également aux tâches, consultez récupération d’exemples d' [éléments de travail](retrieving-work-item-property-examples.md).</span><span class="sxs-lookup"><span data-stu-id="bc580-108">For other [*work item*](w.md) properties that also apply to tasks, see [Retrieving Work Item Examples](retrieving-work-item-property-examples.md).</span></span>

> [!Note]  
> <span data-ttu-id="bc580-109">Dans l’exemple de code suivant, toutes les interfaces sont libérées après qu’elles ne sont plus nécessaires.</span><span class="sxs-lookup"><span data-stu-id="bc580-109">In the following code example, all interfaces are released after they are no longer needed.</span></span>

 

<span data-ttu-id="bc580-110">Notez que si vous récupérez une propriété de type chaîne (par exemple, le nom de l’application, les paramètres ou le répertoire de travail), vous devez appeler [CoTaskMemFree](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) pour libérer la mémoire allouée pour la chaîne retournée.</span><span class="sxs-lookup"><span data-stu-id="bc580-110">Note that if you are retrieving a string property (such as the application name, parameters, or working directory), you must call [CoTaskMemFree](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) to free the memory allocated for the returned string.</span></span>

<span data-ttu-id="bc580-111">La procédure suivante décrit comment récupérer une propriété de tâche.</span><span class="sxs-lookup"><span data-stu-id="bc580-111">The following procedure describes how to retrieve a task property.</span></span>

<span data-ttu-id="bc580-112">**Pour récupérer une propriété de tâche**</span><span class="sxs-lookup"><span data-stu-id="bc580-112">**To retrieve a task property**</span></span>

1.  <span data-ttu-id="bc580-113">Appelez [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) pour initialiser la bibliothèque com et [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) pour obtenir un objet planificateur de tâches.</span><span class="sxs-lookup"><span data-stu-id="bc580-113">Call [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) to initialize the COM library and [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) to get a Task Scheduler object.</span></span> <span data-ttu-id="bc580-114">(Ces exemples supposent que le service Planificateur de tâches est en cours d’exécution.)</span><span class="sxs-lookup"><span data-stu-id="bc580-114">(These examples assume that the Task Scheduler service is running.)</span></span>
2.  <span data-ttu-id="bc580-115">Appelez [**ITaskScheduler :: Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) pour récupérer l’interface [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) de l’objet Task.</span><span class="sxs-lookup"><span data-stu-id="bc580-115">Call [**ITaskScheduler::Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) to get the [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) interface of the task object.</span></span> <span data-ttu-id="bc580-116">(Notez que cet exemple obtient la tâche « tester la tâche ».)</span><span class="sxs-lookup"><span data-stu-id="bc580-116">(Note that this example gets the "Test Task" task.)</span></span>
3.  <span data-ttu-id="bc580-117">Appelez la méthode [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) appropriée pour récupérer la propriété qui vous intéresse.</span><span class="sxs-lookup"><span data-stu-id="bc580-117">Call the appropriate [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) method to retrieve the property you are interested in.</span></span>
4.  <span data-ttu-id="bc580-118">Traitez la propriété en fonction des besoins.</span><span class="sxs-lookup"><span data-stu-id="bc580-118">Process the property as needed.</span></span> <span data-ttu-id="bc580-119">(Ces exemples impriment la propriété à l’écran.)</span><span class="sxs-lookup"><span data-stu-id="bc580-119">(These examples print the property to the screen.)</span></span>
5.  <span data-ttu-id="bc580-120">Si la propriété retournée est une chaîne, appelez [CoTaskMemFree](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) pour libérer la mémoire allouée à la chaîne retournée.</span><span class="sxs-lookup"><span data-stu-id="bc580-120">If the returned property is a string, call [CoTaskMemFree](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) to free the memory allocated for the returned string.</span></span>



| <span data-ttu-id="bc580-121">Pour obtenir un exemple de code de</span><span class="sxs-lookup"><span data-stu-id="bc580-121">For a code example of</span></span>                                                                                                                           | <span data-ttu-id="bc580-122">Consultez</span><span class="sxs-lookup"><span data-stu-id="bc580-122">See</span></span>                                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bc580-123">Récupération du nom de l’application associée à une tâche donnée</span><span class="sxs-lookup"><span data-stu-id="bc580-123">Retrieving the name of the application associated with a given task</span></span>                                                                             | [<span data-ttu-id="bc580-124">Exemple de code C/C++ : récupération du nom de l’application de tâche</span><span class="sxs-lookup"><span data-stu-id="bc580-124">C/C++ Code Example: Retrieving the Task Application Name</span></span>](c-c-code-example-retrieving-the-task-application-name.md)   |
| <span data-ttu-id="bc580-125">Récupération de la durée maximale pendant laquelle la tâche peut s’exécuter et afficher ce nombre à l’écran</span><span class="sxs-lookup"><span data-stu-id="bc580-125">Retrieving the maximum amount of time the task can run and displaying that number on the screen</span></span>                                                 | [<span data-ttu-id="bc580-126">Exemple de code C/C++ : récupération de la tâche durée maximale</span><span class="sxs-lookup"><span data-stu-id="bc580-126">C/C++ Code Example: Retrieving the Task MaxRunTime</span></span>](c-c-code-example-retrieving-the-task-maxruntime.md)               |
| <span data-ttu-id="bc580-127">Récupération de la chaîne de paramètre qui est exécutée lorsque la tâche est exécutée et affiche cette chaîne à l’écran</span><span class="sxs-lookup"><span data-stu-id="bc580-127">Retrieving the parameter string that is executed when the task is run and displaying that string on the screen</span></span>                                  | [<span data-ttu-id="bc580-128">Exemple de code C/C++ : récupération des paramètres de tâche</span><span class="sxs-lookup"><span data-stu-id="bc580-128">C/C++ Code Example: Retrieving Task Parameters</span></span>](c-c-code-example-retrieving-task-parameters.md)                       |
| <span data-ttu-id="bc580-129">Récupération du [*niveau de priorité*](p.md) de la tâche</span><span class="sxs-lookup"><span data-stu-id="bc580-129">Retrieving the [*priority level*](p.md) of the task</span></span>                                                                    | [<span data-ttu-id="bc580-130">Exemple de code C/C++ : récupération de la priorité d’une tâche</span><span class="sxs-lookup"><span data-stu-id="bc580-130">C/C++ Code Example: Retrieving Task Priority</span></span>](c-c-code-example-retrieving-task-priority.md)                           |
| <span data-ttu-id="bc580-131">Récupération du [*Répertoire de travail*](w.md) d’une tâche et affichage du chemin d’accès au répertoire de travail à l’écran</span><span class="sxs-lookup"><span data-stu-id="bc580-131">Retrieving the [*working directory*](w.md) of a task and displaying the path to the working directory on the screen</span></span> | [<span data-ttu-id="bc580-132">Exemple de code C/C++ : récupération du répertoire de travail des tâches</span><span class="sxs-lookup"><span data-stu-id="bc580-132">C/C++ Code Example: Retrieving the Task Working Directory</span></span>](c-c-code-example-retrieving-the-task-working-directory.md) |



 

## <a name="related-topics"></a><span data-ttu-id="bc580-133">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="bc580-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bc580-134">Exemples de Planificateur de tâches 1,0</span><span class="sxs-lookup"><span data-stu-id="bc580-134">Task Scheduler 1.0 Examples</span></span>](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 