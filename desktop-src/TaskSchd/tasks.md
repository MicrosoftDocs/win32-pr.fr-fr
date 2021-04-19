---
title: Tâches
description: Une tâche correspond au travail planifié effectué par le service Planificateur de tâches.
ms.assetid: 24c43834-5731-4b14-9409-7d7cf20b1a71
keywords:
- tâches Planificateur de tâches
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: efbb4ef41915ec70c98b59c9a7ba74c00f283ce6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106510631"
---
# <a name="tasks"></a><span data-ttu-id="ff02a-104">Tâches</span><span class="sxs-lookup"><span data-stu-id="ff02a-104">Tasks</span></span>

<span data-ttu-id="ff02a-105">Une tâche correspond au travail planifié effectué par le service Planificateur de tâches.</span><span class="sxs-lookup"><span data-stu-id="ff02a-105">A task is the scheduled work that the Task Scheduler service performs.</span></span> <span data-ttu-id="ff02a-106">Une tâche est composée de différents composants, mais une tâche doit contenir un déclencheur que le Planificateur de tâches utilise pour démarrer la tâche et une action qui décrit le travail que le Planificateur de tâches effectuera.</span><span class="sxs-lookup"><span data-stu-id="ff02a-106">A task is composed of different components, but a task must contain a trigger that the Task Scheduler uses to start the task and an action that describes what work the Task Scheduler will perform.</span></span>

<span data-ttu-id="ff02a-107">Quand une tâche est créée, elle est stockée dans un dossier de tâches.</span><span class="sxs-lookup"><span data-stu-id="ff02a-107">When a task is created, it is stored in a task folder.</span></span> <span data-ttu-id="ff02a-108">Les dossiers de tâches sont accessibles par le biais de l’interface [**ITaskFolder**](/windows/desktop/api/taskschd/nn-taskschd-itaskfolder) ([**TaskFolder**](taskfolder.md) pour les scripts), et les tâches sont accessibles via l’interface [**IRegisteredTask**](/windows/desktop/api/taskschd/nn-taskschd-iregisteredtask) ([**RegisteredTask**](registeredtask.md) pour les scripts) lors de leur création.</span><span class="sxs-lookup"><span data-stu-id="ff02a-108">Task folders can be accessed through the [**ITaskFolder**](/windows/desktop/api/taskschd/nn-taskschd-itaskfolder) interface ([**TaskFolder**](taskfolder.md) for scripting), and tasks can be accessed through the [**IRegisteredTask**](/windows/desktop/api/taskschd/nn-taskschd-iregisteredtask) interface ([**RegisteredTask**](registeredtask.md) for scripting) when they are created.</span></span> <span data-ttu-id="ff02a-109">Vous pouvez modifier les listes de contrôle d’accès (ACL) pour les tâches et les dossiers de tâches afin d’accorder ou de refuser à certains utilisateurs et groupes l’accès à un dossier de tâches ou de tâches.</span><span class="sxs-lookup"><span data-stu-id="ff02a-109">You can change access control lists (ACLs) for tasks and task folders in order to grant or deny certain users and groups access to a task or task folder.</span></span> <span data-ttu-id="ff02a-110">Cela peut être fait à l’aide de la méthode [**IRegisteredTask :: SetSecurityDescriptor**](/windows/desktop/api/taskschd/nf-taskschd-iregisteredtask-setsecuritydescriptor) , de la méthode [**ITaskFolder :: SetSecurityDescriptor**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-setsecuritydescriptor) ou en spécifiant un descripteur de sécurité lorsqu’une tâche est inscrite à l’aide de la méthode [**RegisterTaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertaskdefinition) ou [**RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) .</span><span class="sxs-lookup"><span data-stu-id="ff02a-110">This can be done by using the [**IRegisteredTask::SetSecurityDescriptor**](/windows/desktop/api/taskschd/nf-taskschd-iregisteredtask-setsecuritydescriptor) method, the [**ITaskFolder::SetSecurityDescriptor**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-setsecuritydescriptor) method, or by specifying a security descriptor when a task is registered by using the [**RegisterTaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertaskdefinition) or [**RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) method.</span></span>

> [!Note]  
> <span data-ttu-id="ff02a-111">Si le compte système local se voit refuser l’accès à un fichier de tâche ou à un dossier de tâches, le service Planificateur de tâches peut produire des résultats inattendus.</span><span class="sxs-lookup"><span data-stu-id="ff02a-111">If the Local System account is denied access to a task file or task folder, then the Task Scheduler service can produce unexpected results.</span></span>

 

## <a name="components-of-a-task"></a><span data-ttu-id="ff02a-112">Composants d’une tâche</span><span class="sxs-lookup"><span data-stu-id="ff02a-112">Components of a Task</span></span>

<span data-ttu-id="ff02a-113">L’illustration suivante montre les composants de tâche.</span><span class="sxs-lookup"><span data-stu-id="ff02a-113">The following illustration shows the task components.</span></span>

![composants de tâche](images/taskcomponents.png)

<span data-ttu-id="ff02a-115">La liste suivante contient une brève description de chaque composant de tâche :</span><span class="sxs-lookup"><span data-stu-id="ff02a-115">The following list contains a brief description of each task component:</span></span>

-   <span data-ttu-id="ff02a-116">Déclencheurs : Planificateur de tâches utilise des déclencheurs basés sur des événements ou sur le temps pour savoir quand démarrer une tâche.</span><span class="sxs-lookup"><span data-stu-id="ff02a-116">Triggers: Task Scheduler uses event or time-based triggers to know when to start a task.</span></span> <span data-ttu-id="ff02a-117">Chaque tâche peut spécifier un ou plusieurs déclencheurs pour démarrer la tâche.</span><span class="sxs-lookup"><span data-stu-id="ff02a-117">Every task can specify one or more triggers to start the task.</span></span>

    <span data-ttu-id="ff02a-118">Pour plus d’informations sur les déclencheurs, consultez [déclencheurs de tâches](task-triggers.md).</span><span class="sxs-lookup"><span data-stu-id="ff02a-118">For more information about triggers, see [Task Triggers](task-triggers.md).</span></span>

-   <span data-ttu-id="ff02a-119">Actions : actions, le travail réel, effectuées par la tâche.</span><span class="sxs-lookup"><span data-stu-id="ff02a-119">Actions: These are the actions, the actual work, that is performed by the task.</span></span> <span data-ttu-id="ff02a-120">Chaque tâche peut spécifier une ou plusieurs actions pour terminer son travail.</span><span class="sxs-lookup"><span data-stu-id="ff02a-120">Every task can specify one or more actions to complete its work.</span></span>

    <span data-ttu-id="ff02a-121">Pour plus d’informations sur les actions, consultez [actions des tâches](task-actions.md).</span><span class="sxs-lookup"><span data-stu-id="ff02a-121">For more information about actions, see [Task Actions](task-actions.md).</span></span>

-   <span data-ttu-id="ff02a-122">Principaux : les principaux définissent le contexte de sécurité dans lequel la tâche est exécutée.</span><span class="sxs-lookup"><span data-stu-id="ff02a-122">Principals: Principals define the security context in which the task is run.</span></span> <span data-ttu-id="ff02a-123">Par exemple, un principal peut définir un utilisateur ou un groupe d’utilisateurs spécifique qui peut exécuter la tâche.</span><span class="sxs-lookup"><span data-stu-id="ff02a-123">For example, a principal might define a specific user or user group that can run the task.</span></span>

    <span data-ttu-id="ff02a-124">Pour plus d’informations sur les principaux, consultez [contextes de sécurité pour les tâches](security-contexts-for-running-tasks.md).</span><span class="sxs-lookup"><span data-stu-id="ff02a-124">For more information about principals, see [Security Contexts for Tasks](security-contexts-for-running-tasks.md).</span></span>

-   <span data-ttu-id="ff02a-125">Paramètres : il s’agit des paramètres que le Planificateur de tâches utilise pour exécuter la tâche en ce qui concerne les conditions qui sont externes à la tâche elle-même.</span><span class="sxs-lookup"><span data-stu-id="ff02a-125">Settings: These are the settings that the Task Scheduler uses to run the task with respect to conditions that are external to the task itself.</span></span> <span data-ttu-id="ff02a-126">Par exemple, ces paramètres peuvent spécifier la priorité de la tâche par rapport à d’autres tâches, si plusieurs instances de la tâche peuvent être exécutées, comment la tâche est traitée lorsque l’ordinateur est dans une condition d’inactivité, ainsi que d’autres conditions.</span><span class="sxs-lookup"><span data-stu-id="ff02a-126">For example, these settings can specify the priority of the task with respect to other tasks, whether multiple instances of the task can be run, how the task is handled when the computer is in an idle condition, and other conditions.</span></span>

    <span data-ttu-id="ff02a-127">Pour plus d’informations sur les paramètres de tâche, consultez [**ITaskSettings**](/windows/desktop/api/taskschd/nn-taskschd-itasksettings) ([**TaskSettings**](tasksettings.md) pour les scripts).</span><span class="sxs-lookup"><span data-stu-id="ff02a-127">For more information about task settings, see [**ITaskSettings**](/windows/desktop/api/taskschd/nn-taskschd-itasksettings) ([**TaskSettings**](tasksettings.md) for scripting).</span></span>

    > [!Note]  
    > <span data-ttu-id="ff02a-128">Par défaut, une tâche sera arrêtée 72 heures après son démarrage.</span><span class="sxs-lookup"><span data-stu-id="ff02a-128">By default, a task will be stopped 72 hours after it starts to run.</span></span> <span data-ttu-id="ff02a-129">Vous pouvez modifier ce paramètre en modifiant le paramètre [**ExecutionTimeLimit**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_executiontimelimit) .</span><span class="sxs-lookup"><span data-stu-id="ff02a-129">You can change this by changing the [**ExecutionTimeLimit**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_executiontimelimit) setting.</span></span>

     

-   <span data-ttu-id="ff02a-130">Informations d’inscription : il s’agit d’informations d’administration collectées lorsque la tâche est inscrite.</span><span class="sxs-lookup"><span data-stu-id="ff02a-130">Registration Information: This is administrative information that is gathered when the task is registered.</span></span> <span data-ttu-id="ff02a-131">Par exemple, ces informations décrivent l’auteur de la tâche, la date à laquelle la tâche a été inscrite, une description XML de la tâche et d’autres informations.</span><span class="sxs-lookup"><span data-stu-id="ff02a-131">For example, this information describes the author of the task, the date when the task was registered, an XML description of the task, and other information.</span></span>

    <span data-ttu-id="ff02a-132">Pour plus d’informations sur l’inscription des tâches, consultez [informations d’inscription des tâches](task-registration-information.md).</span><span class="sxs-lookup"><span data-stu-id="ff02a-132">For more information about task registration information, see [Task Registration Information](task-registration-information.md).</span></span>

-   <span data-ttu-id="ff02a-133">Données : il s’agit d’une documentation supplémentaire sur la tâche fournie par l’auteur de la tâche.</span><span class="sxs-lookup"><span data-stu-id="ff02a-133">Data: This is additional documentation about the task that is supplied by the author of the task.</span></span> <span data-ttu-id="ff02a-134">Par exemple, ces données peuvent contenir une aide XML qui peut être utilisée par les utilisateurs lorsqu’ils exécutent la tâche.</span><span class="sxs-lookup"><span data-stu-id="ff02a-134">For example, this data may contain XML Help that can be used by users when they run the task.</span></span>

## <a name="task-apis"></a><span data-ttu-id="ff02a-135">API de tâche</span><span class="sxs-lookup"><span data-stu-id="ff02a-135">Task APIs</span></span>

<span data-ttu-id="ff02a-136">Planificateur de tâches 2,0 fournit deux ensembles d’API : un ensemble d’interfaces et d’objets de script pour Planificateur de tâches 2,0.</span><span class="sxs-lookup"><span data-stu-id="ff02a-136">Task Scheduler 2.0 provides two sets of APIs: a set of scripting objects and interfaces for Task Scheduler 2.0.</span></span> <span data-ttu-id="ff02a-137">Pour plus d’informations, consultez [Planificateur de tâches référence](task-scheduler-reference.md).</span><span class="sxs-lookup"><span data-stu-id="ff02a-137">For more information, see [Task Scheduler Reference](task-scheduler-reference.md).</span></span>

<span data-ttu-id="ff02a-138">La compatibilité des tâches, définie par la propriété de [**compatibilité**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_compatibility) , doit uniquement être définie sur \_ compatibilité \_ des tâches v1 si une tâche doit être accessible ou modifiée à partir d’un ordinateur Windows XP, Windows Server 2003 ou Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="ff02a-138">Task compatibility, which is set through the [**Compatibility**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_compatibility) property, should only be set to TASK\_COMPATIBILITY\_V1 if a task must be accessed or modified from a Windows XP, Windows Server 2003, or Windows 2000 computer.</span></span> <span data-ttu-id="ff02a-139">Dans le cas contraire, il est recommandé d’utiliser la compatibilité Planificateur de tâches 2,0, car elle a plus de fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="ff02a-139">Otherwise, it is recommended that you use Task Scheduler 2.0 compatibility because it has more features.</span></span>

<span data-ttu-id="ff02a-140">À compter de Planificateur de tâches 2,0, l’interface [**la**](/windows/desktop/api/taskschd/nn-taskschd-itaskservice) ([**TaskService**](taskservice.md) pour les scripts) est utilisée comme point de départ pour créer des tâches dans les dossiers spécifiés.</span><span class="sxs-lookup"><span data-stu-id="ff02a-140">Starting with Task Scheduler 2.0, the [**ITaskService**](/windows/desktop/api/taskschd/nn-taskschd-itaskservice) interface ([**TaskService**](taskservice.md) for scripting) is used as a starting point to create tasks in specified folders.</span></span> <span data-ttu-id="ff02a-141">L’interface [**ITaskDefinition**](/windows/desktop/api/taskschd/nn-taskschd-itaskdefinition) ([**TaskDefinition**](taskdefinition.md) pour les scripts) est utilisée pour contenir tous les composants d’une tâche, tels que les paramètres, les actions et les déclencheurs.</span><span class="sxs-lookup"><span data-stu-id="ff02a-141">The [**ITaskDefinition**](/windows/desktop/api/taskschd/nn-taskschd-itaskdefinition) interface ([**TaskDefinition**](taskdefinition.md) for scripting) is used to hold all the components of a task, such as the settings, actions, and triggers.</span></span> <span data-ttu-id="ff02a-142">Les API [**ITaskTrigger**](/windows/desktop/api/Mstask/nn-mstask-itasktrigger), [**IAction**](/windows/desktop/api/taskschd/nn-taskschd-iaction)et [**ITaskSettings**](/windows/desktop/api/taskschd/nn-taskschd-itasksettings) fournissent des propriétés qui sont ensuite utilisées pour définir les autres composants de la tâche.</span><span class="sxs-lookup"><span data-stu-id="ff02a-142">The [**ITaskTrigger**](/windows/desktop/api/Mstask/nn-mstask-itasktrigger), [**IAction**](/windows/desktop/api/taskschd/nn-taskschd-iaction), and [**ITaskSettings**](/windows/desktop/api/taskschd/nn-taskschd-itasksettings) APIs provide properties that are then used to define the other components of the task.</span></span> <span data-ttu-id="ff02a-143">Planificateur de tâches 1,0 fournit l’interface [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) , qui est prise en charge uniquement pour la compatibilité descendante.</span><span class="sxs-lookup"><span data-stu-id="ff02a-143">Task Scheduler 1.0 provides the [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) interface, which is supported only for backward compatibility.</span></span>

<span data-ttu-id="ff02a-144">Pour les scripts, les interfaces de Planificateur de tâches mappent aux objets de script qui ont des noms, des propriétés et des méthodes similaires.</span><span class="sxs-lookup"><span data-stu-id="ff02a-144">For scripting, the Task Scheduler interfaces map to scripting objects that have the similar names, properties, and methods.</span></span> <span data-ttu-id="ff02a-145">Par exemple, l’objet de script [**TaskService**](taskservice.md) a les mêmes propriétés et méthodes que l’interface [**la**](/windows/desktop/api/taskschd/nn-taskschd-itaskservice) .</span><span class="sxs-lookup"><span data-stu-id="ff02a-145">For example, the [**TaskService**](taskservice.md) scripting object has the same properties and methods as the [**ITaskService**](/windows/desktop/api/taskschd/nn-taskschd-itaskservice) interface.</span></span>

<span data-ttu-id="ff02a-146">Pour plus d’informations et des exemples sur l’utilisation des interfaces Planificateur de tâches, les objets de script et XML, consultez [utilisation du planificateur de tâches](using-the-task-scheduler.md).</span><span class="sxs-lookup"><span data-stu-id="ff02a-146">For more information and examples about how to use the Task Scheduler interfaces, scripting objects, and XML, see [Using the Task Scheduler](using-the-task-scheduler.md).</span></span>

### <a name="task-scheduler-10-tasks"></a><span data-ttu-id="ff02a-147">Planificateur de tâches les tâches 1,0</span><span class="sxs-lookup"><span data-stu-id="ff02a-147">Task Scheduler 1.0 Tasks</span></span>

<span data-ttu-id="ff02a-148">Une tâche Planificateur de tâches 1,0 est tout type d’application ou de fichier que le Planificateur de tâches peut exécuter.</span><span class="sxs-lookup"><span data-stu-id="ff02a-148">A Task Scheduler 1.0 task is any application or file type that the Task Scheduler can execute.</span></span> <span data-ttu-id="ff02a-149">Il peut s’agir de l’un des éléments suivants (pris en charge par le système d’exploitation sur lequel la tâche s’exécute) : les applications Win32, les applications Win16, les applications du système d’exploitation/2, les applications MS-DOS, les fichiers de commandes ( \* . bat), les fichiers de commandes ( \* . cmd) ou tout type de fichier correctement inscrit.</span><span class="sxs-lookup"><span data-stu-id="ff02a-149">These may include any of the following (as supported by the operating system on which the task will execute): Win32 applications, Win16 applications, OS/2 applications, MS-DOS applications, batch files (\*.bat), command files (\*.cmd), or any properly registered file type.</span></span>

<span data-ttu-id="ff02a-150">Les données qui décrivent une tâche sont conservées dans un fichier de tâches qui est stocké dans le dossier tâches planifiées.</span><span class="sxs-lookup"><span data-stu-id="ff02a-150">Data that describes a task is kept in a task file that is stored in the Scheduled Tasks folder.</span></span> <span data-ttu-id="ff02a-151">Pour plus d’informations, consultez [*dossier tâches planifiées*](s.md).</span><span class="sxs-lookup"><span data-stu-id="ff02a-151">For more information, see [*Scheduled Tasks folder*](s.md).</span></span> <span data-ttu-id="ff02a-152">Le nom de ces fichiers de tâches inclut le nom de la tâche, suivi de l’extension de nom de fichier. job.</span><span class="sxs-lookup"><span data-stu-id="ff02a-152">The name of these task files include the name of the task, followed by a .job file name extension.</span></span>

<span data-ttu-id="ff02a-153">Pour plus d’informations sur l’ajout d’Planificateur de tâches tâches 1,0, consultez [Ajout d’éléments de travail](adding-work-items.md).</span><span class="sxs-lookup"><span data-stu-id="ff02a-153">For more information about adding Task Scheduler 1.0 tasks, see [Adding Work Items](adding-work-items.md).</span></span>

<span data-ttu-id="ff02a-154">Pour plus d’informations sur l’énumération par le biais de Planificateur de tâches tâches 1,0, consultez [énumération de tâches](enumerating-tasks.md).</span><span class="sxs-lookup"><span data-stu-id="ff02a-154">For more information about enumerating through Task Scheduler 1.0 tasks, see [Enumerating Tasks](enumerating-tasks.md).</span></span>

<span data-ttu-id="ff02a-155">Pour qu’un ordinateur Windows Server 2003, Windows XP ou Windows 2000 crée, surveille ou contrôle des tâches sur un ordinateur Windows Vista, les opérations suivantes doivent être effectuées sur l’ordinateur Windows Vista, et l’utilisateur qui appelle la méthode [**ITaskScheduler :: SetTargetComputer**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-settargetcomputer) doit être membre du groupe Administrateurs sur l’ordinateur Windows Vista distant.</span><span class="sxs-lookup"><span data-stu-id="ff02a-155">For a Windows Server 2003, Windows XP, or Windows 2000 computer to create, monitor, or control tasks on a Windows Vista computer, the following operations should be completed on the Windows Vista computer, and the user who is calling the [**ITaskScheduler::SetTargetComputer**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-settargetcomputer) method must be a member of the Administrators group on the remote Windows Vista computer.</span></span>

<span data-ttu-id="ff02a-156">**Pour activer l’exception de partage de fichiers et d’imprimantes dans le pare-feu Windows**</span><span class="sxs-lookup"><span data-stu-id="ff02a-156">**To enable the "Share File and Printers" exception in Windows Firewall**</span></span>

1.  <span data-ttu-id="ff02a-157">Cliquez sur **Démarrer**, puis sur **Panneau de configuration**.</span><span class="sxs-lookup"><span data-stu-id="ff02a-157">Click **Start**, and then click **Control Panel**.</span></span>
2.  <span data-ttu-id="ff02a-158">Dans le **panneau de configuration**, cliquez sur **affichage classique** , puis double-cliquez sur l’icône **pare-feu Windows** .</span><span class="sxs-lookup"><span data-stu-id="ff02a-158">In **Control Panel**, click **Classic View** and then double-click the **Windows Firewall** icon.</span></span>
3.  <span data-ttu-id="ff02a-159">Dans la fenêtre **pare-feu Windows** , cliquez sur l’onglet **exceptions** et activez la case à cocher exception de **partage de fichiers et d’imprimantes** .</span><span class="sxs-lookup"><span data-stu-id="ff02a-159">In the **Windows Firewall** window, click the **Exceptions** tab and select **File and Printer Sharing exception** check box.</span></span>

<span data-ttu-id="ff02a-160">**Pour activer le service « Registre distant »**</span><span class="sxs-lookup"><span data-stu-id="ff02a-160">**To enable the "Remote Registry" service**</span></span>

-   <span data-ttu-id="ff02a-161">Ouvrez une fenêtre d’invite de commandes et entrez la commande suivante : **net start « Remote Registry »**.</span><span class="sxs-lookup"><span data-stu-id="ff02a-161">Open a Command Prompt window and enter the following command: **net start "Remote Registry"**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ff02a-162">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ff02a-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ff02a-163">À propos de l’Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="ff02a-163">About the Task Scheduler</span></span>](about-the-task-scheduler.md)
</dt> <dt>

[<span data-ttu-id="ff02a-164">Déclencheurs de tâche</span><span class="sxs-lookup"><span data-stu-id="ff02a-164">Task Triggers</span></span>](task-triggers.md)
</dt> <dt>

[<span data-ttu-id="ff02a-165">Actions de tâche</span><span class="sxs-lookup"><span data-stu-id="ff02a-165">Task Actions</span></span>](task-actions.md)
</dt> <dt>

[<span data-ttu-id="ff02a-166">**ITaskDefinition**</span><span class="sxs-lookup"><span data-stu-id="ff02a-166">**ITaskDefinition**</span></span>](/windows/desktop/api/taskschd/nn-taskschd-itaskdefinition)
</dt> <dt>

[<span data-ttu-id="ff02a-167">**TaskDefinition**</span><span class="sxs-lookup"><span data-stu-id="ff02a-167">**TaskDefinition**</span></span>](taskdefinition.md)
</dt> <dt>

[<span data-ttu-id="ff02a-168">**La**</span><span class="sxs-lookup"><span data-stu-id="ff02a-168">**ITaskService**</span></span>](/windows/desktop/api/taskschd/nn-taskschd-itaskservice)
</dt> <dt>

[<span data-ttu-id="ff02a-169">**TaskService**</span><span class="sxs-lookup"><span data-stu-id="ff02a-169">**TaskService**</span></span>](taskservice.md)
</dt> </dl>

 

 




