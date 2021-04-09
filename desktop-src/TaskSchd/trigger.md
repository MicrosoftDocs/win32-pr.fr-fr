---
title: Objet Trigger
description: Objet de script qui fournit les propriétés communes qui sont héritées par tous les objets déclencheurs.
ms.assetid: dfc4cb36-8bdb-4aec-963e-5f1ec1ff85aa
keywords:
- déclencheurs Planificateur de tâches, objet déclencheur
- Objet Trigger Planificateur de tâches
- Planificateur de tâches de l’objet de déclencheur, décrit
topic_type:
- apiref
api_name:
- Trigger
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f4a7edc6eff0bb04c81ba3bff3bb86ec0455b25
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843317"
---
# <a name="trigger-object"></a><span data-ttu-id="cd6f4-106">Objet Trigger</span><span class="sxs-lookup"><span data-stu-id="cd6f4-106">Trigger object</span></span>

<span data-ttu-id="cd6f4-107">Objet de script qui fournit les propriétés communes qui sont héritées par tous les objets déclencheurs.</span><span class="sxs-lookup"><span data-stu-id="cd6f4-107">Scripting object that provides the common properties that are inherited by all trigger objects.</span></span>

## <a name="members"></a><span data-ttu-id="cd6f4-108">Membres</span><span class="sxs-lookup"><span data-stu-id="cd6f4-108">Members</span></span>

<span data-ttu-id="cd6f4-109">L’objet **déclencheur** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="cd6f4-109">The **Trigger** object has these types of members:</span></span>

-   [<span data-ttu-id="cd6f4-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="cd6f4-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="cd6f4-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="cd6f4-111">Properties</span></span>

<span data-ttu-id="cd6f4-112">L’objet **déclencheur** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="cd6f4-112">The **Trigger** object has these properties.</span></span>



| <span data-ttu-id="cd6f4-113">Propriété</span><span class="sxs-lookup"><span data-stu-id="cd6f4-113">Property</span></span>                                                            | <span data-ttu-id="cd6f4-114">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="cd6f4-114">Access type</span></span>           | <span data-ttu-id="cd6f4-115">Description</span><span class="sxs-lookup"><span data-stu-id="cd6f4-115">Description</span></span>                                                                                                                                         |
|:--------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cd6f4-116">**activé**</span><span class="sxs-lookup"><span data-stu-id="cd6f4-116">**Enabled**</span></span>](trigger-enabled.md)<br/>                       | <span data-ttu-id="cd6f4-117">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="cd6f4-117">Read/write</span></span><br/> | <span data-ttu-id="cd6f4-118">Obtient ou définit une valeur booléenne qui indique si le déclencheur est activé.</span><span class="sxs-lookup"><span data-stu-id="cd6f4-118">Gets or sets a Boolean value that indicates whether the trigger is enabled.</span></span><br/>                                                              |
| [<span data-ttu-id="cd6f4-119">**EndBoundary**</span><span class="sxs-lookup"><span data-stu-id="cd6f4-119">**EndBoundary**</span></span>](trigger-endboundary.md)<br/>               | <span data-ttu-id="cd6f4-120">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="cd6f4-120">Read/write</span></span><br/> | <span data-ttu-id="cd6f4-121">Obtient ou définit la date et l’heure de désactivation du déclencheur.</span><span class="sxs-lookup"><span data-stu-id="cd6f4-121">Gets or sets the date and time when the trigger is deactivated.</span></span> <span data-ttu-id="cd6f4-122">Le déclencheur ne peut pas démarrer la tâche une fois qu’elle est désactivée.</span><span class="sxs-lookup"><span data-stu-id="cd6f4-122">The trigger cannot start the task after it is deactivated.</span></span><br/>               |
| [<span data-ttu-id="cd6f4-123">**ExecutionTimeLimit**</span><span class="sxs-lookup"><span data-stu-id="cd6f4-123">**ExecutionTimeLimit**</span></span>](trigger-executiontimelimit.md)<br/> | <span data-ttu-id="cd6f4-124">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="cd6f4-124">Read/write</span></span><br/> | <span data-ttu-id="cd6f4-125">Obtient ou définit la durée maximale pendant laquelle la tâche lancée par le déclencheur est autorisée à s’exécuter.</span><span class="sxs-lookup"><span data-stu-id="cd6f4-125">Gets or sets the maximum amount of time that the task launched by the trigger is allowed to run.</span></span><br/>                                         |
| [<span data-ttu-id="cd6f4-126">**Identifi**</span><span class="sxs-lookup"><span data-stu-id="cd6f4-126">**Id**</span></span>](trigger-id.md)<br/>                                 | <span data-ttu-id="cd6f4-127">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="cd6f4-127">Read/write</span></span><br/> | <span data-ttu-id="cd6f4-128">Obtient ou définit l’identificateur pour le déclencheur.</span><span class="sxs-lookup"><span data-stu-id="cd6f4-128">Gets or sets the identifier for the trigger.</span></span><br/>                                                                                             |
| [<span data-ttu-id="cd6f4-129">**Répétition**</span><span class="sxs-lookup"><span data-stu-id="cd6f4-129">**Repetition**</span></span>](trigger-repetition.md)<br/>                 | <span data-ttu-id="cd6f4-130">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="cd6f4-130">Read/write</span></span><br/> | <span data-ttu-id="cd6f4-131">Obtient ou définit une valeur qui indique la fréquence d’exécution de la tâche et la durée de répétition du modèle de répétition après le démarrage de la tâche.</span><span class="sxs-lookup"><span data-stu-id="cd6f4-131">Gets or sets a value that indicates how often the task is run and how long the repetition pattern is repeated after the task is started.</span></span><br/> |
| [<span data-ttu-id="cd6f4-132">**StartBoundary**</span><span class="sxs-lookup"><span data-stu-id="cd6f4-132">**StartBoundary**</span></span>](trigger-startboundary.md)<br/>           | <span data-ttu-id="cd6f4-133">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="cd6f4-133">Read/write</span></span><br/> | <span data-ttu-id="cd6f4-134">Obtient ou définit la date et l’heure d’activation du déclencheur.</span><span class="sxs-lookup"><span data-stu-id="cd6f4-134">Gets or sets the date and time when the trigger is activated.</span></span> <span data-ttu-id="cd6f4-135">Le déclencheur peut démarrer la tâche une fois que le déclencheur est activé.</span><span class="sxs-lookup"><span data-stu-id="cd6f4-135">The trigger can start the task after the trigger is activated.</span></span><br/>             |
| [<span data-ttu-id="cd6f4-136">**Entrer**</span><span class="sxs-lookup"><span data-stu-id="cd6f4-136">**Type**</span></span>](trigger-type.md)<br/>                             |                       | <span data-ttu-id="cd6f4-137">Obtient le type du déclencheur.</span><span class="sxs-lookup"><span data-stu-id="cd6f4-137">Gets the type of the trigger.</span></span><br/>                                                                                                            |



 

## <a name="remarks"></a><span data-ttu-id="cd6f4-138">Notes</span><span class="sxs-lookup"><span data-stu-id="cd6f4-138">Remarks</span></span>

<span data-ttu-id="cd6f4-139">L’Planificateur de tâches fournit les objets individuels suivants pour les différents déclencheurs qu’une tâche peut utiliser :</span><span class="sxs-lookup"><span data-stu-id="cd6f4-139">The Task Scheduler provides the following individual objects for the different triggers that a task can use:</span></span>

-   [<span data-ttu-id="cd6f4-140">**BootTrigger**</span><span class="sxs-lookup"><span data-stu-id="cd6f4-140">**BootTrigger**</span></span>](boottrigger.md)
-   [<span data-ttu-id="cd6f4-141">**DailyTrigger**</span><span class="sxs-lookup"><span data-stu-id="cd6f4-141">**DailyTrigger**</span></span>](dailytrigger.md)
-   [<span data-ttu-id="cd6f4-142">**EventTrigger**</span><span class="sxs-lookup"><span data-stu-id="cd6f4-142">**EventTrigger**</span></span>](eventtrigger.md)
-   [<span data-ttu-id="cd6f4-143">**IdleTrigger**</span><span class="sxs-lookup"><span data-stu-id="cd6f4-143">**IdleTrigger**</span></span>](idletrigger.md)
-   [<span data-ttu-id="cd6f4-144">**LogonTrigger**</span><span class="sxs-lookup"><span data-stu-id="cd6f4-144">**LogonTrigger**</span></span>](logontrigger.md)
-   [<span data-ttu-id="cd6f4-145">**MonthlyDOWTrigger**</span><span class="sxs-lookup"><span data-stu-id="cd6f4-145">**MonthlyDOWTrigger**</span></span>](monthlydowtrigger.md)
-   [<span data-ttu-id="cd6f4-146">**MonthlyTrigger**</span><span class="sxs-lookup"><span data-stu-id="cd6f4-146">**MonthlyTrigger**</span></span>](monthlytrigger.md)
-   [<span data-ttu-id="cd6f4-147">**RegistrationTrigger**</span><span class="sxs-lookup"><span data-stu-id="cd6f4-147">**RegistrationTrigger**</span></span>](registrationtrigger.md)
-   [<span data-ttu-id="cd6f4-148">**TimeTrigger**</span><span class="sxs-lookup"><span data-stu-id="cd6f4-148">**TimeTrigger**</span></span>](timetrigger.md)
-   [<span data-ttu-id="cd6f4-149">**WeeklyTrigger**</span><span class="sxs-lookup"><span data-stu-id="cd6f4-149">**WeeklyTrigger**</span></span>](weeklytrigger.md)
-   [<span data-ttu-id="cd6f4-150">**SessionStateChangeTrigger**</span><span class="sxs-lookup"><span data-stu-id="cd6f4-150">**SessionStateChangeTrigger**</span></span>](sessionstatechangetrigger.md)

<span data-ttu-id="cd6f4-151">Lors de la lecture ou de l’écriture de données XML, les déclencheurs d’une tâche sont spécifiés dans l’élément [**triggers**](taskschedulerschema-triggers-tasktype-element.md) du schéma planificateur de tâches.</span><span class="sxs-lookup"><span data-stu-id="cd6f4-151">When reading or writing XML, the triggers of a task are specified in the [**Triggers**](taskschedulerschema-triggers-tasktype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="examples"></a><span data-ttu-id="cd6f4-152">Exemples</span><span class="sxs-lookup"><span data-stu-id="cd6f4-152">Examples</span></span>

<span data-ttu-id="cd6f4-153">Pour plus d’informations et pour obtenir un exemple de code pour cet objet de script, consultez [exemple de déclenchement temporel (script)](time-trigger-example--scripting-.md).</span><span class="sxs-lookup"><span data-stu-id="cd6f4-153">For more information and example code for this scripting object, see [Time Trigger Example (Scripting)](time-trigger-example--scripting-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="cd6f4-154">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cd6f4-154">Requirements</span></span>



| <span data-ttu-id="cd6f4-155">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cd6f4-155">Requirement</span></span> | <span data-ttu-id="cd6f4-156">Valeur</span><span class="sxs-lookup"><span data-stu-id="cd6f4-156">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cd6f4-157">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cd6f4-157">Minimum supported client</span></span><br/> | <span data-ttu-id="cd6f4-158">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cd6f4-158">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="cd6f4-159">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cd6f4-159">Minimum supported server</span></span><br/> | <span data-ttu-id="cd6f4-160">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cd6f4-160">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="cd6f4-161">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="cd6f4-161">Type library</span></span><br/>             | <dl> <span data-ttu-id="cd6f4-162"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="cd6f4-162"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="cd6f4-163">DLL</span><span class="sxs-lookup"><span data-stu-id="cd6f4-163">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cd6f4-164"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cd6f4-164"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cd6f4-165">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cd6f4-165">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd6f4-166">**TriggerCollection**</span><span class="sxs-lookup"><span data-stu-id="cd6f4-166">**TriggerCollection**</span></span>](triggercollection.md)
</dt> </dl>

 

 





