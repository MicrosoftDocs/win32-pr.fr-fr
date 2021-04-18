---
description: Les threads sont planifiés pour s’exécuter en fonction de leur priorité de planification.
ms.assetid: 8710cd56-6bf3-4317-a1f6-1a159394ce2a
title: Planification des priorités
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e80c8baf4ed066ec7034c97850248f81c298c65
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519891"
---
# <a name="scheduling-priorities"></a><span data-ttu-id="04357-103">Planification des priorités</span><span class="sxs-lookup"><span data-stu-id="04357-103">Scheduling Priorities</span></span>

<span data-ttu-id="04357-104">Les threads sont planifiés pour s’exécuter en fonction de leur *priorité de planification*.</span><span class="sxs-lookup"><span data-stu-id="04357-104">Threads are scheduled to run based on their *scheduling priority*.</span></span> <span data-ttu-id="04357-105">Une priorité de planification est affectée à chaque thread.</span><span class="sxs-lookup"><span data-stu-id="04357-105">Each thread is assigned a scheduling priority.</span></span> <span data-ttu-id="04357-106">La plage des niveaux de priorité est comprise entre zéro (priorité la plus basse) et 31 (priorité la plus élevée).</span><span class="sxs-lookup"><span data-stu-id="04357-106">The priority levels range from zero (lowest priority) to 31 (highest priority).</span></span> <span data-ttu-id="04357-107">Seul le thread de page zéro peut avoir une priorité de zéro.</span><span class="sxs-lookup"><span data-stu-id="04357-107">Only the zero-page thread can have a priority of zero.</span></span> <span data-ttu-id="04357-108">(Le thread de page zéro est un thread système chargé de la mise à zéro des pages libres lorsqu’il n’y a pas d’autres threads qui doivent s’exécuter.)</span><span class="sxs-lookup"><span data-stu-id="04357-108">(The zero-page thread is a system thread responsible for zeroing any free pages when there are no other threads that need to run.)</span></span>

<span data-ttu-id="04357-109">Le système traite tous les threads ayant la même priorité comme étant égaux.</span><span class="sxs-lookup"><span data-stu-id="04357-109">The system treats all threads with the same priority as equal.</span></span> <span data-ttu-id="04357-110">Le système affecte les tranches de temps dans un mode de tourniquet (Round Robin) à tous les threads ayant la priorité la plus élevée.</span><span class="sxs-lookup"><span data-stu-id="04357-110">The system assigns time slices in a round-robin fashion to all threads with the highest priority.</span></span> <span data-ttu-id="04357-111">Si aucun de ces threads n’est prêt à être exécuté, le système affecte les tranches de temps de manière répétée à tous les threads ayant la priorité la plus élevée suivante.</span><span class="sxs-lookup"><span data-stu-id="04357-111">If none of these threads are ready to run, the system assigns time slices in a round-robin fashion to all threads with the next highest priority.</span></span> <span data-ttu-id="04357-112">Si un thread de priorité plus élevée est disponible pour exécution, le système cesse d’exécuter le thread de priorité inférieure (sans l’autoriser à terminer son tranche de temps) et affecte une tranche horaire complète au thread de priorité plus élevée.</span><span class="sxs-lookup"><span data-stu-id="04357-112">If a higher-priority thread becomes available to run, the system ceases to execute the lower-priority thread (without allowing it to finish using its time slice) and assigns a full time slice to the higher-priority thread.</span></span> <span data-ttu-id="04357-113">Pour plus d’informations, consultez [changements de contexte](context-switches.md).</span><span class="sxs-lookup"><span data-stu-id="04357-113">For more information, see [Context Switches](context-switches.md).</span></span>

<span data-ttu-id="04357-114">La priorité de chaque thread est déterminée par les critères suivants :</span><span class="sxs-lookup"><span data-stu-id="04357-114">The priority of each thread is determined by the following criteria:</span></span>

-   <span data-ttu-id="04357-115">Classe de priorité de son processus</span><span class="sxs-lookup"><span data-stu-id="04357-115">The priority class of its process</span></span>
-   <span data-ttu-id="04357-116">Niveau de priorité du thread dans la classe de priorité de son processus</span><span class="sxs-lookup"><span data-stu-id="04357-116">The priority level of the thread within the priority class of its process</span></span>

<span data-ttu-id="04357-117">La classe de priorité et le niveau de priorité sont combinés pour former la *priorité de base* d’un thread.</span><span class="sxs-lookup"><span data-stu-id="04357-117">The priority class and priority level are combined to form the *base priority* of a thread.</span></span> <span data-ttu-id="04357-118">Pour plus d’informations sur la priorité dynamique d’un thread, consultez [augmentations de priorité](priority-boosts.md).</span><span class="sxs-lookup"><span data-stu-id="04357-118">For information on the dynamic priority of a thread, see [Priority Boosts](priority-boosts.md).</span></span>

## <a name="priority-class"></a><span data-ttu-id="04357-119">Classe de priorité</span><span class="sxs-lookup"><span data-stu-id="04357-119">Priority Class</span></span>

<span data-ttu-id="04357-120">Chaque processus appartient à l’une des classes de priorité suivantes :</span><span class="sxs-lookup"><span data-stu-id="04357-120">Each process belongs to one of the following priority classes:</span></span><dl> <span data-ttu-id="04357-121">\_classe de priorité Idle \_</span><span class="sxs-lookup"><span data-stu-id="04357-121">IDLE\_PRIORITY\_CLASS</span></span>  
<span data-ttu-id="04357-122">classe de priorité inférieure à la \_ normale \_ \_</span><span class="sxs-lookup"><span data-stu-id="04357-122">BELOW\_NORMAL\_PRIORITY\_CLASS</span></span>  
<span data-ttu-id="04357-123">\_classe de priorité normale \_</span><span class="sxs-lookup"><span data-stu-id="04357-123">NORMAL\_PRIORITY\_CLASS</span></span>  
<span data-ttu-id="04357-124">classe de priorité supérieure à la \_ normale \_ \_</span><span class="sxs-lookup"><span data-stu-id="04357-124">ABOVE\_NORMAL\_PRIORITY\_CLASS</span></span>  
<span data-ttu-id="04357-125">\_classe de priorité élevée \_</span><span class="sxs-lookup"><span data-stu-id="04357-125">HIGH\_PRIORITY\_CLASS</span></span>  
<span data-ttu-id="04357-126">\_classe de priorité en temps réel \_</span><span class="sxs-lookup"><span data-stu-id="04357-126">REALTIME\_PRIORITY\_CLASS</span></span>  
</dl>

<span data-ttu-id="04357-127">Par défaut, la classe de priorité d’un processus est une \_ classe de priorité normale \_ .</span><span class="sxs-lookup"><span data-stu-id="04357-127">By default, the priority class of a process is NORMAL\_PRIORITY\_CLASS.</span></span> <span data-ttu-id="04357-128">Utilisez la fonction [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) pour spécifier la classe de priorité d’un processus enfant lorsque vous le créez.</span><span class="sxs-lookup"><span data-stu-id="04357-128">Use the [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) function to specify the priority class of a child process when you create it.</span></span> <span data-ttu-id="04357-129">Si le processus appelant est une \_ classe de priorité inactive \_ ou une classe de \_ \_ priorité normale \_ , le nouveau processus hérite de cette classe.</span><span class="sxs-lookup"><span data-stu-id="04357-129">If the calling process is IDLE\_PRIORITY\_CLASS or BELOW\_NORMAL\_PRIORITY\_CLASS, the new process will inherit this class.</span></span> <span data-ttu-id="04357-130">Utilisez la fonction [**GetPriorityClass**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getpriorityclass) pour déterminer la classe de priorité actuelle d’un processus et la fonction [**SetPriorityClass**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setpriorityclass) pour modifier la classe de priorité d’un processus.</span><span class="sxs-lookup"><span data-stu-id="04357-130">Use the [**GetPriorityClass**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getpriorityclass) function to determine the current priority class of a process and the [**SetPriorityClass**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setpriorityclass) function to change the priority class of a process.</span></span>

<span data-ttu-id="04357-131">Les processus qui surveillent le système, tels que les économiseurs d’écran ou les applications qui mettent régulièrement à jour un affichage, doivent utiliser la classe de priorité inactive \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="04357-131">Processes that monitor the system, such as screen savers or applications that periodically update a display, should use IDLE\_PRIORITY\_CLASS.</span></span> <span data-ttu-id="04357-132">Cela empêche les threads de ce processus, qui n’ont pas de priorité élevée, d’interférer avec les threads de priorité supérieure.</span><span class="sxs-lookup"><span data-stu-id="04357-132">This prevents the threads of this process, which do not have high priority, from interfering with higher priority threads.</span></span>

<span data-ttu-id="04357-133">Utilisez la \_ classe High Priority \_ avec précaution.</span><span class="sxs-lookup"><span data-stu-id="04357-133">Use HIGH\_PRIORITY\_CLASS with care.</span></span> <span data-ttu-id="04357-134">Si un thread s’exécute au niveau de priorité le plus élevé pour des périodes prolongées, les autres threads du système n’obtiendront pas de temps processeur.</span><span class="sxs-lookup"><span data-stu-id="04357-134">If a thread runs at the highest priority level for extended periods, other threads in the system will not get processor time.</span></span> <span data-ttu-id="04357-135">Si plusieurs threads sont définis en priorité élevée en même temps, les threads perdent leur efficacité.</span><span class="sxs-lookup"><span data-stu-id="04357-135">If several threads are set at high priority at the same time, the threads lose their effectiveness.</span></span> <span data-ttu-id="04357-136">La classe de priorité élevée doit être réservée pour les threads qui doivent répondre à des événements critiques dans le temps.</span><span class="sxs-lookup"><span data-stu-id="04357-136">The high-priority class should be reserved for threads that must respond to time-critical events.</span></span> <span data-ttu-id="04357-137">Si votre application exécute une tâche qui requiert la classe de priorité élevée alors que le reste de ses tâches est une priorité normale, utilisez [**SetPriorityClass**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setpriorityclass) pour augmenter temporairement la classe de priorité de l’application ; Ensuite, réduisez-la après la fin de la tâche critique du temps.</span><span class="sxs-lookup"><span data-stu-id="04357-137">If your application performs one task that requires the high-priority class while the rest of its tasks are normal priority, use [**SetPriorityClass**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setpriorityclass) to raise the priority class of the application temporarily; then reduce it after the time-critical task has been completed.</span></span> <span data-ttu-id="04357-138">Une autre stratégie consiste à créer un processus de haute priorité qui a tous les threads bloqués la plupart du temps, en réveillent les threads uniquement quand des tâches critiques sont nécessaires.</span><span class="sxs-lookup"><span data-stu-id="04357-138">Another strategy is to create a high-priority process that has all of its threads blocked most of the time, awakening threads only when critical tasks are needed.</span></span> <span data-ttu-id="04357-139">Le point important est qu’un thread à priorité élevée doit s’exécuter pendant une courte période, et uniquement lorsqu’il a un travail critique dans le temps.</span><span class="sxs-lookup"><span data-stu-id="04357-139">The important point is that a high-priority thread should execute for a brief time, and only when it has time-critical work to perform.</span></span>

<span data-ttu-id="04357-140">Vous ne devriez presque jamais utiliser \_ la classe de priorité en temps réel \_ , car cela interrompt les threads système qui gèrent l’entrée de la souris, l’entrée au clavier et le vidage du disque en arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="04357-140">You should almost never use REALTIME\_PRIORITY\_CLASS, because this interrupts system threads that manage mouse input, keyboard input, and background disk flushing.</span></span> <span data-ttu-id="04357-141">Cette classe peut être appropriée pour les applications qui « communiquent » directement au matériel ou qui effectuent de brèves tâches qui doivent avoir des interruptions limitées.</span><span class="sxs-lookup"><span data-stu-id="04357-141">This class can be appropriate for applications that "talk" directly to hardware or that perform brief tasks that should have limited interruptions.</span></span>

## <a name="priority-level"></a><span data-ttu-id="04357-142">Niveau de priorité</span><span class="sxs-lookup"><span data-stu-id="04357-142">Priority Level</span></span>

<span data-ttu-id="04357-143">Voici les niveaux de priorité de chaque classe de priorité :</span><span class="sxs-lookup"><span data-stu-id="04357-143">The following are priority levels within each priority class:</span></span><dl> <span data-ttu-id="04357-144">priorité de THREAD \_ \_ inactive</span><span class="sxs-lookup"><span data-stu-id="04357-144">THREAD\_PRIORITY\_IDLE</span></span>  
<span data-ttu-id="04357-145">priorité de THREAD la \_ \_ plus basse</span><span class="sxs-lookup"><span data-stu-id="04357-145">THREAD\_PRIORITY\_LOWEST</span></span>  
<span data-ttu-id="04357-146">priorité de THREAD inférieure à la \_ \_ \_ normale</span><span class="sxs-lookup"><span data-stu-id="04357-146">THREAD\_PRIORITY\_BELOW\_NORMAL</span></span>  
<span data-ttu-id="04357-147">priorité de THREAD \_ \_ normale</span><span class="sxs-lookup"><span data-stu-id="04357-147">THREAD\_PRIORITY\_NORMAL</span></span>  
<span data-ttu-id="04357-148">priorité de THREAD supérieure à la \_ \_ \_ normale</span><span class="sxs-lookup"><span data-stu-id="04357-148">THREAD\_PRIORITY\_ABOVE\_NORMAL</span></span>  
<span data-ttu-id="04357-149">priorité de THREAD la \_ \_ plus élevée</span><span class="sxs-lookup"><span data-stu-id="04357-149">THREAD\_PRIORITY\_HIGHEST</span></span>  
<span data-ttu-id="04357-150">temps de priorité des THREADs \_ \_ \_ critique</span><span class="sxs-lookup"><span data-stu-id="04357-150">THREAD\_PRIORITY\_TIME\_CRITICAL</span></span>  
</dl>

<span data-ttu-id="04357-151">Tous les threads sont créés à l’aide de la priorité de THREAD \_ \_ normal.</span><span class="sxs-lookup"><span data-stu-id="04357-151">All threads are created using THREAD\_PRIORITY\_NORMAL.</span></span> <span data-ttu-id="04357-152">Cela signifie que la priorité de thread est la même que la classe de priorité de processus.</span><span class="sxs-lookup"><span data-stu-id="04357-152">This means that the thread priority is the same as the process priority class.</span></span> <span data-ttu-id="04357-153">Après avoir créé un thread, utilisez la fonction [**SetThreadPriority**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadpriority) pour ajuster sa priorité par rapport à d’autres threads dans le processus.</span><span class="sxs-lookup"><span data-stu-id="04357-153">After you create a thread, use the [**SetThreadPriority**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadpriority) function to adjust its priority relative to other threads in the process.</span></span>

<span data-ttu-id="04357-154">Une stratégie classique consiste à utiliser la priorité de THREAD supérieure à la \_ \_ \_ normale ou \_ \_ la priorité de thread la plus élevée pour le thread d’entrée du processus, afin de garantir la réactivité de l’application à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="04357-154">A typical strategy is to use THREAD\_PRIORITY\_ABOVE\_NORMAL or THREAD\_PRIORITY\_HIGHEST for the process's input thread, to ensure that the application is responsive to the user.</span></span> <span data-ttu-id="04357-155">Les threads d’arrière-plan, en particulier ceux qui utilisent beaucoup de ressources processeur, peuvent être définis sur la priorité de THREAD inférieure à la \_ \_ \_ normale ou la \_ priorité de thread la \_ plus faible, pour s’assurer qu’elles peuvent être anticipées si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="04357-155">Background threads, particularly those that are processor intensive, can be set to THREAD\_PRIORITY\_BELOW\_NORMAL or THREAD\_PRIORITY\_LOWEST, to ensure that they can be preempted when necessary.</span></span> <span data-ttu-id="04357-156">Toutefois, si un thread attend un autre thread avec une priorité plus basse pour terminer une tâche, veillez à bloquer l’exécution du thread en attente de haute priorité.</span><span class="sxs-lookup"><span data-stu-id="04357-156">However, if you have a thread waiting for another thread with a lower priority to complete some task, be sure to block the execution of the waiting high-priority thread.</span></span> <span data-ttu-id="04357-157">Pour ce faire, utilisez une [fonction Wait](../sync/wait-functions.md), [une section critique](../sync/critical-section-objects.md)ou la fonction [**Sleep**](/windows/win32/api/synchapi/nf-synchapi-sleep) , [**SleepEx**](/windows/win32/api/synchapi/nf-synchapi-sleepex)ou [**SwitchToThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-switchtothread) .</span><span class="sxs-lookup"><span data-stu-id="04357-157">To do this, use a [wait function](../sync/wait-functions.md), [critical section](../sync/critical-section-objects.md), or the [**Sleep**](/windows/win32/api/synchapi/nf-synchapi-sleep) function, [**SleepEx**](/windows/win32/api/synchapi/nf-synchapi-sleepex), or [**SwitchToThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-switchtothread) function.</span></span> <span data-ttu-id="04357-158">Cela est préférable à l’exécution d’une boucle par le thread.</span><span class="sxs-lookup"><span data-stu-id="04357-158">This is preferable to having the thread execute a loop.</span></span> <span data-ttu-id="04357-159">Dans le cas contraire, le processus peut être bloqué, car le thread avec une priorité plus faible n’est jamais planifié.</span><span class="sxs-lookup"><span data-stu-id="04357-159">Otherwise, the process may become deadlocked, because the thread with lower priority is never scheduled.</span></span>

<span data-ttu-id="04357-160">Pour déterminer le niveau de priorité actuel d’un thread, utilisez la fonction [**GetThreadPriority**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getthreadpriority) .</span><span class="sxs-lookup"><span data-stu-id="04357-160">To determine the current priority level of a thread, use the [**GetThreadPriority**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getthreadpriority) function.</span></span>

## <a name="base-priority"></a><span data-ttu-id="04357-161">Priorité de base</span><span class="sxs-lookup"><span data-stu-id="04357-161">Base Priority</span></span>

<span data-ttu-id="04357-162">La classe de priorité du processus et le niveau de priorité du thread sont combinés pour former la priorité de base de chaque thread.</span><span class="sxs-lookup"><span data-stu-id="04357-162">The process priority class and thread priority level are combined to form the base priority of each thread.</span></span>

<span data-ttu-id="04357-163">Le tableau suivant indique la priorité de base pour les combinaisons de la classe de priorité du processus et la valeur de priorité du thread.</span><span class="sxs-lookup"><span data-stu-id="04357-163">The following table shows the base priority for combinations of process priority class and thread priority value.</span></span>


<table>
<tr>
<th colspan="2"><span data-ttu-id="04357-164">Classe de priorité du processus</span><span class="sxs-lookup"><span data-stu-id="04357-164">Process priority class</span></span></th>
<th><span data-ttu-id="04357-165">Niveau de priorité du thread</span><span class="sxs-lookup"><span data-stu-id="04357-165">Thread priority level</span></span></th>
<th><span data-ttu-id="04357-166">Priorité de base</span><span class="sxs-lookup"><span data-stu-id="04357-166">Base priority</span></span></th>
</tr>
<tr>
<td rowspan="7" colspan="2"><span data-ttu-id="04357-167">IDLE_PRIORITY_CLASS</span><span class="sxs-lookup"><span data-stu-id="04357-167">IDLE_PRIORITY_CLASS</span></span> </td>
<td><span data-ttu-id="04357-168">THREAD_PRIORITY_IDLE</span><span class="sxs-lookup"><span data-stu-id="04357-168">THREAD_PRIORITY_IDLE</span></span></td>
<td><span data-ttu-id="04357-169">1</span><span class="sxs-lookup"><span data-stu-id="04357-169">1</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04357-170">THREAD_PRIORITY_LOWEST</span><span class="sxs-lookup"><span data-stu-id="04357-170">THREAD_PRIORITY_LOWEST</span></span></td>
<td><span data-ttu-id="04357-171">2</span><span class="sxs-lookup"><span data-stu-id="04357-171">2</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04357-172">THREAD_PRIORITY_BELOW_NORMAL</span><span class="sxs-lookup"><span data-stu-id="04357-172">THREAD_PRIORITY_BELOW_NORMAL</span></span></td>
<td><span data-ttu-id="04357-173">3</span><span class="sxs-lookup"><span data-stu-id="04357-173">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04357-174">THREAD_PRIORITY_NORMAL</span><span class="sxs-lookup"><span data-stu-id="04357-174">THREAD_PRIORITY_NORMAL</span></span></td>
<td><span data-ttu-id="04357-175">4</span><span class="sxs-lookup"><span data-stu-id="04357-175">4</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04357-176">THREAD_PRIORITY_ABOVE_NORMAL</span><span class="sxs-lookup"><span data-stu-id="04357-176">THREAD_PRIORITY_ABOVE_NORMAL</span></span></td>
<td><span data-ttu-id="04357-177">5</span><span class="sxs-lookup"><span data-stu-id="04357-177">5</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04357-178">THREAD_PRIORITY_HIGHEST</span><span class="sxs-lookup"><span data-stu-id="04357-178">THREAD_PRIORITY_HIGHEST</span></span></td>
<td><span data-ttu-id="04357-179">6</span><span class="sxs-lookup"><span data-stu-id="04357-179">6</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04357-180">THREAD_PRIORITY_TIME_CRITICAL</span><span class="sxs-lookup"><span data-stu-id="04357-180">THREAD_PRIORITY_TIME_CRITICAL</span></span></td>
<td><span data-ttu-id="04357-181">15</span><span class="sxs-lookup"><span data-stu-id="04357-181">15</span></span></td>
</tr>
<tr>
<td rowspan="7" colspan="2"><span data-ttu-id="04357-182">BELOW_NORMAL_PRIORITY_CLASS</span><span class="sxs-lookup"><span data-stu-id="04357-182">BELOW_NORMAL_PRIORITY_CLASS</span></span> </td>
<td><span data-ttu-id="04357-183">THREAD_PRIORITY_IDLE</span><span class="sxs-lookup"><span data-stu-id="04357-183">THREAD_PRIORITY_IDLE</span></span></td>
<td><span data-ttu-id="04357-184">1</span><span class="sxs-lookup"><span data-stu-id="04357-184">1</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04357-185">THREAD_PRIORITY_LOWEST</span><span class="sxs-lookup"><span data-stu-id="04357-185">THREAD_PRIORITY_LOWEST</span></span></td>
<td><span data-ttu-id="04357-186">4</span><span class="sxs-lookup"><span data-stu-id="04357-186">4</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04357-187">THREAD_PRIORITY_BELOW_NORMAL</span><span class="sxs-lookup"><span data-stu-id="04357-187">THREAD_PRIORITY_BELOW_NORMAL</span></span></td>
<td><span data-ttu-id="04357-188">5</span><span class="sxs-lookup"><span data-stu-id="04357-188">5</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04357-189">THREAD_PRIORITY_NORMAL</span><span class="sxs-lookup"><span data-stu-id="04357-189">THREAD_PRIORITY_NORMAL</span></span></td>
<td><span data-ttu-id="04357-190">6</span><span class="sxs-lookup"><span data-stu-id="04357-190">6</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04357-191">THREAD_PRIORITY_ABOVE_NORMAL</span><span class="sxs-lookup"><span data-stu-id="04357-191">THREAD_PRIORITY_ABOVE_NORMAL</span></span></td>
<td><span data-ttu-id="04357-192">7</span><span class="sxs-lookup"><span data-stu-id="04357-192">7</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04357-193">THREAD_PRIORITY_HIGHEST</span><span class="sxs-lookup"><span data-stu-id="04357-193">THREAD_PRIORITY_HIGHEST</span></span></td>
<td><span data-ttu-id="04357-194">8</span><span class="sxs-lookup"><span data-stu-id="04357-194">8</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04357-195">THREAD_PRIORITY_TIME_CRITICAL</span><span class="sxs-lookup"><span data-stu-id="04357-195">THREAD_PRIORITY_TIME_CRITICAL</span></span></td>
<td><span data-ttu-id="04357-196">15</span><span class="sxs-lookup"><span data-stu-id="04357-196">15</span></span></td>
</tr>
<tr>
<td rowspan="7" colspan="2"><span data-ttu-id="04357-197">NORMAL_PRIORITY_CLASS</span><span class="sxs-lookup"><span data-stu-id="04357-197">NORMAL_PRIORITY_CLASS</span></span> </td>
<td><span data-ttu-id="04357-198">THREAD_PRIORITY_IDLE</span><span class="sxs-lookup"><span data-stu-id="04357-198">THREAD_PRIORITY_IDLE</span></span></td>
<td><span data-ttu-id="04357-199">1</span><span class="sxs-lookup"><span data-stu-id="04357-199">1</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04357-200">THREAD_PRIORITY_LOWEST</span><span class="sxs-lookup"><span data-stu-id="04357-200">THREAD_PRIORITY_LOWEST</span></span></td>
<td><span data-ttu-id="04357-201">6</span><span class="sxs-lookup"><span data-stu-id="04357-201">6</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04357-202">THREAD_PRIORITY_BELOW_NORMAL</span><span class="sxs-lookup"><span data-stu-id="04357-202">THREAD_PRIORITY_BELOW_NORMAL</span></span></td>
<td><span data-ttu-id="04357-203">7</span><span class="sxs-lookup"><span data-stu-id="04357-203">7</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04357-204">THREAD_PRIORITY_NORMAL</span><span class="sxs-lookup"><span data-stu-id="04357-204">THREAD_PRIORITY_NORMAL</span></span></td>
<td><span data-ttu-id="04357-205">8</span><span class="sxs-lookup"><span data-stu-id="04357-205">8</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04357-206">THREAD_PRIORITY_ABOVE_NORMAL</span><span class="sxs-lookup"><span data-stu-id="04357-206">THREAD_PRIORITY_ABOVE_NORMAL</span></span></td>
<td><span data-ttu-id="04357-207">9</span><span class="sxs-lookup"><span data-stu-id="04357-207">9</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04357-208">THREAD_PRIORITY_HIGHEST</span><span class="sxs-lookup"><span data-stu-id="04357-208">THREAD_PRIORITY_HIGHEST</span></span></td>
<td><span data-ttu-id="04357-209">10</span><span class="sxs-lookup"><span data-stu-id="04357-209">10</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04357-210">THREAD_PRIORITY_TIME_CRITICAL</span><span class="sxs-lookup"><span data-stu-id="04357-210">THREAD_PRIORITY_TIME_CRITICAL</span></span></td>
<td><span data-ttu-id="04357-211">15</span><span class="sxs-lookup"><span data-stu-id="04357-211">15</span></span></td>
</tr>
<tr>
<td rowspan="7" colspan="2"><span data-ttu-id="04357-212">ABOVE_NORMAL_PRIORITY_CLASS</span><span class="sxs-lookup"><span data-stu-id="04357-212">ABOVE_NORMAL_PRIORITY_CLASS</span></span> </td>
<td><span data-ttu-id="04357-213">THREAD_PRIORITY_IDLE</span><span class="sxs-lookup"><span data-stu-id="04357-213">THREAD_PRIORITY_IDLE</span></span></td>
<td><span data-ttu-id="04357-214">1</span><span class="sxs-lookup"><span data-stu-id="04357-214">1</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04357-215">THREAD_PRIORITY_LOWEST</span><span class="sxs-lookup"><span data-stu-id="04357-215">THREAD_PRIORITY_LOWEST</span></span></td>
<td><span data-ttu-id="04357-216">8</span><span class="sxs-lookup"><span data-stu-id="04357-216">8</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04357-217">THREAD_PRIORITY_BELOW_NORMAL</span><span class="sxs-lookup"><span data-stu-id="04357-217">THREAD_PRIORITY_BELOW_NORMAL</span></span></td>
<td><span data-ttu-id="04357-218">9</span><span class="sxs-lookup"><span data-stu-id="04357-218">9</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04357-219">THREAD_PRIORITY_NORMAL</span><span class="sxs-lookup"><span data-stu-id="04357-219">THREAD_PRIORITY_NORMAL</span></span></td>
<td><span data-ttu-id="04357-220">10</span><span class="sxs-lookup"><span data-stu-id="04357-220">10</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04357-221">THREAD_PRIORITY_ABOVE_NORMAL</span><span class="sxs-lookup"><span data-stu-id="04357-221">THREAD_PRIORITY_ABOVE_NORMAL</span></span></td>
<td><span data-ttu-id="04357-222">11</span><span class="sxs-lookup"><span data-stu-id="04357-222">11</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04357-223">THREAD_PRIORITY_HIGHEST</span><span class="sxs-lookup"><span data-stu-id="04357-223">THREAD_PRIORITY_HIGHEST</span></span></td>
<td><span data-ttu-id="04357-224">12</span><span class="sxs-lookup"><span data-stu-id="04357-224">12</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04357-225">THREAD_PRIORITY_TIME_CRITICAL</span><span class="sxs-lookup"><span data-stu-id="04357-225">THREAD_PRIORITY_TIME_CRITICAL</span></span></td>
<td><span data-ttu-id="04357-226">15</span><span class="sxs-lookup"><span data-stu-id="04357-226">15</span></span></td>
</tr>
<tr>
<td rowspan="7" colspan="2"><span data-ttu-id="04357-227">HIGH_PRIORITY_CLASS</span><span class="sxs-lookup"><span data-stu-id="04357-227">HIGH_PRIORITY_CLASS</span></span> </td>
<td><span data-ttu-id="04357-228">THREAD_PRIORITY_IDLE</span><span class="sxs-lookup"><span data-stu-id="04357-228">THREAD_PRIORITY_IDLE</span></span></td>
<td><span data-ttu-id="04357-229">1</span><span class="sxs-lookup"><span data-stu-id="04357-229">1</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04357-230">THREAD_PRIORITY_LOWEST</span><span class="sxs-lookup"><span data-stu-id="04357-230">THREAD_PRIORITY_LOWEST</span></span></td>
<td><span data-ttu-id="04357-231">11</span><span class="sxs-lookup"><span data-stu-id="04357-231">11</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04357-232">THREAD_PRIORITY_BELOW_NORMAL</span><span class="sxs-lookup"><span data-stu-id="04357-232">THREAD_PRIORITY_BELOW_NORMAL</span></span></td>
<td><span data-ttu-id="04357-233">12</span><span class="sxs-lookup"><span data-stu-id="04357-233">12</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04357-234">THREAD_PRIORITY_NORMAL</span><span class="sxs-lookup"><span data-stu-id="04357-234">THREAD_PRIORITY_NORMAL</span></span></td>
<td><span data-ttu-id="04357-235">13</span><span class="sxs-lookup"><span data-stu-id="04357-235">13</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04357-236">THREAD_PRIORITY_ABOVE_NORMAL</span><span class="sxs-lookup"><span data-stu-id="04357-236">THREAD_PRIORITY_ABOVE_NORMAL</span></span></td>
<td><span data-ttu-id="04357-237">14</span><span class="sxs-lookup"><span data-stu-id="04357-237">14</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04357-238">THREAD_PRIORITY_HIGHEST</span><span class="sxs-lookup"><span data-stu-id="04357-238">THREAD_PRIORITY_HIGHEST</span></span></td>
<td><span data-ttu-id="04357-239">15</span><span class="sxs-lookup"><span data-stu-id="04357-239">15</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04357-240">THREAD_PRIORITY_TIME_CRITICAL</span><span class="sxs-lookup"><span data-stu-id="04357-240">THREAD_PRIORITY_TIME_CRITICAL</span></span></td>
<td><span data-ttu-id="04357-241">15</span><span class="sxs-lookup"><span data-stu-id="04357-241">15</span></span></td>
</tr>
<tr>
<td rowspan="7" colspan="2"><span data-ttu-id="04357-242">REALTIME_PRIORITY_CLASS</span><span class="sxs-lookup"><span data-stu-id="04357-242">REALTIME_PRIORITY_CLASS</span></span> </td>
<td><span data-ttu-id="04357-243">THREAD_PRIORITY_IDLE</span><span class="sxs-lookup"><span data-stu-id="04357-243">THREAD_PRIORITY_IDLE</span></span></td>
<td><span data-ttu-id="04357-244">16</span><span class="sxs-lookup"><span data-stu-id="04357-244">16</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04357-245">THREAD_PRIORITY_LOWEST</span><span class="sxs-lookup"><span data-stu-id="04357-245">THREAD_PRIORITY_LOWEST</span></span></td>
<td><span data-ttu-id="04357-246">22</span><span class="sxs-lookup"><span data-stu-id="04357-246">22</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04357-247">THREAD_PRIORITY_BELOW_NORMAL</span><span class="sxs-lookup"><span data-stu-id="04357-247">THREAD_PRIORITY_BELOW_NORMAL</span></span></td>
<td><span data-ttu-id="04357-248">23</span><span class="sxs-lookup"><span data-stu-id="04357-248">23</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04357-249">THREAD_PRIORITY_NORMAL</span><span class="sxs-lookup"><span data-stu-id="04357-249">THREAD_PRIORITY_NORMAL</span></span></td>
<td><span data-ttu-id="04357-250">24</span><span class="sxs-lookup"><span data-stu-id="04357-250">24</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04357-251">THREAD_PRIORITY_ABOVE_NORMAL</span><span class="sxs-lookup"><span data-stu-id="04357-251">THREAD_PRIORITY_ABOVE_NORMAL</span></span></td>
<td><span data-ttu-id="04357-252">25</span><span class="sxs-lookup"><span data-stu-id="04357-252">25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04357-253">THREAD_PRIORITY_HIGHEST</span><span class="sxs-lookup"><span data-stu-id="04357-253">THREAD_PRIORITY_HIGHEST</span></span></td>
<td><span data-ttu-id="04357-254">26</span><span class="sxs-lookup"><span data-stu-id="04357-254">26</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04357-255">THREAD_PRIORITY_TIME_CRITICAL</span><span class="sxs-lookup"><span data-stu-id="04357-255">THREAD_PRIORITY_TIME_CRITICAL</span></span></td>
<td><span data-ttu-id="04357-256">31</span><span class="sxs-lookup"><span data-stu-id="04357-256">31</span></span></td>
</tr>
</table>

 

 

 
