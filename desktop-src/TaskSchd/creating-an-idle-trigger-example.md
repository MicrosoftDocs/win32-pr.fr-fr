---
title: Exemple de création d’un déclencheur inactif
description: Pour créer un déclencheur inactif, vous devez spécifier un déclencheur inactif lorsque vous créez le déclencheur, et vous devez définir la durée d’inactivité de la tâche. Pour plus d’informations sur les conditions d’inactivité, consultez conditions d’inactivité de la tâche.
ms.assetid: d36a621c-4011-4c3d-b6f4-b56d1f50983c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6a7f8333c79d05dfade609f028f93a816e61adf
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315924"
---
# <a name="creating-an-idle-trigger-example"></a><span data-ttu-id="a0cda-104">Exemple de création d’un déclencheur inactif</span><span class="sxs-lookup"><span data-stu-id="a0cda-104">Creating an Idle Trigger Example</span></span>

<span data-ttu-id="a0cda-105">Pour créer un déclencheur inactif, vous devez spécifier un déclencheur inactif lorsque vous créez le déclencheur, et vous devez définir la durée d’inactivité de la tâche.</span><span class="sxs-lookup"><span data-stu-id="a0cda-105">To create an idle trigger, you must specify an idle trigger when you create the trigger, and you must set the idle time for the task.</span></span> <span data-ttu-id="a0cda-106">Pour plus d’informations sur les conditions d’inactivité, consultez conditions d’inactivité de la [tâche](task-idle-conditions.md).</span><span class="sxs-lookup"><span data-stu-id="a0cda-106">For information about idle conditions, see [Task Idle Conditions](task-idle-conditions.md).</span></span>

<span data-ttu-id="a0cda-107">Après avoir créé le déclencheur inactif, appelez [**IPersistFile :: Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save) pour enregistrer le nouveau déclencheur sur le disque.</span><span class="sxs-lookup"><span data-stu-id="a0cda-107">After creating the idle trigger, call [**IPersistFile::Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save) to save the new trigger to disk.</span></span>

<span data-ttu-id="a0cda-108">La procédure suivante décrit comment créer un déclencheur inactif pour une tâche connue.</span><span class="sxs-lookup"><span data-stu-id="a0cda-108">The following procedure describes how to create an idle trigger for a known task.</span></span>

<span data-ttu-id="a0cda-109">**Pour créer un déclencheur inactif pour une tâche connue**</span><span class="sxs-lookup"><span data-stu-id="a0cda-109">**To create an idle trigger for a known task**</span></span>

1.  <span data-ttu-id="a0cda-110">Appelez [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) pour initialiser la bibliothèque com et [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) pour obtenir un objet planificateur de tâches.</span><span class="sxs-lookup"><span data-stu-id="a0cda-110">Call [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) to initialize the COM library and [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) to get a Task Scheduler object.</span></span> <span data-ttu-id="a0cda-111">(Cet exemple suppose que le service Planificateur de tâches est en cours d’exécution.)</span><span class="sxs-lookup"><span data-stu-id="a0cda-111">(This example assumes that the Task Scheduler service is running.)</span></span>
2.  <span data-ttu-id="a0cda-112">Appelez [**ITaskScheduler :: Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) pour récupérer l’interface [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) de l’objet Task.</span><span class="sxs-lookup"><span data-stu-id="a0cda-112">Call [**ITaskScheduler::Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) to get the [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) interface of the task object.</span></span> <span data-ttu-id="a0cda-113">(Notez que cet exemple obtient la tâche « tester la tâche ».)</span><span class="sxs-lookup"><span data-stu-id="a0cda-113">(Note that this example gets the "Test Task" task.)</span></span>
3.  <span data-ttu-id="a0cda-114">Appelez [**SetIdleWait**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-setidlewait) pour définir la durée pendant laquelle le système doit rester inactif avant que le déclencheur ne se déclenche.</span><span class="sxs-lookup"><span data-stu-id="a0cda-114">Call [**SetIdleWait**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-setidlewait) to set how long the system must remain idle before the trigger will fire.</span></span> <span data-ttu-id="a0cda-115">(Notez que **SetIdleWait** est héritée de [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem).)</span><span class="sxs-lookup"><span data-stu-id="a0cda-115">(Note that **SetIdleWait** is inherited from [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem).)</span></span>
4.  <span data-ttu-id="a0cda-116">Définissez la structure de [**\_ déclencheur de tâche**](/windows/desktop/api/Mstask/ns-mstask-task_trigger) et appelez [**CreateTrigger**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-createtrigger) pour créer le déclencheur inactif.</span><span class="sxs-lookup"><span data-stu-id="a0cda-116">Define the [**TASK\_TRIGGER**](/windows/desktop/api/Mstask/ns-mstask-task_trigger) structure and call [**CreateTrigger**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-createtrigger) to create the idle trigger.</span></span> <span data-ttu-id="a0cda-117">(Notez que **CreateTrigger** est héritée de [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem).)</span><span class="sxs-lookup"><span data-stu-id="a0cda-117">(Note that **CreateTrigger** is inherited from [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem).)</span></span>
5.  <span data-ttu-id="a0cda-118">Enregistrez la tâche avec le nouveau déclencheur inactif sur le disque à l’aide de [**IPersistFile :: Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save).</span><span class="sxs-lookup"><span data-stu-id="a0cda-118">Save the task with the new idle trigger to disk using [**IPersistFile::Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save).</span></span> <span data-ttu-id="a0cda-119">(L’interface [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) est une interface COM standard prise en charge par l’interface [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) .)</span><span class="sxs-lookup"><span data-stu-id="a0cda-119">(The [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) interface is a standard COM interface supported by the [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) interface.)</span></span>
6.  <span data-ttu-id="a0cda-120">Appelez **ITask :: Release** pour libérer toutes les ressources.</span><span class="sxs-lookup"><span data-stu-id="a0cda-120">Call **ITask::Release** to release all resources.</span></span> <span data-ttu-id="a0cda-121">(Notez que [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) est une méthode [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) héritée par [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask).)</span><span class="sxs-lookup"><span data-stu-id="a0cda-121">(Note that [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) is an [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) method inherited by [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask).)</span></span>



| <span data-ttu-id="a0cda-122">Pour obtenir un exemple de code de</span><span class="sxs-lookup"><span data-stu-id="a0cda-122">For a code example of</span></span>                         | <span data-ttu-id="a0cda-123">Consultez</span><span class="sxs-lookup"><span data-stu-id="a0cda-123">See</span></span>                                                                                           |
|-----------------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="a0cda-124">Création d’un déclencheur inactif pour une tâche existante</span><span class="sxs-lookup"><span data-stu-id="a0cda-124">Creating an idle trigger for an existing task</span></span> | [<span data-ttu-id="a0cda-125">Exemple de code C/C++ : création d’un déclencheur inactif</span><span class="sxs-lookup"><span data-stu-id="a0cda-125">C/C++ Code Example: Creating an Idle Trigger</span></span>](c-c-code-example-creating-an-idle-trigger.md) |



 

## <a name="related-topics"></a><span data-ttu-id="a0cda-126">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a0cda-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a0cda-127">Exemples de Planificateur de tâches 1,0</span><span class="sxs-lookup"><span data-stu-id="a0cda-127">Task Scheduler 1.0 Examples</span></span>](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 