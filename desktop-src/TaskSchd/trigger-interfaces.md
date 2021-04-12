---
title: Interfaces de déclencheur
description: Les API utilisées pour gérer les déclencheurs varient en fonction de la version de la Planificateur de tâches. Toutefois, dans les deux cas, ces API vous permettent de créer des déclencheurs, de récupérer et de mettre à jour des déclencheurs existants et de supprimer des déclencheurs qui ne sont plus nécessaires.
ms.assetid: 94c11f11-72e2-404f-b396-ab7b1be71942
keywords:
- déclencheurs Planificateur de tâches, interfaces
- déclencheurs Planificateur de tâches, interfaces, Description
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5357bb745b43c51707d9571c7582a44c9225a7fe
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/04/2020
ms.locfileid: "104316817"
---
# <a name="trigger-interfaces"></a><span data-ttu-id="2a25b-106">Interfaces de déclencheur</span><span class="sxs-lookup"><span data-stu-id="2a25b-106">Trigger Interfaces</span></span>

<span data-ttu-id="2a25b-107">Les API utilisées pour gérer les déclencheurs varient en fonction de la version de la Planificateur de tâches.</span><span class="sxs-lookup"><span data-stu-id="2a25b-107">The APIs that are used to manage triggers vary depending on the version of the Task Scheduler.</span></span> <span data-ttu-id="2a25b-108">Toutefois, dans les deux cas, ces API vous permettent de créer des déclencheurs, de récupérer et de mettre à jour des déclencheurs existants et de supprimer des déclencheurs qui ne sont plus nécessaires.</span><span class="sxs-lookup"><span data-stu-id="2a25b-108">However, in both cases these APIs enable you to create new triggers, retrieve and update existing triggers, and delete triggers that are no longer required.</span></span>


<span data-ttu-id="2a25b-109">Les applications développées à l’aide de Planificateur de tâches 2,0 peuvent utiliser des objets et des interfaces pour créer, récupérer, modifier et supprimer les déclencheurs d’une tâche.</span><span class="sxs-lookup"><span data-stu-id="2a25b-109">Applications that are developed using Task Scheduler 2.0 can use objects and interfaces to create, retrieve, modify, and delete the triggers for a task.</span></span>

<span data-ttu-id="2a25b-110">Dans l’illustration suivante, une tâche spécifie une collection de déclencheurs à l’aide de sa propriété déclencheurs.</span><span class="sxs-lookup"><span data-stu-id="2a25b-110">In the following illustration, a task specifies a collection of triggers using its Triggers property.</span></span> <span data-ttu-id="2a25b-111">Cette collection contient une ou plusieurs API de déclencheur individuelles avec chaque API spécifiant un type de déclencheur spécifique.</span><span class="sxs-lookup"><span data-stu-id="2a25b-111">This collection contains one or more individual trigger APIs with each API specifying a specific trigger type.</span></span> <span data-ttu-id="2a25b-112">Par exemple, dans l’illustration ci-dessous, la collection de déclencheurs contient un déclencheur de démarrage, un déclencheur d’ouverture de session et un déclencheur quotidien.</span><span class="sxs-lookup"><span data-stu-id="2a25b-112">For example, in the illustration below the trigger collection contains a boot trigger, logon trigger, and a daily trigger.</span></span>

![interfaces de déclencheur du planificateur de tâches 2,0](images/tsktri4.png)

### <a name="object-apis-for-scripting-development"></a><span data-ttu-id="2a25b-114">API d’objet pour le développement de scripts</span><span class="sxs-lookup"><span data-stu-id="2a25b-114">Object APIs for Scripting Development</span></span>

<span data-ttu-id="2a25b-115">Pour plus d’informations sur les méthodes et les propriétés des objets utilisés pour spécifier des déclencheurs, consultez :</span><span class="sxs-lookup"><span data-stu-id="2a25b-115">For more information about the methods and properties of the objects that are used to specify triggers, see:</span></span>

-   [<span data-ttu-id="2a25b-116">**TaskDefinition**</span><span class="sxs-lookup"><span data-stu-id="2a25b-116">**TaskDefinition**</span></span>](taskdefinition.md)
-   [<span data-ttu-id="2a25b-117">**TriggerCollection**</span><span class="sxs-lookup"><span data-stu-id="2a25b-117">**TriggerCollection**</span></span>](triggercollection.md)
-   [<span data-ttu-id="2a25b-118">**Stead**</span><span class="sxs-lookup"><span data-stu-id="2a25b-118">**Trigger**</span></span>](trigger.md)
-   [<span data-ttu-id="2a25b-119">**BootTrigger**</span><span class="sxs-lookup"><span data-stu-id="2a25b-119">**BootTrigger**</span></span>](boottrigger.md)
-   [<span data-ttu-id="2a25b-120">**DailyTrigger**</span><span class="sxs-lookup"><span data-stu-id="2a25b-120">**DailyTrigger**</span></span>](dailytrigger.md)
-   [<span data-ttu-id="2a25b-121">**EventTrigger**</span><span class="sxs-lookup"><span data-stu-id="2a25b-121">**EventTrigger**</span></span>](eventtrigger.md)
-   [<span data-ttu-id="2a25b-122">**IdleTrigger**</span><span class="sxs-lookup"><span data-stu-id="2a25b-122">**IdleTrigger**</span></span>](idletrigger.md)
-   [<span data-ttu-id="2a25b-123">**LogonTrigger**</span><span class="sxs-lookup"><span data-stu-id="2a25b-123">**LogonTrigger**</span></span>](logontrigger.md)
-   [<span data-ttu-id="2a25b-124">**MonthlyDOWTrigger**</span><span class="sxs-lookup"><span data-stu-id="2a25b-124">**MonthlyDOWTrigger**</span></span>](monthlydowtrigger.md)
-   [<span data-ttu-id="2a25b-125">**MonthlyTrigger**</span><span class="sxs-lookup"><span data-stu-id="2a25b-125">**MonthlyTrigger**</span></span>](monthlytrigger.md)
-   [<span data-ttu-id="2a25b-126">**RegistrationTrigger**</span><span class="sxs-lookup"><span data-stu-id="2a25b-126">**RegistrationTrigger**</span></span>](registrationtrigger.md)
-   [<span data-ttu-id="2a25b-127">**TimeTrigger**</span><span class="sxs-lookup"><span data-stu-id="2a25b-127">**TimeTrigger**</span></span>](timetrigger.md)
-   [<span data-ttu-id="2a25b-128">**WeeklyTrigger**</span><span class="sxs-lookup"><span data-stu-id="2a25b-128">**WeeklyTrigger**</span></span>](weeklytrigger.md)

### <a name="interfaces-apis-for-c-development"></a><span data-ttu-id="2a25b-129">Interfaces API pour le développement C++</span><span class="sxs-lookup"><span data-stu-id="2a25b-129">Interfaces APIs for C++ Development</span></span>

<span data-ttu-id="2a25b-130">Pour plus d’informations sur les méthodes et les propriétés des interfaces utilisées pour spécifier des déclencheurs, consultez :</span><span class="sxs-lookup"><span data-stu-id="2a25b-130">For more information about the methods and properties of the interfaces that are used to specify triggers, see:</span></span>

-   [<span data-ttu-id="2a25b-131">**ITaskDefinition**</span><span class="sxs-lookup"><span data-stu-id="2a25b-131">**ITaskDefinition**</span></span>](/windows/desktop/api/taskschd/nn-taskschd-itaskdefinition)
-   [<span data-ttu-id="2a25b-132">**ITriggerCollection**</span><span class="sxs-lookup"><span data-stu-id="2a25b-132">**ITriggerCollection**</span></span>](/windows/desktop/api/taskschd/nn-taskschd-itriggercollection)
-   [<span data-ttu-id="2a25b-133">**ITrigger**</span><span class="sxs-lookup"><span data-stu-id="2a25b-133">**ITrigger**</span></span>](/windows/desktop/api/taskschd/nn-taskschd-itrigger)
-   [<span data-ttu-id="2a25b-134">**IBootTrigger**</span><span class="sxs-lookup"><span data-stu-id="2a25b-134">**IBootTrigger**</span></span>](/windows/desktop/api/taskschd/nn-taskschd-iboottrigger)
-   [<span data-ttu-id="2a25b-135">**IDailyTrigger**</span><span class="sxs-lookup"><span data-stu-id="2a25b-135">**IDailyTrigger**</span></span>](/windows/desktop/api/taskschd/nn-taskschd-idailytrigger)
-   [<span data-ttu-id="2a25b-136">**IEventTrigger**</span><span class="sxs-lookup"><span data-stu-id="2a25b-136">**IEventTrigger**</span></span>](/windows/desktop/api/taskschd/nn-taskschd-ieventtrigger)
-   [<span data-ttu-id="2a25b-137">**IIdleTrigger**</span><span class="sxs-lookup"><span data-stu-id="2a25b-137">**IIdleTrigger**</span></span>](/windows/win32/api/taskschd/nn-taskschd-iidletrigger)
-   [<span data-ttu-id="2a25b-138">**ILogonTrigger**</span><span class="sxs-lookup"><span data-stu-id="2a25b-138">**ILogonTrigger**</span></span>](/windows/desktop/api/taskschd/nn-taskschd-ilogontrigger)
-   [<span data-ttu-id="2a25b-139">**IMonthlyDOWTrigger**</span><span class="sxs-lookup"><span data-stu-id="2a25b-139">**IMonthlyDOWTrigger**</span></span>](/windows/desktop/api/taskschd/nn-taskschd-imonthlydowtrigger)
-   [<span data-ttu-id="2a25b-140">**IMonthlyTrigger**</span><span class="sxs-lookup"><span data-stu-id="2a25b-140">**IMonthlyTrigger**</span></span>](/windows/desktop/api/taskschd/nn-taskschd-imonthlytrigger)
-   [<span data-ttu-id="2a25b-141">**IRegistrationTrigger**</span><span class="sxs-lookup"><span data-stu-id="2a25b-141">**IRegistrationTrigger**</span></span>](/windows/desktop/api/taskschd/nn-taskschd-iregistrationtrigger)
-   [<span data-ttu-id="2a25b-142">**ITimeTrigger**</span><span class="sxs-lookup"><span data-stu-id="2a25b-142">**ITimeTrigger**</span></span>](/windows/desktop/api/taskschd/nn-taskschd-itimetrigger)
-   [<span data-ttu-id="2a25b-143">**IWeeklyTrigger**</span><span class="sxs-lookup"><span data-stu-id="2a25b-143">**IWeeklyTrigger**</span></span>](/windows/desktop/api/taskschd/nn-taskschd-iweeklytrigger)

## <a name="task-scheduler-10-trigger-interfaces"></a><span data-ttu-id="2a25b-144">Interfaces de déclencheur Planificateur de tâches 1,0</span><span class="sxs-lookup"><span data-stu-id="2a25b-144">Task Scheduler 1.0 Trigger Interfaces</span></span>

<span data-ttu-id="2a25b-145">Les applications existantes développées à l’aide de Planificateur de tâches 1,0 peuvent utiliser les méthodes disponibles à partir des interfaces Planificateur de tâches 1,0 pour créer, récupérer, modifier et supprimer les déclencheurs d’un [*élément de travail*](w.md).</span><span class="sxs-lookup"><span data-stu-id="2a25b-145">Existing applications that are developed using Task Scheduler 1.0 can use the methods that are available from the Task Scheduler 1.0 interfaces to create, retrieve, modify, and delete the triggers for a [*work item*](w.md).</span></span> <span data-ttu-id="2a25b-146">Toutefois, Notez que toutes les interfaces, énumérations et structures Planificateur de tâches 1,0 sont obsolètes et ne doivent pas être utilisées pour le développement de nouvelles applications.</span><span class="sxs-lookup"><span data-stu-id="2a25b-146">However, note that all Task Scheduler 1.0 interfaces, enumerations, and structures are obsolete and should not be used for the development of new applications.</span></span>

<span data-ttu-id="2a25b-147">Les deux interfaces utilisées pour effectuer cette opération sont présentées dans l’illustration suivante.</span><span class="sxs-lookup"><span data-stu-id="2a25b-147">The two interfaces that are used to do this are shown in the following illustration.</span></span> <span data-ttu-id="2a25b-148">L’interface [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) est utilisée pour gérer tous les déclencheurs associés à un élément de travail (ce type de gestion comprend la création d’un déclencheur pour l’élément de travail).</span><span class="sxs-lookup"><span data-stu-id="2a25b-148">The [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) interface is used to manage all the triggers that are associated with a work item (such management includes creating a new trigger for the work item).</span></span> <span data-ttu-id="2a25b-149">L’interface [**ITaskTrigger**](/windows/desktop/api/Mstask/nn-mstask-itasktrigger) est utilisée pour gérer un déclencheur spécifique.</span><span class="sxs-lookup"><span data-stu-id="2a25b-149">The [**ITaskTrigger**](/windows/desktop/api/Mstask/nn-mstask-itasktrigger) interface is used to manage a specific trigger.</span></span>

![interfaces de déclencheur du planificateur de tâches 1,0](images/tsktri2.png)

<span data-ttu-id="2a25b-151">L’interface [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) fournit des méthodes pour créer un déclencheur pour un élément de travail, récupérer le nombre de déclencheurs associés à un élément de travail, récupérer les [*structures de déclencheur*](t.md) associées à l’élément de travail, récupérer les [*chaînes de déclencheur*](t.md) associées à l’élément de travail et supprimer des déclencheurs.</span><span class="sxs-lookup"><span data-stu-id="2a25b-151">The [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) interface provides methods for creating a new trigger for a work item, retrieving the number of triggers that are associated with a work item, retrieving the [*trigger structures*](t.md) that are associated with the work item, retrieving [*trigger strings*](t.md) that are associated with the work item, and for deleting triggers.</span></span>

<span data-ttu-id="2a25b-152">Une fois que l’objet déclencheur est disponible, vous pouvez utiliser l’interface [**ITaskTrigger**](/windows/desktop/api/Mstask/nn-mstask-itasktrigger) pour récupérer la structure du déclencheur et la chaîne du déclencheur et pour définir les critères utilisés pour activer le déclencheur.</span><span class="sxs-lookup"><span data-stu-id="2a25b-152">Once the trigger object is available, you can use the [**ITaskTrigger**](/windows/desktop/api/Mstask/nn-mstask-itasktrigger) interface to retrieve the trigger structure and the string of the trigger and to set the criteria that is used to fire the trigger.</span></span> <span data-ttu-id="2a25b-153">Cette interface est utilisée uniquement lorsque vous travaillez avec un [*objet déclencheur de tâche*](t.md).</span><span class="sxs-lookup"><span data-stu-id="2a25b-153">This interface is used only when you are working with a [*task trigger object*](t.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="2a25b-154">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="2a25b-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2a25b-155">Déclencheurs de tâche</span><span class="sxs-lookup"><span data-stu-id="2a25b-155">Task Triggers</span></span>](task-triggers.md)
</dt> <dt>

[<span data-ttu-id="2a25b-156">Types de déclencheurs</span><span class="sxs-lookup"><span data-stu-id="2a25b-156">Trigger Types</span></span>](trigger-types.md)
</dt> <dt>

[<span data-ttu-id="2a25b-157">Structures de déclencheur</span><span class="sxs-lookup"><span data-stu-id="2a25b-157">Trigger Structures</span></span>](trigger-structures.md)
</dt> </dl>

 

 