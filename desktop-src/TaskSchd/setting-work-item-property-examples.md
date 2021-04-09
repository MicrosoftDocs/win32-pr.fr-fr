---
title: Définition d’exemples de propriétés d’élément de travail
description: Pour définir les propriétés d’un élément de travail, appelez ITaskScheduler Activate pour récupérer l’interface de l’objet d’élément de travail, puis appelez la méthode appropriée pour définir la propriété de tâche qui vous intéresse. Actuellement, les seuls éléments de travail valides sont les tâches.
ms.assetid: 80a158de-d312-499d-8ff0-b95e794cf169
keywords:
- définition des propriétés de l’élément de travail Planificateur de tâches
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e026ea3d2b3f6677a3d229e9289ab9b201e02b94
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103941206"
---
# <a name="setting-work-item-property-examples"></a><span data-ttu-id="44143-105">Définition d’exemples de propriétés d’élément de travail</span><span class="sxs-lookup"><span data-stu-id="44143-105">Setting Work Item Property Examples</span></span>

<span data-ttu-id="44143-106">Pour définir les propriétés d’un élément de travail, appelez [**ITaskScheduler :: Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) pour récupérer l’interface de l’objet d’élément de travail, puis appelez la méthode appropriée pour définir la propriété de tâche qui vous intéresse.</span><span class="sxs-lookup"><span data-stu-id="44143-106">To set the properties of a work item, call [**ITaskScheduler::Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) to retrieve the interface of the work item object, then call the appropriate method to set the task property you are interested in.</span></span> <span data-ttu-id="44143-107">Actuellement, les seuls éléments de travail valides sont les tâches.</span><span class="sxs-lookup"><span data-stu-id="44143-107">Currently, the only valid work items are tasks.</span></span>

<span data-ttu-id="44143-108">Les exemples de code figurant en bas de la page montrent comment définir les propriétés qui s’appliquent à tous les éléments de travail.</span><span class="sxs-lookup"><span data-stu-id="44143-108">The code examples listed at the bottom of the page show how to set the properties that apply to all work items.</span></span> <span data-ttu-id="44143-109">Pour les autres propriétés qui sont propres aux tâches, consultez [définition d’exemples de propriétés de tâche](setting-task-property-examples.md).</span><span class="sxs-lookup"><span data-stu-id="44143-109">For other properties that are unique to tasks, see [Setting Task Property Examples](setting-task-property-examples.md).</span></span>

> [!Note]  
> <span data-ttu-id="44143-110">Dans l’exemple de code suivant, toutes les interfaces sont libérées après qu’elles ne sont plus nécessaires.</span><span class="sxs-lookup"><span data-stu-id="44143-110">In the following code example, all interfaces are released after they are no longer needed.</span></span>

 

<span data-ttu-id="44143-111">Dans les exemples suivants, l’objet modifié est toujours enregistré sur le disque par un appel à [**IPersistFile :: Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save).</span><span class="sxs-lookup"><span data-stu-id="44143-111">In the following examples, the modified object is always saved to disk by a call to [**IPersistFile::Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save).</span></span> <span data-ttu-id="44143-112">(L’interface [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) est une interface COM standard héritée par l’objet Task.)</span><span class="sxs-lookup"><span data-stu-id="44143-112">(The [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) interface is a standard COM interface inherited by the task object.)</span></span>

<span data-ttu-id="44143-113">La procédure suivante décrit comment définir une propriété de tâche.</span><span class="sxs-lookup"><span data-stu-id="44143-113">The following procedure describes how to set a task property.</span></span>

<span data-ttu-id="44143-114">**Pour définir une propriété de tâche**</span><span class="sxs-lookup"><span data-stu-id="44143-114">**To set a task property**</span></span>

1.  <span data-ttu-id="44143-115">Appelez [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) pour initialiser la bibliothèque com et [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) pour obtenir un objet planificateur de tâches.</span><span class="sxs-lookup"><span data-stu-id="44143-115">Call [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) to initialize the COM library and [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) to get a Task Scheduler object.</span></span> <span data-ttu-id="44143-116">(Ces exemples supposent que le service Planificateur de tâches est en cours d’exécution.)</span><span class="sxs-lookup"><span data-stu-id="44143-116">(These examples assume that the Task Scheduler service is running.)</span></span>
2.  <span data-ttu-id="44143-117">Appelez [**ITaskScheduler :: Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) pour récupérer l’interface [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) de l’objet Task.</span><span class="sxs-lookup"><span data-stu-id="44143-117">Call [**ITaskScheduler::Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) to get the [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) interface of the task object.</span></span> <span data-ttu-id="44143-118">(Notez que les tâches sont actuellement le seul type d’élément de travail valide.)</span><span class="sxs-lookup"><span data-stu-id="44143-118">(Note that tasks are currently the only valid type of work item.)</span></span>
3.  <span data-ttu-id="44143-119">Appelez la méthode [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) appropriée pour définir la propriété qui vous intéresse.</span><span class="sxs-lookup"><span data-stu-id="44143-119">Call the appropriate [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) method to set the property you are interested in.</span></span> <span data-ttu-id="44143-120">Notez que les méthodes **IScheduledWorkItem** sont héritées par l’interface [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) .</span><span class="sxs-lookup"><span data-stu-id="44143-120">Note that **IScheduledWorkItem** methods are inherited by the [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) interface.</span></span>
4.  <span data-ttu-id="44143-121">Appelez [**IPersistFile :: Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save) pour stocker l’objet de tâche modifié sur le disque.</span><span class="sxs-lookup"><span data-stu-id="44143-121">Call [**IPersistFile::Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save) to store the modified task object to disk.</span></span>



| <span data-ttu-id="44143-122">Pour obtenir un exemple de code de</span><span class="sxs-lookup"><span data-stu-id="44143-122">For a code example of</span></span>                            | <span data-ttu-id="44143-123">Consultez</span><span class="sxs-lookup"><span data-stu-id="44143-123">See</span></span>                                                                                                           |
|--------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="44143-124">Définition des informations de compte pour une tâche connue</span><span class="sxs-lookup"><span data-stu-id="44143-124">Setting the account information for a known task</span></span> | [<span data-ttu-id="44143-125">Exemple de code C/C++ : définition des informations de compte de tâche</span><span class="sxs-lookup"><span data-stu-id="44143-125">C/C++ Code Example: Setting Task Account Information</span></span>](c-c-code-example-setting-task-account-information.md) |
| <span data-ttu-id="44143-126">Définition du commentaire d’une tâche connue</span><span class="sxs-lookup"><span data-stu-id="44143-126">Setting the comment of a known task</span></span>              | [<span data-ttu-id="44143-127">Exemple de code C/C++ : définition d’un commentaire de tâche</span><span class="sxs-lookup"><span data-stu-id="44143-127">C/C++ Code Example: Setting Task Comment</span></span>](c-c-code-example-setting-task-comment.md)                         |



 

## <a name="related-topics"></a><span data-ttu-id="44143-128">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="44143-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="44143-129">Exemples de Planificateur de tâches 1,0</span><span class="sxs-lookup"><span data-stu-id="44143-129">Task Scheduler 1.0 Examples</span></span>](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 