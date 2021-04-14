---
title: Création d’un déclencheur
description: Pour créer un déclencheur, vous devez utiliser trois interfaces.
ms.assetid: c0f121ff-d0a5-4b6c-935c-6f47b4ea26d5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f48ecb7b06e5bade6d5ad80e4c9a82794f6a17e8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382318"
---
# <a name="creating-a-new-trigger"></a><span data-ttu-id="6fefa-103">Création d’un déclencheur</span><span class="sxs-lookup"><span data-stu-id="6fefa-103">Creating a New Trigger</span></span>

<span data-ttu-id="6fefa-104">Pour créer un déclencheur, vous devez utiliser trois interfaces.</span><span class="sxs-lookup"><span data-stu-id="6fefa-104">To create a trigger you must use three interfaces.</span></span> <span data-ttu-id="6fefa-105">[**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) fournit la méthode [**IScheduledWorkItem :: CreateTrigger**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-createtrigger) pour la création de l’objet déclencheur, [**ITaskTrigger**](/windows/desktop/api/Mstask/nn-mstask-itasktrigger) fournit la méthode [**ITaskTrigger :: SetTrigger**](/windows/desktop/api/Mstask/nf-mstask-itasktrigger-settrigger) pour définir les critères pour le déclencheur, et l’interface com [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) fournit une méthode **Save** pour enregistrer le nouveau déclencheur sur le disque.</span><span class="sxs-lookup"><span data-stu-id="6fefa-105">[**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) provides the [**IScheduledWorkItem::CreateTrigger**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-createtrigger) method for creating the trigger object, [**ITaskTrigger**](/windows/desktop/api/Mstask/nn-mstask-itasktrigger) provides the [**ITaskTrigger::SetTrigger**](/windows/desktop/api/Mstask/nf-mstask-itasktrigger-settrigger) method for setting the criteria for the trigger, and the COM interface [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) provides a **Save** method for saving the new trigger to disk.</span></span>

<span data-ttu-id="6fefa-106">La procédure suivante décrit comment créer un nouveau déclencheur.</span><span class="sxs-lookup"><span data-stu-id="6fefa-106">The following procedure describes how to create a new trigger.</span></span>

<span data-ttu-id="6fefa-107">**Pour créer un déclencheur**</span><span class="sxs-lookup"><span data-stu-id="6fefa-107">**To create a new trigger**</span></span>

1.  <span data-ttu-id="6fefa-108">Appelez [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) pour initialiser la bibliothèque com et [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) pour obtenir un objet planificateur de tâches.</span><span class="sxs-lookup"><span data-stu-id="6fefa-108">Call [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) to initialize the COM library and [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) to get a Task Scheduler object.</span></span> <span data-ttu-id="6fefa-109">(Cet exemple suppose que le service Planificateur de tâches est en cours d’exécution.)</span><span class="sxs-lookup"><span data-stu-id="6fefa-109">(This example assumes that the Task Scheduler service is running.)</span></span>
2.  <span data-ttu-id="6fefa-110">Appelez [**ITaskScheduler :: Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) pour récupérer l’interface [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) de l’objet Task.</span><span class="sxs-lookup"><span data-stu-id="6fefa-110">Call [**ITaskScheduler::Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) to get the [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) interface of the task object.</span></span> <span data-ttu-id="6fefa-111">(Notez que cet exemple obtient la tâche « tester la tâche ».)</span><span class="sxs-lookup"><span data-stu-id="6fefa-111">(Note that this example gets the "Test Task" task.)</span></span>
3.  <span data-ttu-id="6fefa-112">Appelez [**CreateTrigger**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-createtrigger) pour créer un objet déclencheur.</span><span class="sxs-lookup"><span data-stu-id="6fefa-112">Call [**CreateTrigger**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-createtrigger) to create a trigger object.</span></span> <span data-ttu-id="6fefa-113">(Notez que [**CreateTrigger**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-createtrigger) est héritée de [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem).)</span><span class="sxs-lookup"><span data-stu-id="6fefa-113">(Note that [**CreateTrigger**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-createtrigger) is inherited from [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem).)</span></span>
4.  <span data-ttu-id="6fefa-114">Définissez une structure de [**\_ déclencheur de tâche**](/windows/desktop/api/Mstask/ns-mstask-task_trigger) .</span><span class="sxs-lookup"><span data-stu-id="6fefa-114">Define a [**TASK\_TRIGGER**](/windows/desktop/api/Mstask/ns-mstask-task_trigger) structure.</span></span> <span data-ttu-id="6fefa-115">Notez que les membres wBeginDay, wBeginMonth et wBeginYear du **\_ déclencheur de tâche** doivent être définis sur un jour, un mois et une année valides respectivement.</span><span class="sxs-lookup"><span data-stu-id="6fefa-115">Note that wBeginDay, wBeginMonth, and wBeginYear members of **TASK\_TRIGGER** must be set to a valid day, month, and year respectively.</span></span>
5.  <span data-ttu-id="6fefa-116">Appelez [**ITaskTrigger :: SetTrigger**](/windows/desktop/api/Mstask/nf-mstask-itasktrigger-settrigger) pour définir les critères de déclenchement.</span><span class="sxs-lookup"><span data-stu-id="6fefa-116">Call [**ITaskTrigger::SetTrigger**](/windows/desktop/api/Mstask/nf-mstask-itasktrigger-settrigger) to set the trigger criteria.</span></span>
6.  <span data-ttu-id="6fefa-117">Enregistrez la tâche avec le nouveau déclencheur sur le disque à l’aide de [**IPersistFile :: Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save).</span><span class="sxs-lookup"><span data-stu-id="6fefa-117">Save the task with the new trigger to disk using [**IPersistFile::Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save).</span></span> <span data-ttu-id="6fefa-118">(L’interface [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) est une interface COM standard prise en charge par l’interface [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) .)</span><span class="sxs-lookup"><span data-stu-id="6fefa-118">(The [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) interface is a standard COM interface supported by the [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) interface.)</span></span>
7.  <span data-ttu-id="6fefa-119">Appelez [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) pour libérer toutes les ressources.</span><span class="sxs-lookup"><span data-stu-id="6fefa-119">Call [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) to release all resources.</span></span> <span data-ttu-id="6fefa-120">(Notez que **Release** est une méthode [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) héritée par [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask).)</span><span class="sxs-lookup"><span data-stu-id="6fefa-120">(Note that **Release** is an [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) method inherited by [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask).)</span></span>



| <span data-ttu-id="6fefa-121">Pour obtenir un exemple de code de</span><span class="sxs-lookup"><span data-stu-id="6fefa-121">For a code example of</span></span>                       | <span data-ttu-id="6fefa-122">Consultez</span><span class="sxs-lookup"><span data-stu-id="6fefa-122">See</span></span>                                                                                         |
|---------------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="6fefa-123">Création d’un déclencheur pour une tâche existante</span><span class="sxs-lookup"><span data-stu-id="6fefa-123">Creating a new trigger for an existing task</span></span> | [<span data-ttu-id="6fefa-124">Exemple de code C/C++ : création d’un déclencheur de tâche</span><span class="sxs-lookup"><span data-stu-id="6fefa-124">C/C++ Code Example: Creating a Task Trigger</span></span>](c-c-code-example-creating-a-task-trigger.md) |



 

## <a name="related-topics"></a><span data-ttu-id="6fefa-125">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="6fefa-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6fefa-126">Exemples de Planificateur de tâches 1,0</span><span class="sxs-lookup"><span data-stu-id="6fefa-126">Task Scheduler 1.0 Examples</span></span>](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 