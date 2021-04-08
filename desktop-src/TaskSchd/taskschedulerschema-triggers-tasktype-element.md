---
title: Élément Triggers (taskType)
description: Spécifie les déclencheurs qui démarrent la tâche.
ms.assetid: 4bf8e85e-3742-433d-821f-736fb2ff7139
keywords:
- Déclenche l’élément Planificateur de tâches
topic_type:
- apiref
api_name:
- Triggers
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 06994c395fbfbc5b0c6244c9d17930bc4afac885
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743756"
---
# <a name="triggers-tasktype-element"></a><span data-ttu-id="e9c7d-104">Élément Triggers (taskType)</span><span class="sxs-lookup"><span data-stu-id="e9c7d-104">Triggers (taskType) Element</span></span>

<span data-ttu-id="e9c7d-105">Spécifie les déclencheurs qui démarrent la tâche.</span><span class="sxs-lookup"><span data-stu-id="e9c7d-105">Specifies the triggers that start the task.</span></span>

``` syntax
<xs:element name="Triggers"
    type="triggersType"
 />
```

<span data-ttu-id="e9c7d-106">L’élément **triggers** est défini par le type complexe [**triggersType**](taskschedulerschema-triggerstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="e9c7d-106">The **Triggers** element is defined by the [**triggersType**](taskschedulerschema-triggerstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="e9c7d-107">Élément parent</span><span class="sxs-lookup"><span data-stu-id="e9c7d-107">Parent element</span></span>



| <span data-ttu-id="e9c7d-108">Élément</span><span class="sxs-lookup"><span data-stu-id="e9c7d-108">Element</span></span>                                          | <span data-ttu-id="e9c7d-109">Dérivé de</span><span class="sxs-lookup"><span data-stu-id="e9c7d-109">Derived from</span></span>                                                 | <span data-ttu-id="e9c7d-110">Description</span><span class="sxs-lookup"><span data-stu-id="e9c7d-110">Description</span></span>                                                                  |
|--------------------------------------------------|--------------------------------------------------------------|------------------------------------------------------------------------------|
| [<span data-ttu-id="e9c7d-111">**Tâche**</span><span class="sxs-lookup"><span data-stu-id="e9c7d-111">**Task**</span></span>](taskschedulerschema-task-element.md) | [<span data-ttu-id="e9c7d-112">**taskType**</span><span class="sxs-lookup"><span data-stu-id="e9c7d-112">**taskType**</span></span>](taskschedulerschema-tasktype-complextype.md) | <span data-ttu-id="e9c7d-113">Définit la tâche qui est effectuée par le service Planificateur de tâches.</span><span class="sxs-lookup"><span data-stu-id="e9c7d-113">Defines the task that is performed by the Task Scheduler service.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="e9c7d-114">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="e9c7d-114">Child elements</span></span>



| <span data-ttu-id="e9c7d-115">Élément</span><span class="sxs-lookup"><span data-stu-id="e9c7d-115">Element</span></span>                                                                                     | <span data-ttu-id="e9c7d-116">Type</span><span class="sxs-lookup"><span data-stu-id="e9c7d-116">Type</span></span>                                                                                       | <span data-ttu-id="e9c7d-117">Description</span><span class="sxs-lookup"><span data-stu-id="e9c7d-117">Description</span></span>                                                                                  |
|---------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e9c7d-118">**BootTrigger**</span><span class="sxs-lookup"><span data-stu-id="e9c7d-118">**BootTrigger**</span></span>](taskschedulerschema-boottrigger-triggergroup-element.md)                 | [<span data-ttu-id="e9c7d-119">**bootTriggerType**</span><span class="sxs-lookup"><span data-stu-id="e9c7d-119">**bootTriggerType**</span></span>](taskschedulerschema-boottriggertype-complextype.md)                 | <span data-ttu-id="e9c7d-120">Spécifie un déclencheur qui démarre une tâche au démarrage du système.</span><span class="sxs-lookup"><span data-stu-id="e9c7d-120">Specifies a trigger that starts a task when the system is booted.</span></span><br/>                 |
| [<span data-ttu-id="e9c7d-121">**CalendarTrigger**</span><span class="sxs-lookup"><span data-stu-id="e9c7d-121">**CalendarTrigger**</span></span>](taskschedulerschema-calendartrigger-triggergroup-element.md)         | [<span data-ttu-id="e9c7d-122">**calendarTriggerType**</span><span class="sxs-lookup"><span data-stu-id="e9c7d-122">**calendarTriggerType**</span></span>](taskschedulerschema-calendartriggertype-complextype.md)         | <span data-ttu-id="e9c7d-123">Spécifie un déclencheur quotidien, hebdomadaire, mensuel ou un jour de la semaine (DOW) mensuel.</span><span class="sxs-lookup"><span data-stu-id="e9c7d-123">Specifies a daily, weekly, monthly, or a monthly day-of-the-week (DOW) trigger.</span></span><br/>   |
| [<span data-ttu-id="e9c7d-124">**EventTrigger**</span><span class="sxs-lookup"><span data-stu-id="e9c7d-124">**EventTrigger**</span></span>](taskschedulerschema-eventtrigger-triggergroup-element.md)               | [<span data-ttu-id="e9c7d-125">**eventTriggerType**</span><span class="sxs-lookup"><span data-stu-id="e9c7d-125">**eventTriggerType**</span></span>](taskschedulerschema-eventtriggertype-complextype.md)               | <span data-ttu-id="e9c7d-126">Spécifie un déclencheur qui démarre une tâche lorsqu’un événement système se produit.</span><span class="sxs-lookup"><span data-stu-id="e9c7d-126">Specifies a trigger that starts a task when a system event occurs.</span></span><br/>                |
| [<span data-ttu-id="e9c7d-127">**IdleTrigger**</span><span class="sxs-lookup"><span data-stu-id="e9c7d-127">**IdleTrigger**</span></span>](taskschedulerschema-idletrigger-triggergroup-element.md)                 | [<span data-ttu-id="e9c7d-128">**idleTriggerType**</span><span class="sxs-lookup"><span data-stu-id="e9c7d-128">**idleTriggerType**</span></span>](taskschedulerschema-idletriggertype-complextype.md)                 | <span data-ttu-id="e9c7d-129">Spécifie un déclencheur qui démarre une tâche lorsque l’ordinateur passe en état d’inactivité.</span><span class="sxs-lookup"><span data-stu-id="e9c7d-129">Specifies a trigger that starts a task when the computer goes into an idle state.</span></span><br/> |
| [<span data-ttu-id="e9c7d-130">**LogonTrigger**</span><span class="sxs-lookup"><span data-stu-id="e9c7d-130">**LogonTrigger**</span></span>](taskschedulerschema-logontrigger-triggergroup-element.md)               | [<span data-ttu-id="e9c7d-131">**logonTriggerType**</span><span class="sxs-lookup"><span data-stu-id="e9c7d-131">**logonTriggerType**</span></span>](taskschedulerschema-logontriggertype-complextype.md)               | <span data-ttu-id="e9c7d-132">Spécifie un déclencheur qui démarre une tâche lorsqu’un utilisateur ouvre une session.</span><span class="sxs-lookup"><span data-stu-id="e9c7d-132">Specifies a trigger that starts a task when a user logs on.</span></span><br/>                       |
| [<span data-ttu-id="e9c7d-133">**RegistrationTrigger**</span><span class="sxs-lookup"><span data-stu-id="e9c7d-133">**RegistrationTrigger**</span></span>](taskschedulerschema-registrationtrigger-triggergroup-element.md) | [<span data-ttu-id="e9c7d-134">**registrationTriggerType**</span><span class="sxs-lookup"><span data-stu-id="e9c7d-134">**registrationTriggerType**</span></span>](taskschedulerschema-registrationtriggertype-complextype.md) | <span data-ttu-id="e9c7d-135">Spécifie un déclencheur qui démarre une tâche lorsque la tâche est inscrite.</span><span class="sxs-lookup"><span data-stu-id="e9c7d-135">Specifies a trigger that starts a task when the task is registered.</span></span><br/>               |
| [<span data-ttu-id="e9c7d-136">**TimeTrigger**</span><span class="sxs-lookup"><span data-stu-id="e9c7d-136">**TimeTrigger**</span></span>](taskschedulerschema-timetrigger-triggergroup-element.md)                 | [<span data-ttu-id="e9c7d-137">**timeTriggerType**</span><span class="sxs-lookup"><span data-stu-id="e9c7d-137">**timeTriggerType**</span></span>](taskschedulerschema-timetriggertype-complextype.md)                 | <span data-ttu-id="e9c7d-138">Spécifie un déclencheur qui démarre une tâche lorsque le déclencheur est activé.</span><span class="sxs-lookup"><span data-stu-id="e9c7d-138">Specifies a trigger that starts a task when the trigger is activated.</span></span><br/>             |



## <a name="remarks"></a><span data-ttu-id="e9c7d-139">Notes</span><span class="sxs-lookup"><span data-stu-id="e9c7d-139">Remarks</span></span>

<span data-ttu-id="e9c7d-140">Les éléments enfants listés ci-dessus peuvent être ajoutés dans n’importe quel ordre.</span><span class="sxs-lookup"><span data-stu-id="e9c7d-140">The child elements listed above can be added in any order.</span></span>

<span data-ttu-id="e9c7d-141">Pour le développement C++, les déclencheurs d’une tâche sont spécifiés à l’aide [**de la propriété triggers de ITaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_triggers).</span><span class="sxs-lookup"><span data-stu-id="e9c7d-141">For C++ development, the triggers of a task are specified using the [**Triggers property of ITaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_triggers).</span></span>

<span data-ttu-id="e9c7d-142">Pour le développement de scripts, les déclencheurs d’une tâche sont spécifiés à l’aide de la propriété [**TaskDefinition. Triggers**](taskdefinition-triggers.md) .</span><span class="sxs-lookup"><span data-stu-id="e9c7d-142">For scripting development, the triggers of a task are specified using the [**TaskDefinition.Triggers**](taskdefinition-triggers.md) property.</span></span>

## <a name="examples"></a><span data-ttu-id="e9c7d-143">Exemples</span><span class="sxs-lookup"><span data-stu-id="e9c7d-143">Examples</span></span>

<span data-ttu-id="e9c7d-144">Pour obtenir un exemple complet du code XML d’une tâche qui spécifie un déclencheur, consultez [exemple de déclencheur temporel (XML)](time-trigger-example--xml-.md).</span><span class="sxs-lookup"><span data-stu-id="e9c7d-144">For a complete example of the XML for a task that specifies a trigger, see [Time Trigger Example (XML)](time-trigger-example--xml-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e9c7d-145">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e9c7d-145">Requirements</span></span>



| <span data-ttu-id="e9c7d-146">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e9c7d-146">Requirement</span></span> | <span data-ttu-id="e9c7d-147">Valeur</span><span class="sxs-lookup"><span data-stu-id="e9c7d-147">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="e9c7d-148">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e9c7d-148">Minimum supported client</span></span><br/> | <span data-ttu-id="e9c7d-149">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e9c7d-149">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="e9c7d-150">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e9c7d-150">Minimum supported server</span></span><br/> | <span data-ttu-id="e9c7d-151">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e9c7d-151">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e9c7d-152">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e9c7d-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9c7d-153">Éléments de schéma Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="e9c7d-153">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="e9c7d-154">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="e9c7d-154">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





