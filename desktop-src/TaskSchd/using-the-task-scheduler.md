---
title: Utilisation de l’Planificateur de tâches
description: Cette section contient des exemples de code qui illustrent l’utilisation de l’API Planificateur de tâches et des exemples XML qui montrent comment les tâches sont définies dans le schéma de Planificateur de tâches.
ms.assetid: 6346cbd3-b584-47b4-8313-7830f7fd77b3
keywords:
- déclencheurs Planificateur de tâches, exemples
- démarrage d’une tâche Planificateur de tâches
- création de tâches Planificateur de tâches
- Planificateur de tâches Planificateur de tâches, utilisation
- Exemples de Planificateur de tâches Planificateur de tâches
- Planificateur de tâches Planificateur de tâches, vous trouverez des exemples Planificateur de tâches Planificateur de tâches
- exemples Planificateur de tâches consultez Planificateur de tâches des exemples Planificateur de tâches
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f81dda9551917b8f6345248a316bd5941de53f0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106511808"
---
# <a name="using-the-task-scheduler"></a><span data-ttu-id="8fbae-110">Utilisation de l’Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="8fbae-110">Using the Task Scheduler</span></span>

<span data-ttu-id="8fbae-111">Cette section contient des exemples de code qui illustrent l’utilisation de l’API Planificateur de tâches et des exemples XML qui montrent comment les tâches sont définies dans le schéma de Planificateur de tâches.</span><span class="sxs-lookup"><span data-stu-id="8fbae-111">This section contains code examples that illustrate how the Task Scheduler API is used and XML examples that show how tasks are defined in the Task Scheduler schema.</span></span> <span data-ttu-id="8fbae-112">La plupart de ces exemples sont du code autonome qui peut être exécuté indépendamment ou collé dans une application plus volumineuse et modifié selon les exigences de l’application.</span><span class="sxs-lookup"><span data-stu-id="8fbae-112">Most of these examples are stand-alone code that can be run independently, or pasted into a larger application and modified to the requirements of the application.</span></span>

<span data-ttu-id="8fbae-113">Le tableau suivant répertorie Planificateur de tâches exemples 2,0 inclus dans cette section.</span><span class="sxs-lookup"><span data-stu-id="8fbae-113">The following table lists Task Scheduler 2.0 examples included in this section.</span></span>



| <span data-ttu-id="8fbae-114">Exemple</span><span class="sxs-lookup"><span data-stu-id="8fbae-114">Example</span></span>                                                                                                    | <span data-ttu-id="8fbae-115">Description</span><span class="sxs-lookup"><span data-stu-id="8fbae-115">Description</span></span>                                                                            |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [<span data-ttu-id="8fbae-116">Démarrage d’un exécutable à une heure spécifique</span><span class="sxs-lookup"><span data-stu-id="8fbae-116">Starting an Executable at a Specific Time</span></span>](starting-an-executable-at-a-spcific-time.md)                  | <span data-ttu-id="8fbae-117">Définit une tâche qui démarre le bloc-notes à une heure spécifiée.</span><span class="sxs-lookup"><span data-stu-id="8fbae-117">Defines a task that starts Notepad at a specified time.</span></span>                                |
| [<span data-ttu-id="8fbae-118">Démarrage quotidien d’un exécutable</span><span class="sxs-lookup"><span data-stu-id="8fbae-118">Starting an Executable Daily</span></span>](starting-an-executable-daily.md)                                           | <span data-ttu-id="8fbae-119">Définit une tâche qui démarre le bloc-notes quotidiennement.</span><span class="sxs-lookup"><span data-stu-id="8fbae-119">Defines a task that starts Notepad daily.</span></span>                                              |
| [<span data-ttu-id="8fbae-120">Démarrage d’un exécutable au démarrage du système</span><span class="sxs-lookup"><span data-stu-id="8fbae-120">Starting an Executable on System Boot</span></span>](starting-an-executable-on-system-boot.md)                         | <span data-ttu-id="8fbae-121">Définit une tâche qui démarre le bloc-notes au démarrage du système.</span><span class="sxs-lookup"><span data-stu-id="8fbae-121">Defines a task that starts Notepad when the system is booted.</span></span>                          |
| [<span data-ttu-id="8fbae-122">Démarrage d’un exécutable hebdomadaire</span><span class="sxs-lookup"><span data-stu-id="8fbae-122">Starting an Executable Weekly</span></span>](starting-an-executable-weekly.md)                                         | <span data-ttu-id="8fbae-123">Définit une tâche qui démarre le bloc-notes chaque semaine.</span><span class="sxs-lookup"><span data-stu-id="8fbae-123">Defines a task that starts Notepad on a weekly basis.</span></span>                                  |
| [<span data-ttu-id="8fbae-124">Démarrage d’un exécutable quand une tâche est inscrite</span><span class="sxs-lookup"><span data-stu-id="8fbae-124">Starting an Executable When a Task is Registered</span></span>](starting-an-executable-when-a-task-is-registered.md)   | <span data-ttu-id="8fbae-125">Définit une tâche qui démarre le bloc-notes lorsque la tâche est inscrite.</span><span class="sxs-lookup"><span data-stu-id="8fbae-125">Defines a task that starts Notepad when the task is registered.</span></span>                        |
| [<span data-ttu-id="8fbae-126">Démarrage d’un exécutable lorsqu’un utilisateur ouvre une session</span><span class="sxs-lookup"><span data-stu-id="8fbae-126">Starting an Executable When a User Logs On</span></span>](starting-an-executable-when-a-user-logs-on.md)               | <span data-ttu-id="8fbae-127">Définit une tâche qui démarre le bloc-notes lorsqu’un utilisateur ouvre une session.</span><span class="sxs-lookup"><span data-stu-id="8fbae-127">Defines a task that starts Notepad when a user logs on.</span></span>                                |
| [<span data-ttu-id="8fbae-128">Énumération des tâches et affichage des informations sur les tâches</span><span class="sxs-lookup"><span data-stu-id="8fbae-128">Enumerating Tasks and Displaying Task Information</span></span>](enumerating-tasks-and-displaying-task-information.md) | <span data-ttu-id="8fbae-129">Énumère toutes les tâches sur l’ordinateur local et affiche l’état de chaque tâche.</span><span class="sxs-lookup"><span data-stu-id="8fbae-129">Enumerates through all the tasks on the local computer and displays each task's state.</span></span> |



 

<span data-ttu-id="8fbae-130">Le tableau suivant répertorie Planificateur de tâches exemples 1,0 inclus dans cette section.</span><span class="sxs-lookup"><span data-stu-id="8fbae-130">The following table lists Task Scheduler 1.0 examples included in this section.</span></span> 

| <span data-ttu-id="8fbae-131">Exemple</span><span class="sxs-lookup"><span data-stu-id="8fbae-131">Example</span></span>                                                                                    | <span data-ttu-id="8fbae-132">Description</span><span class="sxs-lookup"><span data-stu-id="8fbae-132">Description</span></span>                                                                                   |
|--------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8fbae-133">Exemple de création d’une tâche à l’aide de NewWorkItem</span><span class="sxs-lookup"><span data-stu-id="8fbae-133">Creating a Task Using NewWorkItem Example</span></span>](creating-a-task-using-newworkitem-example.md) | <span data-ttu-id="8fbae-134">Crée une nouvelle tâche.</span><span class="sxs-lookup"><span data-stu-id="8fbae-134">Creates a new task.</span></span>                                                                           |
| [<span data-ttu-id="8fbae-135">Exemple d’énumération de tâches</span><span class="sxs-lookup"><span data-stu-id="8fbae-135">Enumerating Tasks Example</span></span>](enumerating-tasks-example.md)                                 | <span data-ttu-id="8fbae-136">Énumère toutes les tâches sur l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="8fbae-136">Enumerates all the tasks on the local computer.</span></span>                                               |
| [<span data-ttu-id="8fbae-137">Exemple de démarrage d’une tâche</span><span class="sxs-lookup"><span data-stu-id="8fbae-137">Starting a Task Example</span></span>](starting-a-task-example.md)                                     | <span data-ttu-id="8fbae-138">Démarre une tâche connue.</span><span class="sxs-lookup"><span data-stu-id="8fbae-138">Starts a known task.</span></span>                                                                          |
| [<span data-ttu-id="8fbae-139">Modification d’un élément de travail à l’aide des pages de propriétés</span><span class="sxs-lookup"><span data-stu-id="8fbae-139">Editing a Work Item using Property Pages</span></span>](editing-a-work-item-using-property-pages.md)   | <span data-ttu-id="8fbae-140">Affiche les pages de propriétés d’une tâche à modifier.</span><span class="sxs-lookup"><span data-stu-id="8fbae-140">Displays the property pages of a task for editing.</span></span>                                            |
| [<span data-ttu-id="8fbae-141">Récupération d’exemples de propriétés d’élément de travail</span><span class="sxs-lookup"><span data-stu-id="8fbae-141">Retrieving Work Item Property Examples</span></span>](retrieving-work-item-property-examples.md)       | <span data-ttu-id="8fbae-142">Ensemble d’exemples qui montrent comment récupérer des propriétés qui s’appliquent à tous les types d’éléments de travail.</span><span class="sxs-lookup"><span data-stu-id="8fbae-142">A set of examples that show how to retrieve properties that apply to all types of work items.</span></span> |
| [<span data-ttu-id="8fbae-143">Définition d’exemples de propriétés d’élément de travail</span><span class="sxs-lookup"><span data-stu-id="8fbae-143">Setting Work Item Property Examples</span></span>](setting-work-item-property-examples.md)             | <span data-ttu-id="8fbae-144">Ensemble d’exemples qui montrent comment définir les propriétés qui s’appliquent à tous les types d’éléments de travail.</span><span class="sxs-lookup"><span data-stu-id="8fbae-144">A set of examples that show how to set properties that apply to all types of work items.</span></span>      |
| [<span data-ttu-id="8fbae-145">Récupération d’exemples de propriétés de tâche</span><span class="sxs-lookup"><span data-stu-id="8fbae-145">Retrieving Task Property Examples</span></span>](retrieving-task-property-examples.md)                 | <span data-ttu-id="8fbae-146">Ensemble d’exemples qui montrent comment récupérer des propriétés propres aux tâches.</span><span class="sxs-lookup"><span data-stu-id="8fbae-146">A set of examples that show how to retrieve properties unique to tasks.</span></span>                       |
| [<span data-ttu-id="8fbae-147">Définition des exemples de propriétés de tâche</span><span class="sxs-lookup"><span data-stu-id="8fbae-147">Setting Task Property Examples</span></span>](setting-task-property-examples.md)                       | <span data-ttu-id="8fbae-148">Ensemble d’exemples qui montrent comment définir des propriétés propres aux tâches.</span><span class="sxs-lookup"><span data-stu-id="8fbae-148">A set of examples that show how to set properties unique to tasks.</span></span>                            |
| [<span data-ttu-id="8fbae-149">Exemple de récupération d’une page de tâche</span><span class="sxs-lookup"><span data-stu-id="8fbae-149">Retrieving a Task Page Example</span></span>](retrieving-a-task-page-example.md)                       | <span data-ttu-id="8fbae-150">Récupère et affiche la page de tâches générale d’une tâche connue.</span><span class="sxs-lookup"><span data-stu-id="8fbae-150">Retrieves and displays the general task page of a known task.</span></span>                                 |
| [<span data-ttu-id="8fbae-151">Création d’un déclencheur</span><span class="sxs-lookup"><span data-stu-id="8fbae-151">Creating a New Trigger</span></span>](creating-a-new-trigger.md)                                       | <span data-ttu-id="8fbae-152">Crée un déclencheur pour une tâche connue.</span><span class="sxs-lookup"><span data-stu-id="8fbae-152">Creates a new trigger for a known task.</span></span>                                                       |
| [<span data-ttu-id="8fbae-153">Exemple de création d’un déclencheur inactif</span><span class="sxs-lookup"><span data-stu-id="8fbae-153">Creating an Idle Trigger Example</span></span>](creating-an-idle-trigger-example.md)                   | <span data-ttu-id="8fbae-154">Crée un déclencheur inactif basé sur les événements pour une tâche connue.</span><span class="sxs-lookup"><span data-stu-id="8fbae-154">Creates an event-based idle trigger for a known task.</span></span>                                         |
| [<span data-ttu-id="8fbae-155">Exemple de fin d’une tâche</span><span class="sxs-lookup"><span data-stu-id="8fbae-155">Terminating a Task Example</span></span>](terminating-a-task-example.md)                               | <span data-ttu-id="8fbae-156">Met fin à une tâche alors qu’elle est en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="8fbae-156">Terminates a task while it is running.</span></span>                                                        |
| [<span data-ttu-id="8fbae-157">Exemple de récupération de chaînes de déclencheur</span><span class="sxs-lookup"><span data-stu-id="8fbae-157">Retrieving Trigger Strings Example</span></span>](retrieving-trigger-strings-example.md)               | <span data-ttu-id="8fbae-158">Récupère la chaîne de déclenchement de tous les déclencheurs associés à une tâche connue.</span><span class="sxs-lookup"><span data-stu-id="8fbae-158">Retrieves the trigger string of all triggers associated with a known task.</span></span>                    |



 

## <a name="related-topics"></a><span data-ttu-id="8fbae-159">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="8fbae-159">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8fbae-160">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="8fbae-160">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="8fbae-161">À propos de l’Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="8fbae-161">About The Task Scheduler</span></span>](about-the-task-scheduler.md)
</dt> </dl>

 

 




