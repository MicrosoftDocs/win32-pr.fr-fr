---
title: Élément BootTrigger (triggerGroup)
description: Spécifie un déclencheur qui démarre une tâche au démarrage du système.
ms.assetid: c6833547-0daf-4e8a-b8c5-b422827b1d96
keywords:
- déclencheur de démarrage Planificateur de tâches, élément XML
- Élément BootTrigger Planificateur de tâches
topic_type:
- apiref
api_name:
- BootTrigger
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: eb6ccf590893e19340662fd4c47e4aa68047b29d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317357"
---
# <a name="boottrigger-triggergroup-element"></a><span data-ttu-id="80678-105">Élément BootTrigger (triggerGroup)</span><span class="sxs-lookup"><span data-stu-id="80678-105">BootTrigger (triggerGroup) Element</span></span>

<span data-ttu-id="80678-106">Spécifie un déclencheur qui démarre une tâche au démarrage du système.</span><span class="sxs-lookup"><span data-stu-id="80678-106">Specifies a trigger that starts a task when the system is booted.</span></span>

``` syntax
<xs:element name="BootTrigger"
    type="bootTriggerType"
 />
```

<span data-ttu-id="80678-107">L’élément **BootTrigger** est défini par le type complexe [**bootTriggerType**](taskschedulerschema-boottriggertype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="80678-107">The **BootTrigger** element is defined by the [**bootTriggerType**](taskschedulerschema-boottriggertype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="80678-108">Élément parent</span><span class="sxs-lookup"><span data-stu-id="80678-108">Parent element</span></span>



| <span data-ttu-id="80678-109">Élément</span><span class="sxs-lookup"><span data-stu-id="80678-109">Element</span></span>                                                           | <span data-ttu-id="80678-110">Dérivé de</span><span class="sxs-lookup"><span data-stu-id="80678-110">Derived from</span></span>                                                         | <span data-ttu-id="80678-111">Description</span><span class="sxs-lookup"><span data-stu-id="80678-111">Description</span></span>                                            |
|-------------------------------------------------------------------|----------------------------------------------------------------------|--------------------------------------------------------|
| [<span data-ttu-id="80678-112">**Déclencheurs**</span><span class="sxs-lookup"><span data-stu-id="80678-112">**Triggers**</span></span>](taskschedulerschema-triggers-tasktype-element.md) | [<span data-ttu-id="80678-113">**triggersType**</span><span class="sxs-lookup"><span data-stu-id="80678-113">**triggersType**</span></span>](taskschedulerschema-triggerstype-complextype.md) | <span data-ttu-id="80678-114">Spécifie les déclencheurs qui démarrent la tâche.</span><span class="sxs-lookup"><span data-stu-id="80678-114">Specifies the triggers that start the task.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="80678-115">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="80678-115">Child elements</span></span>



| <span data-ttu-id="80678-116">Élément</span><span class="sxs-lookup"><span data-stu-id="80678-116">Element</span></span>                                                                                                        | <span data-ttu-id="80678-117">Type</span><span class="sxs-lookup"><span data-stu-id="80678-117">Type</span></span>                                                                     | <span data-ttu-id="80678-118">Description</span><span class="sxs-lookup"><span data-stu-id="80678-118">Description</span></span>                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="80678-119">**Délai (bootTriggerType)**</span><span class="sxs-lookup"><span data-stu-id="80678-119">**Delay (bootTriggerType)**</span></span>](taskschedulerschema-delay-boottriggertype-element.md)                           | <span data-ttu-id="80678-120">duration</span><span class="sxs-lookup"><span data-stu-id="80678-120">duration</span></span>                                                                 | <span data-ttu-id="80678-121">Spécifie la durée entre le démarrage du système et le démarrage de la tâche.</span><span class="sxs-lookup"><span data-stu-id="80678-121">Specifies the amount of time between when the system is booted and when the task is started.</span></span><br/>                            |
| [<span data-ttu-id="80678-122">**Activé (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="80678-122">**Enabled (triggerBaseType)**</span></span>](taskschedulerschema-enabled-triggerbasetype-element.md)                       | <span data-ttu-id="80678-123">boolean</span><span class="sxs-lookup"><span data-stu-id="80678-123">boolean</span></span>                                                                  | <span data-ttu-id="80678-124">Spécifie que le déclencheur est activé.</span><span class="sxs-lookup"><span data-stu-id="80678-124">Specifies that the trigger is enabled.</span></span><br/>                                                                                  |
| [<span data-ttu-id="80678-125">**EndBoundary (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="80678-125">**EndBoundary (triggerBaseType)**</span></span>](taskschedulerschema-endboundary-triggerbasetype-element.md)               | <span data-ttu-id="80678-126">dateTime</span><span class="sxs-lookup"><span data-stu-id="80678-126">dateTime</span></span>                                                                 | <span data-ttu-id="80678-127">Spécifie la date et l’heure de désactivation du déclencheur.</span><span class="sxs-lookup"><span data-stu-id="80678-127">Specifies the date and time when the trigger is deactivated.</span></span> <span data-ttu-id="80678-128">Le déclencheur ne peut pas démarrer la tâche une fois qu’elle est désactivée.</span><span class="sxs-lookup"><span data-stu-id="80678-128">The trigger cannot start the task after it is deactivated.</span></span><br/> |
| [<span data-ttu-id="80678-129">**ExecutionTimeLimit (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="80678-129">**ExecutionTimeLimit (triggerBaseType)**</span></span>](taskschedulerschema-executiontimelimit-triggerbasetype-element.md) | <span data-ttu-id="80678-130">duration</span><span class="sxs-lookup"><span data-stu-id="80678-130">duration</span></span>                                                                 | <span data-ttu-id="80678-131">Spécifie la durée maximale pendant laquelle la tâche peut être démarrée par le déclencheur.</span><span class="sxs-lookup"><span data-stu-id="80678-131">Specifies the maximum amount of time in which the task can be started by the trigger.</span></span><br/>                                   |
| [<span data-ttu-id="80678-132">**Répétition (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="80678-132">**Repetition (triggerBaseType)**</span></span>](taskschedulerschema-repetition-triggerbasetype-element.md)                 | [<span data-ttu-id="80678-133">**repetitionType**</span><span class="sxs-lookup"><span data-stu-id="80678-133">**repetitionType**</span></span>](taskschedulerschema-repetitiontype-complextype.md) | <span data-ttu-id="80678-134">Spécifie la fréquence d’exécution de la tâche et la durée de répétition du modèle de répétition après le démarrage de la tâche.</span><span class="sxs-lookup"><span data-stu-id="80678-134">Specifies how often the task is run and how long the repetition pattern is repeated after the task is started.</span></span><br/>          |
| [<span data-ttu-id="80678-135">**StartBoundary (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="80678-135">**StartBoundary (triggerBaseType)**</span></span>](taskschedulerschema-startboundary-triggerbasetype-element.md)           | <span data-ttu-id="80678-136">dateTime</span><span class="sxs-lookup"><span data-stu-id="80678-136">dateTime</span></span>                                                                 | <span data-ttu-id="80678-137">Spécifie la date et l’heure d’activation du déclencheur.</span><span class="sxs-lookup"><span data-stu-id="80678-137">Specifies the date and time when the trigger is activated.</span></span><br/>                                                              |



## <a name="attributes"></a><span data-ttu-id="80678-138">Attributs</span><span class="sxs-lookup"><span data-stu-id="80678-138">Attributes</span></span>



| <span data-ttu-id="80678-139">Nom</span><span class="sxs-lookup"><span data-stu-id="80678-139">Name</span></span> | <span data-ttu-id="80678-140">Type</span><span class="sxs-lookup"><span data-stu-id="80678-140">Type</span></span>       | <span data-ttu-id="80678-141">Description</span><span class="sxs-lookup"><span data-stu-id="80678-141">Description</span></span>                               |
|------|------------|-------------------------------------------|
| <span data-ttu-id="80678-142">Id</span><span class="sxs-lookup"><span data-stu-id="80678-142">Id</span></span>   | <span data-ttu-id="80678-143">**string**</span><span class="sxs-lookup"><span data-stu-id="80678-143">**string**</span></span> | <span data-ttu-id="80678-144">Identificateur du déclencheur.</span><span class="sxs-lookup"><span data-stu-id="80678-144">The identifier of the trigger.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="80678-145">Notes</span><span class="sxs-lookup"><span data-stu-id="80678-145">Remarks</span></span>

<span data-ttu-id="80678-146">Pour le développement de scripts, un déclencheur de démarrage est défini par l’objet [**BootTrigger**](boottrigger.md) .</span><span class="sxs-lookup"><span data-stu-id="80678-146">For script development, a boot trigger is defined by the [**BootTrigger**](boottrigger.md) object.</span></span>

<span data-ttu-id="80678-147">Pour le développement C++, un déclencheur de démarrage est défini par l’objet [**IBootTrigger**](/windows/desktop/api/taskschd/nn-taskschd-iboottrigger) .</span><span class="sxs-lookup"><span data-stu-id="80678-147">For C++ development, a boot trigger is defined by the [**IBootTrigger**](/windows/desktop/api/taskschd/nn-taskschd-iboottrigger) object.</span></span>

## <a name="examples"></a><span data-ttu-id="80678-148">Exemples</span><span class="sxs-lookup"><span data-stu-id="80678-148">Examples</span></span>

<span data-ttu-id="80678-149">Pour obtenir un exemple complet du code XML d’une tâche qui spécifie un déclencheur de démarrage, consultez [exemple de déclencheur de démarrage (XML)](boot-trigger-example--xml-.md).</span><span class="sxs-lookup"><span data-stu-id="80678-149">For a complete example of the XML for a task that specifies a boot trigger, see [Boot Trigger Example (XML)](boot-trigger-example--xml-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="80678-150">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="80678-150">Requirements</span></span>



| <span data-ttu-id="80678-151">Condition requise</span><span class="sxs-lookup"><span data-stu-id="80678-151">Requirement</span></span> | <span data-ttu-id="80678-152">Valeur</span><span class="sxs-lookup"><span data-stu-id="80678-152">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="80678-153">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="80678-153">Minimum supported client</span></span><br/> | <span data-ttu-id="80678-154">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="80678-154">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="80678-155">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="80678-155">Minimum supported server</span></span><br/> | <span data-ttu-id="80678-156">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="80678-156">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="80678-157">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="80678-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80678-158">Éléments de schéma Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="80678-158">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="80678-159">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="80678-159">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





