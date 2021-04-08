---
title: Objet WeeklyTrigger
description: Objet de script qui représente un déclencheur qui démarre une tâche basée sur une planification hebdomadaire.
ms.assetid: a000d7a8-0239-440f-b49b-7f0c55b01e8e
keywords:
- déclencheur hebdomadaire Planificateur de tâches, objet
- Objet WeeklyTrigger Planificateur de tâches
- Planificateur de tâches d’objets WeeklyTrigger, Description
topic_type:
- apiref
api_name:
- WeeklyTrigger
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58dec9172d38b53f779f44a048b39bc709dbd54f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743852"
---
# <a name="weeklytrigger-object"></a><span data-ttu-id="2ecd6-106">Objet WeeklyTrigger</span><span class="sxs-lookup"><span data-stu-id="2ecd6-106">WeeklyTrigger object</span></span>

<span data-ttu-id="2ecd6-107">Objet de script qui représente un déclencheur qui démarre une tâche basée sur une planification hebdomadaire.</span><span class="sxs-lookup"><span data-stu-id="2ecd6-107">Scripting object that represents a trigger that starts a task based on a weekly schedule.</span></span> <span data-ttu-id="2ecd6-108">Par exemple, la tâche commence à 8:00 h 00.</span><span class="sxs-lookup"><span data-stu-id="2ecd6-108">For example, the task starts at 8:00 A.M.</span></span> <span data-ttu-id="2ecd6-109">à un jour spécifique de la semaine chaque semaine ou chaque semaine.</span><span class="sxs-lookup"><span data-stu-id="2ecd6-109">on a specific day of the week every week or every other week.</span></span>

## <a name="members"></a><span data-ttu-id="2ecd6-110">Membres</span><span class="sxs-lookup"><span data-stu-id="2ecd6-110">Members</span></span>

<span data-ttu-id="2ecd6-111">L’objet **WeeklyTrigger** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="2ecd6-111">The **WeeklyTrigger** object has these types of members:</span></span>

-   [<span data-ttu-id="2ecd6-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="2ecd6-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2ecd6-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="2ecd6-113">Properties</span></span>

<span data-ttu-id="2ecd6-114">L’objet **WeeklyTrigger** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="2ecd6-114">The **WeeklyTrigger** object has these properties.</span></span>



| <span data-ttu-id="2ecd6-115">Propriété</span><span class="sxs-lookup"><span data-stu-id="2ecd6-115">Property</span></span>                                                            | <span data-ttu-id="2ecd6-116">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="2ecd6-116">Access type</span></span>           | <span data-ttu-id="2ecd6-117">Description</span><span class="sxs-lookup"><span data-stu-id="2ecd6-117">Description</span></span>                                                                                                                                                                                 |
|:--------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2ecd6-118">**DaysOfWeek**</span><span class="sxs-lookup"><span data-stu-id="2ecd6-118">**DaysOfWeek**</span></span>](weeklytrigger-daysofweek.md)<br/>           | <span data-ttu-id="2ecd6-119">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="2ecd6-119">Read/write</span></span><br/> | <span data-ttu-id="2ecd6-120">Obtient ou définit les jours de la semaine où la tâche est exécutée.</span><span class="sxs-lookup"><span data-stu-id="2ecd6-120">Gets or sets the days of the week on which the task runs.</span></span><br/>                                                                                                                        |
| [<span data-ttu-id="2ecd6-121">**Enabled**</span><span class="sxs-lookup"><span data-stu-id="2ecd6-121">**Enabled**</span></span>](trigger-enabled.md)<br/>                       | <span data-ttu-id="2ecd6-122">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="2ecd6-122">Read/write</span></span><br/> | <span data-ttu-id="2ecd6-123">Héritée de l’objet [**déclencheur**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="2ecd6-123">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="2ecd6-124">Obtient ou définit une valeur booléenne qui indique si le déclencheur est activé.</span><span class="sxs-lookup"><span data-stu-id="2ecd6-124">Gets or sets a Boolean value that indicates whether the trigger is enabled.</span></span><br/>                                                |
| [<span data-ttu-id="2ecd6-125">**EndBoundary**</span><span class="sxs-lookup"><span data-stu-id="2ecd6-125">**EndBoundary**</span></span>](trigger-endboundary.md)<br/>               | <span data-ttu-id="2ecd6-126">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="2ecd6-126">Read/write</span></span><br/> | <span data-ttu-id="2ecd6-127">Héritée de l’objet [**déclencheur**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="2ecd6-127">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="2ecd6-128">Obtient ou définit la date et l’heure de désactivation du déclencheur.</span><span class="sxs-lookup"><span data-stu-id="2ecd6-128">Gets or sets the date and time when the trigger is deactivated.</span></span> <span data-ttu-id="2ecd6-129">Le déclencheur ne peut pas démarrer la tâche une fois qu’elle est désactivée.</span><span class="sxs-lookup"><span data-stu-id="2ecd6-129">The trigger cannot start the task after it is deactivated.</span></span><br/> |
| [<span data-ttu-id="2ecd6-130">**ExecutionTimeLimit**</span><span class="sxs-lookup"><span data-stu-id="2ecd6-130">**ExecutionTimeLimit**</span></span>](trigger-executiontimelimit.md)<br/> | <span data-ttu-id="2ecd6-131">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="2ecd6-131">Read/write</span></span><br/> | <span data-ttu-id="2ecd6-132">Héritée de l’objet [**déclencheur**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="2ecd6-132">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="2ecd6-133">Obtient ou définit la durée maximale pendant laquelle la tâche lancée par le déclencheur est autorisée à s’exécuter.</span><span class="sxs-lookup"><span data-stu-id="2ecd6-133">Gets or sets the maximum amount of time that the task launched by the trigger is allowed to run.</span></span><br/>                           |
| [<span data-ttu-id="2ecd6-134">**Identifi**</span><span class="sxs-lookup"><span data-stu-id="2ecd6-134">**Id**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_id)<br/>                                | <span data-ttu-id="2ecd6-135">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="2ecd6-135">Read/write</span></span><br/> | <span data-ttu-id="2ecd6-136">Héritée de l’objet [**déclencheur**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="2ecd6-136">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="2ecd6-137">Obtient ou définit l’identificateur pour le déclencheur.</span><span class="sxs-lookup"><span data-stu-id="2ecd6-137">Gets or sets the identifier for the trigger.</span></span><br/>                                                                               |
| [<span data-ttu-id="2ecd6-138">**RandomDelay**</span><span class="sxs-lookup"><span data-stu-id="2ecd6-138">**RandomDelay**</span></span>](weeklytrigger-randomdelay.md)<br/>         | <span data-ttu-id="2ecd6-139">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="2ecd6-139">Read/write</span></span><br/> | <span data-ttu-id="2ecd6-140">Obtient ou définit un délai qui est ajouté de manière aléatoire à l’heure de début du déclencheur.</span><span class="sxs-lookup"><span data-stu-id="2ecd6-140">Gets or sets a delay time that is randomly added to the start time of the trigger.</span></span><br/>                                                                                               |
| [<span data-ttu-id="2ecd6-141">**Répétition**</span><span class="sxs-lookup"><span data-stu-id="2ecd6-141">**Repetition**</span></span>](trigger-repetition.md)<br/>                 | <span data-ttu-id="2ecd6-142">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="2ecd6-142">Read/write</span></span><br/> | <span data-ttu-id="2ecd6-143">Héritée de l’objet [**déclencheur**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="2ecd6-143">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="2ecd6-144">Obtient ou définit la fréquence d’exécution de la tâche et la durée de répétition du modèle de répétition après le démarrage de la tâche.</span><span class="sxs-lookup"><span data-stu-id="2ecd6-144">Gets or sets how often the task is run and how long the repetition pattern is repeated after the task is started.</span></span><br/>          |
| [<span data-ttu-id="2ecd6-145">**StartBoundary**</span><span class="sxs-lookup"><span data-stu-id="2ecd6-145">**StartBoundary**</span></span>](trigger-startboundary.md)<br/>           | <span data-ttu-id="2ecd6-146">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="2ecd6-146">Read/write</span></span><br/> | <span data-ttu-id="2ecd6-147">Héritée de l’objet [**déclencheur**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="2ecd6-147">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="2ecd6-148">Obtient ou définit la date et l’heure d’activation du déclencheur.</span><span class="sxs-lookup"><span data-stu-id="2ecd6-148">Gets or sets the date and time when the trigger is activated.</span></span><br/>                                                              |
| [<span data-ttu-id="2ecd6-149">**Entrer**</span><span class="sxs-lookup"><span data-stu-id="2ecd6-149">**Type**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_type)<br/>                            | <span data-ttu-id="2ecd6-150">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2ecd6-150">Read-only</span></span><br/>  | <span data-ttu-id="2ecd6-151">Héritée de l’objet [**déclencheur**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="2ecd6-151">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="2ecd6-152">Obtient le type du déclencheur.</span><span class="sxs-lookup"><span data-stu-id="2ecd6-152">Gets the type of the trigger.</span></span><br/>                                                                                              |
| [<span data-ttu-id="2ecd6-153">**WeeksInterval**</span><span class="sxs-lookup"><span data-stu-id="2ecd6-153">**WeeksInterval**</span></span>](weeklytrigger-weeksinterval.md)<br/>     | <span data-ttu-id="2ecd6-154">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="2ecd6-154">Read/write</span></span><br/> | <span data-ttu-id="2ecd6-155">Obtient ou définit l’intervalle entre les semaines de la planification.</span><span class="sxs-lookup"><span data-stu-id="2ecd6-155">Gets or sets the interval between the weeks in the schedule.</span></span><br/>                                                                                                                     |



 

## <a name="remarks"></a><span data-ttu-id="2ecd6-156">Notes</span><span class="sxs-lookup"><span data-stu-id="2ecd6-156">Remarks</span></span>

<span data-ttu-id="2ecd6-157">L’heure de début de la tâche est définie par la propriété [**StartBoundary**](trigger-startboundary.md) .</span><span class="sxs-lookup"><span data-stu-id="2ecd6-157">The time of day that the task is started is set by the [**StartBoundary**](trigger-startboundary.md) property.</span></span>

<span data-ttu-id="2ecd6-158">Lors de la lecture ou de l’écriture de vos propres données XML pour une tâche, un déclencheur hebdomadaire est spécifié à l’aide de l’élément [**ScheduleByWeek**](taskschedulerschema-schedulebyweek-calendartriggertype-element.md) du schéma planificateur de tâches.</span><span class="sxs-lookup"><span data-stu-id="2ecd6-158">When reading or writing your own XML for a task, a weekly trigger is specified using the [**ScheduleByWeek**](taskschedulerschema-schedulebyweek-calendartriggertype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="examples"></a><span data-ttu-id="2ecd6-159">Exemples</span><span class="sxs-lookup"><span data-stu-id="2ecd6-159">Examples</span></span>

<span data-ttu-id="2ecd6-160">Pour plus d’informations et pour obtenir un exemple de code pour cet objet de script, consultez [exemple de déclencheur hebdomadaire (script)](weekly-trigger-example--scripting-.md).</span><span class="sxs-lookup"><span data-stu-id="2ecd6-160">For more information and a code example for this scripting object, see [Weekly Trigger Example (Scripting)](weekly-trigger-example--scripting-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2ecd6-161">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2ecd6-161">Requirements</span></span>



| <span data-ttu-id="2ecd6-162">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2ecd6-162">Requirement</span></span> | <span data-ttu-id="2ecd6-163">Valeur</span><span class="sxs-lookup"><span data-stu-id="2ecd6-163">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2ecd6-164">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2ecd6-164">Minimum supported client</span></span><br/> | <span data-ttu-id="2ecd6-165">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2ecd6-165">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="2ecd6-166">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2ecd6-166">Minimum supported server</span></span><br/> | <span data-ttu-id="2ecd6-167">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2ecd6-167">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="2ecd6-168">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="2ecd6-168">Type library</span></span><br/>             | <dl> <span data-ttu-id="2ecd6-169"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="2ecd6-169"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="2ecd6-170">DLL</span><span class="sxs-lookup"><span data-stu-id="2ecd6-170">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2ecd6-171"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2ecd6-171"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2ecd6-172">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2ecd6-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ecd6-173">**Stead**</span><span class="sxs-lookup"><span data-stu-id="2ecd6-173">**Trigger**</span></span>](trigger.md)
</dt> <dt>

[<span data-ttu-id="2ecd6-174">**TriggerCollection**</span><span class="sxs-lookup"><span data-stu-id="2ecd6-174">**TriggerCollection**</span></span>](triggercollection.md)
</dt> <dt>

[<span data-ttu-id="2ecd6-175">**TriggerCollection. Create**</span><span class="sxs-lookup"><span data-stu-id="2ecd6-175">**TriggerCollection.Create**</span></span>](triggercollection-create.md)
</dt> </dl>

 

 





