---
title: Planificateur de tâches les constantes d’erreur et de réussite (WinError. h)
description: Si une erreur se produit, les API Planificateur de tâches peuvent retourner l’un des codes d’erreur suivants sous la forme d’une valeur HRESULT.
ms.assetid: 54278bbd-7dca-438e-a771-5fcb08c4aa68
keywords:
- Planificateur de tâches Planificateur de tâches, références, erreurs et constantes de réussite
topic_type:
- apiref
api_name:
- SCHED_S_TASK_READY
- SCHED_S_TASK_RUNNING
- SCHED_S_TASK_DISABLED
- SCHED_S_TASK_HAS_NOT_RUN
- SCHED_S_TASK_NO_MORE_RUNS
- SCHED_S_TASK_NOT_SCHEDULED
- SCHED_S_TASK_TERMINATED
- SCHED_S_TASK_NO_VALID_TRIGGERS
- SCHED_S_EVENT_TRIGGER
- SCHED_E_TRIGGER_NOT_FOUND
- SCHED_E_TASK_NOT_READY
- SCHED_E_TASK_NOT_RUNNING
- SCHED_E_SERVICE_NOT_INSTALLED
- SCHED_E_CANNOT_OPEN_TASK
- SCHED_E_INVALID_TASK
- SCHED_E_ACCOUNT_INFORMATION_NOT_SET
- SCHED_E_ACCOUNT_NAME_NOT_FOUND
- SCHED_E_ACCOUNT_DBASE_CORRUPT
- SCHED_E_NO_SECURITY_SERVICES
- SCHED_E_UNKNOWN_OBJECT_VERSION
- SCHED_E_UNSUPPORTED_ACCOUNT_OPTION
- SCHED_E_SERVICE_NOT_RUNNING
- SCHED_E_UNEXPECTEDNODE
- SCHED_E_NAMESPACE
- SCHED_E_INVALIDVALUE
- SCHED_E_MISSINGNODE
- SCHED_E_MALFORMEDXML
- SCHED_S_SOME_TRIGGERS_FAILED
- SCHED_S_BATCH_LOGON_PROBLEM
- SCHED_E_TOO_MANY_NODES
- SCHED_E_PAST_END_BOUNDARY
- SCHED_E_ALREADY_RUNNING
- SCHED_E_USER_NOT_LOGGED_ON
- SCHED_E_INVALID_TASK_HASH
- SCHED_E_SERVICE_NOT_AVAILABLE
- SCHED_E_SERVICE_TOO_BUSY
- SCHED_E_TASK_ATTEMPTED
- SCHED_S_TASK_QUEUED
- SCHED_E_TASK_DISABLED
- SCHED_E_TASK_NOT_V1_COMPAT
- SCHED_E_START_ON_DEMAND
api_location:
- WinError.h
api_type:
- HeaderDef
ms.topic: reference
ms.custom: snippet-project
ms.date: 05/31/2018
ms.openlocfilehash: a1d0347938020ca8937f2764e3b2c62a38fc9273
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542466"
---
# <a name="task-scheduler-error-and-success-constants"></a><span data-ttu-id="7544e-104">Planificateur de tâches les constantes d’erreur et de réussite</span><span class="sxs-lookup"><span data-stu-id="7544e-104">Task Scheduler Error and Success Constants</span></span>

<span data-ttu-id="7544e-105">Si une erreur se produit, les API Planificateur de tâches peuvent retourner l’un des codes d’erreur suivants sous la forme d’une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="7544e-105">If an error occurs, the Task Scheduler APIs can return one of the following error codes as an **HRESULT** value.</span></span>

<span data-ttu-id="7544e-106">Les constantes qui commencent par SCHED \_ S \_ sont des constantes de réussite et les constantes qui commencent par sched \_ E \_ sont des constantes d’erreur.</span><span class="sxs-lookup"><span data-stu-id="7544e-106">The constants that begin with SCHED\_S\_ are success constants, and the constants that begin with SCHED\_E\_ are error constants.</span></span>

```cpp
  HRESULT phrStatus;
  hr = pITask->GetStatus(&phrStatus);
  
  // Release the ITask interface.
  pITask->Release();
    
  switch(phrStatus)
  {
  case SCHED_S_TASK_READY:
       wprintf(L"  SCHED_S_TASK_READY\n");
       break;
  case SCHED_S_TASK_RUNNING:
       wprintf(L"  SCHED_S_TASK_RUNNING\n");
       break;

  //...
  }
```

<span data-ttu-id="7544e-107">Exemple de [code C/C++ : récupération](c-c-code-example-retrieving-task-status.md)de l’état de la tâche.</span><span class="sxs-lookup"><span data-stu-id="7544e-107">Example from [C/C++ Code Example: Retrieving Task Status](c-c-code-example-retrieving-task-status.md).</span></span>

> [!Note]  
> <span data-ttu-id="7544e-108">Certaines API Planificateur de tâches peuvent renvoyer des codes d’erreur système et réseau (64, par exemple).</span><span class="sxs-lookup"><span data-stu-id="7544e-108">Some Task Scheduler APIs can return system and network error codes (64 for example).</span></span> <span data-ttu-id="7544e-109">Vous pouvez vérifier la définition de ces types de codes d’erreur à l’aide de la commande **net helpmsg** dans la fenêtre d’invite de commandes.</span><span class="sxs-lookup"><span data-stu-id="7544e-109">You can check the definition of these types of error codes by using the **net helpmsg** command in the command prompt window.</span></span> <span data-ttu-id="7544e-110">Par exemple, la commande **net helpmsg 64** retourne le message : le nom réseau spécifié n’est plus disponible.</span><span class="sxs-lookup"><span data-stu-id="7544e-110">For example, the command **net helpmsg 64** returns the message: The specified network name is no longer available.</span></span>

 

<span data-ttu-id="7544e-111">Pour plus d’informations sur les événements et les messages d’erreur, consultez [Centre de messages d’erreurs et](https://www.microsoft.com/technet/support/ee/ee_advanced.aspx)d’événements.</span><span class="sxs-lookup"><span data-stu-id="7544e-111">For more information about events and error messages, see [Events and Errors Message Center](https://www.microsoft.com/technet/support/ee/ee_advanced.aspx).</span></span>

<dl> <dt>

<span data-ttu-id="7544e-112"><span id="SCHED_S_TASK_READY"></span><span id="sched_s_task_ready"></span>**\_tâche sched \_ S \_ prête**</span><span class="sxs-lookup"><span data-stu-id="7544e-112"><span id="SCHED_S_TASK_READY"></span><span id="sched_s_task_ready"></span>**SCHED\_S\_TASK\_READY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7544e-113">0x00041300</span><span class="sxs-lookup"><span data-stu-id="7544e-113">0x00041300</span></span>
</dt> <dt>



<span data-ttu-id="7544e-114">La tâche est prête à s’exécuter à la prochaine heure planifiée.</span><span class="sxs-lookup"><span data-stu-id="7544e-114">The task is ready to run at its next scheduled time.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7544e-115"><span id="SCHED_S_TASK_RUNNING"></span><span id="sched_s_task_running"></span>**\_tâche sched \_ S \_ en cours d’exécution**</span><span class="sxs-lookup"><span data-stu-id="7544e-115"><span id="SCHED_S_TASK_RUNNING"></span><span id="sched_s_task_running"></span>**SCHED\_S\_TASK\_RUNNING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7544e-116">0x00041301</span><span class="sxs-lookup"><span data-stu-id="7544e-116">0x00041301</span></span>
</dt> <dt>



<span data-ttu-id="7544e-117">La tâche est en cours d'exécution.</span><span class="sxs-lookup"><span data-stu-id="7544e-117">The task is currently running.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7544e-118"><span id="SCHED_S_TASK_DISABLED"></span><span id="sched_s_task_disabled"></span>**\_tâche sched \_ S \_ désactivée**</span><span class="sxs-lookup"><span data-stu-id="7544e-118"><span id="SCHED_S_TASK_DISABLED"></span><span id="sched_s_task_disabled"></span>**SCHED\_S\_TASK\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7544e-119">0x00041302</span><span class="sxs-lookup"><span data-stu-id="7544e-119">0x00041302</span></span>
</dt> <dt>



<span data-ttu-id="7544e-120">La tâche ne s’exécutera pas aux heures planifiées, car elle a été désactivée.</span><span class="sxs-lookup"><span data-stu-id="7544e-120">The task will not run at the scheduled times because it has been disabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7544e-121"><span id="SCHED_S_TASK_HAS_NOT_RUN"></span><span id="sched_s_task_has_not_run"></span>**la \_ tâche sched S \_ \_ \_ n’a pas été \_ exécutée**</span><span class="sxs-lookup"><span data-stu-id="7544e-121"><span id="SCHED_S_TASK_HAS_NOT_RUN"></span><span id="sched_s_task_has_not_run"></span>**SCHED\_S\_TASK\_HAS\_NOT\_RUN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7544e-122">0x00041303</span><span class="sxs-lookup"><span data-stu-id="7544e-122">0x00041303</span></span>
</dt> <dt>



<span data-ttu-id="7544e-123">La tâche n’a pas encore été exécutée.</span><span class="sxs-lookup"><span data-stu-id="7544e-123">The task has not yet run.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7544e-124"><span id="SCHED_S_TASK_NO_MORE_RUNS"></span><span id="sched_s_task_no_more_runs"></span>**PLANIFICATION \_ \_ des tâches \_ \_ S \_**</span><span class="sxs-lookup"><span data-stu-id="7544e-124"><span id="SCHED_S_TASK_NO_MORE_RUNS"></span><span id="sched_s_task_no_more_runs"></span>**SCHED\_S\_TASK\_NO\_MORE\_RUNS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7544e-125">0x00041304</span><span class="sxs-lookup"><span data-stu-id="7544e-125">0x00041304</span></span>
</dt> <dt>



<span data-ttu-id="7544e-126">Il n’y a plus d’exécutions planifiées pour cette tâche.</span><span class="sxs-lookup"><span data-stu-id="7544e-126">There are no more runs scheduled for this task.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7544e-127"><span id="SCHED_S_TASK_NOT_SCHEDULED"></span><span id="sched_s_task_not_scheduled"></span>**\_tâche sched \_ S \_ non \_ planifiée**</span><span class="sxs-lookup"><span data-stu-id="7544e-127"><span id="SCHED_S_TASK_NOT_SCHEDULED"></span><span id="sched_s_task_not_scheduled"></span>**SCHED\_S\_TASK\_NOT\_SCHEDULED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7544e-128">0x00041305</span><span class="sxs-lookup"><span data-stu-id="7544e-128">0x00041305</span></span>
</dt> <dt>



<span data-ttu-id="7544e-129">Une ou plusieurs des propriétés nécessaires pour exécuter cette tâche sur une planification n’ont pas été définies.</span><span class="sxs-lookup"><span data-stu-id="7544e-129">One or more of the properties that are needed to run this task on a schedule have not been set.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7544e-130"><span id="SCHED_S_TASK_TERMINATED"></span><span id="sched_s_task_terminated"></span>**\_tâche sched \_ S \_ terminée**</span><span class="sxs-lookup"><span data-stu-id="7544e-130"><span id="SCHED_S_TASK_TERMINATED"></span><span id="sched_s_task_terminated"></span>**SCHED\_S\_TASK\_TERMINATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7544e-131">0x00041306</span><span class="sxs-lookup"><span data-stu-id="7544e-131">0x00041306</span></span>
</dt> <dt>



<span data-ttu-id="7544e-132">La dernière exécution de la tâche a été arrêtée par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="7544e-132">The last run of the task was terminated by the user.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7544e-133"><span id="SCHED_S_TASK_NO_VALID_TRIGGERS"></span><span id="sched_s_task_no_valid_triggers"></span>**PLANIFICATION \_ des \_ tâches \_ S \_ aucun \_ déclencheur valide**</span><span class="sxs-lookup"><span data-stu-id="7544e-133"><span id="SCHED_S_TASK_NO_VALID_TRIGGERS"></span><span id="sched_s_task_no_valid_triggers"></span>**SCHED\_S\_TASK\_NO\_VALID\_TRIGGERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7544e-134">0x00041307</span><span class="sxs-lookup"><span data-stu-id="7544e-134">0x00041307</span></span>
</dt> <dt>



<span data-ttu-id="7544e-135">Soit la tâche n’a aucun déclencheur, soit les déclencheurs existants sont désactivés ou non définis.</span><span class="sxs-lookup"><span data-stu-id="7544e-135">Either the task has no triggers or the existing triggers are disabled or not set.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7544e-136"><span id="SCHED_S_EVENT_TRIGGER"></span><span id="sched_s_event_trigger"></span>**\_ \_ déclencheur d’événement sched S \_**</span><span class="sxs-lookup"><span data-stu-id="7544e-136"><span id="SCHED_S_EVENT_TRIGGER"></span><span id="sched_s_event_trigger"></span>**SCHED\_S\_EVENT\_TRIGGER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7544e-137">0x00041308</span><span class="sxs-lookup"><span data-stu-id="7544e-137">0x00041308</span></span>
</dt> <dt>



<span data-ttu-id="7544e-138">Les déclencheurs d’événements n’ont pas de durée d’exécution définie.</span><span class="sxs-lookup"><span data-stu-id="7544e-138">Event triggers do not have set run times.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7544e-139"><span id="SCHED_E_TRIGGER_NOT_FOUND"></span><span id="sched_e_trigger_not_found"></span>**\_ \_ déclencheur sched \_ E \_ introuvable**</span><span class="sxs-lookup"><span data-stu-id="7544e-139"><span id="SCHED_E_TRIGGER_NOT_FOUND"></span><span id="sched_e_trigger_not_found"></span>**SCHED\_E\_TRIGGER\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7544e-140">0x80041309</span><span class="sxs-lookup"><span data-stu-id="7544e-140">0x80041309</span></span>
</dt> <dt>



<span data-ttu-id="7544e-141">Le déclencheur d’une tâche est introuvable.</span><span class="sxs-lookup"><span data-stu-id="7544e-141">A task's trigger is not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7544e-142"><span id="SCHED_E_TASK_NOT_READY"></span><span id="sched_e_task_not_ready"></span>**\_tâche sched \_ E \_ non \_ prête**</span><span class="sxs-lookup"><span data-stu-id="7544e-142"><span id="SCHED_E_TASK_NOT_READY"></span><span id="sched_e_task_not_ready"></span>**SCHED\_E\_TASK\_NOT\_READY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7544e-143">0x8004130A</span><span class="sxs-lookup"><span data-stu-id="7544e-143">0x8004130A</span></span>
</dt> <dt>



<span data-ttu-id="7544e-144">Une ou plusieurs des propriétés requises pour exécuter cette tâche n’ont pas été définies.</span><span class="sxs-lookup"><span data-stu-id="7544e-144">One or more of the properties required to run this task have not been set.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7544e-145"><span id="SCHED_E_TASK_NOT_RUNNING"></span><span id="sched_e_task_not_running"></span>**\_tâche sched \_ E \_ non \_ en cours d’exécution**</span><span class="sxs-lookup"><span data-stu-id="7544e-145"><span id="SCHED_E_TASK_NOT_RUNNING"></span><span id="sched_e_task_not_running"></span>**SCHED\_E\_TASK\_NOT\_RUNNING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7544e-146">0x8004130B</span><span class="sxs-lookup"><span data-stu-id="7544e-146">0x8004130B</span></span>
</dt> <dt>



<span data-ttu-id="7544e-147">Il n’y a aucune instance en cours d’exécution de la tâche.</span><span class="sxs-lookup"><span data-stu-id="7544e-147">There is no running instance of the task.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7544e-148"><span id="SCHED_E_SERVICE_NOT_INSTALLED"></span><span id="sched_e_service_not_installed"></span>**\_service sched \_ E \_ non \_ installé**</span><span class="sxs-lookup"><span data-stu-id="7544e-148"><span id="SCHED_E_SERVICE_NOT_INSTALLED"></span><span id="sched_e_service_not_installed"></span>**SCHED\_E\_SERVICE\_NOT\_INSTALLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7544e-149">0x8004130C</span><span class="sxs-lookup"><span data-stu-id="7544e-149">0x8004130C</span></span>
</dt> <dt>



<span data-ttu-id="7544e-150">Le service Planificateur de tâches n’est pas installé sur cet ordinateur.</span><span class="sxs-lookup"><span data-stu-id="7544e-150">The Task Scheduler service is not installed on this computer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7544e-151"><span id="SCHED_E_CANNOT_OPEN_TASK"></span><span id="sched_e_cannot_open_task"></span>**la grille \_ E \_ ne peut pas \_ ouvrir la \_ tâche**</span><span class="sxs-lookup"><span data-stu-id="7544e-151"><span id="SCHED_E_CANNOT_OPEN_TASK"></span><span id="sched_e_cannot_open_task"></span>**SCHED\_E\_CANNOT\_OPEN\_TASK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7544e-152">0x8004130D</span><span class="sxs-lookup"><span data-stu-id="7544e-152">0x8004130D</span></span>
</dt> <dt>



<span data-ttu-id="7544e-153">Impossible d’ouvrir l’objet de tâche.</span><span class="sxs-lookup"><span data-stu-id="7544e-153">The task object could not be opened.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7544e-154"><span id="SCHED_E_INVALID_TASK"></span><span id="sched_e_invalid_task"></span>**PLANIFICATION \_ E \_ tâche non valide \_**</span><span class="sxs-lookup"><span data-stu-id="7544e-154"><span id="SCHED_E_INVALID_TASK"></span><span id="sched_e_invalid_task"></span>**SCHED\_E\_INVALID\_TASK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7544e-155">0x8004130E</span><span class="sxs-lookup"><span data-stu-id="7544e-155">0x8004130E</span></span>
</dt> <dt>



<span data-ttu-id="7544e-156">L’objet est un objet de tâche non valide ou n’est pas un objet de tâche.</span><span class="sxs-lookup"><span data-stu-id="7544e-156">The object is either an invalid task object or is not a task object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7544e-157"><span id="SCHED_E_ACCOUNT_INFORMATION_NOT_SET"></span><span id="sched_e_account_information_not_set"></span>**\_ \_ informations sur le compte sched E \_ \_ non \_ définies**</span><span class="sxs-lookup"><span data-stu-id="7544e-157"><span id="SCHED_E_ACCOUNT_INFORMATION_NOT_SET"></span><span id="sched_e_account_information_not_set"></span>**SCHED\_E\_ACCOUNT\_INFORMATION\_NOT\_SET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7544e-158">0x8004130F</span><span class="sxs-lookup"><span data-stu-id="7544e-158">0x8004130F</span></span>
</dt> <dt>



<span data-ttu-id="7544e-159">Aucune information de compte n’a été trouvée dans la base de données de sécurité Planificateur de tâches pour la tâche indiquée.</span><span class="sxs-lookup"><span data-stu-id="7544e-159">No account information could be found in the Task Scheduler security database for the task indicated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7544e-160"><span id="SCHED_E_ACCOUNT_NAME_NOT_FOUND"></span><span id="sched_e_account_name_not_found"></span>**\_nom du compte sched E \_ \_ \_ \_ introuvable**</span><span class="sxs-lookup"><span data-stu-id="7544e-160"><span id="SCHED_E_ACCOUNT_NAME_NOT_FOUND"></span><span id="sched_e_account_name_not_found"></span>**SCHED\_E\_ACCOUNT\_NAME\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7544e-161">0x80041310</span><span class="sxs-lookup"><span data-stu-id="7544e-161">0x80041310</span></span>
</dt> <dt>



<span data-ttu-id="7544e-162">Impossible d’établir l’existence du compte spécifié.</span><span class="sxs-lookup"><span data-stu-id="7544e-162">Unable to establish existence of the account specified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7544e-163"><span id="SCHED_E_ACCOUNT_DBASE_CORRUPT"></span><span id="sched_e_account_dbase_corrupt"></span>**le \_ compte sched E \_ \_ dBASE est \_ endommagé**</span><span class="sxs-lookup"><span data-stu-id="7544e-163"><span id="SCHED_E_ACCOUNT_DBASE_CORRUPT"></span><span id="sched_e_account_dbase_corrupt"></span>**SCHED\_E\_ACCOUNT\_DBASE\_CORRUPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7544e-164">0x80041311</span><span class="sxs-lookup"><span data-stu-id="7544e-164">0x80041311</span></span>
</dt> <dt>



<span data-ttu-id="7544e-165">Une altération a été détectée dans la base de données de sécurité Planificateur de tâches ; la base de données a été réinitialisée.</span><span class="sxs-lookup"><span data-stu-id="7544e-165">Corruption was detected in the Task Scheduler security database; the database has been reset.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7544e-166"><span id="SCHED_E_NO_SECURITY_SERVICES"></span><span id="sched_e_no_security_services"></span>**SCHED \_ E \_ aucun \_ service de sécurité \_**</span><span class="sxs-lookup"><span data-stu-id="7544e-166"><span id="SCHED_E_NO_SECURITY_SERVICES"></span><span id="sched_e_no_security_services"></span>**SCHED\_E\_NO\_SECURITY\_SERVICES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7544e-167">0x80041312</span><span class="sxs-lookup"><span data-stu-id="7544e-167">0x80041312</span></span>
</dt> <dt>



<span data-ttu-id="7544e-168">Les services de sécurité Planificateur de tâches ne sont disponibles que sur Windows NT.</span><span class="sxs-lookup"><span data-stu-id="7544e-168">Task Scheduler security services are available only on Windows NT.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7544e-169"><span id="SCHED_E_UNKNOWN_OBJECT_VERSION"></span><span id="sched_e_unknown_object_version"></span>**PLANIFICATION d’une \_ \_ version d’objet inconnue \_ \_**</span><span class="sxs-lookup"><span data-stu-id="7544e-169"><span id="SCHED_E_UNKNOWN_OBJECT_VERSION"></span><span id="sched_e_unknown_object_version"></span>**SCHED\_E\_UNKNOWN\_OBJECT\_VERSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7544e-170">0x80041313</span><span class="sxs-lookup"><span data-stu-id="7544e-170">0x80041313</span></span>
</dt> <dt>



<span data-ttu-id="7544e-171">La version de l’objet de tâche n’est pas prise en charge ou n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="7544e-171">The task object version is either unsupported or invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7544e-172"><span id="SCHED_E_UNSUPPORTED_ACCOUNT_OPTION"></span><span id="sched_e_unsupported_account_option"></span>**\_option de compte sched E \_ non prise en charge \_ \_**</span><span class="sxs-lookup"><span data-stu-id="7544e-172"><span id="SCHED_E_UNSUPPORTED_ACCOUNT_OPTION"></span><span id="sched_e_unsupported_account_option"></span>**SCHED\_E\_UNSUPPORTED\_ACCOUNT\_OPTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7544e-173">0x80041314</span><span class="sxs-lookup"><span data-stu-id="7544e-173">0x80041314</span></span>
</dt> <dt>



<span data-ttu-id="7544e-174">La tâche a été configurée avec une combinaison non prise en charge de paramètres de compte et d’options d’exécution.</span><span class="sxs-lookup"><span data-stu-id="7544e-174">The task has been configured with an unsupported combination of account settings and run time options.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7544e-175"><span id="SCHED_E_SERVICE_NOT_RUNNING"></span><span id="sched_e_service_not_running"></span>**le \_ service sched E \_ \_ n’est pas \_ en cours d’exécution**</span><span class="sxs-lookup"><span data-stu-id="7544e-175"><span id="SCHED_E_SERVICE_NOT_RUNNING"></span><span id="sched_e_service_not_running"></span>**SCHED\_E\_SERVICE\_NOT\_RUNNING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7544e-176">0x80041315</span><span class="sxs-lookup"><span data-stu-id="7544e-176">0x80041315</span></span>
</dt> <dt>



<span data-ttu-id="7544e-177">Le service Planificateur de tâches n’est pas en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="7544e-177">The Task Scheduler Service is not running.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7544e-178"><span id="SCHED_E_UNEXPECTEDNODE"></span><span id="sched_e_unexpectednode"></span>**PLANIFICATION \_ E \_ UNEXPECTEDNODE**</span><span class="sxs-lookup"><span data-stu-id="7544e-178"><span id="SCHED_E_UNEXPECTEDNODE"></span><span id="sched_e_unexpectednode"></span>**SCHED\_E\_UNEXPECTEDNODE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7544e-179">0x80041316</span><span class="sxs-lookup"><span data-stu-id="7544e-179">0x80041316</span></span>
</dt> <dt>



<span data-ttu-id="7544e-180">Le code XML de la tâche contient un nœud inattendu.</span><span class="sxs-lookup"><span data-stu-id="7544e-180">The task XML contains an unexpected node.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7544e-181"><span id="SCHED_E_NAMESPACE"></span><span id="sched_e_namespace"></span>**\_espace de \_ noms sched E**</span><span class="sxs-lookup"><span data-stu-id="7544e-181"><span id="SCHED_E_NAMESPACE"></span><span id="sched_e_namespace"></span>**SCHED\_E\_NAMESPACE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7544e-182">0x80041317</span><span class="sxs-lookup"><span data-stu-id="7544e-182">0x80041317</span></span>
</dt> <dt>



<span data-ttu-id="7544e-183">Le code XML de la tâche contient un élément ou un attribut d’un espace de noms inattendu.</span><span class="sxs-lookup"><span data-stu-id="7544e-183">The task XML contains an element or attribute from an unexpected namespace.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7544e-184"><span id="SCHED_E_INVALIDVALUE"></span><span id="sched_e_invalidvalue"></span>**PLANIFICATION \_ E \_ INVALIDVALUE**</span><span class="sxs-lookup"><span data-stu-id="7544e-184"><span id="SCHED_E_INVALIDVALUE"></span><span id="sched_e_invalidvalue"></span>**SCHED\_E\_INVALIDVALUE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7544e-185">0x80041318</span><span class="sxs-lookup"><span data-stu-id="7544e-185">0x80041318</span></span>
</dt> <dt>



<span data-ttu-id="7544e-186">Le fichier XML de la tâche contient une valeur qui n’est pas correctement mise en forme ou en dehors de la plage.</span><span class="sxs-lookup"><span data-stu-id="7544e-186">The task XML contains a value which is incorrectly formatted or out of range.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7544e-187"><span id="SCHED_E_MISSINGNODE"></span><span id="sched_e_missingnode"></span>**PLANIFICATION \_ E \_ MISSINGNODE**</span><span class="sxs-lookup"><span data-stu-id="7544e-187"><span id="SCHED_E_MISSINGNODE"></span><span id="sched_e_missingnode"></span>**SCHED\_E\_MISSINGNODE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7544e-188">0x80041319</span><span class="sxs-lookup"><span data-stu-id="7544e-188">0x80041319</span></span>
</dt> <dt>



<span data-ttu-id="7544e-189">L’élément ou l’attribut requis est manquant dans le fichier XML de la tâche.</span><span class="sxs-lookup"><span data-stu-id="7544e-189">The task XML is missing a required element or attribute.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7544e-190"><span id="SCHED_E_MALFORMEDXML"></span><span id="sched_e_malformedxml"></span>**PLANIFICATION \_ E \_ MALFORMEDXML**</span><span class="sxs-lookup"><span data-stu-id="7544e-190"><span id="SCHED_E_MALFORMEDXML"></span><span id="sched_e_malformedxml"></span>**SCHED\_E\_MALFORMEDXML**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7544e-191">0x8004131A</span><span class="sxs-lookup"><span data-stu-id="7544e-191">0x8004131A</span></span>
</dt> <dt>



<span data-ttu-id="7544e-192">Le code XML de la tâche est incorrect.</span><span class="sxs-lookup"><span data-stu-id="7544e-192">The task XML is malformed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7544e-193"><span id="SCHED_S_SOME_TRIGGERS_FAILED"></span><span id="sched_s_some_triggers_failed"></span>**échec de la planification de \_ \_ certains \_ déclencheurs \_**</span><span class="sxs-lookup"><span data-stu-id="7544e-193"><span id="SCHED_S_SOME_TRIGGERS_FAILED"></span><span id="sched_s_some_triggers_failed"></span>**SCHED\_S\_SOME\_TRIGGERS\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7544e-194">0x0004131B</span><span class="sxs-lookup"><span data-stu-id="7544e-194">0x0004131B</span></span>
</dt> <dt>



<span data-ttu-id="7544e-195">La tâche est inscrite, mais tous les déclencheurs spécifiés ne démarrent pas la tâche.</span><span class="sxs-lookup"><span data-stu-id="7544e-195">The task is registered, but not all specified triggers will start the task.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7544e-196"><span id="SCHED_S_BATCH_LOGON_PROBLEM"></span><span id="sched_s_batch_logon_problem"></span>**\_problème de \_ connexion par lot de sched S \_ \_**</span><span class="sxs-lookup"><span data-stu-id="7544e-196"><span id="SCHED_S_BATCH_LOGON_PROBLEM"></span><span id="sched_s_batch_logon_problem"></span>**SCHED\_S\_BATCH\_LOGON\_PROBLEM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7544e-197">0x0004131C</span><span class="sxs-lookup"><span data-stu-id="7544e-197">0x0004131C</span></span>
</dt> <dt>



<span data-ttu-id="7544e-198">La tâche est inscrite, mais peut ne pas démarrer.</span><span class="sxs-lookup"><span data-stu-id="7544e-198">The task is registered, but may fail to start.</span></span> <span data-ttu-id="7544e-199">Le privilège de connexion par lot doit être activé pour le principal de tâche.</span><span class="sxs-lookup"><span data-stu-id="7544e-199">Batch logon privilege needs to be enabled for the task principal.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7544e-200"><span id="SCHED_E_TOO_MANY_NODES"></span><span id="sched_e_too_many_nodes"></span>**PLANIFICATION \_ d' \_ \_ un trop grand nombre de \_ nœuds**</span><span class="sxs-lookup"><span data-stu-id="7544e-200"><span id="SCHED_E_TOO_MANY_NODES"></span><span id="sched_e_too_many_nodes"></span>**SCHED\_E\_TOO\_MANY\_NODES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7544e-201">0x8004131D</span><span class="sxs-lookup"><span data-stu-id="7544e-201">0x8004131D</span></span>
</dt> <dt>



<span data-ttu-id="7544e-202">Le code XML de la tâche contient un trop grand nombre de nœuds du même type.</span><span class="sxs-lookup"><span data-stu-id="7544e-202">The task XML contains too many nodes of the same type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7544e-203"><span id="SCHED_E_PAST_END_BOUNDARY"></span><span id="sched_e_past_end_boundary"></span>**\_ \_ \_ délimiteur de fin \_ de la grille**</span><span class="sxs-lookup"><span data-stu-id="7544e-203"><span id="SCHED_E_PAST_END_BOUNDARY"></span><span id="sched_e_past_end_boundary"></span>**SCHED\_E\_PAST\_END\_BOUNDARY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7544e-204">0x8004131E</span><span class="sxs-lookup"><span data-stu-id="7544e-204">0x8004131E</span></span>
</dt> <dt>



<span data-ttu-id="7544e-205">La tâche ne peut pas être démarrée après la limite de fin du déclencheur.</span><span class="sxs-lookup"><span data-stu-id="7544e-205">The task cannot be started after the trigger end boundary.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7544e-206"><span id="SCHED_E_ALREADY_RUNNING"></span><span id="sched_e_already_running"></span>**SCHED \_ E \_ déjà \_ en cours d’exécution**</span><span class="sxs-lookup"><span data-stu-id="7544e-206"><span id="SCHED_E_ALREADY_RUNNING"></span><span id="sched_e_already_running"></span>**SCHED\_E\_ALREADY\_RUNNING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7544e-207">0x8004131F</span><span class="sxs-lookup"><span data-stu-id="7544e-207">0x8004131F</span></span>
</dt> <dt>



<span data-ttu-id="7544e-208">Une instance de cette tâche est déjà en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="7544e-208">An instance of this task is already running.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7544e-209"><span id="SCHED_E_USER_NOT_LOGGED_ON"></span><span id="sched_e_user_not_logged_on"></span>**\_utilisateur sched \_ E \_ non \_ connecté \_**</span><span class="sxs-lookup"><span data-stu-id="7544e-209"><span id="SCHED_E_USER_NOT_LOGGED_ON"></span><span id="sched_e_user_not_logged_on"></span>**SCHED\_E\_USER\_NOT\_LOGGED\_ON**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7544e-210">0x80041320</span><span class="sxs-lookup"><span data-stu-id="7544e-210">0x80041320</span></span>
</dt> <dt>



<span data-ttu-id="7544e-211">La tâche ne s’exécute pas, car l’utilisateur n’est pas connecté.</span><span class="sxs-lookup"><span data-stu-id="7544e-211">The task will not run because the user is not logged on.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7544e-212"><span id="SCHED_E_INVALID_TASK_HASH"></span><span id="sched_e_invalid_task_hash"></span>**\_ligne de \_ \_ hachage de tâche non valide \_**</span><span class="sxs-lookup"><span data-stu-id="7544e-212"><span id="SCHED_E_INVALID_TASK_HASH"></span><span id="sched_e_invalid_task_hash"></span>**SCHED\_E\_INVALID\_TASK\_HASH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7544e-213">0x80041321</span><span class="sxs-lookup"><span data-stu-id="7544e-213">0x80041321</span></span>
</dt> <dt>



<span data-ttu-id="7544e-214">L’image de tâche est endommagée ou a été falsifiée.</span><span class="sxs-lookup"><span data-stu-id="7544e-214">The task image is corrupt or has been tampered with.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7544e-215"><span id="SCHED_E_SERVICE_NOT_AVAILABLE"></span><span id="sched_e_service_not_available"></span>**\_service sched \_ E \_ non \_ disponible**</span><span class="sxs-lookup"><span data-stu-id="7544e-215"><span id="SCHED_E_SERVICE_NOT_AVAILABLE"></span><span id="sched_e_service_not_available"></span>**SCHED\_E\_SERVICE\_NOT\_AVAILABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7544e-216">0x80041322</span><span class="sxs-lookup"><span data-stu-id="7544e-216">0x80041322</span></span>
</dt> <dt>



<span data-ttu-id="7544e-217">Le service Planificateur de tâches n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="7544e-217">The Task Scheduler service is not available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7544e-218"><span id="SCHED_E_SERVICE_TOO_BUSY"></span><span id="sched_e_service_too_busy"></span>**\_service sched \_ E \_ trop \_ occupé**</span><span class="sxs-lookup"><span data-stu-id="7544e-218"><span id="SCHED_E_SERVICE_TOO_BUSY"></span><span id="sched_e_service_too_busy"></span>**SCHED\_E\_SERVICE\_TOO\_BUSY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7544e-219">0x80041323</span><span class="sxs-lookup"><span data-stu-id="7544e-219">0x80041323</span></span>
</dt> <dt>



<span data-ttu-id="7544e-220">Le service Planificateur de tâches est trop occupé pour traiter votre demande.</span><span class="sxs-lookup"><span data-stu-id="7544e-220">The Task Scheduler service is too busy to handle your request.</span></span> <span data-ttu-id="7544e-221">Veuillez réessayer plus tard.</span><span class="sxs-lookup"><span data-stu-id="7544e-221">Please try again later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7544e-222"><span id="SCHED_E_TASK_ATTEMPTED"></span><span id="sched_e_task_attempted"></span>**\_tâche sched \_ E \_ tentée**</span><span class="sxs-lookup"><span data-stu-id="7544e-222"><span id="SCHED_E_TASK_ATTEMPTED"></span><span id="sched_e_task_attempted"></span>**SCHED\_E\_TASK\_ATTEMPTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7544e-223">0x80041324</span><span class="sxs-lookup"><span data-stu-id="7544e-223">0x80041324</span></span>
</dt> <dt>



<span data-ttu-id="7544e-224">Le service de Planificateur de tâches a tenté d’exécuter la tâche, mais la tâche n’a pas été exécutée en raison de l’une des contraintes dans la définition de la tâche.</span><span class="sxs-lookup"><span data-stu-id="7544e-224">The Task Scheduler service attempted to run the task, but the task did not run due to one of the constraints in the task definition.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7544e-225"><span id="SCHED_S_TASK_QUEUED"></span><span id="sched_s_task_queued"></span>**\_tâche sched S en \_ \_ attente**</span><span class="sxs-lookup"><span data-stu-id="7544e-225"><span id="SCHED_S_TASK_QUEUED"></span><span id="sched_s_task_queued"></span>**SCHED\_S\_TASK\_QUEUED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7544e-226">0x00041325</span><span class="sxs-lookup"><span data-stu-id="7544e-226">0x00041325</span></span>
</dt> <dt>



<span data-ttu-id="7544e-227">Le service de Planificateur de tâches a demandé l’exécution de la tâche.</span><span class="sxs-lookup"><span data-stu-id="7544e-227">The Task Scheduler service has asked the task to run.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7544e-228"><span id="SCHED_E_TASK_DISABLED"></span><span id="sched_e_task_disabled"></span>**\_tâche sched \_ E \_ désactivée**</span><span class="sxs-lookup"><span data-stu-id="7544e-228"><span id="SCHED_E_TASK_DISABLED"></span><span id="sched_e_task_disabled"></span>**SCHED\_E\_TASK\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7544e-229">0x80041326</span><span class="sxs-lookup"><span data-stu-id="7544e-229">0x80041326</span></span>
</dt> <dt>



<span data-ttu-id="7544e-230">La tâche est désactivée.</span><span class="sxs-lookup"><span data-stu-id="7544e-230">The task is disabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7544e-231"><span id="SCHED_E_TASK_NOT_V1_COMPAT"></span><span id="sched_e_task_not_v1_compat"></span>**Compatibilité de la \_ tâche sched E \_ \_ non \_ v1 \_**</span><span class="sxs-lookup"><span data-stu-id="7544e-231"><span id="SCHED_E_TASK_NOT_V1_COMPAT"></span><span id="sched_e_task_not_v1_compat"></span>**SCHED\_E\_TASK\_NOT\_V1\_COMPAT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7544e-232">0x80041327</span><span class="sxs-lookup"><span data-stu-id="7544e-232">0x80041327</span></span>
</dt> <dt>



<span data-ttu-id="7544e-233">La tâche a des propriétés qui ne sont pas compatibles avec les versions antérieures de Windows.</span><span class="sxs-lookup"><span data-stu-id="7544e-233">The task has properties that are not compatible with earlier versions of Windows.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7544e-234"><span id="SCHED_E_START_ON_DEMAND"></span><span id="sched_e_start_on_demand"></span>**PLANIFICATION \_ \_ d’un démarrage \_ à \_ la demande**</span><span class="sxs-lookup"><span data-stu-id="7544e-234"><span id="SCHED_E_START_ON_DEMAND"></span><span id="sched_e_start_on_demand"></span>**SCHED\_E\_START\_ON\_DEMAND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7544e-235">0x80041328</span><span class="sxs-lookup"><span data-stu-id="7544e-235">0x80041328</span></span>
</dt> <dt>



<span data-ttu-id="7544e-236">Les paramètres de tâche n’autorisent pas le démarrage de la tâche à la demande.</span><span class="sxs-lookup"><span data-stu-id="7544e-236">The task settings do not allow the task to start on demand.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7544e-237">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7544e-237">Requirements</span></span>



| <span data-ttu-id="7544e-238">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7544e-238">Requirement</span></span> | <span data-ttu-id="7544e-239">Valeur</span><span class="sxs-lookup"><span data-stu-id="7544e-239">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7544e-240">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7544e-240">Minimum supported client</span></span><br/> | <span data-ttu-id="7544e-241">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7544e-241">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7544e-242">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7544e-242">Minimum supported server</span></span><br/> | <span data-ttu-id="7544e-243">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7544e-243">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7544e-244">En-tête</span><span class="sxs-lookup"><span data-stu-id="7544e-244">Header</span></span><br/>                   | <dl> <span data-ttu-id="7544e-245"><dt>WinError. h</dt></span><span class="sxs-lookup"><span data-stu-id="7544e-245"><dt>WinError.h</dt></span></span> </dl> |



 

 





