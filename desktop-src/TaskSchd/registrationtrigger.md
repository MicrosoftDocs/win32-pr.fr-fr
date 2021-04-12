---
title: Objet RegistrationTrigger
description: Objet de script qui représente un déclencheur qui démarre une tâche lorsque la tâche est inscrite ou mise à jour.
ms.assetid: 430ef3e0-9409-49ff-8ffb-31833938d8b2
keywords:
- Planificateur de tâches de déclencheur d’inscription, objet
- Objet RegistrationTrigger Planificateur de tâches
- Planificateur de tâches d’objets RegistrationTrigger, Description
topic_type:
- apiref
api_name:
- RegistrationTrigger
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08bf84fa92b1736b2989c1920abb8f0af2c0b97c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508777"
---
# <a name="registrationtrigger-object"></a><span data-ttu-id="6cf26-106">Objet RegistrationTrigger</span><span class="sxs-lookup"><span data-stu-id="6cf26-106">RegistrationTrigger object</span></span>

<span data-ttu-id="6cf26-107">Objet de script qui représente un déclencheur qui démarre une tâche lorsque la tâche est inscrite ou mise à jour.</span><span class="sxs-lookup"><span data-stu-id="6cf26-107">Scripting object that represents a trigger that starts a task when the task is registered or updated.</span></span>

## <a name="members"></a><span data-ttu-id="6cf26-108">Membres</span><span class="sxs-lookup"><span data-stu-id="6cf26-108">Members</span></span>

<span data-ttu-id="6cf26-109">L’objet **RegistrationTrigger** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="6cf26-109">The **RegistrationTrigger** object has these types of members:</span></span>

-   [<span data-ttu-id="6cf26-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="6cf26-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6cf26-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="6cf26-111">Properties</span></span>

<span data-ttu-id="6cf26-112">L’objet **RegistrationTrigger** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="6cf26-112">The **RegistrationTrigger** object has these properties.</span></span>



| <span data-ttu-id="6cf26-113">Propriété</span><span class="sxs-lookup"><span data-stu-id="6cf26-113">Property</span></span>                                                            | <span data-ttu-id="6cf26-114">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="6cf26-114">Access type</span></span>           | <span data-ttu-id="6cf26-115">Description</span><span class="sxs-lookup"><span data-stu-id="6cf26-115">Description</span></span>                                                                                                                                                                                 |
|:--------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6cf26-116">**Retard**</span><span class="sxs-lookup"><span data-stu-id="6cf26-116">**Delay**</span></span>](registrationtrigger-delay.md)<br/>               | <span data-ttu-id="6cf26-117">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="6cf26-117">Read/write</span></span><br/> | <span data-ttu-id="6cf26-118">Obtient ou définit le laps de temps entre le moment où la tâche est inscrite et le moment où elle est démarrée.</span><span class="sxs-lookup"><span data-stu-id="6cf26-118">Gets or sets the amount of time between when the task is registered and when the task is started.</span></span><br/>                                                                                |
| [<span data-ttu-id="6cf26-119">**Enabled**</span><span class="sxs-lookup"><span data-stu-id="6cf26-119">**Enabled**</span></span>](trigger-enabled.md)<br/>                       | <span data-ttu-id="6cf26-120">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="6cf26-120">Read/write</span></span><br/> | <span data-ttu-id="6cf26-121">Héritée de l’objet [**déclencheur**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="6cf26-121">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="6cf26-122">Obtient ou définit une valeur booléenne qui indique si le déclencheur est activé.</span><span class="sxs-lookup"><span data-stu-id="6cf26-122">Gets or sets a Boolean value that indicates whether the trigger is enabled.</span></span><br/>                                                |
| [<span data-ttu-id="6cf26-123">**EndBoundary**</span><span class="sxs-lookup"><span data-stu-id="6cf26-123">**EndBoundary**</span></span>](trigger-endboundary.md)<br/>               | <span data-ttu-id="6cf26-124">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="6cf26-124">Read/write</span></span><br/> | <span data-ttu-id="6cf26-125">Héritée de l’objet [**déclencheur**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="6cf26-125">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="6cf26-126">Obtient ou définit la date et l’heure de désactivation du déclencheur.</span><span class="sxs-lookup"><span data-stu-id="6cf26-126">Gets or sets the date and time when the trigger is deactivated.</span></span> <span data-ttu-id="6cf26-127">Le déclencheur ne peut pas démarrer la tâche une fois qu’elle est désactivée.</span><span class="sxs-lookup"><span data-stu-id="6cf26-127">The trigger cannot start the task after it is deactivated.</span></span><br/> |
| [<span data-ttu-id="6cf26-128">**ExecutionTimeLimit**</span><span class="sxs-lookup"><span data-stu-id="6cf26-128">**ExecutionTimeLimit**</span></span>](trigger-executiontimelimit.md)<br/> | <span data-ttu-id="6cf26-129">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="6cf26-129">Read/write</span></span><br/> | <span data-ttu-id="6cf26-130">Héritée de l’objet [**déclencheur**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="6cf26-130">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="6cf26-131">Obtient ou définit la durée maximale pendant laquelle la tâche lancée par le déclencheur est autorisée à s’exécuter.</span><span class="sxs-lookup"><span data-stu-id="6cf26-131">Gets or sets the maximum amount of time that the task launched by the trigger is allowed to run.</span></span><br/>                           |
| [<span data-ttu-id="6cf26-132">**Identifi**</span><span class="sxs-lookup"><span data-stu-id="6cf26-132">**Id**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_id)<br/>                                | <span data-ttu-id="6cf26-133">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="6cf26-133">Read/write</span></span><br/> | <span data-ttu-id="6cf26-134">Héritée de l’objet [**déclencheur**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="6cf26-134">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="6cf26-135">Obtient ou définit l’identificateur pour le déclencheur.</span><span class="sxs-lookup"><span data-stu-id="6cf26-135">Gets or sets the identifier for the trigger.</span></span><br/>                                                                               |
| [<span data-ttu-id="6cf26-136">**Répétition**</span><span class="sxs-lookup"><span data-stu-id="6cf26-136">**Repetition**</span></span>](trigger-repetition.md)<br/>                 | <span data-ttu-id="6cf26-137">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="6cf26-137">Read/write</span></span><br/> | <span data-ttu-id="6cf26-138">Héritée de l’objet [**déclencheur**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="6cf26-138">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="6cf26-139">Obtient ou définit la fréquence d’exécution de la tâche et la durée de répétition du modèle de répétition après le démarrage de la tâche.</span><span class="sxs-lookup"><span data-stu-id="6cf26-139">Gets or sets how often the task is run and how long the repetition pattern is repeated after the task is started.</span></span><br/>          |
| [<span data-ttu-id="6cf26-140">**StartBoundary**</span><span class="sxs-lookup"><span data-stu-id="6cf26-140">**StartBoundary**</span></span>](trigger-startboundary.md)<br/>           | <span data-ttu-id="6cf26-141">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="6cf26-141">Read/write</span></span><br/> | <span data-ttu-id="6cf26-142">Héritée de l’objet [**déclencheur**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="6cf26-142">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="6cf26-143">Obtient ou définit la date et l’heure d’activation du déclencheur.</span><span class="sxs-lookup"><span data-stu-id="6cf26-143">Gets or sets the date and time when the trigger is activated.</span></span><br/>                                                              |
| [<span data-ttu-id="6cf26-144">**Entrer**</span><span class="sxs-lookup"><span data-stu-id="6cf26-144">**Type**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_type)<br/>                            | <span data-ttu-id="6cf26-145">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6cf26-145">Read-only</span></span><br/>  | <span data-ttu-id="6cf26-146">Héritée de l’objet [**déclencheur**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="6cf26-146">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="6cf26-147">Obtient le type du déclencheur.</span><span class="sxs-lookup"><span data-stu-id="6cf26-147">Gets the type of the trigger.</span></span><br/>                                                                                              |



 

## <a name="remarks"></a><span data-ttu-id="6cf26-148">Notes</span><span class="sxs-lookup"><span data-stu-id="6cf26-148">Remarks</span></span>

<span data-ttu-id="6cf26-149">Lors de la création de votre propre XML pour une tâche, un déclencheur d’inscription est spécifié à l’aide de l’élément [**RegistrationTrigger**](taskschedulerschema-registrationtrigger-triggergroup-element.md) du schéma planificateur de tâches.</span><span class="sxs-lookup"><span data-stu-id="6cf26-149">When creating your own XML for a task, a registration trigger is specified using the [**RegistrationTrigger**](taskschedulerschema-registrationtrigger-triggergroup-element.md) element of the Task Scheduler schema.</span></span>

<span data-ttu-id="6cf26-150">Si une tâche avec un déclencheur d’inscription différé est inscrite et que l’ordinateur sur lequel la tâche est inscrite est arrêté ou redémarré pendant le délai, avant l’exécution de la tâche, la tâche ne s’exécutera pas et le délai sera perdu.</span><span class="sxs-lookup"><span data-stu-id="6cf26-150">If a task with a delayed registration trigger is registered, and the computer that the task is registered on is shutdown or restarted during the delay, before the task runs, then the task will not run and the delay will be lost.</span></span>

## <a name="examples"></a><span data-ttu-id="6cf26-151">Exemples</span><span class="sxs-lookup"><span data-stu-id="6cf26-151">Examples</span></span>

<span data-ttu-id="6cf26-152">Pour plus d’informations et pour obtenir un exemple de code pour cet objet de script, consultez [exemple de déclencheur d’inscription (script)](registration-trigger-example--scripting-.md).</span><span class="sxs-lookup"><span data-stu-id="6cf26-152">For more information and a code example for this scripting object, see [Registration Trigger Example (Scripting)](registration-trigger-example--scripting-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6cf26-153">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6cf26-153">Requirements</span></span>



| <span data-ttu-id="6cf26-154">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6cf26-154">Requirement</span></span> | <span data-ttu-id="6cf26-155">Valeur</span><span class="sxs-lookup"><span data-stu-id="6cf26-155">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6cf26-156">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6cf26-156">Minimum supported client</span></span><br/> | <span data-ttu-id="6cf26-157">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6cf26-157">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="6cf26-158">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6cf26-158">Minimum supported server</span></span><br/> | <span data-ttu-id="6cf26-159">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6cf26-159">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="6cf26-160">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="6cf26-160">Type library</span></span><br/>             | <dl> <span data-ttu-id="6cf26-161"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="6cf26-161"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="6cf26-162">DLL</span><span class="sxs-lookup"><span data-stu-id="6cf26-162">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6cf26-163"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6cf26-163"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6cf26-164">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6cf26-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6cf26-165">**Stead**</span><span class="sxs-lookup"><span data-stu-id="6cf26-165">**Trigger**</span></span>](trigger.md)
</dt> <dt>

[<span data-ttu-id="6cf26-166">**TriggerCollection**</span><span class="sxs-lookup"><span data-stu-id="6cf26-166">**TriggerCollection**</span></span>](triggercollection.md)
</dt> <dt>

[<span data-ttu-id="6cf26-167">**TriggerCollection. Create**</span><span class="sxs-lookup"><span data-stu-id="6cf26-167">**TriggerCollection.Create**</span></span>](triggercollection-create.md)
</dt> </dl>

 

 





