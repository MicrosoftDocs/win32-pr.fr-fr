---
title: Propriété Trigger. type
description: Pour les scripts, obtient le type du déclencheur.
ms.assetid: 346e6b02-c89e-4644-aa19-2bbf3d0fb3c3
keywords:
- Planificateur de tâches de propriété de type
- Propriété type Planificateur de tâches, objet Trigger
- Planificateur de tâches de l’objet de déclencheur, propriété type
topic_type:
- apiref
api_name:
- Trigger.Type
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba2cef2d6ae33ceeac028e10a0f545afbc0a0ec8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740789"
---
# <a name="triggertype-property"></a><span data-ttu-id="d6eed-106">Propriété Trigger. type</span><span class="sxs-lookup"><span data-stu-id="d6eed-106">Trigger.Type property</span></span>

<span data-ttu-id="d6eed-107">Pour les scripts, obtient le type du déclencheur.</span><span class="sxs-lookup"><span data-stu-id="d6eed-107">For scripting, gets the type of the trigger.</span></span> <span data-ttu-id="d6eed-108">Le type de déclencheur est défini lors de la création du déclencheur et ne peut pas être modifié ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="d6eed-108">The trigger type is defined when the trigger is created and cannot be changed later.</span></span> <span data-ttu-id="d6eed-109">Pour plus d’informations sur la création d’un déclencheur, consultez [**TriggerCollection. Create**](triggercollection-create.md).</span><span class="sxs-lookup"><span data-stu-id="d6eed-109">For information on creating a trigger, see [**TriggerCollection.Create**](triggercollection-create.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="d6eed-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d6eed-110">Syntax</span></span>


```VB
Trigger.Type As TASK_TRIGGER_TYPE2
```



## <a name="property-value"></a><span data-ttu-id="d6eed-111">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="d6eed-111">Property value</span></span>

<span data-ttu-id="d6eed-112">L’une des [**tâches suivantes \_ déclenchent \_**](/windows/desktop/api/taskschd/ne-taskschd-task_trigger_type2) des valeurs d’énumération type2.</span><span class="sxs-lookup"><span data-stu-id="d6eed-112">One of the following [**TASK\_TRIGGER\_TYPE2**](/windows/desktop/api/taskschd/ne-taskschd-task_trigger_type2) enumeration values.</span></span>



| <span data-ttu-id="d6eed-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="d6eed-113">Value</span></span>                                                                                                                                                                                                                                                                                | <span data-ttu-id="d6eed-114">Signification</span><span class="sxs-lookup"><span data-stu-id="d6eed-114">Meaning</span></span>                                                               |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <span id="TASK_TRIGGER_EVENT"></span><span id="task_trigger_event"></span><dl> <span data-ttu-id="d6eed-115"><dt>**Tâche \_ DÉCLENCHER l' \_ événement**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="d6eed-115"><dt>**TASK\_TRIGGER\_EVENT**</dt> <dt>0</dt></span></span> </dl>                                                 | <span data-ttu-id="d6eed-116">Démarre la tâche lorsqu’un événement spécifique se produit.</span><span class="sxs-lookup"><span data-stu-id="d6eed-116">Starts the task when a specific event occurs.</span></span><br/>              |
| <span id="TASK_TRIGGER_TIME"></span><span id="task_trigger_time"></span><dl> <span data-ttu-id="d6eed-117"><dt>**Tâche \_ \_Heure du déclencheur**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="d6eed-117"><dt>**TASK\_TRIGGER\_TIME**</dt> <dt>1</dt></span></span> </dl>                                                    | <span data-ttu-id="d6eed-118">Démarre la tâche à une heure spécifique de la journée.</span><span class="sxs-lookup"><span data-stu-id="d6eed-118">Starts the task at a specific time of day.</span></span><br/>                 |
| <span id="TASK_TRIGGER_DAILY"></span><span id="task_trigger_daily"></span><dl> <span data-ttu-id="d6eed-119"><dt>**Tâche \_ DÉCLENCHEur \_ quotidien**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="d6eed-119"><dt>**TASK\_TRIGGER\_DAILY**</dt> <dt>2</dt></span></span> </dl>                                                 | <span data-ttu-id="d6eed-120">Démarre la tâche quotidiennement.</span><span class="sxs-lookup"><span data-stu-id="d6eed-120">Starts the task daily.</span></span><br/>                                     |
| <span id="TASK_TRIGGER_WEEKLY"></span><span id="task_trigger_weekly"></span><dl> <span data-ttu-id="d6eed-121"><dt>**Tâche \_ DÉCLENCHEur \_ hebdomadaire**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="d6eed-121"><dt>**TASK\_TRIGGER\_WEEKLY**</dt> <dt>3</dt></span></span> </dl>                                              | <span data-ttu-id="d6eed-122">Démarre la tâche toutes les semaines.</span><span class="sxs-lookup"><span data-stu-id="d6eed-122">Starts the task weekly.</span></span><br/>                                    |
| <span id="TASK_TRIGGER_MONTHLY"></span><span id="task_trigger_monthly"></span><dl> <span data-ttu-id="d6eed-123"><dt>**Tâche \_ DÉCLENCHEur \_ mensuel**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="d6eed-123"><dt>**TASK\_TRIGGER\_MONTHLY**</dt> <dt>4</dt></span></span> </dl>                                           | <span data-ttu-id="d6eed-124">Démarre la tâche tous les mois.</span><span class="sxs-lookup"><span data-stu-id="d6eed-124">Starts the task monthly.</span></span><br/>                                   |
| <span id="TASK_TRIGGER_MONTHLYDOW"></span><span id="task_trigger_monthlydow"></span><dl> <span data-ttu-id="d6eed-125"><dt>**Tâche \_ DÉCLENCHEur \_ MONTHLYDOW**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="d6eed-125"><dt>**TASK\_TRIGGER\_MONTHLYDOW**</dt> <dt>5</dt></span></span> </dl>                                  | <span data-ttu-id="d6eed-126">Démarre la tâche chaque mois à un jour spécifique de la semaine.</span><span class="sxs-lookup"><span data-stu-id="d6eed-126">Starts the task every month on a specific day of the week.</span></span><br/> |
| <span id="TASK_TRIGGER_IDLE"></span><span id="task_trigger_idle"></span><dl> <span data-ttu-id="d6eed-127"><dt>**Tâche \_ DÉCLENCHEur \_ inactif**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="d6eed-127"><dt>**TASK\_TRIGGER\_IDLE**</dt> <dt>6</dt></span></span> </dl>                                                    | <span data-ttu-id="d6eed-128">Démarre la tâche lorsque l’ordinateur passe en état d’inactivité.</span><span class="sxs-lookup"><span data-stu-id="d6eed-128">Starts the task when the computer goes into an idle state.</span></span><br/> |
| <span id="TASK_TRIGGER_REGISTRATION"></span><span id="task_trigger_registration"></span><dl> <span data-ttu-id="d6eed-129"><dt>**Tâche \_ \_Inscription du déclencheur**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="d6eed-129"><dt>**TASK\_TRIGGER\_REGISTRATION**</dt> <dt>7</dt></span></span> </dl>                            | <span data-ttu-id="d6eed-130">Démarre la tâche lorsque la tâche est inscrite.</span><span class="sxs-lookup"><span data-stu-id="d6eed-130">Starts the task when the task is registered.</span></span><br/>               |
| <span id="TASK_TRIGGER_BOOT"></span><span id="task_trigger_boot"></span><dl> <span data-ttu-id="d6eed-131"><dt>**Tâche \_ DÉCLENCHER le \_ démarrage**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="d6eed-131"><dt>**TASK\_TRIGGER\_BOOT**</dt> <dt>8</dt></span></span> </dl>                                                    | <span data-ttu-id="d6eed-132">Démarre la tâche au démarrage de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="d6eed-132">Starts the task when the computer boots.</span></span><br/>                   |
| <span id="TASK_TRIGGER_LOGON"></span><span id="task_trigger_logon"></span><dl> <span data-ttu-id="d6eed-133"><dt>**Tâche \_ DÉCLENCHER l' \_ ouverture de session**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="d6eed-133"><dt>**TASK\_TRIGGER\_LOGON**</dt> <dt>9</dt></span></span> </dl>                                                 | <span data-ttu-id="d6eed-134">Démarre la tâche lorsqu’un utilisateur spécifique ouvre une session.</span><span class="sxs-lookup"><span data-stu-id="d6eed-134">Starts the task when a specific user logs on.</span></span><br/>              |
| <span id="TASK_TRIGGER_SESSION_STATE_CHANGE"></span><span id="task_trigger_session_state_change"></span><dl> <span data-ttu-id="d6eed-135"><dt>**Tâche \_ \_Changement d' \_ état \_ de session du déclencheur**</dt> <dt>11</dt></span><span class="sxs-lookup"><span data-stu-id="d6eed-135"><dt>**TASK\_TRIGGER\_SESSION\_STATE\_CHANGE**</dt> <dt>11</dt></span></span> </dl> | <span data-ttu-id="d6eed-136">Déclenche la tâche lorsqu’un état de session spécifique change.</span><span class="sxs-lookup"><span data-stu-id="d6eed-136">Triggers the task when a specific session state changes.</span></span><br/>   |



 

## <a name="requirements"></a><span data-ttu-id="d6eed-137">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d6eed-137">Requirements</span></span>



| <span data-ttu-id="d6eed-138">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d6eed-138">Requirement</span></span> | <span data-ttu-id="d6eed-139">Valeur</span><span class="sxs-lookup"><span data-stu-id="d6eed-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d6eed-140">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d6eed-140">Minimum supported client</span></span><br/> | <span data-ttu-id="d6eed-141">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d6eed-141">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="d6eed-142">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d6eed-142">Minimum supported server</span></span><br/> | <span data-ttu-id="d6eed-143">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d6eed-143">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d6eed-144">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="d6eed-144">Type library</span></span><br/>             | <dl> <span data-ttu-id="d6eed-145"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="d6eed-145"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="d6eed-146">DLL</span><span class="sxs-lookup"><span data-stu-id="d6eed-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d6eed-147"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d6eed-147"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d6eed-148">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d6eed-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6eed-149">**TriggerCollection. Create**</span><span class="sxs-lookup"><span data-stu-id="d6eed-149">**TriggerCollection.Create**</span></span>](triggercollection-create.md)
</dt> <dt>

[<span data-ttu-id="d6eed-150">**\_Déclencheur de tâche \_ type2**</span><span class="sxs-lookup"><span data-stu-id="d6eed-150">**TASK\_TRIGGER\_TYPE2**</span></span>](/windows/desktop/api/taskschd/ne-taskschd-task_trigger_type2)
</dt> <dt>

[<span data-ttu-id="d6eed-151">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="d6eed-151">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





