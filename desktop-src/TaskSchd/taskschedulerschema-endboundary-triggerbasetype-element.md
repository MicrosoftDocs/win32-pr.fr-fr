---
title: Élément EndBoundary (triggerBaseType)
description: Spécifie la date et l’heure de désactivation du déclencheur. Le déclencheur ne peut pas démarrer la tâche une fois qu’elle est désactivée.
ms.assetid: 84731c0b-3fb8-44dd-be1a-67547add1f9e
keywords:
- Élément EndBoundary Planificateur de tâches
topic_type:
- apiref
api_name:
- EndBoundary
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d687655498301595c1ab888fcc179ec0694f0aef
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510738"
---
# <a name="endboundary-triggerbasetype-element"></a><span data-ttu-id="72e21-105">Élément EndBoundary (triggerBaseType)</span><span class="sxs-lookup"><span data-stu-id="72e21-105">EndBoundary (triggerBaseType) Element</span></span>

<span data-ttu-id="72e21-106">Spécifie la date et l’heure de désactivation du déclencheur.</span><span class="sxs-lookup"><span data-stu-id="72e21-106">Specifies the date and time when the trigger is deactivated.</span></span> <span data-ttu-id="72e21-107">Le déclencheur ne peut pas démarrer la tâche une fois qu’elle est désactivée.</span><span class="sxs-lookup"><span data-stu-id="72e21-107">The trigger cannot start the task after it is deactivated.</span></span>

``` syntax
<xs:element name="EndBoundary"
    type="dateTime"
 />
```

<span data-ttu-id="72e21-108">L’élément **EndBoundary** est défini par le type complexe [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="72e21-108">The **EndBoundary** element is defined by the [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="72e21-109">Élément parent</span><span class="sxs-lookup"><span data-stu-id="72e21-109">Parent element</span></span>



| <span data-ttu-id="72e21-110">Élément</span><span class="sxs-lookup"><span data-stu-id="72e21-110">Element</span></span>                                                                                     | <span data-ttu-id="72e21-111">Dérivé de</span><span class="sxs-lookup"><span data-stu-id="72e21-111">Derived from</span></span>                                                                               | <span data-ttu-id="72e21-112">Description</span><span class="sxs-lookup"><span data-stu-id="72e21-112">Description</span></span>                                                                                  |
|---------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="72e21-113">**BootTrigger**</span><span class="sxs-lookup"><span data-stu-id="72e21-113">**BootTrigger**</span></span>](taskschedulerschema-boottrigger-triggergroup-element.md)                 | [<span data-ttu-id="72e21-114">**bootTriggerType**</span><span class="sxs-lookup"><span data-stu-id="72e21-114">**bootTriggerType**</span></span>](taskschedulerschema-boottriggertype-complextype.md)                 | <span data-ttu-id="72e21-115">Spécifie un déclencheur qui démarre une tâche au démarrage du système.</span><span class="sxs-lookup"><span data-stu-id="72e21-115">Specifies a trigger that starts a task when the system is booted.</span></span><br/>                 |
| [<span data-ttu-id="72e21-116">**CalendarTrigger**</span><span class="sxs-lookup"><span data-stu-id="72e21-116">**CalendarTrigger**</span></span>](taskschedulerschema-calendartrigger-triggergroup-element.md)         | [<span data-ttu-id="72e21-117">**calendarTriggerType**</span><span class="sxs-lookup"><span data-stu-id="72e21-117">**calendarTriggerType**</span></span>](taskschedulerschema-calendartriggertype-complextype.md)         | <span data-ttu-id="72e21-118">Spécifie un déclencheur quotidien, hebdomadaire, mensuel ou un jour de la semaine (DOW) mensuel.</span><span class="sxs-lookup"><span data-stu-id="72e21-118">Specifies a daily, weekly, monthly, or a monthly day-of-the-week (DOW) trigger.</span></span><br/>   |
| [<span data-ttu-id="72e21-119">**EventTrigger**</span><span class="sxs-lookup"><span data-stu-id="72e21-119">**EventTrigger**</span></span>](taskschedulerschema-eventtrigger-triggergroup-element.md)               | [<span data-ttu-id="72e21-120">**eventTriggerType**</span><span class="sxs-lookup"><span data-stu-id="72e21-120">**eventTriggerType**</span></span>](taskschedulerschema-eventtriggertype-complextype.md)               | <span data-ttu-id="72e21-121">Spécifie un déclencheur qui démarre une tâche lorsqu’un événement système se produit.</span><span class="sxs-lookup"><span data-stu-id="72e21-121">Specifies a trigger that starts a task when a system event occurs.</span></span><br/>                |
| [<span data-ttu-id="72e21-122">**IdleTrigger**</span><span class="sxs-lookup"><span data-stu-id="72e21-122">**IdleTrigger**</span></span>](taskschedulerschema-idletrigger-triggergroup-element.md)                 | [<span data-ttu-id="72e21-123">**idleTriggerType**</span><span class="sxs-lookup"><span data-stu-id="72e21-123">**idleTriggerType**</span></span>](taskschedulerschema-idletriggertype-complextype.md)                 | <span data-ttu-id="72e21-124">Spécifie un déclencheur qui démarre une tâche lorsque l’ordinateur passe en état d’inactivité.</span><span class="sxs-lookup"><span data-stu-id="72e21-124">Specifies a trigger that starts a task when the computer goes into an idle state.</span></span><br/> |
| [<span data-ttu-id="72e21-125">**LogonTrigger**</span><span class="sxs-lookup"><span data-stu-id="72e21-125">**LogonTrigger**</span></span>](taskschedulerschema-logontrigger-triggergroup-element.md)               | [<span data-ttu-id="72e21-126">**logonTriggerType**</span><span class="sxs-lookup"><span data-stu-id="72e21-126">**logonTriggerType**</span></span>](taskschedulerschema-logontriggertype-complextype.md)               | <span data-ttu-id="72e21-127">Spécifie un déclencheur qui démarre une tâche lorsqu’un utilisateur ouvre une session.</span><span class="sxs-lookup"><span data-stu-id="72e21-127">Specifies a trigger that starts a task when a user logs on.</span></span><br/>                       |
| [<span data-ttu-id="72e21-128">**RegistrationTrigger**</span><span class="sxs-lookup"><span data-stu-id="72e21-128">**RegistrationTrigger**</span></span>](taskschedulerschema-registrationtrigger-triggergroup-element.md) | [<span data-ttu-id="72e21-129">**registrationTriggerType**</span><span class="sxs-lookup"><span data-stu-id="72e21-129">**registrationTriggerType**</span></span>](taskschedulerschema-registrationtriggertype-complextype.md) | <span data-ttu-id="72e21-130">Spécifie un déclencheur qui démarre une tâche lorsque la tâche est inscrite.</span><span class="sxs-lookup"><span data-stu-id="72e21-130">Specifies a trigger that starts a task when the task is registered.</span></span><br/>               |
| [<span data-ttu-id="72e21-131">**TimeTrigger**</span><span class="sxs-lookup"><span data-stu-id="72e21-131">**TimeTrigger**</span></span>](taskschedulerschema-timetrigger-triggergroup-element.md)                 | [<span data-ttu-id="72e21-132">**timeTriggerType**</span><span class="sxs-lookup"><span data-stu-id="72e21-132">**timeTriggerType**</span></span>](taskschedulerschema-timetriggertype-complextype.md)                 | <span data-ttu-id="72e21-133">Spécifie un déclencheur qui démarre une tâche lorsque le déclencheur est activé.</span><span class="sxs-lookup"><span data-stu-id="72e21-133">Specifies a trigger that starts a task when the trigger is activated.</span></span><br/>             |



## <a name="remarks"></a><span data-ttu-id="72e21-134">Notes</span><span class="sxs-lookup"><span data-stu-id="72e21-134">Remarks</span></span>

<span data-ttu-id="72e21-135">Pour le développement de script, la limite de fin est spécifiée à l’aide de la propriété [**Trigger. EndBoundary**](trigger-endboundary.md) qui est héritée par tous les objets déclencheurs.</span><span class="sxs-lookup"><span data-stu-id="72e21-135">For scripting development, the end boundary is specified using the [**Trigger.EndBoundary**](trigger-endboundary.md) property that is inherited by the all trigger objects.</span></span>

<span data-ttu-id="72e21-136">Pour le développement C++, la limite de fin est spécifiée à l’aide de la propriété [**ITrigger :: EndBoundary**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_endboundary) qui est héritée par les interfaces de déclencheur All.</span><span class="sxs-lookup"><span data-stu-id="72e21-136">For C++ development, the end boundary is specified using the [**ITrigger::EndBoundary**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_endboundary) property that is inherited by the all trigger interfaces.</span></span>

## <a name="examples"></a><span data-ttu-id="72e21-137">Exemples</span><span class="sxs-lookup"><span data-stu-id="72e21-137">Examples</span></span>

<span data-ttu-id="72e21-138">Le code XML suivant définit un élément de déclencheur de démarrage qui définit une limite de fin du 1er janvier 2007:8:00 AM.</span><span class="sxs-lookup"><span data-stu-id="72e21-138">The following XML defines a boot trigger element that defines an end boundary of January 1, 2007: 8:00 AM.</span></span>


```XML
<BootTrigger>
    <StartBoundary>2005-01-01T08:00:00</StartBoundary>
    <EndBounadry>2007-01-01T08:00:00</EndBoundary>
    <Enabled>true</Enabled>
    <Repetition></Repetition>
    <ExecutionTimeLimit></ExecutionTimeLimit>
    <Delay><Delay>
 </BootTrigger>
```



## <a name="requirements"></a><span data-ttu-id="72e21-139">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="72e21-139">Requirements</span></span>



| <span data-ttu-id="72e21-140">Condition requise</span><span class="sxs-lookup"><span data-stu-id="72e21-140">Requirement</span></span> | <span data-ttu-id="72e21-141">Valeur</span><span class="sxs-lookup"><span data-stu-id="72e21-141">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="72e21-142">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="72e21-142">Minimum supported client</span></span><br/> | <span data-ttu-id="72e21-143">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="72e21-143">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="72e21-144">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="72e21-144">Minimum supported server</span></span><br/> | <span data-ttu-id="72e21-145">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="72e21-145">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="72e21-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="72e21-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72e21-147">Éléments de schéma Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="72e21-147">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="72e21-148">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="72e21-148">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





