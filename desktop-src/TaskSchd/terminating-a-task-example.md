---
title: Exemple de fin d’une tâche
description: Vous pouvez arrêter une tâche pendant qu’elle s’exécute en appelant IScheduledWorkItem Terminate.
ms.assetid: f8401650-e196-4959-8f23-3d649a55f73d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73e632b00a9e957849a5735d31018e3444113190
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104199315"
---
# <a name="terminating-a-task-example"></a><span data-ttu-id="0472e-103">Exemple de fin d’une tâche</span><span class="sxs-lookup"><span data-stu-id="0472e-103">Terminating a Task Example</span></span>

<span data-ttu-id="0472e-104">Vous pouvez arrêter une tâche pendant qu’elle s’exécute en appelant [**IScheduledWorkItem :: Terminate**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-terminate).</span><span class="sxs-lookup"><span data-stu-id="0472e-104">You can terminate a task while it is running by calling [**IScheduledWorkItem::Terminate**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-terminate).</span></span>

<span data-ttu-id="0472e-105">La procédure suivante décrit comment arrêter une tâche si elle est en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="0472e-105">The following procedure describes how to terminate a task if it is running.</span></span>

<span data-ttu-id="0472e-106">**Pour arrêter une tâche si elle est en cours d’exécution**</span><span class="sxs-lookup"><span data-stu-id="0472e-106">**To terminate a task if it is running**</span></span>

1.  <span data-ttu-id="0472e-107">Appelez [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) pour initialiser la bibliothèque com et [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) pour obtenir un objet planificateur de tâches.</span><span class="sxs-lookup"><span data-stu-id="0472e-107">Call [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) to initialize the COM library and [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) to get a Task Scheduler object.</span></span> <span data-ttu-id="0472e-108">(Cet exemple suppose que le service Planificateur de tâches est en cours d’exécution.)</span><span class="sxs-lookup"><span data-stu-id="0472e-108">(This example assumes that the Task Scheduler service is running.)</span></span>
2.  <span data-ttu-id="0472e-109">Appelez [**ITaskScheduler :: Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) pour récupérer l’interface [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) de l’objet Task.</span><span class="sxs-lookup"><span data-stu-id="0472e-109">Call [**ITaskScheduler::Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) to get the [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) interface of the task object.</span></span> <span data-ttu-id="0472e-110">(Notez que cet exemple obtient la tâche « tester la tâche ».)</span><span class="sxs-lookup"><span data-stu-id="0472e-110">(Note that this example gets the "Test Task" task.)</span></span>
3.  <span data-ttu-id="0472e-111">Appelez **ITask :: GetStatus** pour déterminer si la tâche est en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="0472e-111">Call **ITask::GetStatus** to find out if the task is running.</span></span> <span data-ttu-id="0472e-112">(Notez que [**GetStatus**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-getstatus) est une méthode [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) héritée par [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask).)</span><span class="sxs-lookup"><span data-stu-id="0472e-112">(Note that [**GetStatus**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-getstatus) is an [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) method inherited by [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask).)</span></span>
4.  <span data-ttu-id="0472e-113">Vérifiez l’état de la tâche, puis appelez **ITask :: Terminate** si la tâche est en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="0472e-113">Check the status of the task and then call **ITask::Terminate** if the task is running.</span></span> <span data-ttu-id="0472e-114">(Notez que [**Terminate**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-terminate) est une méthode [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) héritée par [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask).)</span><span class="sxs-lookup"><span data-stu-id="0472e-114">(Note that [**Terminate**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-terminate) is an [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) method inherited by [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask).)</span></span>



| <span data-ttu-id="0472e-115">Pour obtenir un exemple de code de</span><span class="sxs-lookup"><span data-stu-id="0472e-115">For a code example of</span></span>                | <span data-ttu-id="0472e-116">Consultez</span><span class="sxs-lookup"><span data-stu-id="0472e-116">See</span></span>                                                                               |
|--------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="0472e-117">Vérification de l’état d’une tâche connue</span><span class="sxs-lookup"><span data-stu-id="0472e-117">Verifying the status of a known task</span></span> | [<span data-ttu-id="0472e-118">Exemple de code C/C++ : fin d’une tâche</span><span class="sxs-lookup"><span data-stu-id="0472e-118">C/C++ Code Example: Terminating a Task</span></span>](c-c-code-example-terminating-a-task.md) |



 

## <a name="related-topics"></a><span data-ttu-id="0472e-119">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="0472e-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0472e-120">Exemples de Planificateur de tâches 1,0</span><span class="sxs-lookup"><span data-stu-id="0472e-120">Task Scheduler 1.0 Examples</span></span>](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 