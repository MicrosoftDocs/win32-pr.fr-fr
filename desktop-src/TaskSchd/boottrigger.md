---
title: Objet BootTrigger
description: Objet de script qui représente un déclencheur qui démarre une tâche au démarrage du système.
ms.assetid: 9d5a7cf6-2e1d-44ae-bb45-66424770d61b
keywords:
- Planificateur de tâches de déclencheur de démarrage, objet
- Objet BootTrigger Planificateur de tâches
- Planificateur de tâches d’objets BootTrigger, Description
topic_type:
- apiref
api_name:
- BootTrigger
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 346a4bc7b20606f59c26b131590b92593d40d07e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466991"
---
# <a name="boottrigger-object"></a><span data-ttu-id="612a4-106">Objet BootTrigger</span><span class="sxs-lookup"><span data-stu-id="612a4-106">BootTrigger object</span></span>

<span data-ttu-id="612a4-107">Objet de script qui représente un déclencheur qui démarre une tâche au démarrage du système.</span><span class="sxs-lookup"><span data-stu-id="612a4-107">Scripting object that represents a trigger that starts a task when the system is booted.</span></span>

## <a name="members"></a><span data-ttu-id="612a4-108">Membres</span><span class="sxs-lookup"><span data-stu-id="612a4-108">Members</span></span>

<span data-ttu-id="612a4-109">L’objet **BootTrigger** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="612a4-109">The **BootTrigger** object has these types of members:</span></span>

-   [<span data-ttu-id="612a4-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="612a4-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="612a4-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="612a4-111">Properties</span></span>

<span data-ttu-id="612a4-112">L’objet **BootTrigger** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="612a4-112">The **BootTrigger** object has these properties.</span></span>



| <span data-ttu-id="612a4-113">Propriété</span><span class="sxs-lookup"><span data-stu-id="612a4-113">Property</span></span>                                                            | <span data-ttu-id="612a4-114">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="612a4-114">Access type</span></span>           | <span data-ttu-id="612a4-115">Description</span><span class="sxs-lookup"><span data-stu-id="612a4-115">Description</span></span>                                                                                                                                                                                 |
|:--------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="612a4-116">**Retard**</span><span class="sxs-lookup"><span data-stu-id="612a4-116">**Delay**</span></span>](boottrigger-delay.md)<br/>                       |                       | <span data-ttu-id="612a4-117">Obtient ou définit une valeur qui indique la durée entre le démarrage du système et le démarrage de la tâche.</span><span class="sxs-lookup"><span data-stu-id="612a4-117">Gets or sets a value that indicates the amount of time between when the system is booted and when the task is started.</span></span><br/>                                                           |
| [<span data-ttu-id="612a4-118">**Enabled**</span><span class="sxs-lookup"><span data-stu-id="612a4-118">**Enabled**</span></span>](trigger-enabled.md)<br/>                       | <span data-ttu-id="612a4-119">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="612a4-119">Read/write</span></span><br/> | <span data-ttu-id="612a4-120">Héritée de l’objet [**déclencheur**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="612a4-120">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="612a4-121">Obtient ou définit une valeur booléenne qui indique si le déclencheur est activé.</span><span class="sxs-lookup"><span data-stu-id="612a4-121">Gets or sets a Boolean value that indicates whether the trigger is enabled.</span></span><br/>                                                |
| [<span data-ttu-id="612a4-122">**EndBoundary**</span><span class="sxs-lookup"><span data-stu-id="612a4-122">**EndBoundary**</span></span>](trigger-endboundary.md)<br/>               | <span data-ttu-id="612a4-123">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="612a4-123">Read/write</span></span><br/> | <span data-ttu-id="612a4-124">Héritée de l’objet [**déclencheur**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="612a4-124">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="612a4-125">Obtient ou définit la date et l’heure de désactivation du déclencheur.</span><span class="sxs-lookup"><span data-stu-id="612a4-125">Gets or sets the date and time when the trigger is deactivated.</span></span> <span data-ttu-id="612a4-126">Le déclencheur ne peut pas démarrer la tâche une fois qu’elle est désactivée.</span><span class="sxs-lookup"><span data-stu-id="612a4-126">The trigger cannot start the task after it is deactivated.</span></span><br/> |
| [<span data-ttu-id="612a4-127">**ExecutionTimeLimit**</span><span class="sxs-lookup"><span data-stu-id="612a4-127">**ExecutionTimeLimit**</span></span>](trigger-executiontimelimit.md)<br/> | <span data-ttu-id="612a4-128">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="612a4-128">Read/write</span></span><br/> | <span data-ttu-id="612a4-129">Héritée de l’objet [**déclencheur**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="612a4-129">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="612a4-130">Obtient ou définit la durée maximale pendant laquelle la tâche lancée par le déclencheur est autorisée à s’exécuter.</span><span class="sxs-lookup"><span data-stu-id="612a4-130">Gets or sets the maximum amount of time that the task launched by the trigger is allowed to run.</span></span><br/>                           |
| [<span data-ttu-id="612a4-131">**Identifi**</span><span class="sxs-lookup"><span data-stu-id="612a4-131">**Id**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_id)<br/>                                | <span data-ttu-id="612a4-132">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="612a4-132">Read/write</span></span><br/> | <span data-ttu-id="612a4-133">Héritée de l’objet [**déclencheur**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="612a4-133">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="612a4-134">Obtient ou définit l’identificateur pour le déclencheur.</span><span class="sxs-lookup"><span data-stu-id="612a4-134">Gets or sets the identifier for the trigger.</span></span><br/>                                                                               |
| [<span data-ttu-id="612a4-135">**Répétition**</span><span class="sxs-lookup"><span data-stu-id="612a4-135">**Repetition**</span></span>](trigger-repetition.md)<br/>                 | <span data-ttu-id="612a4-136">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="612a4-136">Read/write</span></span><br/> | <span data-ttu-id="612a4-137">Héritée de l’objet [**déclencheur**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="612a4-137">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="612a4-138">Obtient ou définit la fréquence d’exécution de la tâche et la durée de répétition du modèle de répétition après le démarrage de la tâche.</span><span class="sxs-lookup"><span data-stu-id="612a4-138">Gets or sets how often the task is run and how long the repetition pattern is repeated after the task is started.</span></span><br/>          |
| [<span data-ttu-id="612a4-139">**StartBoundary**</span><span class="sxs-lookup"><span data-stu-id="612a4-139">**StartBoundary**</span></span>](trigger-startboundary.md)<br/>           | <span data-ttu-id="612a4-140">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="612a4-140">Read/write</span></span><br/> | <span data-ttu-id="612a4-141">Héritée de l’objet [**déclencheur**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="612a4-141">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="612a4-142">Obtient ou définit la date et l’heure d’activation du déclencheur.</span><span class="sxs-lookup"><span data-stu-id="612a4-142">Gets or sets the date and time when the trigger is activated.</span></span><br/>                                                              |
| [<span data-ttu-id="612a4-143">**Entrer**</span><span class="sxs-lookup"><span data-stu-id="612a4-143">**Type**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_type)<br/>                            | <span data-ttu-id="612a4-144">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="612a4-144">Read-only</span></span><br/>  | <span data-ttu-id="612a4-145">Héritée de l’objet [**déclencheur**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="612a4-145">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="612a4-146">Obtient le type du déclencheur.</span><span class="sxs-lookup"><span data-stu-id="612a4-146">Gets the type of the trigger.</span></span><br/>                                                                                              |



 

## <a name="remarks"></a><span data-ttu-id="612a4-147">Notes</span><span class="sxs-lookup"><span data-stu-id="612a4-147">Remarks</span></span>

<span data-ttu-id="612a4-148">Le service Planificateur de tâches est démarré lorsque le système d’exploitation est démarré et les tâches de déclencheur de démarrage sont définies pour démarrer au démarrage du service Planificateur de tâches.</span><span class="sxs-lookup"><span data-stu-id="612a4-148">The Task Scheduler service is started when the operating system is booted, and boot trigger tasks are set to start when the Task Scheduler service starts.</span></span>

<span data-ttu-id="612a4-149">Seul un membre du groupe administrateurs peut créer une tâche avec un déclencheur de démarrage.</span><span class="sxs-lookup"><span data-stu-id="612a4-149">Only a member of the Administrators group can create a task with a boot trigger.</span></span>

<span data-ttu-id="612a4-150">Lors de la création de votre propre XML pour une tâche, un déclencheur de démarrage est spécifié à l’aide de l’élément [**BootTrigger**](taskschedulerschema-boottrigger-triggergroup-element.md) du schéma planificateur de tâches.</span><span class="sxs-lookup"><span data-stu-id="612a4-150">When creating your own XML for a task, a boot trigger is specified using the [**BootTrigger**](taskschedulerschema-boottrigger-triggergroup-element.md) element of the Task Scheduler schema.</span></span>

## <a name="examples"></a><span data-ttu-id="612a4-151">Exemples</span><span class="sxs-lookup"><span data-stu-id="612a4-151">Examples</span></span>

<span data-ttu-id="612a4-152">Pour plus d’informations et pour obtenir un exemple de code pour cet objet de script, consultez [exemple de déclencheur de démarrage (script)](boot-trigger-example--scripting-.md).</span><span class="sxs-lookup"><span data-stu-id="612a4-152">For more information and example code for this scripting object, see [Boot Trigger Example (Scripting)](boot-trigger-example--scripting-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="612a4-153">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="612a4-153">Requirements</span></span>



| <span data-ttu-id="612a4-154">Condition requise</span><span class="sxs-lookup"><span data-stu-id="612a4-154">Requirement</span></span> | <span data-ttu-id="612a4-155">Valeur</span><span class="sxs-lookup"><span data-stu-id="612a4-155">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="612a4-156">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="612a4-156">Minimum supported client</span></span><br/> | <span data-ttu-id="612a4-157">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="612a4-157">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="612a4-158">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="612a4-158">Minimum supported server</span></span><br/> | <span data-ttu-id="612a4-159">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="612a4-159">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="612a4-160">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="612a4-160">Type library</span></span><br/>             | <dl> <span data-ttu-id="612a4-161"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="612a4-161"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="612a4-162">DLL</span><span class="sxs-lookup"><span data-stu-id="612a4-162">DLL</span></span><br/>                      | <dl> <span data-ttu-id="612a4-163"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="612a4-163"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="612a4-164">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="612a4-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="612a4-165">**Stead**</span><span class="sxs-lookup"><span data-stu-id="612a4-165">**Trigger**</span></span>](trigger.md)
</dt> <dt>

[<span data-ttu-id="612a4-166">**TriggerCollection**</span><span class="sxs-lookup"><span data-stu-id="612a4-166">**TriggerCollection**</span></span>](triggercollection.md)
</dt> <dt>

[<span data-ttu-id="612a4-167">**TriggerCollection. Create**</span><span class="sxs-lookup"><span data-stu-id="612a4-167">**TriggerCollection.Create**</span></span>](triggercollection-create.md)
</dt> </dl>

 

 





