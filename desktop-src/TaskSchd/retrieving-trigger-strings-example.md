---
title: Exemple de récupération de chaînes de déclencheur
description: Vous pouvez récupérer les chaînes de déclenchement d’un déclencheur connu à l’aide de l’interface IScheduledWorkItem ou ITaskTrigger, selon le type d’objet que vous utilisez.
ms.assetid: adfa95b1-54f0-4bcd-a260-ca76fd77d43e
keywords:
- récupération des chaînes de déclencheur Planificateur de tâches
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f44708fdbb4025f5d99409297dda65504a909aec
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106511700"
---
# <a name="retrieving-trigger-strings-example"></a><span data-ttu-id="7463c-104">Exemple de récupération de chaînes de déclencheur</span><span class="sxs-lookup"><span data-stu-id="7463c-104">Retrieving Trigger Strings Example</span></span>

<span data-ttu-id="7463c-105">Vous pouvez récupérer les chaînes de déclenchement d’un déclencheur connu à l’aide de l’interface [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) ou [**ITaskTrigger**](/windows/desktop/api/Mstask/nn-mstask-itasktrigger) , selon le type d’objet que vous utilisez.</span><span class="sxs-lookup"><span data-stu-id="7463c-105">You can retrieve the trigger strings of a known trigger using the [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) or [**ITaskTrigger**](/windows/desktop/api/Mstask/nn-mstask-itasktrigger) interface, depending on the type of object you are working with.</span></span>

<span data-ttu-id="7463c-106">Lors de l’utilisation d’un [*objet Task*](t.md), utilisez les méthodes de l’interface [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) pour récupérer les chaînes de déclenchement d’un élément de travail.</span><span class="sxs-lookup"><span data-stu-id="7463c-106">When working with a [*task object*](t.md), use the methods of the [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) interface to retrieve the trigger strings of a work item.</span></span>

<span data-ttu-id="7463c-107">Lorsque vous travaillez avec un [*objet déclencheur de tâche*](t.md), utilisez les méthodes de l’interface [**ITaskTrigger**](/windows/desktop/api/Mstask/nn-mstask-itasktrigger) pour récupérer la chaîne de déclenchement du déclencheur.</span><span class="sxs-lookup"><span data-stu-id="7463c-107">When you are working with a [*task trigger object*](t.md), use the methods of the [**ITaskTrigger**](/windows/desktop/api/Mstask/nn-mstask-itasktrigger) interface to retrieve the trigger string of the trigger.</span></span>

<span data-ttu-id="7463c-108">L’exemple suivant montre comment utiliser [**IScheduledWorkItem :: GetTriggerString**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-gettriggerstring) pour afficher les chaînes de tous les déclencheurs associés à une tâche connue.</span><span class="sxs-lookup"><span data-stu-id="7463c-108">The following example shows how to use [**IScheduledWorkItem::GetTriggerString**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-gettriggerstring) to display the strings of all triggers associated with a known task.</span></span>

<span data-ttu-id="7463c-109">La procédure suivante décrit comment récupérer les chaînes de déclenchement d’une tâche.</span><span class="sxs-lookup"><span data-stu-id="7463c-109">The following procedure describes how to retrieve the trigger strings of a task.</span></span>

<span data-ttu-id="7463c-110">**Pour récupérer les chaînes de déclenchement d’une tâche**</span><span class="sxs-lookup"><span data-stu-id="7463c-110">**To retrieve the trigger strings of a task**</span></span>

1.  <span data-ttu-id="7463c-111">Appelez [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) pour initialiser la bibliothèque com et [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) pour obtenir un objet planificateur de tâches.</span><span class="sxs-lookup"><span data-stu-id="7463c-111">Call [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) to initialize the COM library and [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) to get a Task Scheduler object.</span></span> <span data-ttu-id="7463c-112">(Cet exemple suppose que le service Planificateur de tâches est en cours d’exécution.)</span><span class="sxs-lookup"><span data-stu-id="7463c-112">(This example assumes that the Task Scheduler service is running.)</span></span>
2.  <span data-ttu-id="7463c-113">Appelez [**ITaskScheduler :: Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) pour récupérer l’interface [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) de l’objet Task.</span><span class="sxs-lookup"><span data-stu-id="7463c-113">Call [**ITaskScheduler::Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) to get the [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) interface of the task object.</span></span> <span data-ttu-id="7463c-114">(Notez que cet exemple obtient la tâche « tester la tâche ».)</span><span class="sxs-lookup"><span data-stu-id="7463c-114">(Note that this example gets the "Test Task" task.)</span></span>
3.  <span data-ttu-id="7463c-115">Appelez **ITask :: GetTriggerCount** pour connaître le nombre de déclencheurs associés à une tâche.</span><span class="sxs-lookup"><span data-stu-id="7463c-115">Call **ITask::GetTriggerCount** to find out how many triggers are associated with a task.</span></span> <span data-ttu-id="7463c-116">(Notez que [**GetTriggerCount**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-gettriggercount) est une méthode [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) héritée par [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask).)</span><span class="sxs-lookup"><span data-stu-id="7463c-116">(Note that [**GetTriggerCount**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-gettriggercount) is an [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) method inherited by [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask).)</span></span>
4.  <span data-ttu-id="7463c-117">Affichez les chaînes de déclenchement, en appelant **ITask :: GetTriggerString** pour chaque déclencheur associé à la tâche.</span><span class="sxs-lookup"><span data-stu-id="7463c-117">Display the trigger strings, calling **ITask::GetTriggerString** for each trigger associated with the task.</span></span> <span data-ttu-id="7463c-118">(Notez que [**GetTriggerString**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-gettriggerstring) est une méthode [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) héritée par [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask).)</span><span class="sxs-lookup"><span data-stu-id="7463c-118">(Note that [**GetTriggerString**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-gettriggerstring) is an [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) method inherited by [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask).)</span></span>
5.  <span data-ttu-id="7463c-119">Libérer toutes les ressources.</span><span class="sxs-lookup"><span data-stu-id="7463c-119">Release all resources.</span></span> <span data-ttu-id="7463c-120">Appelez [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) pour libérer les chaînes de déclenchement et **ITask :: Release** pour libérer l’interface [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) .</span><span class="sxs-lookup"><span data-stu-id="7463c-120">Call [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) to release the trigger strings and **ITask::Release** to release the [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) interface.</span></span> <span data-ttu-id="7463c-121">(Notez que [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) est une méthode [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) héritée par **ITask**.)</span><span class="sxs-lookup"><span data-stu-id="7463c-121">(Note that [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) is an [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) method inherited by **ITask**.)</span></span>



| <span data-ttu-id="7463c-122">Pour obtenir un exemple de code de</span><span class="sxs-lookup"><span data-stu-id="7463c-122">For a code example of</span></span>                                                         | <span data-ttu-id="7463c-123">Consultez</span><span class="sxs-lookup"><span data-stu-id="7463c-123">See</span></span>                                                                                         |
|-------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="7463c-124">Récupération d’une chaîne de déclenchement pour tous les déclencheurs associés à une tâche connue</span><span class="sxs-lookup"><span data-stu-id="7463c-124">Retrieving a trigger string for all the triggers associated with a known task</span></span> | [<span data-ttu-id="7463c-125">Exemple de code : récupération de chaînes de déclencheur</span><span class="sxs-lookup"><span data-stu-id="7463c-125">Code Example: Retrieving Trigger Strings</span></span>](c-c-code-example-retrieving-trigger-strings.md) |



 

## <a name="related-topics"></a><span data-ttu-id="7463c-126">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="7463c-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7463c-127">Exemples de Planificateur de tâches 1,0</span><span class="sxs-lookup"><span data-stu-id="7463c-127">Task Scheduler 1.0 Examples</span></span>](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 