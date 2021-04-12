---
title: Objet MonthlyDOWTrigger
description: Objet de script qui représente un déclencheur qui démarre une tâche sur une planification mensuelle de jour de semaine.
ms.assetid: 18607189-295f-4f7d-bf72-f0ac8d5067cf
keywords:
- Planificateur de tâches du déclencheur DOW mensuel, objet
- Objet MonthlyDOWTrigger Planificateur de tâches
- Planificateur de tâches d’objets MonthlyDOWTrigger, Description
topic_type:
- apiref
api_name:
- MonthlyDOWTrigger
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b7e43925c6ebe27933a39fe5e25f37ffe6cf72e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032650"
---
# <a name="monthlydowtrigger-object"></a><span data-ttu-id="5137a-106">Objet MonthlyDOWTrigger</span><span class="sxs-lookup"><span data-stu-id="5137a-106">MonthlyDOWTrigger object</span></span>

<span data-ttu-id="5137a-107">Objet de script qui représente un déclencheur qui démarre une tâche sur une planification mensuelle de jour de semaine.</span><span class="sxs-lookup"><span data-stu-id="5137a-107">Scripting object that represents a trigger that starts a task on a monthly day-of-week schedule.</span></span> <span data-ttu-id="5137a-108">Par exemple, la tâche commence à chaque jeudi, du 1er mai au octobre.</span><span class="sxs-lookup"><span data-stu-id="5137a-108">For example, the task starts on every first Thursday, May through October.</span></span>

## <a name="members"></a><span data-ttu-id="5137a-109">Membres</span><span class="sxs-lookup"><span data-stu-id="5137a-109">Members</span></span>

<span data-ttu-id="5137a-110">L’objet **MonthlyDOWTrigger** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="5137a-110">The **MonthlyDOWTrigger** object has these types of members:</span></span>

-   [<span data-ttu-id="5137a-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="5137a-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5137a-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="5137a-112">Properties</span></span>

<span data-ttu-id="5137a-113">L’objet **MonthlyDOWTrigger** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="5137a-113">The **MonthlyDOWTrigger** object has these properties.</span></span>



| <span data-ttu-id="5137a-114">Propriété</span><span class="sxs-lookup"><span data-stu-id="5137a-114">Property</span></span>                                                                          | <span data-ttu-id="5137a-115">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="5137a-115">Access type</span></span>           | <span data-ttu-id="5137a-116">Description</span><span class="sxs-lookup"><span data-stu-id="5137a-116">Description</span></span>                                                                                                                                                                                 |
|:----------------------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5137a-117">**DaysOfWeek**</span><span class="sxs-lookup"><span data-stu-id="5137a-117">**DaysOfWeek**</span></span>](monthlydowtrigger-daysofweek.md)<br/>                     | <span data-ttu-id="5137a-118">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="5137a-118">Read/write</span></span><br/> | <span data-ttu-id="5137a-119">Obtient ou définit les jours de la semaine pendant lesquels la tâche est exécutée.</span><span class="sxs-lookup"><span data-stu-id="5137a-119">Gets or sets the days of the week during which the task runs.</span></span><br/>                                                                                                                    |
| [<span data-ttu-id="5137a-120">**Enabled**</span><span class="sxs-lookup"><span data-stu-id="5137a-120">**Enabled**</span></span>](trigger-enabled.md)<br/>                                     | <span data-ttu-id="5137a-121">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="5137a-121">Read/write</span></span><br/> | <span data-ttu-id="5137a-122">Héritée de l’objet [**déclencheur**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="5137a-122">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="5137a-123">Obtient ou définit une valeur booléenne qui indique si le déclencheur est activé.</span><span class="sxs-lookup"><span data-stu-id="5137a-123">Gets or sets a Boolean value that indicates whether the trigger is enabled.</span></span><br/>                                                |
| [<span data-ttu-id="5137a-124">EndBoundary</span><span class="sxs-lookup"><span data-stu-id="5137a-124">EndBoundary</span></span>](trigger-endboundary.md)<br/>                                 | <span data-ttu-id="5137a-125">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="5137a-125">Read/write</span></span><br/> | <span data-ttu-id="5137a-126">Héritée de l’objet [**déclencheur**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="5137a-126">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="5137a-127">Obtient ou définit la date et l’heure de désactivation du déclencheur.</span><span class="sxs-lookup"><span data-stu-id="5137a-127">Gets or sets the date and time when the trigger is deactivated.</span></span> <span data-ttu-id="5137a-128">Le déclencheur ne peut pas démarrer la tâche une fois qu’elle est désactivée.</span><span class="sxs-lookup"><span data-stu-id="5137a-128">The trigger cannot start the task after it is deactivated.</span></span><br/> |
| [<span data-ttu-id="5137a-129">**ExecutionTimeLimit**</span><span class="sxs-lookup"><span data-stu-id="5137a-129">**ExecutionTimeLimit**</span></span>](trigger-executiontimelimit.md)<br/>               | <span data-ttu-id="5137a-130">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="5137a-130">Read/write</span></span><br/> | <span data-ttu-id="5137a-131">Héritée de l’objet [**déclencheur**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="5137a-131">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="5137a-132">Obtient ou définit la durée maximale pendant laquelle la tâche lancée par ce déclencheur est autorisée à s’exécuter.</span><span class="sxs-lookup"><span data-stu-id="5137a-132">Gets or sets the maximum amount of time that the task launched by this trigger is allowed to run.</span></span><br/>                          |
| [<span data-ttu-id="5137a-133">**Identifi**</span><span class="sxs-lookup"><span data-stu-id="5137a-133">**Id**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_id)<br/>                                              | <span data-ttu-id="5137a-134">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="5137a-134">Read/write</span></span><br/> | <span data-ttu-id="5137a-135">Héritée de l’objet [**déclencheur**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="5137a-135">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="5137a-136">Obtient ou définit l’identificateur pour le déclencheur.</span><span class="sxs-lookup"><span data-stu-id="5137a-136">Gets or sets the identifier for the trigger.</span></span><br/>                                                                               |
| [<span data-ttu-id="5137a-137">**MonthsOfYear**</span><span class="sxs-lookup"><span data-stu-id="5137a-137">**MonthsOfYear**</span></span>](monthlydowtrigger-monthsofyear.md)<br/>                 | <span data-ttu-id="5137a-138">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="5137a-138">Read/write</span></span><br/> | <span data-ttu-id="5137a-139">Obtient ou définit les mois de l’année pendant laquelle la tâche s’exécute.</span><span class="sxs-lookup"><span data-stu-id="5137a-139">Gets or sets the months of the year during which the task runs.</span></span><br/>                                                                                                                  |
| [<span data-ttu-id="5137a-140">**RandomDelay**</span><span class="sxs-lookup"><span data-stu-id="5137a-140">**RandomDelay**</span></span>](monthlydowtrigger-randomdelay.md)<br/>                   | <span data-ttu-id="5137a-141">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="5137a-141">Read/write</span></span><br/> | <span data-ttu-id="5137a-142">Obtient ou définit un délai qui est ajouté de manière aléatoire à l’heure de début du déclencheur.</span><span class="sxs-lookup"><span data-stu-id="5137a-142">Gets or sets a delay time that is randomly added to the start time of the trigger.</span></span><br/>                                                                                               |
| [<span data-ttu-id="5137a-143">**Répétition**</span><span class="sxs-lookup"><span data-stu-id="5137a-143">**Repetition**</span></span>](trigger-repetition.md)<br/>                               | <span data-ttu-id="5137a-144">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="5137a-144">Read/write</span></span><br/> | <span data-ttu-id="5137a-145">Héritée de l’objet [**déclencheur**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="5137a-145">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="5137a-146">Obtient ou définit la fréquence d’exécution de la tâche et la durée de répétition du modèle de répétition après le démarrage de la tâche.</span><span class="sxs-lookup"><span data-stu-id="5137a-146">Gets or sets how often the task is run and how long the repetition pattern is repeated after the task is started.</span></span><br/>          |
| [<span data-ttu-id="5137a-147">**RunOnLastWeekOfMonth**</span><span class="sxs-lookup"><span data-stu-id="5137a-147">**RunOnLastWeekOfMonth**</span></span>](monthlydowtrigger-runonlastweekofmonth.md)<br/> | <span data-ttu-id="5137a-148">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="5137a-148">Read/write</span></span><br/> | <span data-ttu-id="5137a-149">Obtient ou définit une valeur booléenne qui indique que la tâche s’exécute à la dernière semaine du mois.</span><span class="sxs-lookup"><span data-stu-id="5137a-149">Gets or sets a Boolean value that indicates that the task runs on the last week of the month.</span></span><br/>                                                                                    |
| [<span data-ttu-id="5137a-150">**StartBoundary**</span><span class="sxs-lookup"><span data-stu-id="5137a-150">**StartBoundary**</span></span>](trigger-startboundary.md)<br/>                         | <span data-ttu-id="5137a-151">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="5137a-151">Read/write</span></span><br/> | <span data-ttu-id="5137a-152">Héritée de l’objet [**déclencheur**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="5137a-152">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="5137a-153">Obtient ou définit la date et l’heure d’activation du déclencheur.</span><span class="sxs-lookup"><span data-stu-id="5137a-153">Gets or sets the date and time when the trigger is activated.</span></span><br/>                                                              |
| [<span data-ttu-id="5137a-154">**Entrer**</span><span class="sxs-lookup"><span data-stu-id="5137a-154">**Type**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_type)<br/>                                          | <span data-ttu-id="5137a-155">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5137a-155">Read-only</span></span><br/>  | <span data-ttu-id="5137a-156">Héritée de l’objet [**déclencheur**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="5137a-156">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="5137a-157">Obtient le type du déclencheur.</span><span class="sxs-lookup"><span data-stu-id="5137a-157">Gets the type of the trigger.</span></span><br/>                                                                                              |
| [<span data-ttu-id="5137a-158">**WeeksOfMonth**</span><span class="sxs-lookup"><span data-stu-id="5137a-158">**WeeksOfMonth**</span></span>](monthlydowtrigger-weeksofmonth.md)<br/>                 | <span data-ttu-id="5137a-159">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="5137a-159">Read/write</span></span><br/> | <span data-ttu-id="5137a-160">Obtient ou définit les semaines du mois pendant lequel la tâche s’exécute.</span><span class="sxs-lookup"><span data-stu-id="5137a-160">Gets or sets the weeks of the month during which the task runs.</span></span><br/>                                                                                                                  |



 

## <a name="remarks"></a><span data-ttu-id="5137a-161">Notes</span><span class="sxs-lookup"><span data-stu-id="5137a-161">Remarks</span></span>

<span data-ttu-id="5137a-162">L’heure de début de la tâche est définie par la propriété [**StartBoundary**](trigger-startboundary.md) .</span><span class="sxs-lookup"><span data-stu-id="5137a-162">The time of day that the task is started is set by the [**StartBoundary**](trigger-startboundary.md) property.</span></span>

<span data-ttu-id="5137a-163">Lors de la lecture ou de l’écriture de données XML pour une tâche, un déclencheur de jour de semaine mensuel est spécifié à l’aide de l’élément [**ScheduleByMonthDayOfWeek**](taskschedulerschema-schedulebymonthdayofweek-calendartriggertype-element.md) du schéma planificateur de tâches.</span><span class="sxs-lookup"><span data-stu-id="5137a-163">When reading or writing XML for a task, a monthly day-of-week trigger is specified using the [**ScheduleByMonthDayOfWeek**](taskschedulerschema-schedulebymonthdayofweek-calendartriggertype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="5137a-164">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5137a-164">Requirements</span></span>



| <span data-ttu-id="5137a-165">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5137a-165">Requirement</span></span> | <span data-ttu-id="5137a-166">Valeur</span><span class="sxs-lookup"><span data-stu-id="5137a-166">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5137a-167">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5137a-167">Minimum supported client</span></span><br/> | <span data-ttu-id="5137a-168">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5137a-168">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="5137a-169">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5137a-169">Minimum supported server</span></span><br/> | <span data-ttu-id="5137a-170">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5137a-170">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="5137a-171">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="5137a-171">Type library</span></span><br/>             | <dl> <span data-ttu-id="5137a-172"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="5137a-172"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="5137a-173">DLL</span><span class="sxs-lookup"><span data-stu-id="5137a-173">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5137a-174"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5137a-174"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5137a-175">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5137a-175">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5137a-176">**Stead**</span><span class="sxs-lookup"><span data-stu-id="5137a-176">**Trigger**</span></span>](trigger.md)
</dt> <dt>

[<span data-ttu-id="5137a-177">Objets Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="5137a-177">Task Scheduler Objects</span></span>](task-scheduler-objects.md)
</dt> <dt>

[<span data-ttu-id="5137a-178">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="5137a-178">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="5137a-179">**TriggerCollection**</span><span class="sxs-lookup"><span data-stu-id="5137a-179">**TriggerCollection**</span></span>](triggercollection.md)
</dt> <dt>

[<span data-ttu-id="5137a-180">**TriggerCollection. Create**</span><span class="sxs-lookup"><span data-stu-id="5137a-180">**TriggerCollection.Create**</span></span>](triggercollection-create.md)
</dt> </dl>

 

 





