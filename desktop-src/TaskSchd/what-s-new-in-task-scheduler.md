---
title: Nouveautés de Planificateur de tâches
description: Liste des nouvelles fonctionnalités introduites par différentes versions de Planificateur de tâches.
ms.assetid: 43fbbbd2-6e97-4ba5-9474-23c5e2b33612
keywords:
- Planificateur de tâches Planificateur de tâches, nouveautés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5245ab4e681af937924cfbd217095009d80d6a11
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106541178"
---
# <a name="whats-new-in-task-scheduler"></a><span data-ttu-id="7f74f-104">Nouveautés de Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="7f74f-104">What's New in Task Scheduler</span></span>

<span data-ttu-id="7f74f-105">Les modifications suivantes résument ce qui est nouveau dans les différentes versions de Planificateur de tâches.</span><span class="sxs-lookup"><span data-stu-id="7f74f-105">The following changes summarize what is new in different versions of Task Scheduler.</span></span>

## <a name="windows-10-and-windows-server-2016"></a><span data-ttu-id="7f74f-106">Windows 10 (et Windows Server 2016)</span><span class="sxs-lookup"><span data-stu-id="7f74f-106">Windows 10 (and Windows Server 2016)</span></span>

<span data-ttu-id="7f74f-107">Les modifications de Planificateur de tâches suivantes sont introduites dans Windows 10.</span><span class="sxs-lookup"><span data-stu-id="7f74f-107">The following Task Scheduler changes are introduced in Windows 10.</span></span>

-   <span data-ttu-id="7f74f-108">Lorsque l’économiseur de batterie est activé, les tâches de Planificateur de tâches Windows sont déclenchées uniquement si la tâche est :</span><span class="sxs-lookup"><span data-stu-id="7f74f-108">When battery saver is on, Windows Task Scheduler tasks are triggered only if the task is:</span></span>

    -   <span data-ttu-id="7f74f-109">Non défini pour **Démarrer la tâche uniquement si l’ordinateur est inactif... (la** tâche n’utilise pas [**IdleSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_idlesettings))</span><span class="sxs-lookup"><span data-stu-id="7f74f-109">Not set to **Start the task only if the computer is idle...** (task doesn't use [**IdleSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_idlesettings))</span></span>
    -   <span data-ttu-id="7f74f-110">Non défini pour s’exécuter pendant la maintenance automatique (la tâche n’utilise pas [**MaintenanceSettings**](/windows/desktop/api/Taskschd/nf-taskschd-itasksettings3-get_maintenancesettings))</span><span class="sxs-lookup"><span data-stu-id="7f74f-110">Not set to run during automatic maintenance (task doesn't use [**MaintenanceSettings**](/windows/desktop/api/Taskschd/nf-taskschd-itasksettings3-get_maintenancesettings))</span></span>
    -   <span data-ttu-id="7f74f-111">Est configuré pour **s’exécuter uniquement quand l’utilisateur a ouvert une session** (la tâche [**LogonType**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_logontype) est un **\_ \_ \_ jeton interactif d’ouverture de session de tâche** ou un **\_ \_ groupe d’ouverture de session de tâche**)</span><span class="sxs-lookup"><span data-stu-id="7f74f-111">Is set to **Run only when user is logged on** (task [**LogonType**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_logontype) is **TASK\_LOGON\_INTERACTIVE\_TOKEN** or **TASK\_LOGON\_GROUP**)</span></span>

    <span data-ttu-id="7f74f-112">Tous les autres déclencheurs sont retardés jusqu’à ce que l’économiseur de batterie soit désactivé.</span><span class="sxs-lookup"><span data-stu-id="7f74f-112">All other triggers are delayed until battery saver is off.</span></span> <span data-ttu-id="7f74f-113">Pour plus d’informations sur l’accès à l’état de l’économiseur de batterie dans votre application, consultez [**\_ \_ État**](/windows/desktop/api/winbase/ns-winbase-system_power_status)de l’alimentation du système.</span><span class="sxs-lookup"><span data-stu-id="7f74f-113">For more information about accessing battery saver status in your application, see [**SYSTEM\_POWER\_STATUS**](/windows/desktop/api/winbase/ns-winbase-system_power_status).</span></span> <span data-ttu-id="7f74f-114">Pour obtenir des informations générales sur l’économiseur de batterie, consultez [économiseur de batterie (dans les instructions relatives aux composants matériels)](/windows-hardware/design/component-guidelines/battery-saver).</span><span class="sxs-lookup"><span data-stu-id="7f74f-114">For general information about battery saver, see [battery saver (in the hardware component guidelines)](/windows-hardware/design/component-guidelines/battery-saver).</span></span>

-   <span data-ttu-id="7f74f-115">Pour des raisons de sécurité, un utilisateur non-administrateur ne peut pas afficher ni gérer une tâche de Planificateur de tâches Windows qui a été créée par un autre utilisateur.</span><span class="sxs-lookup"><span data-stu-id="7f74f-115">For security reasons, a non-administrator user cannot view nor manage a Windows Task Scheduler task that was created by another user.</span></span>

## <a name="windows-8"></a><span data-ttu-id="7f74f-116">Windows 8</span><span class="sxs-lookup"><span data-stu-id="7f74f-116">Windows 8</span></span>

<span data-ttu-id="7f74f-117">Les modifications suivantes Planificateur de tâches 2,0 sont introduites dans Windows 8 :</span><span class="sxs-lookup"><span data-stu-id="7f74f-117">The following Task Scheduler 2.0 changes are introduced in Windows 8:</span></span>

-   <span data-ttu-id="7f74f-118">Prise en charge de PowerShell : les utilisateurs peuvent gérer (créer, supprimer, modifier, démarrer explicitement, arrêter, etc.) Windows Planificateur de tâches les tâches à l’aide du module PowerShell ScheduledTasks.</span><span class="sxs-lookup"><span data-stu-id="7f74f-118">Powershell support: users can manage (create, delete, modify, explicitly start, stop etc.) Windows Task Scheduler tasks using the ScheduledTasks powershell module.</span></span>
-   <span data-ttu-id="7f74f-119">Mots de passe managés : les administrateurs peuvent utiliser les comptes de mots de passe gérés Active Directory en tant que principaux de tâche.</span><span class="sxs-lookup"><span data-stu-id="7f74f-119">Managed passwords: administrators can use the Active Directory managed password accounts as task principals.</span></span> <span data-ttu-id="7f74f-120">Ces tâches ne nécessitent plus une stratégie de réinitialisation de mot de passe appliquée.</span><span class="sxs-lookup"><span data-stu-id="7f74f-120">These tasks no longer require an enforced password reset policy.</span></span>
-   <span data-ttu-id="7f74f-121">Modifications de l’API : a introduit deux nouveaux paramètres de tâche avec l’interface [**ITaskSettings3**](/windows/desktop/api/taskschd/nn-taskschd-itasksettings3) .</span><span class="sxs-lookup"><span data-stu-id="7f74f-121">API changes: Introduced two new task settings with the [**ITaskSettings3**](/windows/desktop/api/taskschd/nn-taskschd-itasksettings3) interface.</span></span>
    -   <span data-ttu-id="7f74f-122">[**MaintenanceSettings**](/windows/desktop/api/Taskschd/nf-taskschd-itasksettings3-get_maintenancesettings): les tâches qui utilisent ces paramètres sont traitées comme un nouveau type de tâches planifiées qui sont appelées pendant la durée de maintenance automatique du système d’exploitation, en fonction de la périodicité et de l’échéance spécifiées.</span><span class="sxs-lookup"><span data-stu-id="7f74f-122">[**MaintenanceSettings**](/windows/desktop/api/Taskschd/nf-taskschd-itasksettings3-get_maintenancesettings): tasks using these settings are treated as a new type of scheduled tasks that are invoked during OS automatic maintenance time, according to the specified periodicity and deadline.</span></span>
    -   <span data-ttu-id="7f74f-123">[**Volatile**](/windows/desktop/api/Taskschd/nf-taskschd-itasksettings3-get_volatile): les tâches qui sont configurées pour être volatiles sont toujours désactivées sur un démarrage du système d’exploitation et doivent être explicitement réactivées quand cela est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="7f74f-123">[**Volatile**](/windows/desktop/api/Taskschd/nf-taskschd-itasksettings3-get_volatile): tasks that are set to be volatile are always disabled on an OS boot and must be explicitly re-enabled back when required.</span></span> <span data-ttu-id="7f74f-124">Les tâches volatiles sont utilisées par les clusters de basculement pour s’assurer qu’une seule instance de tâche est planifiée sur un cluster à la fois.</span><span class="sxs-lookup"><span data-stu-id="7f74f-124">Volatile tasks are utilized by the failover clusters to ensure only one task instance is scheduled on a cluster at a time.</span></span>
-   <span data-ttu-id="7f74f-125">Le moteur de planification unifiée prend désormais en charge les fonctionnalités suivantes :</span><span class="sxs-lookup"><span data-stu-id="7f74f-125">The unified scheduling engine now supports the following features:</span></span>
    -   <span data-ttu-id="7f74f-126">Type d’ouverture de session S4U, via l’élément [**LogonType**](taskschedulerschema-logontype-principaltype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="7f74f-126">S4U Logon type, through the [**LogonType**](taskschedulerschema-logontype-principaltype-element.md) element.</span></span>
    -   <span data-ttu-id="7f74f-127">Valeurs de requête XPath pour les déclencheurs d’événements, via l’élément [**ValueQueries**](taskschedulerschema-valuequeries-eventtriggertype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="7f74f-127">XPath query values for event triggers, through the [**ValueQueries**](taskschedulerschema-valuequeries-eventtriggertype-element.md) element.</span></span>
    -   <span data-ttu-id="7f74f-128">N’autorisez pas l’arrêt forcé de la tâche, via l’élément [**AllowHardTerminate**](taskschedulerschema-allowhardterminate-settingstype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="7f74f-128">Do not allow task hard terminate, through the [**AllowHardTerminate**](taskschedulerschema-allowhardterminate-settingstype-element.md) element.</span></span>
-   <span data-ttu-id="7f74f-129">Fonctionnalités dépréciées dans cette version</span><span class="sxs-lookup"><span data-stu-id="7f74f-129">Features deprecated in this release</span></span>
    -   <span data-ttu-id="7f74f-130">Action : [**SendEmail**](taskschedulerschema-sendemail-actiongroup-element.md) (vous pouvez utiliser [**IExecAction**](/windows/desktop/api/taskschd/nn-taskschd-iexecaction) avec l’applet de commande [Windows PowerShell](https://technet.microsoft.com/library/bb978526.aspx)[Send-MailMessage](/powershell/module/microsoft.powershell.utility/send-mailmessage?view=powershell-7&preserve-view=true) comme solution de contournement).</span><span class="sxs-lookup"><span data-stu-id="7f74f-130">Action: [**sendEmail**](taskschedulerschema-sendemail-actiongroup-element.md) (you can use [**IExecAction**](/windows/desktop/api/taskschd/nn-taskschd-iexecaction) with the [Windows PowerShell](https://technet.microsoft.com/library/bb978526.aspx)[Send-MailMessage](/powershell/module/microsoft.powershell.utility/send-mailmessage?view=powershell-7&preserve-view=true) cmdlet as a workaround).</span></span>
    -   <span data-ttu-id="7f74f-131">Action : [**showMessage**](taskschedulerschema-showmessage-actiongroup-element.md).</span><span class="sxs-lookup"><span data-stu-id="7f74f-131">Action: [**showMessage**](taskschedulerschema-showmessage-actiongroup-element.md).</span></span>
    -   <span data-ttu-id="7f74f-132">Utilitaire AT.exe cmdline</span><span class="sxs-lookup"><span data-stu-id="7f74f-132">AT.exe cmdline utility</span></span>

## <a name="windows-7"></a><span data-ttu-id="7f74f-133">Windows 7</span><span class="sxs-lookup"><span data-stu-id="7f74f-133">Windows 7</span></span>

<span data-ttu-id="7f74f-134">Les modifications suivantes de l’Planificateur de tâches 2,0 sont introduites dans Windows 7 :</span><span class="sxs-lookup"><span data-stu-id="7f74f-134">The following Task Scheduler 2.0 changes are introduced in Windows 7:</span></span>

-   <span data-ttu-id="7f74f-135">Utilisation du moteur de planification unifié fourni par le système d’exploitation sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="7f74f-135">Using the unified scheduling engine provided by the underlying operating system.</span></span>
-   <span data-ttu-id="7f74f-136">Possibilité de rejeter les tâches de démarrage dans les sessions d’applications à distance intégrées (RAIL).</span><span class="sxs-lookup"><span data-stu-id="7f74f-136">Ability to reject starting tasks in Remote Applications Integrated Locally (RAIL) sessions.</span></span>
-   <span data-ttu-id="7f74f-137">Renforcement de la sécurité des tâches (pour les tâches qui s’exécutent en tant que « SERVICE réseau » ou « SERVICE LOCAL » uniquement) :</span><span class="sxs-lookup"><span data-stu-id="7f74f-137">Task security hardening (for tasks running as "NETWORK SERVICE" or "LOCAL SERVICE" only):</span></span>

    -   <span data-ttu-id="7f74f-138">Possibilité d’assigner un type d’identificateur de sécurité (SID) de jeton de processus (par exemple, sans restriction ou aucune) à une tâche.</span><span class="sxs-lookup"><span data-stu-id="7f74f-138">Ability to assign a process token security identifier (SID) type (for example, unrestricted or none) to a task.</span></span>
    -   <span data-ttu-id="7f74f-139">Autorisez les développeurs de tâches à demander le jeu exact de privilèges requis par leur tâche.</span><span class="sxs-lookup"><span data-stu-id="7f74f-139">Allow task developers to request the exact set of privileges that their task requires.</span></span>

-   <span data-ttu-id="7f74f-140">Modifications de l’API :</span><span class="sxs-lookup"><span data-stu-id="7f74f-140">API changes:</span></span>

    -   <span data-ttu-id="7f74f-141">Prise en charge du renforcement de la sécurité des tâches : la nouvelle fonctionnalité de renforcement de la sécurité des tâches est introduite avec une nouvelle interface IPrincipal2.</span><span class="sxs-lookup"><span data-stu-id="7f74f-141">Task security hardening support: new task security hardening feature is introduced with new IPrincipal2 interface.</span></span>
    -   <span data-ttu-id="7f74f-142">A introduit deux nouveaux paramètres de tâche avec la nouvelle interface ITaskSettings2.</span><span class="sxs-lookup"><span data-stu-id="7f74f-142">Introduced two new task settings with the new ITaskSettings2 interface.</span></span>

        -   <span data-ttu-id="7f74f-143">DisallowStartOnRemoteAppSession : le nouveau paramètre DisallowStartOnRemoteAppSession peut rejeter le démarrage d’une tâche si elle est déclenchée dans des sessions [intégrées (rail) intégrées à des applications distantes](/openspecs/windows_protocols/MS-WINPROTLP/df36f95e-6a6b-48d6-a3ae-35a17674f546) .</span><span class="sxs-lookup"><span data-stu-id="7f74f-143">DisallowStartOnRemoteAppSession: The new DisallowStartOnRemoteAppSession setting can reject a task start if triggered in [Remote Applications Integrated Locally (RAIL)](/openspecs/windows_protocols/MS-WINPROTLP/df36f95e-6a6b-48d6-a3ae-35a17674f546) sessions.</span></span>
        -   <span data-ttu-id="7f74f-144">UseUnifiedSchedulingEngine : l’utilisation du paramètre UseUnifiedSchedulingEngine fournit un comportement cohésif pour les tâches et les services Windows, car elle est gérée de façon uniforme par un moteur de planification commun à l’ensemble du système.</span><span class="sxs-lookup"><span data-stu-id="7f74f-144">UseUnifiedSchedulingEngine: Using the UseUnifiedSchedulingEngine setting provides a cohesive behavior for Windows Tasks and Services because it is being managed in a uniform manner by a common system-wide scheduling engine.</span></span> <span data-ttu-id="7f74f-145">Bien qu’il soit recommandé d’utiliser un moteur unifié, il ne prend pas en charge certaines fonctionnalités de Planificateur de tâches.</span><span class="sxs-lookup"><span data-stu-id="7f74f-145">Although using a unified engine is recommended, it does not support some of the Task Scheduler features.</span></span> <span data-ttu-id="7f74f-146">Si la combinaison de propriétés n’autorise pas l’exécution de la tâche sous un moteur unifié, son enregistrement est rejeté.</span><span class="sxs-lookup"><span data-stu-id="7f74f-146">If the combination of properties will not allow running of the task under a unified engine, the registration of such will be rejected.</span></span>
        -   <span data-ttu-id="7f74f-147">Les fonctionnalités de tâche qui ne sont pas prises en charge par le moteur de planification unifié sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="7f74f-147">The task features that are not supported by the unified scheduling engine include:</span></span>

            -   <span data-ttu-id="7f74f-148">Types d’ouverture de session :</span><span class="sxs-lookup"><span data-stu-id="7f74f-148">Logon types:</span></span>

                -   [<span data-ttu-id="7f74f-149">\_ \_ \_ jeton \_ ou \_ mot de passe interactif de connexion à la tâche</span><span class="sxs-lookup"><span data-stu-id="7f74f-149">TASK\_LOGON\_INTERACTIVE\_TOKEN\_OR\_PASSWORD</span></span>](./taskschedulerschema-logontype-principaltype-element.md)

            -   <span data-ttu-id="7f74f-150">Stratégie de plusieurs instances :</span><span class="sxs-lookup"><span data-stu-id="7f74f-150">Multiple instance policy:</span></span>

                -   [<span data-ttu-id="7f74f-151">**les instances de tâche ne sont pas \_ \_ \_ existantes**</span><span class="sxs-lookup"><span data-stu-id="7f74f-151">**TASK\_INSTANCES\_STOP\_EXISTING**</span></span>](taskschedulerschema-multipleinstancespolicy-settingstype-element.md)

            -   <span data-ttu-id="7f74f-152">Actions :</span><span class="sxs-lookup"><span data-stu-id="7f74f-152">Actions:</span></span>

                -   [<span data-ttu-id="7f74f-153">Envoi d’e-mail</span><span class="sxs-lookup"><span data-stu-id="7f74f-153">Send email</span></span>](./taskschedulerschema-sendemail-actiongroup-element.md)
                -   [<span data-ttu-id="7f74f-154">Afficher un message</span><span class="sxs-lookup"><span data-stu-id="7f74f-154">Display message</span></span>](./taskschedulerschema-showmessage-actiongroup-element.md)

            -   <span data-ttu-id="7f74f-155">Paramètres :</span><span class="sxs-lookup"><span data-stu-id="7f74f-155">Settings:</span></span>

                -   [<span data-ttu-id="7f74f-156">Paramètres réseau de la tâche</span><span class="sxs-lookup"><span data-stu-id="7f74f-156">Task network settings</span></span>](./taskschedulerschema-networksettings-settingstype-element.md)
                -   [<span data-ttu-id="7f74f-157">Ne pas autoriser l’arrêt forcé des tâches</span><span class="sxs-lookup"><span data-stu-id="7f74f-157">Do not allow task hard terminate</span></span>](./taskschedulerschema-allowhardterminate-settingstype-element.md)

            -   <span data-ttu-id="7f74f-158">Déclencheurs :</span><span class="sxs-lookup"><span data-stu-id="7f74f-158">Triggers:</span></span>

                -   [<span data-ttu-id="7f74f-159">Limite de la durée d’exécution du déclencheur</span><span class="sxs-lookup"><span data-stu-id="7f74f-159">Trigger execution time limit</span></span>](./taskschedulerschema-executiontimelimit-triggerbasetype-element.md)
                -   [<span data-ttu-id="7f74f-160">Modèles de répétition pour les déclencheurs de calendrier</span><span class="sxs-lookup"><span data-stu-id="7f74f-160">Repetition patterns for calendar triggers</span></span>]( ./taskschedulerschema-repetition-triggerbasetype-element.md)
                -   [<span data-ttu-id="7f74f-161">Valeurs de requête XPath pour les déclencheurs d’événements</span><span class="sxs-lookup"><span data-stu-id="7f74f-161">XPath query values for event triggers</span></span>]( ./taskschedulerschema-valuequeries-eventtriggertype-element.md)
                -   <span data-ttu-id="7f74f-162">Types de déclencheurs [de jour de semaine](./taskschedulerschema-schedulebymonthdayofweek-calendartriggertype-element.md) [mensuels et](./taskschedulerschema-schedulebymonth-calendartriggertype-element.md) mensuels</span><span class="sxs-lookup"><span data-stu-id="7f74f-162">[Monthly](./taskschedulerschema-schedulebymonth-calendartriggertype-element.md) and [Monthly day-of-week](./taskschedulerschema-schedulebymonthdayofweek-calendartriggertype-element.md) trigger types</span></span>

## <a name="windows-vista"></a><span data-ttu-id="7f74f-163">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7f74f-163">Windows Vista</span></span>

<span data-ttu-id="7f74f-164">L’API Planificateur de tâches 2,0 doit être utilisée pour développer des applications qui utilisent le service Planificateur de tâches sur Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="7f74f-164">The Task Scheduler 2.0 API should be used in developing applications that use the Task Scheduler service on Windows Vista.</span></span> <span data-ttu-id="7f74f-165">Pour plus d’informations, consultez [Planificateur de tâches référence](task-scheduler-reference.md) et [utilisation du planificateur de tâches](using-the-task-scheduler.md).</span><span class="sxs-lookup"><span data-stu-id="7f74f-165">For more information, see [Task Scheduler Reference](task-scheduler-reference.md) and [Using the Task Scheduler](using-the-task-scheduler.md).</span></span>

## <a name="windows-2000-windows-xp-and-windows-server-2003"></a><span data-ttu-id="7f74f-166">Windows 2000, Windows XP et Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="7f74f-166">Windows 2000, Windows XP, and Windows Server 2003</span></span>

<span data-ttu-id="7f74f-167">L’API Planificateur de tâches 2,0 n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="7f74f-167">The Task Scheduler 2.0 API is not available.</span></span> <span data-ttu-id="7f74f-168">Utilisez Planificateur de tâches 1,0.</span><span class="sxs-lookup"><span data-stu-id="7f74f-168">Use Task Scheduler 1.0.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7f74f-169">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="7f74f-169">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7f74f-170">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="7f74f-170">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="7f74f-171">À propos de l’Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="7f74f-171">About The Task Scheduler</span></span>](about-the-task-scheduler.md)
</dt> </dl>

 

 
