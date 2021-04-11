---
title: Objet TimeTrigger (Windows. ApplicationModel. Background. h)
description: Objet de script qui représente un déclencheur qui démarre une tâche à une date et une heure spécifiques.
ms.assetid: 3c277827-8e70-42e7-a849-773ecc997a93
keywords:
- Planificateur de tâches de déclencheur d’heure, objet
- Objet TimeTrigger Planificateur de tâches
- Planificateur de tâches d’objets TimeTrigger, Description
topic_type:
- apiref
api_name:
- TimeTrigger
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a8403b93e1c5292ade9f6f402b7e41994339140
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317329"
---
# <a name="timetrigger-object"></a><span data-ttu-id="a25cc-106">Objet TimeTrigger</span><span class="sxs-lookup"><span data-stu-id="a25cc-106">TimeTrigger object</span></span>

<span data-ttu-id="a25cc-107">Objet de script qui représente un déclencheur qui démarre une tâche à une date et une heure spécifiques.</span><span class="sxs-lookup"><span data-stu-id="a25cc-107">Scripting object that represents a trigger that starts a task at a specific date and time.</span></span>

## <a name="members"></a><span data-ttu-id="a25cc-108">Membres</span><span class="sxs-lookup"><span data-stu-id="a25cc-108">Members</span></span>

<span data-ttu-id="a25cc-109">L’objet **timetrigger** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="a25cc-109">The **TimeTrigger** object has these types of members:</span></span>

-   [<span data-ttu-id="a25cc-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="a25cc-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a25cc-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="a25cc-111">Properties</span></span>

<span data-ttu-id="a25cc-112">L’objet **timetrigger** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="a25cc-112">The **TimeTrigger** object has these properties.</span></span>



| <span data-ttu-id="a25cc-113">Propriété</span><span class="sxs-lookup"><span data-stu-id="a25cc-113">Property</span></span>                                                            | <span data-ttu-id="a25cc-114">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="a25cc-114">Access type</span></span>           | <span data-ttu-id="a25cc-115">Description</span><span class="sxs-lookup"><span data-stu-id="a25cc-115">Description</span></span>                                                                                                                                                                      |
|:--------------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a25cc-116">**activé**</span><span class="sxs-lookup"><span data-stu-id="a25cc-116">**Enabled**</span></span>](trigger-enabled.md)<br/>                       | <span data-ttu-id="a25cc-117">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="a25cc-117">Read/write</span></span><br/> | <span data-ttu-id="a25cc-118">Héritée du [**déclencheur**](trigger.md).</span><span class="sxs-lookup"><span data-stu-id="a25cc-118">Inherited from [**Trigger**](trigger.md).</span></span> <span data-ttu-id="a25cc-119">Obtient ou définit une valeur booléenne qui indique si le déclencheur est activé.</span><span class="sxs-lookup"><span data-stu-id="a25cc-119">Gets or sets a Boolean value that indicates whether the trigger is enabled.</span></span><br/>                                                |
| [<span data-ttu-id="a25cc-120">**EndBoundary**</span><span class="sxs-lookup"><span data-stu-id="a25cc-120">**EndBoundary**</span></span>](trigger-endboundary.md)<br/>               | <span data-ttu-id="a25cc-121">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="a25cc-121">Read/write</span></span><br/> | <span data-ttu-id="a25cc-122">Héritée du [**déclencheur**](trigger.md).</span><span class="sxs-lookup"><span data-stu-id="a25cc-122">Inherited from [**Trigger**](trigger.md).</span></span> <span data-ttu-id="a25cc-123">Obtient ou définit la date et l’heure de désactivation du déclencheur.</span><span class="sxs-lookup"><span data-stu-id="a25cc-123">Gets or sets the date and time when the trigger is deactivated.</span></span> <span data-ttu-id="a25cc-124">Le déclencheur ne peut pas démarrer la tâche une fois qu’elle est désactivée.</span><span class="sxs-lookup"><span data-stu-id="a25cc-124">The trigger cannot start the task after it is deactivated.</span></span><br/> |
| [<span data-ttu-id="a25cc-125">**ExecutionTimeLimit**</span><span class="sxs-lookup"><span data-stu-id="a25cc-125">**ExecutionTimeLimit**</span></span>](trigger-executiontimelimit.md)<br/> | <span data-ttu-id="a25cc-126">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="a25cc-126">Read/write</span></span><br/> | <span data-ttu-id="a25cc-127">Héritée du [**déclencheur**](trigger.md).</span><span class="sxs-lookup"><span data-stu-id="a25cc-127">Inherited from [**Trigger**](trigger.md).</span></span> <span data-ttu-id="a25cc-128">Obtient ou définit la durée maximale pendant laquelle la tâche lancée par le déclencheur est autorisée à s’exécuter.</span><span class="sxs-lookup"><span data-stu-id="a25cc-128">Gets or sets the maximum amount of time that the task launched by the trigger is allowed to run.</span></span><br/>                           |
| [<span data-ttu-id="a25cc-129">**Identifi**</span><span class="sxs-lookup"><span data-stu-id="a25cc-129">**Id**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_id)<br/>                                | <span data-ttu-id="a25cc-130">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="a25cc-130">Read/write</span></span><br/> | <span data-ttu-id="a25cc-131">Héritée du [**déclencheur**](trigger.md).</span><span class="sxs-lookup"><span data-stu-id="a25cc-131">Inherited from [**Trigger**](trigger.md).</span></span> <span data-ttu-id="a25cc-132">Obtient ou définit l’identificateur pour le déclencheur.</span><span class="sxs-lookup"><span data-stu-id="a25cc-132">Gets or sets the identifier for the trigger.</span></span><br/>                                                                               |
| [<span data-ttu-id="a25cc-133">**RandomDelay**</span><span class="sxs-lookup"><span data-stu-id="a25cc-133">**RandomDelay**</span></span>](dailytrigger-randomdelay.md)<br/>          | <span data-ttu-id="a25cc-134">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="a25cc-134">Read/write</span></span><br/> | <span data-ttu-id="a25cc-135">Obtient ou définit un délai qui est ajouté de manière aléatoire à l’heure de début du déclencheur.</span><span class="sxs-lookup"><span data-stu-id="a25cc-135">Gets or sets a delay time that is randomly added to the start time of the trigger.</span></span><br/>                                                                                    |
| [<span data-ttu-id="a25cc-136">**Répétition**</span><span class="sxs-lookup"><span data-stu-id="a25cc-136">**Repetition**</span></span>](trigger-repetition.md)<br/>                 | <span data-ttu-id="a25cc-137">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="a25cc-137">Read/write</span></span><br/> | <span data-ttu-id="a25cc-138">Héritée du [**déclencheur**](trigger.md).</span><span class="sxs-lookup"><span data-stu-id="a25cc-138">Inherited from [**Trigger**](trigger.md).</span></span> <span data-ttu-id="a25cc-139">Obtient ou définit la fréquence d’exécution de la tâche et la durée de répétition du modèle de répétition après le démarrage de la tâche.</span><span class="sxs-lookup"><span data-stu-id="a25cc-139">Gets or sets how often the task is run and how long the repetition pattern is repeated after the task is started.</span></span><br/>          |
| [<span data-ttu-id="a25cc-140">**StartBoundary**</span><span class="sxs-lookup"><span data-stu-id="a25cc-140">**StartBoundary**</span></span>](trigger-startboundary.md)<br/>           | <span data-ttu-id="a25cc-141">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="a25cc-141">Read/write</span></span><br/> | <span data-ttu-id="a25cc-142">Héritée du [**déclencheur**](trigger.md).</span><span class="sxs-lookup"><span data-stu-id="a25cc-142">Inherited from [**Trigger**](trigger.md).</span></span> <span data-ttu-id="a25cc-143">Obtient ou définit la date et l’heure d’activation du déclencheur.</span><span class="sxs-lookup"><span data-stu-id="a25cc-143">Gets or sets the date and time when the trigger is activated.</span></span> <span data-ttu-id="a25cc-144">Cet élément est obligatoire.</span><span class="sxs-lookup"><span data-stu-id="a25cc-144">This element is required.</span></span><br/>                                    |
| [<span data-ttu-id="a25cc-145">**Entrer**</span><span class="sxs-lookup"><span data-stu-id="a25cc-145">**Type**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_type)<br/>                            | <span data-ttu-id="a25cc-146">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a25cc-146">Read-only</span></span><br/>  | <span data-ttu-id="a25cc-147">Héritée du [**déclencheur**](trigger.md).</span><span class="sxs-lookup"><span data-stu-id="a25cc-147">Inherited from [**Trigger**](trigger.md).</span></span> <span data-ttu-id="a25cc-148">Obtient le type du déclencheur.</span><span class="sxs-lookup"><span data-stu-id="a25cc-148">Gets the type of the trigger.</span></span><br/>                                                                                              |



 

## <a name="remarks"></a><span data-ttu-id="a25cc-149">Notes</span><span class="sxs-lookup"><span data-stu-id="a25cc-149">Remarks</span></span>

<span data-ttu-id="a25cc-150">L’élément [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) est un élément requis pour les déclencheurs de temps et de calendrier ([**timetrigger**](taskschedulerschema-timetrigger-triggergroup-element.md) et [**CalendarTrigger**](taskschedulerschema-calendartrigger-triggergroup-element.md)).</span><span class="sxs-lookup"><span data-stu-id="a25cc-150">The [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) element is a required element for time and calendar triggers ([**TimeTrigger**](taskschedulerschema-timetrigger-triggergroup-element.md) and [**CalendarTrigger**](taskschedulerschema-calendartrigger-triggergroup-element.md)).</span></span>

<span data-ttu-id="a25cc-151">Lors de la lecture ou de l’écriture de données XML pour une tâche, un déclencheur inactif est spécifié à l’aide de l’élément [**timetrigger**](taskschedulerschema-timetrigger-triggergroup-element.md) du schéma planificateur de tâches.</span><span class="sxs-lookup"><span data-stu-id="a25cc-151">When reading or writing XML for a task, an idle trigger is specified using the [**TimeTrigger**](taskschedulerschema-timetrigger-triggergroup-element.md) element of the Task Scheduler schema.</span></span>

## <a name="examples"></a><span data-ttu-id="a25cc-152">Exemples</span><span class="sxs-lookup"><span data-stu-id="a25cc-152">Examples</span></span>

<span data-ttu-id="a25cc-153">Pour plus d’informations et pour obtenir un exemple de code pour cet objet de script, consultez [exemple de déclenchement temporel (script)](time-trigger-example--scripting-.md).</span><span class="sxs-lookup"><span data-stu-id="a25cc-153">For more information and example code for this scripting object, see [Time Trigger Example (Scripting)](time-trigger-example--scripting-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a25cc-154">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a25cc-154">Requirements</span></span>



| <span data-ttu-id="a25cc-155">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a25cc-155">Requirement</span></span> | <span data-ttu-id="a25cc-156">Valeur</span><span class="sxs-lookup"><span data-stu-id="a25cc-156">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a25cc-157">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a25cc-157">Minimum supported client</span></span><br/> | <span data-ttu-id="a25cc-158">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a25cc-158">Windows Vista \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="a25cc-159">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a25cc-159">Minimum supported server</span></span><br/> | <span data-ttu-id="a25cc-160">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a25cc-160">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="a25cc-161">En-tête</span><span class="sxs-lookup"><span data-stu-id="a25cc-161">Header</span></span><br/>                   | <dl> <span data-ttu-id="a25cc-162"><dt>Windows. ApplicationModel. Background. h</dt></span><span class="sxs-lookup"><span data-stu-id="a25cc-162"><dt>Windows.applicationmodel.background.h</dt></span></span> </dl> |
| <span data-ttu-id="a25cc-163">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="a25cc-163">Type library</span></span><br/>             | <dl> <span data-ttu-id="a25cc-164"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="a25cc-164"><dt>Taskschd.tlb</dt></span></span> </dl>                          |
| <span data-ttu-id="a25cc-165">DLL</span><span class="sxs-lookup"><span data-stu-id="a25cc-165">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a25cc-166"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a25cc-166"><dt>Taskschd.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="a25cc-167">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a25cc-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a25cc-168">**Stead**</span><span class="sxs-lookup"><span data-stu-id="a25cc-168">**Trigger**</span></span>](trigger.md)
</dt> <dt>

[<span data-ttu-id="a25cc-169">**TriggerCollection**</span><span class="sxs-lookup"><span data-stu-id="a25cc-169">**TriggerCollection**</span></span>](triggercollection.md)
</dt> <dt>

[<span data-ttu-id="a25cc-170">**TriggerCollection. Create**</span><span class="sxs-lookup"><span data-stu-id="a25cc-170">**TriggerCollection.Create**</span></span>](triggercollection-create.md)
</dt> </dl>

 

 





