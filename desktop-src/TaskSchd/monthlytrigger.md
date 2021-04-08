---
title: Objet MonthlyTrigger
description: Objet de script qui représente un déclencheur qui démarre une tâche basée sur une planification mensuelle.
ms.assetid: d73715cb-a52e-4daf-930f-e94fbe28881e
keywords:
- Planificateur de tâches de déclencheur mensuel, objet
- Objet MonthlyTrigger Planificateur de tâches
- Planificateur de tâches d’objets MonthlyTrigger, Description
topic_type:
- apiref
api_name:
- MonthlyTrigger
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce433f626fbe45e209f881c00787495cc6343bc1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741884"
---
# <a name="monthlytrigger-object"></a><span data-ttu-id="93516-106">Objet MonthlyTrigger</span><span class="sxs-lookup"><span data-stu-id="93516-106">MonthlyTrigger object</span></span>

<span data-ttu-id="93516-107">Objet de script qui représente un déclencheur qui démarre une tâche basée sur une planification mensuelle.</span><span class="sxs-lookup"><span data-stu-id="93516-107">Scripting object that represents a trigger that starts a task based on a monthly schedule.</span></span> <span data-ttu-id="93516-108">Par exemple, la tâche démarre sur des jours spécifiques de mois spécifiques.</span><span class="sxs-lookup"><span data-stu-id="93516-108">For example, the task starts on specific days of specific months.</span></span>

## <a name="members"></a><span data-ttu-id="93516-109">Membres</span><span class="sxs-lookup"><span data-stu-id="93516-109">Members</span></span>

<span data-ttu-id="93516-110">L’objet **MonthlyTrigger** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="93516-110">The **MonthlyTrigger** object has these types of members:</span></span>

-   [<span data-ttu-id="93516-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="93516-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="93516-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="93516-112">Properties</span></span>

<span data-ttu-id="93516-113">L’objet **MonthlyTrigger** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="93516-113">The **MonthlyTrigger** object has these properties.</span></span>



| <span data-ttu-id="93516-114">Propriété</span><span class="sxs-lookup"><span data-stu-id="93516-114">Property</span></span>                                                                     | <span data-ttu-id="93516-115">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="93516-115">Access type</span></span>           | <span data-ttu-id="93516-116">Description</span><span class="sxs-lookup"><span data-stu-id="93516-116">Description</span></span>                                                                                                                                                                                 |
|:-----------------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="93516-117">**DaysOfMonth**</span><span class="sxs-lookup"><span data-stu-id="93516-117">**DaysOfMonth**</span></span>](monthlytrigger-daysofmonth.md)<br/>                 | <span data-ttu-id="93516-118">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="93516-118">Read/write</span></span><br/> | <span data-ttu-id="93516-119">Obtient ou définit les jours du mois pendant lesquels la tâche s’exécute.</span><span class="sxs-lookup"><span data-stu-id="93516-119">Gets or sets the days of the month during which the task runs.</span></span><br/>                                                                                                                   |
| [<span data-ttu-id="93516-120">**Enabled**</span><span class="sxs-lookup"><span data-stu-id="93516-120">**Enabled**</span></span>](trigger-enabled.md)<br/>                                | <span data-ttu-id="93516-121">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="93516-121">Read/write</span></span><br/> | <span data-ttu-id="93516-122">Héritée de l’objet [**déclencheur**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="93516-122">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="93516-123">Obtient ou définit une valeur booléenne qui indique si le déclencheur est activé.</span><span class="sxs-lookup"><span data-stu-id="93516-123">Gets or sets a Boolean value that indicates whether the trigger is enabled.</span></span><br/>                                                |
| [<span data-ttu-id="93516-124">EndBoundary</span><span class="sxs-lookup"><span data-stu-id="93516-124">EndBoundary</span></span>](trigger-endboundary.md)<br/>                            | <span data-ttu-id="93516-125">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="93516-125">Read/write</span></span><br/> | <span data-ttu-id="93516-126">Héritée de l’objet [**déclencheur**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="93516-126">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="93516-127">Obtient ou définit la date et l’heure de désactivation du déclencheur.</span><span class="sxs-lookup"><span data-stu-id="93516-127">Gets or sets the date and time when the trigger is deactivated.</span></span> <span data-ttu-id="93516-128">Le déclencheur ne peut pas démarrer la tâche une fois qu’elle est désactivée.</span><span class="sxs-lookup"><span data-stu-id="93516-128">The trigger cannot start the task after it is deactivated.</span></span><br/> |
| [<span data-ttu-id="93516-129">**ExecutionTimeLimit**</span><span class="sxs-lookup"><span data-stu-id="93516-129">**ExecutionTimeLimit**</span></span>](trigger-executiontimelimit.md)<br/>          | <span data-ttu-id="93516-130">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="93516-130">Read/write</span></span><br/> | <span data-ttu-id="93516-131">Héritée de l’objet [**déclencheur**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="93516-131">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="93516-132">Obtient ou définit la durée maximale pendant laquelle la tâche lancée par le déclencheur est autorisée à s’exécuter.</span><span class="sxs-lookup"><span data-stu-id="93516-132">Gets or sets the maximum amount of time that the task launched by the trigger is allowed to run.</span></span><br/>                           |
| [<span data-ttu-id="93516-133">**Identifi**</span><span class="sxs-lookup"><span data-stu-id="93516-133">**Id**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_id)<br/>                                         | <span data-ttu-id="93516-134">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="93516-134">Read/write</span></span><br/> | <span data-ttu-id="93516-135">Héritée de l’objet [**déclencheur**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="93516-135">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="93516-136">Obtient ou définit l’identificateur pour le déclencheur.</span><span class="sxs-lookup"><span data-stu-id="93516-136">Gets or sets the identifier for the trigger.</span></span><br/>                                                                               |
| [<span data-ttu-id="93516-137">**MonthsOfYear**</span><span class="sxs-lookup"><span data-stu-id="93516-137">**MonthsOfYear**</span></span>](monthlytrigger-monthsofyear.md)<br/>               | <span data-ttu-id="93516-138">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="93516-138">Read/write</span></span><br/> | <span data-ttu-id="93516-139">Obtient ou définit les mois de l’année pendant laquelle la tâche s’exécute.</span><span class="sxs-lookup"><span data-stu-id="93516-139">Gets or sets the months of the year during which the task runs.</span></span><br/>                                                                                                                  |
| [<span data-ttu-id="93516-140">**RandomDelay**</span><span class="sxs-lookup"><span data-stu-id="93516-140">**RandomDelay**</span></span>](monthlytrigger-randomdelay.md)<br/>                 | <span data-ttu-id="93516-141">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="93516-141">Read/write</span></span><br/> | <span data-ttu-id="93516-142">Obtient ou définit un délai qui est ajouté de manière aléatoire à l’heure de début du déclencheur.</span><span class="sxs-lookup"><span data-stu-id="93516-142">Gets or sets a delay time that is randomly added to the start time of the trigger.</span></span><br/>                                                                                               |
| [<span data-ttu-id="93516-143">**Répétition**</span><span class="sxs-lookup"><span data-stu-id="93516-143">**Repetition**</span></span>](trigger-repetition.md)<br/>                          | <span data-ttu-id="93516-144">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="93516-144">Read/write</span></span><br/> | <span data-ttu-id="93516-145">Héritée de l’objet [**déclencheur**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="93516-145">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="93516-146">Obtient ou définit la fréquence d’exécution de la tâche et la durée de répétition du modèle de répétition après le démarrage de la tâche.</span><span class="sxs-lookup"><span data-stu-id="93516-146">Gets or sets how often the task is run and how long the repetition pattern is repeated after the task is started.</span></span><br/>          |
| [<span data-ttu-id="93516-147">**RunOnLastDayOfMonth**</span><span class="sxs-lookup"><span data-stu-id="93516-147">**RunOnLastDayOfMonth**</span></span>](monthlytrigger-runonlastdayofmonth.md)<br/> | <span data-ttu-id="93516-148">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="93516-148">Read/write</span></span><br/> | <span data-ttu-id="93516-149">Obtient ou définit une valeur booléenne qui indique que la tâche s’exécute le dernier jour du mois.</span><span class="sxs-lookup"><span data-stu-id="93516-149">Gets or sets a Boolean value that indicates that the task runs on the last day of the month.</span></span><br/>                                                                                     |
| [<span data-ttu-id="93516-150">**StartBoundary**</span><span class="sxs-lookup"><span data-stu-id="93516-150">**StartBoundary**</span></span>](trigger-startboundary.md)<br/>                    | <span data-ttu-id="93516-151">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="93516-151">Read/write</span></span><br/> | <span data-ttu-id="93516-152">Héritée de l’objet [**déclencheur**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="93516-152">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="93516-153">Obtient ou définit la date et l’heure d’activation du déclencheur.</span><span class="sxs-lookup"><span data-stu-id="93516-153">Gets or sets the date and time when the trigger is activated.</span></span><br/>                                                              |
| [<span data-ttu-id="93516-154">**Entrer**</span><span class="sxs-lookup"><span data-stu-id="93516-154">**Type**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_type)<br/>                                     | <span data-ttu-id="93516-155">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="93516-155">Read-only</span></span><br/>  | <span data-ttu-id="93516-156">Héritée de l’objet [**déclencheur**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="93516-156">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="93516-157">Obtient le type du déclencheur.</span><span class="sxs-lookup"><span data-stu-id="93516-157">Gets the type of the trigger.</span></span><br/>                                                                                              |



 

## <a name="remarks"></a><span data-ttu-id="93516-158">Notes</span><span class="sxs-lookup"><span data-stu-id="93516-158">Remarks</span></span>

<span data-ttu-id="93516-159">L’heure de début de la tâche est définie par la propriété [**StartBoundary**](trigger-startboundary.md) .</span><span class="sxs-lookup"><span data-stu-id="93516-159">The time of day that the task is started is set by the [**StartBoundary**](trigger-startboundary.md) property.</span></span>

<span data-ttu-id="93516-160">Lors de la lecture ou de l’écriture de votre propre XML pour une tâche, un déclencheur mensuel est spécifié à l’aide de l’élément [**ScheduleByMonth**](taskschedulerschema-schedulebymonth-calendartriggertype-element.md) du schéma planificateur de tâches.</span><span class="sxs-lookup"><span data-stu-id="93516-160">When reading or writing your own XML for a task, a monthly trigger is specified using the [**ScheduleByMonth**](taskschedulerschema-schedulebymonth-calendartriggertype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="93516-161">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="93516-161">Requirements</span></span>



| <span data-ttu-id="93516-162">Condition requise</span><span class="sxs-lookup"><span data-stu-id="93516-162">Requirement</span></span> | <span data-ttu-id="93516-163">Valeur</span><span class="sxs-lookup"><span data-stu-id="93516-163">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="93516-164">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="93516-164">Minimum supported client</span></span><br/> | <span data-ttu-id="93516-165">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="93516-165">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="93516-166">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="93516-166">Minimum supported server</span></span><br/> | <span data-ttu-id="93516-167">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="93516-167">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="93516-168">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="93516-168">Type library</span></span><br/>             | <dl> <span data-ttu-id="93516-169"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="93516-169"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="93516-170">DLL</span><span class="sxs-lookup"><span data-stu-id="93516-170">DLL</span></span><br/>                      | <dl> <span data-ttu-id="93516-171"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="93516-171"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="93516-172">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="93516-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93516-173">**Stead**</span><span class="sxs-lookup"><span data-stu-id="93516-173">**Trigger**</span></span>](trigger.md)
</dt> <dt>

[<span data-ttu-id="93516-174">Objets Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="93516-174">Task Scheduler Objects</span></span>](task-scheduler-objects.md)
</dt> <dt>

[<span data-ttu-id="93516-175">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="93516-175">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="93516-176">**TriggerCollection**</span><span class="sxs-lookup"><span data-stu-id="93516-176">**TriggerCollection**</span></span>](triggercollection.md)
</dt> <dt>

[<span data-ttu-id="93516-177">**TriggerCollection. Create**</span><span class="sxs-lookup"><span data-stu-id="93516-177">**TriggerCollection.Create**</span></span>](triggercollection-create.md)
</dt> </dl>

 

 





