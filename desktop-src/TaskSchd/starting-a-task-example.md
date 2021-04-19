---
title: Exemple de démarrage d’une tâche
description: Pour démarrer une tâche, appelez la méthode Run de l’interface ITask. Run est une méthode asynchrone qui tente d’exécuter la tâche et retourne dès que la tâche a démarré. Le service de Planificateur de tâches doit être en cours d’exécution pour que cette méthode aboutisse.
ms.assetid: 90f197de-7a32-4e4b-b4c0-d3f706e47de1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 325d8d990367a810351ec4eea8b03b7dc0240cd5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106545745"
---
# <a name="starting-a-task-example"></a><span data-ttu-id="035d2-105">Exemple de démarrage d’une tâche</span><span class="sxs-lookup"><span data-stu-id="035d2-105">Starting a Task Example</span></span>

<span data-ttu-id="035d2-106">Pour démarrer une tâche, appelez la méthode [**Run**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-run) de l’interface [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) .</span><span class="sxs-lookup"><span data-stu-id="035d2-106">To start a task, call the [**Run**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-run) method of the [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) interface.</span></span> <span data-ttu-id="035d2-107">**Run** est une méthode asynchrone qui tente d’exécuter la tâche et retourne dès que la tâche a démarré.</span><span class="sxs-lookup"><span data-stu-id="035d2-107">**Run** is an asynchronous method that attempts to execute the task and returns as soon as the task has started.</span></span> <span data-ttu-id="035d2-108">Le service de Planificateur de tâches doit être en cours d’exécution pour que cette méthode aboutisse.</span><span class="sxs-lookup"><span data-stu-id="035d2-108">The Task Scheduler service must be running for this method to succeed.</span></span>

<span data-ttu-id="035d2-109">La procédure suivante décrit comment démarrer une tâche.</span><span class="sxs-lookup"><span data-stu-id="035d2-109">The following procedure describes how to start a task.</span></span>

<span data-ttu-id="035d2-110">**Pour démarrer une tâche**</span><span class="sxs-lookup"><span data-stu-id="035d2-110">**To start a task**</span></span>

1.  <span data-ttu-id="035d2-111">Appelez [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) pour initialiser la bibliothèque com et [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) pour obtenir un objet planificateur de tâches.</span><span class="sxs-lookup"><span data-stu-id="035d2-111">Call [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) to initialize the COM library and [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) to get a Task Scheduler object.</span></span> <span data-ttu-id="035d2-112">(Cet exemple suppose que le service Planificateur de tâches est en cours d’exécution.)</span><span class="sxs-lookup"><span data-stu-id="035d2-112">(This example assumes that the Task Scheduler service is running.)</span></span>
2.  <span data-ttu-id="035d2-113">Appelez [**ITaskScheduler :: Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) pour récupérer l’interface [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) de l’objet Task.</span><span class="sxs-lookup"><span data-stu-id="035d2-113">Call [**ITaskScheduler::Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) to get the [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) interface of the task object.</span></span> <span data-ttu-id="035d2-114">(Notez que cet exemple obtient la tâche « tester la tâche ».)</span><span class="sxs-lookup"><span data-stu-id="035d2-114">(Note that this example gets the "Test Task" task.)</span></span>
3.  <span data-ttu-id="035d2-115">Appelez [**Run**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-run) pour démarrer la tâche.</span><span class="sxs-lookup"><span data-stu-id="035d2-115">Call [**Run**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-run) to start the task.</span></span> <span data-ttu-id="035d2-116">Notez que cette méthode est héritée par l’interface [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) .</span><span class="sxs-lookup"><span data-stu-id="035d2-116">Note that this method is inherited by the [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) interface.</span></span>
4.  <span data-ttu-id="035d2-117">Poursuivez le traitement en fonction des besoins.</span><span class="sxs-lookup"><span data-stu-id="035d2-117">Continue processing as needed.</span></span>
5.  <span data-ttu-id="035d2-118">Appelez **ITask :: Release** pour libérer des ressources et [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) pour annuler l’initialisation de com.</span><span class="sxs-lookup"><span data-stu-id="035d2-118">Call **ITask::Release** to free resources and [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) to uninitialize COM.</span></span> <span data-ttu-id="035d2-119">Cet exemple appelle [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) pour libérer le pointeur vers l’interface [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) .</span><span class="sxs-lookup"><span data-stu-id="035d2-119">This example calls [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) to free the pointer to the [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) interface.</span></span> <span data-ttu-id="035d2-120">(Notez que **Release** est une méthode [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) héritée par **ITask**.)</span><span class="sxs-lookup"><span data-stu-id="035d2-120">(Note that **Release** is an [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) method inherited by **ITask**.)</span></span>



| <span data-ttu-id="035d2-121">Pour obtenir un exemple de code de</span><span class="sxs-lookup"><span data-stu-id="035d2-121">For a code example of</span></span>    | <span data-ttu-id="035d2-122">Consultez</span><span class="sxs-lookup"><span data-stu-id="035d2-122">See</span></span>                                                                         |
|--------------------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="035d2-123">Exécution d’une tâche existante</span><span class="sxs-lookup"><span data-stu-id="035d2-123">Running an existing task</span></span> | [<span data-ttu-id="035d2-124">Exemple de code C/C++ : démarrage d’une tâche</span><span class="sxs-lookup"><span data-stu-id="035d2-124">C/C++ Code Example: Starting a Task</span></span>](c-c-code-example-starting-a-task.md) |



 

## <a name="related-topics"></a><span data-ttu-id="035d2-125">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="035d2-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="035d2-126">Exemples de Planificateur de tâches 1,0</span><span class="sxs-lookup"><span data-stu-id="035d2-126">Task Scheduler 1.0 Examples</span></span>](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 