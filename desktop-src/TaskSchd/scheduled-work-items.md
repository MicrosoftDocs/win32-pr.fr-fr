---
title: Éléments de travail planifiés
description: Le Planificateur de tâches utilise deux termes pour décrire ce qu’il peut planifier des tâches et des éléments de travail.
ms.assetid: 6ca182c3-eba8-43dd-bf2e-27dd972e3cf8
keywords:
- éléments de travail Planificateur de tâches
- éléments de travail Planificateur de tâches, comparés aux tâches
- tâches Planificateur de tâches
- tâches Planificateur de tâches, comparées aux éléments de travail
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 586747e4049529dcfe747959aae994360a7b1485
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309705"
---
# <a name="scheduled-work-items"></a><span data-ttu-id="9f605-107">Éléments de travail planifiés</span><span class="sxs-lookup"><span data-stu-id="9f605-107">Scheduled Work Items</span></span>

<span data-ttu-id="9f605-108">Le Planificateur de tâches utilise deux termes pour décrire ce qu’il peut planifier : les éléments de travail et les tâches.</span><span class="sxs-lookup"><span data-stu-id="9f605-108">The Task Scheduler uses two terms to describe what it can schedule: work items and tasks.</span></span> <span data-ttu-id="9f605-109">Parmi ces deux termes, l' [*élément de travail*](w.md) est un terme plus général qui décrit tout type d’élément pouvant être planifié.</span><span class="sxs-lookup"><span data-stu-id="9f605-109">Of these two terms, [*work item*](w.md) is a more general term that describes any type of item that can be scheduled.</span></span> <span data-ttu-id="9f605-110">Un *élément de travail* peut être n’importe quel élément que le service Planificateur de tâches exécute à une heure spécifiée par le ou les déclencheurs de l’élément.</span><span class="sxs-lookup"><span data-stu-id="9f605-110">A *work item* can be any item that the Task Scheduler service runs at a time that is specified by the item's trigger(s).</span></span>

<span data-ttu-id="9f605-111">En revanche, une [*tâche*](t.md) est un type spécifique d’élément de travail.</span><span class="sxs-lookup"><span data-stu-id="9f605-111">In contrast, a [*task*](t.md) is a specific type of work item.</span></span> <span data-ttu-id="9f605-112">Actuellement, le seul type d’élément de travail planifié pris en charge est une tâche.</span><span class="sxs-lookup"><span data-stu-id="9f605-112">Currently, the only type of scheduled work item that is supported is a task.</span></span>

<span data-ttu-id="9f605-113">L’interface [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) contient des méthodes prises en charge par tous les types d’éléments de travail planifiés.</span><span class="sxs-lookup"><span data-stu-id="9f605-113">The [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) interface contains methods that are supported by all types of scheduled work items.</span></span> <span data-ttu-id="9f605-114">Par exemple, les informations de compte, les durées d’exécution et les commentaires définis par l’application sont des propriétés qui peuvent s’appliquer à tous les types d’éléments de travail.</span><span class="sxs-lookup"><span data-stu-id="9f605-114">For example, account information, run times, and application-defined comments are properties that may apply to all types of work items.</span></span> <span data-ttu-id="9f605-115">Ces propriétés peuvent être définies et récupérées par le biais de l’interface **IScheduledWorkItem** .</span><span class="sxs-lookup"><span data-stu-id="9f605-115">These properties can be set and retrieved through the **IScheduledWorkItem** interface.</span></span>

<span data-ttu-id="9f605-116">L’interface [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) contient des méthodes prises en charge uniquement par les tâches.</span><span class="sxs-lookup"><span data-stu-id="9f605-116">The [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) interface contains methods that are supported only by tasks.</span></span>

<span data-ttu-id="9f605-117">Les méthodes de l’interface [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) sont actuellement héritées par l’interface [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) et seront à l’avenir héritées par d’autres interfaces d’élément de travail.</span><span class="sxs-lookup"><span data-stu-id="9f605-117">The methods of the [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) interface are currently inherited by the [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) interface and in the future will be inherited by other work item interfaces.</span></span>

| <span data-ttu-id="9f605-118">Pour obtenir des exemples de</span><span class="sxs-lookup"><span data-stu-id="9f605-118">For examples of</span></span>                                              | <span data-ttu-id="9f605-119">Consultez</span><span class="sxs-lookup"><span data-stu-id="9f605-119">See</span></span>                                                                                        |
|--------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="9f605-120">Création d’une nouvelle tâche.</span><span class="sxs-lookup"><span data-stu-id="9f605-120">Creating a new task.</span></span>                                         | [<span data-ttu-id="9f605-121">Exemple de création d’une tâche à l’aide de NewWorkItem</span><span class="sxs-lookup"><span data-stu-id="9f605-121">Creating a Task Using NewWorkItem Example</span></span>](creating-a-task-using-newworkitem-example.md) |
| <span data-ttu-id="9f605-122">Exécution d’une tâche existante.</span><span class="sxs-lookup"><span data-stu-id="9f605-122">Running an existing task.</span></span>                                    | [<span data-ttu-id="9f605-123">Exemple de démarrage d’une tâche</span><span class="sxs-lookup"><span data-stu-id="9f605-123">Starting a Task Example</span></span>](starting-a-task-example.md)                                     |
| <span data-ttu-id="9f605-124">Récupération des propriétés qui s’appliquent à tous les types d’éléments de travail.</span><span class="sxs-lookup"><span data-stu-id="9f605-124">Retrieving properties that apply to all types of work items.</span></span> | [<span data-ttu-id="9f605-125">Récupération d’exemples de propriétés d’élément de travail</span><span class="sxs-lookup"><span data-stu-id="9f605-125">Retrieving Work Item Property Examples</span></span>](retrieving-work-item-property-examples.md)       |
| <span data-ttu-id="9f605-126">Définition des propriétés qui s’appliquent à tous les types d’éléments de travail.</span><span class="sxs-lookup"><span data-stu-id="9f605-126">Setting properties that apply to all types of work items.</span></span>    | [<span data-ttu-id="9f605-127">Définition d’exemples de propriétés d’élément de travail</span><span class="sxs-lookup"><span data-stu-id="9f605-127">Setting Work Item Property Examples</span></span>](setting-work-item-property-examples.md)             |



 

 

 




