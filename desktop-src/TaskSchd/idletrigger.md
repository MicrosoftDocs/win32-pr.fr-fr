---
title: Objet IdleTrigger
description: Objet de script qui représente un déclencheur qui démarre une tâche lorsqu’une condition d’inactivité se produit.
ms.assetid: 627d83cf-27bd-47ce-a647-fa1e9af5263e
keywords:
- Planificateur de tâches de déclencheur inactif, objet
- Objet IdleTrigger Planificateur de tâches
- Planificateur de tâches d’objets IdleTrigger, Description
topic_type:
- apiref
api_name:
- IdleTrigger
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e72288827fec34257bf4f54a152031ef37068790
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106514255"
---
# <a name="idletrigger-object"></a><span data-ttu-id="0af10-106">Objet IdleTrigger</span><span class="sxs-lookup"><span data-stu-id="0af10-106">IdleTrigger object</span></span>

<span data-ttu-id="0af10-107">Objet de script qui représente un déclencheur qui démarre une tâche lorsqu’une condition d’inactivité se produit.</span><span class="sxs-lookup"><span data-stu-id="0af10-107">Scripting object that represents a trigger that starts a task when an idle condition occurs.</span></span> <span data-ttu-id="0af10-108">Pour plus d’informations sur les conditions d’inactivité, consultez conditions d’inactivité de la [tâche](task-idle-conditions.md).</span><span class="sxs-lookup"><span data-stu-id="0af10-108">For information about idle conditions, see [Task Idle Conditions](task-idle-conditions.md).</span></span>

## <a name="members"></a><span data-ttu-id="0af10-109">Membres</span><span class="sxs-lookup"><span data-stu-id="0af10-109">Members</span></span>

<span data-ttu-id="0af10-110">L’objet **IdleTrigger** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="0af10-110">The **IdleTrigger** object has these types of members:</span></span>

-   [<span data-ttu-id="0af10-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="0af10-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0af10-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="0af10-112">Properties</span></span>

<span data-ttu-id="0af10-113">L’objet **IdleTrigger** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="0af10-113">The **IdleTrigger** object has these properties.</span></span>



| <span data-ttu-id="0af10-114">Propriété</span><span class="sxs-lookup"><span data-stu-id="0af10-114">Property</span></span>                                                            | <span data-ttu-id="0af10-115">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="0af10-115">Access type</span></span>           | <span data-ttu-id="0af10-116">Description</span><span class="sxs-lookup"><span data-stu-id="0af10-116">Description</span></span>                                                                                                                                                                                               |
|:--------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0af10-117">**activé**</span><span class="sxs-lookup"><span data-stu-id="0af10-117">**Enabled**</span></span>](trigger-enabled.md)<br/>                       | <span data-ttu-id="0af10-118">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0af10-118">Read/write</span></span><br/> | <span data-ttu-id="0af10-119">Héritée de l’objet [**déclencheur**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="0af10-119">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="0af10-120">Obtient ou définit une valeur booléenne qui indique si le déclencheur est activé.</span><span class="sxs-lookup"><span data-stu-id="0af10-120">Gets or sets a Boolean value that indicates whether the trigger is enabled.</span></span><br/>                                                              |
| [<span data-ttu-id="0af10-121">EndBoundary</span><span class="sxs-lookup"><span data-stu-id="0af10-121">EndBoundary</span></span>](trigger-endboundary.md)<br/>                   | <span data-ttu-id="0af10-122">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0af10-122">Read/write</span></span><br/> | <span data-ttu-id="0af10-123">Héritée de l’objet [**déclencheur**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="0af10-123">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="0af10-124">Obtient ou définit la date et l’heure de désactivation du déclencheur.</span><span class="sxs-lookup"><span data-stu-id="0af10-124">Gets or sets the date and time when the trigger is deactivated.</span></span> <span data-ttu-id="0af10-125">Le déclencheur ne peut pas démarrer la tâche une fois qu’elle est désactivée.</span><span class="sxs-lookup"><span data-stu-id="0af10-125">The trigger cannot start the task after it is deactivated.</span></span><br/>               |
| [<span data-ttu-id="0af10-126">**ExecutionTimeLimit**</span><span class="sxs-lookup"><span data-stu-id="0af10-126">**ExecutionTimeLimit**</span></span>](trigger-executiontimelimit.md)<br/> | <span data-ttu-id="0af10-127">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0af10-127">Read/write</span></span><br/> | <span data-ttu-id="0af10-128">Héritée de l’objet [**déclencheur**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="0af10-128">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="0af10-129">Obtient ou définit la durée maximale pendant laquelle la tâche peut être démarrée par le déclencheur.</span><span class="sxs-lookup"><span data-stu-id="0af10-129">Gets or sets the maximum amount of time in which the task can be started by the trigger.</span></span><br/>                                                 |
| [<span data-ttu-id="0af10-130">**Identifi**</span><span class="sxs-lookup"><span data-stu-id="0af10-130">**Id**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_id)<br/>                                | <span data-ttu-id="0af10-131">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0af10-131">Read/write</span></span><br/> | <span data-ttu-id="0af10-132">Héritée de l’objet [**déclencheur**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="0af10-132">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="0af10-133">Obtient ou définit l’identificateur pour le déclencheur.</span><span class="sxs-lookup"><span data-stu-id="0af10-133">Gets or sets the identifier for the trigger.</span></span><br/>                                                                                             |
| [<span data-ttu-id="0af10-134">**Répétition**</span><span class="sxs-lookup"><span data-stu-id="0af10-134">**Repetition**</span></span>](trigger-repetition.md)<br/>                 | <span data-ttu-id="0af10-135">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0af10-135">Read/write</span></span><br/> | <span data-ttu-id="0af10-136">Héritée de l’objet [**déclencheur**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="0af10-136">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="0af10-137">Obtient ou définit une valeur qui indique la fréquence d’exécution de la tâche et la durée de répétition du modèle de répétition après le démarrage de la tâche.</span><span class="sxs-lookup"><span data-stu-id="0af10-137">Gets or sets a value that indicates how often the task is run and how long the repetition pattern is repeated after the task is started.</span></span><br/> |
| [<span data-ttu-id="0af10-138">**StartBoundary**</span><span class="sxs-lookup"><span data-stu-id="0af10-138">**StartBoundary**</span></span>](trigger-startboundary.md)<br/>           | <span data-ttu-id="0af10-139">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0af10-139">Read/write</span></span><br/> | <span data-ttu-id="0af10-140">Héritée de l’objet [**déclencheur**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="0af10-140">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="0af10-141">Obtient ou définit la date et l’heure d’activation du déclencheur.</span><span class="sxs-lookup"><span data-stu-id="0af10-141">Gets or sets the date and time when the trigger is activated.</span></span><br/>                                                                            |
| [<span data-ttu-id="0af10-142">**Entrer**</span><span class="sxs-lookup"><span data-stu-id="0af10-142">**Type**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_type)<br/>                            | <span data-ttu-id="0af10-143">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0af10-143">Read-only</span></span><br/>  | <span data-ttu-id="0af10-144">Héritée de l’objet [**déclencheur**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="0af10-144">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="0af10-145">Obtient le type du déclencheur.</span><span class="sxs-lookup"><span data-stu-id="0af10-145">Gets the type of the trigger.</span></span><br/>                                                                                                            |



 

## <a name="remarks"></a><span data-ttu-id="0af10-146">Notes</span><span class="sxs-lookup"><span data-stu-id="0af10-146">Remarks</span></span>

<span data-ttu-id="0af10-147">Un déclencheur inactif déclenche une action de tâche uniquement si l’ordinateur passe en état d’inactivité après la limite de démarrage du déclencheur.</span><span class="sxs-lookup"><span data-stu-id="0af10-147">An idle trigger will only trigger a task action if the computer goes into an idle state after the start boundary of the trigger.</span></span>

<span data-ttu-id="0af10-148">Lors de la lecture ou de l’écriture de données XML pour une tâche, un déclencheur inactif est spécifié à l’aide de l’élément [**IdleTrigger**](taskschedulerschema-idletrigger-triggergroup-element.md) du schéma planificateur de tâches.</span><span class="sxs-lookup"><span data-stu-id="0af10-148">When reading or writing XML for a task, an idle trigger is specified using the [**IdleTrigger**](taskschedulerschema-idletrigger-triggergroup-element.md) element of the Task Scheduler schema.</span></span>

<span data-ttu-id="0af10-149">Si une tâche est déclenchée par un déclencheur inactif, la propriété [**IdleSettings. WaitTimeout**](idlesettings-waittimeout.md) est ignorée.</span><span class="sxs-lookup"><span data-stu-id="0af10-149">If a task is triggered by an idle trigger, then the [**IdleSettings.WaitTimeout**](idlesettings-waittimeout.md) property is ignored.</span></span>

<span data-ttu-id="0af10-150">Si l’instance initiale d’une tâche avec un déclencheur inactif est toujours en cours d’exécution, la tâche est lancée une seule fois sans répétitions, même si plusieurs répétitions sont définies dans la propriété [**répétition**](trigger-repetition.md) .</span><span class="sxs-lookup"><span data-stu-id="0af10-150">If the initial instance of a task with an idle trigger is still running, then the task is only launched once with no repetitions, even if multiple repetition is defined in the [**Repetition**](trigger-repetition.md) property.</span></span> <span data-ttu-id="0af10-151">Ce comportement ne se produit pas si la tâche s’arrête de lui-même.</span><span class="sxs-lookup"><span data-stu-id="0af10-151">This behavior does not occur if the task stops by itself.</span></span>

## <a name="requirements"></a><span data-ttu-id="0af10-152">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0af10-152">Requirements</span></span>



| <span data-ttu-id="0af10-153">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0af10-153">Requirement</span></span> | <span data-ttu-id="0af10-154">Valeur</span><span class="sxs-lookup"><span data-stu-id="0af10-154">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0af10-155">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0af10-155">Minimum supported client</span></span><br/> | <span data-ttu-id="0af10-156">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0af10-156">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="0af10-157">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0af10-157">Minimum supported server</span></span><br/> | <span data-ttu-id="0af10-158">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0af10-158">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="0af10-159">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="0af10-159">Type library</span></span><br/>             | <dl> <span data-ttu-id="0af10-160"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="0af10-160"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="0af10-161">DLL</span><span class="sxs-lookup"><span data-stu-id="0af10-161">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0af10-162"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0af10-162"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0af10-163">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0af10-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0af10-164">**Stead**</span><span class="sxs-lookup"><span data-stu-id="0af10-164">**Trigger**</span></span>](trigger.md)
</dt> <dt>

[<span data-ttu-id="0af10-165">Objets Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="0af10-165">Task Scheduler Objects</span></span>](task-scheduler-objects.md)
</dt> <dt>

[<span data-ttu-id="0af10-166">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="0af10-166">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





