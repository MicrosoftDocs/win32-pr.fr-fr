---
title: Objet DailyTrigger
description: Objet de script qui représente un déclencheur qui démarre une tâche basée sur une planification quotidienne.
ms.assetid: f03f53a0-0060-4793-96c1-b47a96852579
keywords:
- Planificateur de tâches de déclencheur quotidien, objet
- Objet DailyTrigger Planificateur de tâches
- Planificateur de tâches d’objets DailyTrigger, Description
topic_type:
- apiref
api_name:
- DailyTrigger
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 22203ecf7a421f07ccb823745e6619e05f84f550
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464818"
---
# <a name="dailytrigger-object"></a><span data-ttu-id="9699b-106">Objet DailyTrigger</span><span class="sxs-lookup"><span data-stu-id="9699b-106">DailyTrigger object</span></span>

<span data-ttu-id="9699b-107">Objet de script qui représente un déclencheur qui démarre une tâche basée sur une planification quotidienne.</span><span class="sxs-lookup"><span data-stu-id="9699b-107">Scripting object that represents a trigger that starts a task based on a daily schedule.</span></span>

## <a name="members"></a><span data-ttu-id="9699b-108">Membres</span><span class="sxs-lookup"><span data-stu-id="9699b-108">Members</span></span>

<span data-ttu-id="9699b-109">L’objet **DailyTrigger** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="9699b-109">The **DailyTrigger** object has these types of members:</span></span>

-   [<span data-ttu-id="9699b-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="9699b-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9699b-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="9699b-111">Properties</span></span>

<span data-ttu-id="9699b-112">L’objet **DailyTrigger** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="9699b-112">The **DailyTrigger** object has these properties.</span></span>



| <span data-ttu-id="9699b-113">Propriété</span><span class="sxs-lookup"><span data-stu-id="9699b-113">Property</span></span>                                                            | <span data-ttu-id="9699b-114">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="9699b-114">Access type</span></span>           | <span data-ttu-id="9699b-115">Description</span><span class="sxs-lookup"><span data-stu-id="9699b-115">Description</span></span>                                                                                                                                                                                 |
|:--------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9699b-116">**DaysInterval**</span><span class="sxs-lookup"><span data-stu-id="9699b-116">**DaysInterval**</span></span>](dailytrigger-daysinterval.md)<br/>        | <span data-ttu-id="9699b-117">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="9699b-117">Read/write</span></span><br/> | <span data-ttu-id="9699b-118">Obtient ou définit l’intervalle entre les jours de la planification.</span><span class="sxs-lookup"><span data-stu-id="9699b-118">Gets or sets the interval between the days in the schedule.</span></span><br/>                                                                                                                      |
| [<span data-ttu-id="9699b-119">**Enabled**</span><span class="sxs-lookup"><span data-stu-id="9699b-119">**Enabled**</span></span>](trigger-enabled.md)<br/>                       | <span data-ttu-id="9699b-120">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="9699b-120">Read/write</span></span><br/> | <span data-ttu-id="9699b-121">Héritée de l’objet [**déclencheur**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="9699b-121">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="9699b-122">Obtient ou définit une valeur booléenne qui indique si le déclencheur est activé.</span><span class="sxs-lookup"><span data-stu-id="9699b-122">Gets or sets a Boolean value that indicates whether the trigger is enabled.</span></span><br/>                                                |
| [<span data-ttu-id="9699b-123">**EndBoundary**</span><span class="sxs-lookup"><span data-stu-id="9699b-123">**EndBoundary**</span></span>](trigger-endboundary.md)<br/>               | <span data-ttu-id="9699b-124">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="9699b-124">Read/write</span></span><br/> | <span data-ttu-id="9699b-125">Héritée de l’objet [**déclencheur**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="9699b-125">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="9699b-126">Obtient ou définit la date et l’heure de désactivation du déclencheur.</span><span class="sxs-lookup"><span data-stu-id="9699b-126">Gets or sets the date and time when the trigger is deactivated.</span></span> <span data-ttu-id="9699b-127">Le déclencheur ne peut pas démarrer la tâche une fois qu’elle est désactivée.</span><span class="sxs-lookup"><span data-stu-id="9699b-127">The trigger cannot start the task after it is deactivated.</span></span><br/> |
| [<span data-ttu-id="9699b-128">**ExecutionTimeLimit**</span><span class="sxs-lookup"><span data-stu-id="9699b-128">**ExecutionTimeLimit**</span></span>](trigger-executiontimelimit.md)<br/> | <span data-ttu-id="9699b-129">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="9699b-129">Read/write</span></span><br/> | <span data-ttu-id="9699b-130">Héritée de l’objet [**déclencheur**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="9699b-130">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="9699b-131">Obtient ou définit la durée maximale pendant laquelle la tâche lancée par le déclencheur est autorisée à s’exécuter.</span><span class="sxs-lookup"><span data-stu-id="9699b-131">Gets or sets the maximum amount of time that the task launched by the trigger is allowed to run.</span></span><br/>                           |
| [<span data-ttu-id="9699b-132">**Identifi**</span><span class="sxs-lookup"><span data-stu-id="9699b-132">**Id**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_id)<br/>                                | <span data-ttu-id="9699b-133">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="9699b-133">Read/write</span></span><br/> | <span data-ttu-id="9699b-134">Héritée de l’objet [**déclencheur**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="9699b-134">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="9699b-135">Obtient ou définit l’identificateur pour le déclencheur.</span><span class="sxs-lookup"><span data-stu-id="9699b-135">Gets or sets the identifier for the trigger.</span></span><br/>                                                                               |
| [<span data-ttu-id="9699b-136">**RandomDelay**</span><span class="sxs-lookup"><span data-stu-id="9699b-136">**RandomDelay**</span></span>](dailytrigger-randomdelay.md)<br/>          | <span data-ttu-id="9699b-137">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="9699b-137">Read/write</span></span><br/> | <span data-ttu-id="9699b-138">Obtient ou définit un délai qui est ajouté de manière aléatoire à l’heure de début du déclencheur.</span><span class="sxs-lookup"><span data-stu-id="9699b-138">Gets or sets a delay time that is randomly added to the start time of the trigger.</span></span><br/>                                                                                               |
| [<span data-ttu-id="9699b-139">**Répétition**</span><span class="sxs-lookup"><span data-stu-id="9699b-139">**Repetition**</span></span>](trigger-repetition.md)<br/>                 | <span data-ttu-id="9699b-140">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="9699b-140">Read/write</span></span><br/> | <span data-ttu-id="9699b-141">Héritée de l’objet [**déclencheur**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="9699b-141">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="9699b-142">Obtient ou définit la fréquence d’exécution de la tâche et la durée de répétition du modèle de répétition après le démarrage de la tâche.</span><span class="sxs-lookup"><span data-stu-id="9699b-142">Gets or sets how often the task is run and how long the repetition pattern is repeated after the task is started.</span></span><br/>          |
| [<span data-ttu-id="9699b-143">**StartBoundary**</span><span class="sxs-lookup"><span data-stu-id="9699b-143">**StartBoundary**</span></span>](trigger-startboundary.md)<br/>           | <span data-ttu-id="9699b-144">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="9699b-144">Read/write</span></span><br/> | <span data-ttu-id="9699b-145">Héritée de l’objet [**déclencheur**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="9699b-145">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="9699b-146">Obtient ou définit la date et l’heure d’activation du déclencheur.</span><span class="sxs-lookup"><span data-stu-id="9699b-146">Gets or sets the date and time when the trigger is activated.</span></span><br/>                                                              |
| [<span data-ttu-id="9699b-147">**Entrer**</span><span class="sxs-lookup"><span data-stu-id="9699b-147">**Type**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_type)<br/>                            | <span data-ttu-id="9699b-148">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9699b-148">Read-only</span></span><br/>  | <span data-ttu-id="9699b-149">Héritée de l’objet [**déclencheur**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="9699b-149">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="9699b-150">Obtient le type du déclencheur.</span><span class="sxs-lookup"><span data-stu-id="9699b-150">Gets the type of the trigger.</span></span><br/>                                                                                              |



 

## <a name="remarks"></a><span data-ttu-id="9699b-151">Notes</span><span class="sxs-lookup"><span data-stu-id="9699b-151">Remarks</span></span>

<span data-ttu-id="9699b-152">L’heure de début de la tâche est définie par la propriété [**StartBoundary**](trigger-startboundary.md) .</span><span class="sxs-lookup"><span data-stu-id="9699b-152">The time of day that the task is started is set by the [**StartBoundary**](trigger-startboundary.md) property.</span></span>

<span data-ttu-id="9699b-153">Un intervalle de 1 produit une planification quotidienne.</span><span class="sxs-lookup"><span data-stu-id="9699b-153">An interval of 1 produces a daily schedule.</span></span> <span data-ttu-id="9699b-154">Un intervalle de 2 produit une planification tous les jours, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="9699b-154">An interval of 2 produces an every other day schedule and so on.</span></span>

<span data-ttu-id="9699b-155">Lors de la lecture ou de l’écriture de vos propres données XML pour une tâche, un déclencheur quotidien est spécifié à l’aide de l’élément [**ScheduleByDay**](taskschedulerschema-schedulebyday-calendartriggertype-element.md) du schéma planificateur de tâches.</span><span class="sxs-lookup"><span data-stu-id="9699b-155">When reading or writing your own XML for a task, a daily trigger is specified using the [**ScheduleByDay**](taskschedulerschema-schedulebyday-calendartriggertype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="examples"></a><span data-ttu-id="9699b-156">Exemples</span><span class="sxs-lookup"><span data-stu-id="9699b-156">Examples</span></span>

<span data-ttu-id="9699b-157">Pour plus d’informations et pour obtenir un exemple de code pour cet objet de script, consultez [exemple de déclencheur quotidien (script)](daily-trigger-example--scripting-.md).</span><span class="sxs-lookup"><span data-stu-id="9699b-157">For more information and a code example for this scripting object, see [Daily Trigger Example (Scripting)](daily-trigger-example--scripting-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9699b-158">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9699b-158">Requirements</span></span>



| <span data-ttu-id="9699b-159">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9699b-159">Requirement</span></span> | <span data-ttu-id="9699b-160">Valeur</span><span class="sxs-lookup"><span data-stu-id="9699b-160">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9699b-161">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9699b-161">Minimum supported client</span></span><br/> | <span data-ttu-id="9699b-162">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9699b-162">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="9699b-163">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9699b-163">Minimum supported server</span></span><br/> | <span data-ttu-id="9699b-164">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9699b-164">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="9699b-165">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="9699b-165">Type library</span></span><br/>             | <dl> <span data-ttu-id="9699b-166"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="9699b-166"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="9699b-167">DLL</span><span class="sxs-lookup"><span data-stu-id="9699b-167">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9699b-168"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9699b-168"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9699b-169">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9699b-169">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9699b-170">**Stead**</span><span class="sxs-lookup"><span data-stu-id="9699b-170">**Trigger**</span></span>](trigger.md)
</dt> <dt>

[<span data-ttu-id="9699b-171">**TriggerCollection**</span><span class="sxs-lookup"><span data-stu-id="9699b-171">**TriggerCollection**</span></span>](triggercollection.md)
</dt> <dt>

[<span data-ttu-id="9699b-172">**TriggerCollection. Create**</span><span class="sxs-lookup"><span data-stu-id="9699b-172">**TriggerCollection.Create**</span></span>](triggercollection-create.md)
</dt> </dl>

 

 





