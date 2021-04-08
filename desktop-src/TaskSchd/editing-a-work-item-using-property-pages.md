---
title: Modification d’un élément de travail à l’aide des pages de propriétés
description: Vous pouvez modifier les propriétés d’un élément de travail à l’aide de l’interface graphique utilisateur fournie par le service Planificateur de tâches.
ms.assetid: 2d7992ce-fa70-41cc-a8e7-74687171537f
keywords:
- modification des éléments de travail Planificateur de tâches
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0958c361f1c076e8ebed6a7e645bf67694a1d01
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103727988"
---
# <a name="editing-a-work-item-using-property-pages"></a><span data-ttu-id="fae59-104">Modification d’un élément de travail à l’aide des pages de propriétés</span><span class="sxs-lookup"><span data-stu-id="fae59-104">Editing a Work Item using Property Pages</span></span>

<span data-ttu-id="fae59-105">Vous pouvez modifier les propriétés d’un élément de travail à l’aide de l’interface graphique utilisateur fournie par le service Planificateur de tâches.</span><span class="sxs-lookup"><span data-stu-id="fae59-105">You can edit the properties of a work item by using the graphic user interface provided by the Task Scheduler Service.</span></span> <span data-ttu-id="fae59-106">(Actuellement, les seuls éléments de travail valides sont les tâches.)</span><span class="sxs-lookup"><span data-stu-id="fae59-106">(Currently, the only valid work items are tasks.)</span></span>

<span data-ttu-id="fae59-107">La procédure suivante décrit comment modifier une tâche à l’aide de ses pages de propriétés.</span><span class="sxs-lookup"><span data-stu-id="fae59-107">The following procedure describes how to edit a task using its property pages.</span></span>

<span data-ttu-id="fae59-108">**Pour modifier une tâche à l’aide de ses pages de propriétés**</span><span class="sxs-lookup"><span data-stu-id="fae59-108">**To edit a task using its property pages**</span></span>

1.  <span data-ttu-id="fae59-109">Appelez [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) pour initialiser la bibliothèque com et [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) pour obtenir un objet planificateur de tâches.</span><span class="sxs-lookup"><span data-stu-id="fae59-109">Call [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) to initialize the COM library and [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) to get a Task Scheduler object.</span></span> <span data-ttu-id="fae59-110">(Ces exemples supposent que le service Planificateur de tâches est en cours d’exécution.)</span><span class="sxs-lookup"><span data-stu-id="fae59-110">(These examples assume that the Task Scheduler service is running.)</span></span>
2.  <span data-ttu-id="fae59-111">Appelez [**ITaskScheduler :: Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) pour récupérer l’interface [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) de l’objet Task.</span><span class="sxs-lookup"><span data-stu-id="fae59-111">Call [**ITaskScheduler::Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) to get the [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) interface of the task object.</span></span> <span data-ttu-id="fae59-112">(Notez que les tâches sont actuellement le seul type d’élément de travail valide.)</span><span class="sxs-lookup"><span data-stu-id="fae59-112">(Note that tasks are currently the only valid type of work item.)</span></span>
3.  <span data-ttu-id="fae59-113">Appelez [**IScheduledWorkItem :: EditWorkItem**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-editworkitem) pour afficher les pages de propriétés de la tâche.</span><span class="sxs-lookup"><span data-stu-id="fae59-113">Call [**IScheduledWorkItem::EditWorkItem**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-editworkitem) to display the property pages for the task.</span></span>
4.  <span data-ttu-id="fae59-114">Modifiez les propriétés de la tâche en fonction des besoins, puis cliquez sur OK pour accepter les nouvelles valeurs et supprimer les pages de propriétés affichées.</span><span class="sxs-lookup"><span data-stu-id="fae59-114">Edit the properties of the task as needed, then click OK to accept the new values and remove the displayed property pages.</span></span>



| <span data-ttu-id="fae59-115">Pour obtenir un exemple de code de</span><span class="sxs-lookup"><span data-stu-id="fae59-115">For a code example of</span></span>                                                                                      | <span data-ttu-id="fae59-116">Consultez</span><span class="sxs-lookup"><span data-stu-id="fae59-116">See</span></span>                                                                                 |
|------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="fae59-117">Affichage des pages de propriétés d’une tâche connue et autorisation à un utilisateur de modifier les propriétés de l’élément de travail</span><span class="sxs-lookup"><span data-stu-id="fae59-117">Displaying the property pages for a known task and allowing a user to edit the properties of the work item</span></span> | [<span data-ttu-id="fae59-118">Exemple de code C/C++ : modification d’un élément de travail</span><span class="sxs-lookup"><span data-stu-id="fae59-118">C/C++ Code Example: Editing a Work Item</span></span>](c-c-code-example-editing-a-work-item.md) |



 

## <a name="related-topics"></a><span data-ttu-id="fae59-119">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="fae59-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fae59-120">Exemples de Planificateur de tâches 1,0</span><span class="sxs-lookup"><span data-stu-id="fae59-120">Task Scheduler 1.0 Examples</span></span>](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 