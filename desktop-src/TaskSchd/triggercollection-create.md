---
title: TriggerCollection. Create, méthode
description: Pour les scripts, crée un nouveau déclencheur pour la tâche.
ms.assetid: 3d7dc811-0d83-475f-8a6e-87e59dae0113
keywords:
- déclenche Planificateur de tâches, création
- Créer une méthode Planificateur de tâches
- Create Method Planificateur de tâches, objet TriggerCollection
- Planificateur de tâches d’objets TriggerCollection, méthode Create
topic_type:
- apiref
api_name:
- TriggerCollection.Create
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad0f1c5dd8bef3d81a8e9b5859bc2bbd8c969bf3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106513771"
---
# <a name="triggercollectioncreate-method"></a><span data-ttu-id="e165b-107">TriggerCollection. Create, méthode</span><span class="sxs-lookup"><span data-stu-id="e165b-107">TriggerCollection.Create method</span></span>

<span data-ttu-id="e165b-108">Pour les scripts, crée un nouveau déclencheur pour la tâche.</span><span class="sxs-lookup"><span data-stu-id="e165b-108">For scripting, creates a new trigger for the task.</span></span>

## <a name="syntax"></a><span data-ttu-id="e165b-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e165b-109">Syntax</span></span>


```VB
TriggerCollection.Create( _
  ByVal type _
)
```



## <a name="parameters"></a><span data-ttu-id="e165b-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e165b-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e165b-111">*type* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e165b-111">*type* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e165b-112">Ce paramètre est défini sur l’une des constantes d’énumération [**\_ \_ type2**](/windows/desktop/api/taskschd/ne-taskschd-task_trigger_type2) de la tâche suivante.</span><span class="sxs-lookup"><span data-stu-id="e165b-112">This parameter is set to one of the following [**TASK\_TRIGGER\_TYPE2**](/windows/desktop/api/taskschd/ne-taskschd-task_trigger_type2) enumeration constants.</span></span>



| <span data-ttu-id="e165b-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="e165b-113">Value</span></span>                                                                                                                                                                                                                                                                                | <span data-ttu-id="e165b-114">Signification</span><span class="sxs-lookup"><span data-stu-id="e165b-114">Meaning</span></span>                                                                                                                                                                  |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TASK_TRIGGER_EVENT"></span><span id="task_trigger_event"></span><dl> <span data-ttu-id="e165b-115"><dt>**Tâche \_ DÉCLENCHER l' \_ événement**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="e165b-115"><dt>**TASK\_TRIGGER\_EVENT**</dt> <dt>0</dt></span></span> </dl>                                                 | <span data-ttu-id="e165b-116">Déclenche la tâche lorsqu’un événement spécifique se produit.</span><span class="sxs-lookup"><span data-stu-id="e165b-116">Triggers the task when a specific event occurs.</span></span><br/>                                                                                                               |
| <span id="TASK_TRIGGER_TIME"></span><span id="task_trigger_time"></span><dl> <span data-ttu-id="e165b-117"><dt>**Tâche \_ \_Heure du déclencheur**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="e165b-117"><dt>**TASK\_TRIGGER\_TIME**</dt> <dt>1</dt></span></span> </dl>                                                    | <span data-ttu-id="e165b-118">Déclenche la tâche à une heure spécifique de la journée.</span><span class="sxs-lookup"><span data-stu-id="e165b-118">Triggers the task at a specific time of day.</span></span><br/>                                                                                                                  |
| <span id="TASK_TRIGGER_DAILY"></span><span id="task_trigger_daily"></span><dl> <span data-ttu-id="e165b-119"><dt>**Tâche \_ DÉCLENCHEur \_ quotidien**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="e165b-119"><dt>**TASK\_TRIGGER\_DAILY**</dt> <dt>2</dt></span></span> </dl>                                                 | <span data-ttu-id="e165b-120">Déclenche la tâche selon une planification quotidienne.</span><span class="sxs-lookup"><span data-stu-id="e165b-120">Triggers the task on a daily schedule.</span></span> <span data-ttu-id="e165b-121">Par exemple, la tâche commence à une heure spécifique tous les jours, tous les jours, tous les trois jours, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="e165b-121">For example, the task starts at a specific time every day, every-other day, every third day, and so on.</span></span><br/>                |
| <span id="TASK_TRIGGER_WEEKLY"></span><span id="task_trigger_weekly"></span><dl> <span data-ttu-id="e165b-122"><dt>**Tâche \_ DÉCLENCHEur \_ hebdomadaire**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="e165b-122"><dt>**TASK\_TRIGGER\_WEEKLY**</dt> <dt>3</dt></span></span> </dl>                                              | <span data-ttu-id="e165b-123">Déclenche la tâche selon une planification hebdomadaire.</span><span class="sxs-lookup"><span data-stu-id="e165b-123">Triggers the task on a weekly schedule.</span></span> <span data-ttu-id="e165b-124">Par exemple, la tâche commence à 8:00 AM pour un jour spécifique chaque semaine ou une autre semaine.</span><span class="sxs-lookup"><span data-stu-id="e165b-124">For example, the task starts at 8:00 AM on a specific day every week or other week.</span></span><br/>                                   |
| <span id="TASK_TRIGGER_MONTHLY"></span><span id="task_trigger_monthly"></span><dl> <span data-ttu-id="e165b-125"><dt>**Tâche \_ DÉCLENCHEur \_ mensuel**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="e165b-125"><dt>**TASK\_TRIGGER\_MONTHLY**</dt> <dt>4</dt></span></span> </dl>                                           | <span data-ttu-id="e165b-126">Déclenche la tâche selon une planification mensuelle.</span><span class="sxs-lookup"><span data-stu-id="e165b-126">Triggers the task on a monthly schedule.</span></span> <span data-ttu-id="e165b-127">Par exemple, la tâche démarre sur des jours spécifiques de mois spécifiques.</span><span class="sxs-lookup"><span data-stu-id="e165b-127">For example, the task starts on specific days of specific months.</span></span><br/>                                                    |
| <span id="TASK_TRIGGER_MONTHLYDOW"></span><span id="task_trigger_monthlydow"></span><dl> <span data-ttu-id="e165b-128"><dt>**Tâche \_ DÉCLENCHEur \_ MONTHLYDOW**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="e165b-128"><dt>**TASK\_TRIGGER\_MONTHLYDOW**</dt> <dt>5</dt></span></span> </dl>                                  | <span data-ttu-id="e165b-129">Déclenche la tâche selon une planification mensuelle de jour de semaine.</span><span class="sxs-lookup"><span data-stu-id="e165b-129">Triggers the task on a monthly day-of-week schedule.</span></span> <span data-ttu-id="e165b-130">Par exemple, la tâche démarre à des jours spécifiques de la semaine, des semaines du mois et des mois de l’année.</span><span class="sxs-lookup"><span data-stu-id="e165b-130">For example, the task starts on a specific days of the week, weeks of the month, and months of the year.</span></span><br/> |
| <span id="TASK_TRIGGER_IDLE"></span><span id="task_trigger_idle"></span><dl> <span data-ttu-id="e165b-131"><dt>**Tâche \_ DÉCLENCHEur \_ inactif**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="e165b-131"><dt>**TASK\_TRIGGER\_IDLE**</dt> <dt>6</dt></span></span> </dl>                                                    | <span data-ttu-id="e165b-132">Déclenche la tâche lorsque l’ordinateur passe en état d’inactivité.</span><span class="sxs-lookup"><span data-stu-id="e165b-132">Triggers the task when the computer goes into an idle state.</span></span><br/>                                                                                                  |
| <span id="TASK_TRIGGER_REGISTRATION"></span><span id="task_trigger_registration"></span><dl> <span data-ttu-id="e165b-133"><dt>**Tâche \_ \_Inscription du déclencheur**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="e165b-133"><dt>**TASK\_TRIGGER\_REGISTRATION**</dt> <dt>7</dt></span></span> </dl>                            | <span data-ttu-id="e165b-134">Déclenche la tâche lorsque la tâche est inscrite.</span><span class="sxs-lookup"><span data-stu-id="e165b-134">Triggers the task when the task is registered.</span></span><br/>                                                                                                                |
| <span id="TASK_TRIGGER_BOOT"></span><span id="task_trigger_boot"></span><dl> <span data-ttu-id="e165b-135"><dt>**Tâche \_ DÉCLENCHER le \_ démarrage**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="e165b-135"><dt>**TASK\_TRIGGER\_BOOT**</dt> <dt>8</dt></span></span> </dl>                                                    | <span data-ttu-id="e165b-136">Déclenche la tâche au démarrage de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="e165b-136">Triggers the task when the computer boots.</span></span><br/>                                                                                                                    |
| <span id="TASK_TRIGGER_LOGON"></span><span id="task_trigger_logon"></span><dl> <span data-ttu-id="e165b-137"><dt>**Tâche \_ DÉCLENCHER l' \_ ouverture de session**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="e165b-137"><dt>**TASK\_TRIGGER\_LOGON**</dt> <dt>9</dt></span></span> </dl>                                                 | <span data-ttu-id="e165b-138">Déclenche la tâche lorsqu’un utilisateur spécifique ouvre une session.</span><span class="sxs-lookup"><span data-stu-id="e165b-138">Triggers the task when a specific user logs on.</span></span><br/>                                                                                                               |
| <span id="TASK_TRIGGER_SESSION_STATE_CHANGE"></span><span id="task_trigger_session_state_change"></span><dl> <span data-ttu-id="e165b-139"><dt>**Tâche \_ \_Changement d' \_ état \_ de session du déclencheur**</dt> <dt>11</dt></span><span class="sxs-lookup"><span data-stu-id="e165b-139"><dt>**TASK\_TRIGGER\_SESSION\_STATE\_CHANGE**</dt> <dt>11</dt></span></span> </dl> | <span data-ttu-id="e165b-140">Déclenche la tâche lorsqu’un état de session spécifique change.</span><span class="sxs-lookup"><span data-stu-id="e165b-140">Triggers the task when a specific session state changes.</span></span><br/>                                                                                                      |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e165b-141">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e165b-141">Return value</span></span>

<span data-ttu-id="e165b-142">Objet de [**déclencheur**](trigger.md) qui représente le nouveau déclencheur.</span><span class="sxs-lookup"><span data-stu-id="e165b-142">A [**Trigger**](trigger.md) object that represents the new trigger.</span></span>

## <a name="remarks"></a><span data-ttu-id="e165b-143">Notes</span><span class="sxs-lookup"><span data-stu-id="e165b-143">Remarks</span></span>

<span data-ttu-id="e165b-144">Pour plus d’informations sur chaque type de déclencheur, consultez [types de déclencheurs](trigger-types.md).</span><span class="sxs-lookup"><span data-stu-id="e165b-144">For information about each trigger type see [Trigger Types](trigger-types.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e165b-145">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e165b-145">Requirements</span></span>



| <span data-ttu-id="e165b-146">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e165b-146">Requirement</span></span> | <span data-ttu-id="e165b-147">Valeur</span><span class="sxs-lookup"><span data-stu-id="e165b-147">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e165b-148">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e165b-148">Minimum supported client</span></span><br/> | <span data-ttu-id="e165b-149">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e165b-149">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="e165b-150">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e165b-150">Minimum supported server</span></span><br/> | <span data-ttu-id="e165b-151">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e165b-151">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="e165b-152">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="e165b-152">Type library</span></span><br/>             | <dl> <span data-ttu-id="e165b-153"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="e165b-153"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="e165b-154">DLL</span><span class="sxs-lookup"><span data-stu-id="e165b-154">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e165b-155"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e165b-155"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e165b-156">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e165b-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e165b-157">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="e165b-157">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="e165b-158">**Stead**</span><span class="sxs-lookup"><span data-stu-id="e165b-158">**Trigger**</span></span>](trigger.md)
</dt> </dl>

 

 





