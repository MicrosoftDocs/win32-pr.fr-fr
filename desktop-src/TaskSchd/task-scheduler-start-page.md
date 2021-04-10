---
title: Planificateur de tâches pour les développeurs
description: Le Planificateur de tâches vous permet d’effectuer automatiquement des tâches de routine sur un ordinateur choisi. Pour ce faire, Planificateur de tâches analysez les critères que vous choisissez (appelés déclencheurs), puis exécutez les tâches lorsque ces critères sont satisfaits.
ms.assetid: 15970a51-c139-48b8-b82b-605728d0f386
keywords:
- Planificateur de tâches pour les développeurs
- Planificateur de tâches pour le développement
- Développement avec Planificateur de tâches
- Planificateur de tâches, page du portail
ms.topic: article
ms.date: 10/18/2019
ms.openlocfilehash: dfbfb76145e38003e7c501b98c817f4aaca3ff09
ms.sourcegitcommit: 087843ef08ddcd8bce9ed647b610035925da2b3e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/19/2019
ms.locfileid: "104100825"
---
# <a name="task-scheduler-for-developers"></a><span data-ttu-id="39cb2-108">Planificateur de tâches pour les développeurs</span><span class="sxs-lookup"><span data-stu-id="39cb2-108">Task Scheduler for developers</span></span>

> [!IMPORTANT]
> <span data-ttu-id="39cb2-109">Cette rubrique et les autres rubriques de cette section sont destinées aux développeurs.</span><span class="sxs-lookup"><span data-stu-id="39cb2-109">This topic and the other topics in this section are for a developer audience.</span></span> <span data-ttu-id="39cb2-110">Si vous souhaitez utiliser le composant Planificateur de tâches de votre capacité en tant qu’administrateur ou professionnel de l’informatique, consultez [Planificateur de tâches](/dynamics365/business-central/dev-itpro/developer/devenv-task-scheduler).</span><span class="sxs-lookup"><span data-stu-id="39cb2-110">If you're wishing to use the the Task Scheduler component in your capacity as an administrator, or an IT Professional, then see [Task Scheduler](/dynamics365/business-central/dev-itpro/developer/devenv-task-scheduler).</span></span>

## <a name="about-the-task-scheduler"></a><span data-ttu-id="39cb2-111">À propos de l’Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="39cb2-111">About the Task Scheduler</span></span>

<span data-ttu-id="39cb2-112">Le Planificateur de tâches vous permet d’effectuer automatiquement des tâches de routine sur un ordinateur choisi.</span><span class="sxs-lookup"><span data-stu-id="39cb2-112">The Task Scheduler enables you to automatically perform routine tasks on a chosen computer.</span></span> <span data-ttu-id="39cb2-113">Pour ce faire, Planificateur de tâches analysez les critères que vous choisissez (appelés déclencheurs), puis exécutez les tâches lorsque ces critères sont satisfaits.</span><span class="sxs-lookup"><span data-stu-id="39cb2-113">Task Scheduler does this by monitoring whatever criteria you choose (referred to as triggers) and then executing the tasks when those criteria are met.</span></span>

<span data-ttu-id="39cb2-114">Vous pouvez utiliser la Planificateur de tâches pour exécuter des tâches telles que le démarrage d’une application, l’envoi d’un message électronique ou l’émission d’un message.</span><span class="sxs-lookup"><span data-stu-id="39cb2-114">You can use the Task Scheduler to execute tasks such as starting an application, sending an email message, or showing a message box.</span></span> <span data-ttu-id="39cb2-115">Les tâches peuvent être planifiées pour s’exécuter en réponse à ces événements ou à ces déclencheurs.</span><span class="sxs-lookup"><span data-stu-id="39cb2-115">Tasks can be scheduled to execute in response to these events, or triggers.</span></span> 

- <span data-ttu-id="39cb2-116">Lorsqu’un événement système spécifique se produit.</span><span class="sxs-lookup"><span data-stu-id="39cb2-116">When a specific system event occurs.</span></span>
- <span data-ttu-id="39cb2-117">À un moment donné.</span><span class="sxs-lookup"><span data-stu-id="39cb2-117">At a specific time.</span></span>
- <span data-ttu-id="39cb2-118">À un moment donné sur une planification quotidienne.</span><span class="sxs-lookup"><span data-stu-id="39cb2-118">At a specific time on a daily schedule.</span></span>
- <span data-ttu-id="39cb2-119">À un moment donné sur une planification hebdomadaire.</span><span class="sxs-lookup"><span data-stu-id="39cb2-119">At a specific time on a weekly schedule.</span></span>
- <span data-ttu-id="39cb2-120">À un moment donné sur une planification mensuelle.</span><span class="sxs-lookup"><span data-stu-id="39cb2-120">At a specific time on a monthly schedule.</span></span>
- <span data-ttu-id="39cb2-121">À un moment donné, selon une planification mensuelle de jour de semaine.</span><span class="sxs-lookup"><span data-stu-id="39cb2-121">At a specific time on a monthly day-of-week schedule.</span></span>
- <span data-ttu-id="39cb2-122">Lorsque l’ordinateur passe à l’état inactif.</span><span class="sxs-lookup"><span data-stu-id="39cb2-122">When the computer enters an idle state.</span></span>
- <span data-ttu-id="39cb2-123">Lorsque la tâche est inscrite.</span><span class="sxs-lookup"><span data-stu-id="39cb2-123">When the task is registered.</span></span>
- <span data-ttu-id="39cb2-124">Lors du démarrage du système.</span><span class="sxs-lookup"><span data-stu-id="39cb2-124">When the system is booted.</span></span>
- <span data-ttu-id="39cb2-125">Lorsqu’un utilisateur ouvre une session.</span><span class="sxs-lookup"><span data-stu-id="39cb2-125">When a user logs on.</span></span>
- <span data-ttu-id="39cb2-126">Quand une session de Terminal Server change d’État.</span><span class="sxs-lookup"><span data-stu-id="39cb2-126">When a Terminal Server session changes state.</span></span>

## <a name="developers"></a><span data-ttu-id="39cb2-127">Développeurs</span><span class="sxs-lookup"><span data-stu-id="39cb2-127">Developers</span></span>

<span data-ttu-id="39cb2-128">Le Planificateur de tâches fournit des API dans ces formes.</span><span class="sxs-lookup"><span data-stu-id="39cb2-128">The Task Scheduler provides APIs in these forms.</span></span>

- <span data-ttu-id="39cb2-129">Planificateur de tâches 2,0 : les interfaces et les objets sont fournis pour C++ et, pour le développement de script, respectivement.</span><span class="sxs-lookup"><span data-stu-id="39cb2-129">Task Scheduler 2.0: interfaces and objects are provided for C++, and for scripting development, respectively.</span></span>
- <span data-ttu-id="39cb2-130">Planificateur de tâches 1,0 : les interfaces sont fournies pour le développement C++.</span><span class="sxs-lookup"><span data-stu-id="39cb2-130">Task Scheduler 1.0: interfaces are provided for C++ development.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="39cb2-131">Conditions d’exécution</span><span class="sxs-lookup"><span data-stu-id="39cb2-131">Run-time requirements</span></span>

<span data-ttu-id="39cb2-132">Le Planificateur de tâches requiert les systèmes d’exploitation suivants.</span><span class="sxs-lookup"><span data-stu-id="39cb2-132">The Task Scheduler requires the following operating systems.</span></span>

- <span data-ttu-id="39cb2-133">Planificateur de tâches 2,0 : le client requiert Windows Vista ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="39cb2-133">Task Scheduler 2.0: Client requires Windows Vista, or above.</span></span> <span data-ttu-id="39cb2-134">Le serveur nécessite Windows Server 2008 ou une version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="39cb2-134">Server requires Windows Server 2008, or above.</span></span>
- <span data-ttu-id="39cb2-135">Planificateur de tâches 1,0 : le client requiert Windows Vista ou Windows XP.</span><span class="sxs-lookup"><span data-stu-id="39cb2-135">Task Scheduler 1.0: Client requires Windows Vista, or Windows XP.</span></span> <span data-ttu-id="39cb2-136">Le serveur nécessite Windows Server 2008 ou Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="39cb2-136">Server requires Windows Server 2008, or Windows Server 2003.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="39cb2-137">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="39cb2-137">In this section</span></span>

| <span data-ttu-id="39cb2-138">Rubrique</span><span class="sxs-lookup"><span data-stu-id="39cb2-138">Topic</span></span> | <span data-ttu-id="39cb2-139">Description</span><span class="sxs-lookup"><span data-stu-id="39cb2-139">Description</span></span> |
|-|-|
| [<span data-ttu-id="39cb2-140">Nouveautés de Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="39cb2-140">What's new in Task Scheduler</span></span>](what-s-new-in-task-scheduler.md) | <span data-ttu-id="39cb2-141">Résumé des nouvelles fonctionnalités introduites par le Planificateur de tâches.</span><span class="sxs-lookup"><span data-stu-id="39cb2-141">Summary of new functionality introduced by the Task Scheduler.</span></span> |
| [<span data-ttu-id="39cb2-142">À propos de l’Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="39cb2-142">About the Task Scheduler</span></span>](about-the-task-scheduler.md) | <span data-ttu-id="39cb2-143">Informations conceptuelles générales sur l’API Planificateur de tâches.</span><span class="sxs-lookup"><span data-stu-id="39cb2-143">General conceptual information about the Task Scheduler API.</span></span> |
| [<span data-ttu-id="39cb2-144">Utilisation de l’Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="39cb2-144">Using the Task Scheduler</span></span>](using-the-task-scheduler.md) | <span data-ttu-id="39cb2-145">Exemples de code qui montrent comment utiliser les API Planificateur de tâches.</span><span class="sxs-lookup"><span data-stu-id="39cb2-145">Code examples that show how to use the Task Scheduler APIs.</span></span> |
| [<span data-ttu-id="39cb2-146">Référence Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="39cb2-146">Task Scheduler reference</span></span>](task-scheduler-reference.md) | <span data-ttu-id="39cb2-147">Informations de référence détaillées pour les API Planificateur de tâches et le schéma Planificateur de tâches.</span><span class="sxs-lookup"><span data-stu-id="39cb2-147">Detailed reference information for Task Scheduler APIs and the Task Scheduler schema.</span></span> |