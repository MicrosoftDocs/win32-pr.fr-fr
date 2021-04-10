---
title: Déclencheurs de tâche
description: Un déclencheur est un ensemble de critères qui, lorsqu’il est rempli, démarre l’exécution d’une tâche.
ms.assetid: 8b4dff8b-9dc3-4856-aed6-648588a089be
keywords:
- création de déclencheurs Planificateur de tâches
- déclencheurs Planificateur de tâches
- déclencheurs Planificateur de tâches, décrits
- déclencheurs Planificateur de tâches, basés sur la durée
- déclencheurs Planificateur de tâches, basés sur les événements
- déclencheurs basés sur les événements Planificateur de tâches
- déclencheurs basés sur l’heure Planificateur de tâches
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d465dfa015be19ff220a77d3c85f0cbb223c4899
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104190899"
---
# <a name="task-triggers"></a><span data-ttu-id="16b16-110">Déclencheurs de tâche</span><span class="sxs-lookup"><span data-stu-id="16b16-110">Task Triggers</span></span>

<span data-ttu-id="16b16-111">Un déclencheur est un ensemble de critères qui, lorsqu’il est rempli, démarre l’exécution d’une tâche.</span><span class="sxs-lookup"><span data-stu-id="16b16-111">A trigger is a set of criteria that, when met, starts the execution of a task.</span></span> <span data-ttu-id="16b16-112">Planificateur de tâches fournit des déclencheurs basés sur des événements et des temps qui peuvent démarrer une tâche de différentes façons.</span><span class="sxs-lookup"><span data-stu-id="16b16-112">Task Scheduler provides both time-based and event-based triggers that can start a task in several different ways.</span></span> <span data-ttu-id="16b16-113">Une tâche donnée peut être démarrée par un ou plusieurs déclencheurs.</span><span class="sxs-lookup"><span data-stu-id="16b16-113">A given task can be started by one or more triggers.</span></span> <span data-ttu-id="16b16-114">Une tâche peut avoir un maximum de 48 déclencheurs.</span><span class="sxs-lookup"><span data-stu-id="16b16-114">A task can have a maximum of 48 triggers.</span></span>

## <a name="time-based-triggers"></a><span data-ttu-id="16b16-115">Déclencheurs basés sur l’heure</span><span class="sxs-lookup"><span data-stu-id="16b16-115">Time-based Triggers</span></span>

<span data-ttu-id="16b16-116">Les déclencheurs basés sur le temps démarrent les tâches aux heures spécifiées.</span><span class="sxs-lookup"><span data-stu-id="16b16-116">Time-based triggers start tasks at specified times.</span></span> <span data-ttu-id="16b16-117">Cela comprend le démarrage de la tâche une fois à une heure spécifique ou le démarrage de la tâche plusieurs fois selon une planification quotidienne, hebdomadaire, mensuelle ou mensuelle.</span><span class="sxs-lookup"><span data-stu-id="16b16-117">This includes starting the task once at a specific time or starting the task multiple times on a daily, weekly, monthly, or monthly day-of-week schedule.</span></span>

## <a name="event-based-triggers"></a><span data-ttu-id="16b16-118">Déclencheurs basés sur des événements</span><span class="sxs-lookup"><span data-stu-id="16b16-118">Event-based Triggers</span></span>

<span data-ttu-id="16b16-119">Les déclencheurs basés sur des événements démarrent une tâche en réponse à certains événements système.</span><span class="sxs-lookup"><span data-stu-id="16b16-119">Event-based triggers start a task in response to certain system events.</span></span> <span data-ttu-id="16b16-120">Par exemple, les déclencheurs basés sur des événements peuvent être définis pour démarrer une tâche au démarrage du système, lorsqu’un utilisateur ouvre une session sur l’ordinateur local ou lorsque le système devient inactif.</span><span class="sxs-lookup"><span data-stu-id="16b16-120">For example, event-based triggers can be set to start a task when the system starts up, when a user logs on to the local computer, or when the system becomes idle.</span></span>

## <a name="multiple-triggers"></a><span data-ttu-id="16b16-121">Déclencheurs multiples</span><span class="sxs-lookup"><span data-stu-id="16b16-121">Multiple Triggers</span></span>

<span data-ttu-id="16b16-122">Chaque tâche peut être démarrée par un ou plusieurs déclencheurs, ce qui permet à la tâche d’être démarrée de plusieurs façons.</span><span class="sxs-lookup"><span data-stu-id="16b16-122">Each task can be started by one or more triggers, allowing the task to be started in any number of ways.</span></span> <span data-ttu-id="16b16-123">Toutefois, plusieurs déclencheurs sont implémentés différemment dans Planificateur de tâches 1,0 et Planificateur de tâches 2,0.</span><span class="sxs-lookup"><span data-stu-id="16b16-123">However, multiple triggers are implemented differently in Task Scheduler 1.0 and Task Scheduler 2.0.</span></span>

<span data-ttu-id="16b16-124">Dans Planificateur de tâches 2,0, chaque déclencheur est défini par une API de déclencheur distincte associée à la tâche via la collection de déclencheurs.</span><span class="sxs-lookup"><span data-stu-id="16b16-124">In Task Scheduler 2.0, each trigger is defined by a separate trigger API that is associated with the task through the trigger collection.</span></span>

<span data-ttu-id="16b16-125">Dans Planificateur de tâches 1,0, plusieurs déclencheurs peuvent être considérés comme une planification, un ensemble de fois où la tâche démarre.</span><span class="sxs-lookup"><span data-stu-id="16b16-125">In Task Scheduler 1.0, multiple triggers can be thought of as a schedule, a set of times at which the task starts.</span></span> <span data-ttu-id="16b16-126">Dans ce cas, la planification est l’ensemble de fois (spécifié par l’Union de tous les déclencheurs associés à l’élément de travail) à laquelle un élément de travail s’exécutera.</span><span class="sxs-lookup"><span data-stu-id="16b16-126">In this case, the schedule is the set of times (specified by the union of all of the triggers associated with the work item) at which a work item will execute.</span></span>

## <a name="related-topics"></a><span data-ttu-id="16b16-127">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="16b16-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="16b16-128">Répétition d’une tâche</span><span class="sxs-lookup"><span data-stu-id="16b16-128">Repeating A Task</span></span>](repeating-a-task.md)
</dt> <dt>

[<span data-ttu-id="16b16-129">Types de déclencheurs</span><span class="sxs-lookup"><span data-stu-id="16b16-129">Trigger Types</span></span>](trigger-types.md)
</dt> <dt>

[<span data-ttu-id="16b16-130">Interfaces de déclencheur</span><span class="sxs-lookup"><span data-stu-id="16b16-130">Trigger Interfaces</span></span>](trigger-interfaces.md)
</dt> <dt>

[<span data-ttu-id="16b16-131">À propos de l’Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="16b16-131">About The Task Scheduler</span></span>](about-the-task-scheduler.md)
</dt> </dl>

 

 




