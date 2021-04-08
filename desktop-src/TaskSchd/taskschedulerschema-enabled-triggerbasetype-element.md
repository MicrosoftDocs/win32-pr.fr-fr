---
title: Élément Enabled (triggerBaseType)
description: Spécifie que le déclencheur est activé.
ms.assetid: 14c98f40-0ec5-4dc1-978e-b02c08ee2384
keywords:
- Élément activé Planificateur de tâches
topic_type:
- apiref
api_name:
- Enabled
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 42b495ba1af5f3b9b99034b0d6ca9d02040460c4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104033253"
---
# <a name="enabled-triggerbasetype-element"></a><span data-ttu-id="111ff-104">Élément Enabled (triggerBaseType)</span><span class="sxs-lookup"><span data-stu-id="111ff-104">Enabled (triggerBaseType) Element</span></span>

<span data-ttu-id="111ff-105">Spécifie que le déclencheur est activé.</span><span class="sxs-lookup"><span data-stu-id="111ff-105">Specifies that the trigger is enabled.</span></span>

``` syntax
<xs:element name="Enabled"
    type="boolean"
 />
```

<span data-ttu-id="111ff-106">L’élément **activé** est défini par le type complexe [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="111ff-106">The **Enabled** element is defined by the [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="111ff-107">Élément parent</span><span class="sxs-lookup"><span data-stu-id="111ff-107">Parent element</span></span>



| <span data-ttu-id="111ff-108">Élément</span><span class="sxs-lookup"><span data-stu-id="111ff-108">Element</span></span>                                                                                     | <span data-ttu-id="111ff-109">Dérivé de</span><span class="sxs-lookup"><span data-stu-id="111ff-109">Derived from</span></span>                                                                               | <span data-ttu-id="111ff-110">Description</span><span class="sxs-lookup"><span data-stu-id="111ff-110">Description</span></span>                                                                                  |
|---------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="111ff-111">**BootTrigger**</span><span class="sxs-lookup"><span data-stu-id="111ff-111">**BootTrigger**</span></span>](taskschedulerschema-boottrigger-triggergroup-element.md)                 | [<span data-ttu-id="111ff-112">**bootTriggerType**</span><span class="sxs-lookup"><span data-stu-id="111ff-112">**bootTriggerType**</span></span>](taskschedulerschema-boottriggertype-complextype.md)                 | <span data-ttu-id="111ff-113">Spécifie un déclencheur qui démarre une tâche au démarrage du système.</span><span class="sxs-lookup"><span data-stu-id="111ff-113">Specifies a trigger that starts a task when the system is booted.</span></span><br/>                 |
| [<span data-ttu-id="111ff-114">**CalendarTrigger**</span><span class="sxs-lookup"><span data-stu-id="111ff-114">**CalendarTrigger**</span></span>](taskschedulerschema-calendartrigger-triggergroup-element.md)         | [<span data-ttu-id="111ff-115">**calendarTriggerType**</span><span class="sxs-lookup"><span data-stu-id="111ff-115">**calendarTriggerType**</span></span>](taskschedulerschema-calendartriggertype-complextype.md)         | <span data-ttu-id="111ff-116">Spécifie un déclencheur quotidien, hebdomadaire, mensuel ou un jour de la semaine (DOW) mensuel.</span><span class="sxs-lookup"><span data-stu-id="111ff-116">Specifies a daily, weekly, monthly, or a monthly day-of-the-week (DOW) trigger.</span></span><br/>   |
| [<span data-ttu-id="111ff-117">**EventTrigger**</span><span class="sxs-lookup"><span data-stu-id="111ff-117">**EventTrigger**</span></span>](taskschedulerschema-eventtrigger-triggergroup-element.md)               | [<span data-ttu-id="111ff-118">**eventTriggerType**</span><span class="sxs-lookup"><span data-stu-id="111ff-118">**eventTriggerType**</span></span>](taskschedulerschema-eventtriggertype-complextype.md)               | <span data-ttu-id="111ff-119">Spécifie un déclencheur qui démarre une tâche lorsqu’un événement système se produit.</span><span class="sxs-lookup"><span data-stu-id="111ff-119">Specifies a trigger that starts a task when a system event occurs.</span></span><br/>                |
| [<span data-ttu-id="111ff-120">**IdleTrigger**</span><span class="sxs-lookup"><span data-stu-id="111ff-120">**IdleTrigger**</span></span>](taskschedulerschema-idletrigger-triggergroup-element.md)                 | [<span data-ttu-id="111ff-121">**idleTriggerType**</span><span class="sxs-lookup"><span data-stu-id="111ff-121">**idleTriggerType**</span></span>](taskschedulerschema-idletriggertype-complextype.md)                 | <span data-ttu-id="111ff-122">Spécifie un déclencheur qui démarre une tâche lorsque l’ordinateur passe en état d’inactivité.</span><span class="sxs-lookup"><span data-stu-id="111ff-122">Specifies a trigger that starts a task when the computer goes into an idle state.</span></span><br/> |
| [<span data-ttu-id="111ff-123">**LogonTrigger**</span><span class="sxs-lookup"><span data-stu-id="111ff-123">**LogonTrigger**</span></span>](taskschedulerschema-logontrigger-triggergroup-element.md)               | [<span data-ttu-id="111ff-124">**logonTriggerType**</span><span class="sxs-lookup"><span data-stu-id="111ff-124">**logonTriggerType**</span></span>](taskschedulerschema-logontriggertype-complextype.md)               | <span data-ttu-id="111ff-125">Spécifie un déclencheur qui démarre une tâche lorsqu’un utilisateur ouvre une session.</span><span class="sxs-lookup"><span data-stu-id="111ff-125">Specifies a trigger that starts a task when a user logs on.</span></span><br/>                       |
| [<span data-ttu-id="111ff-126">**RegistrationTrigger**</span><span class="sxs-lookup"><span data-stu-id="111ff-126">**RegistrationTrigger**</span></span>](taskschedulerschema-registrationtrigger-triggergroup-element.md) | [<span data-ttu-id="111ff-127">**registrationTriggerType**</span><span class="sxs-lookup"><span data-stu-id="111ff-127">**registrationTriggerType**</span></span>](taskschedulerschema-registrationtriggertype-complextype.md) | <span data-ttu-id="111ff-128">Spécifie un déclencheur qui démarre une tâche lorsque la tâche est inscrite.</span><span class="sxs-lookup"><span data-stu-id="111ff-128">Specifies a trigger that starts a task when the task is registered.</span></span><br/>               |
| [<span data-ttu-id="111ff-129">**TimeTrigger**</span><span class="sxs-lookup"><span data-stu-id="111ff-129">**TimeTrigger**</span></span>](taskschedulerschema-timetrigger-triggergroup-element.md)                 | [<span data-ttu-id="111ff-130">**timeTriggerType**</span><span class="sxs-lookup"><span data-stu-id="111ff-130">**timeTriggerType**</span></span>](taskschedulerschema-timetriggertype-complextype.md)                 | <span data-ttu-id="111ff-131">Spécifie un déclencheur qui démarre une tâche lorsque le déclencheur est activé.</span><span class="sxs-lookup"><span data-stu-id="111ff-131">Specifies a trigger that starts a task when the trigger is activated.</span></span><br/>             |



## <a name="remarks"></a><span data-ttu-id="111ff-132">Notes</span><span class="sxs-lookup"><span data-stu-id="111ff-132">Remarks</span></span>

<span data-ttu-id="111ff-133">Pour le développement de script, ces informations sont accessibles par le biais de la propriété [**déclencheur. Enabled**](trigger-enabled.md) qui est héritée par tous les objets déclencheurs.</span><span class="sxs-lookup"><span data-stu-id="111ff-133">For scripting development, this information is accessed through the [**Trigger.Enabled**](trigger-enabled.md) property that is inherited by the all trigger objects.</span></span>

<span data-ttu-id="111ff-134">Pour le développement C++, ces informations sont accessibles via la propriété [**ITrigger :: Enabled**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_enabled) qui est héritée par les interfaces de déclencheur All.</span><span class="sxs-lookup"><span data-stu-id="111ff-134">For C++ development, this information is accessed through the [**ITrigger::Enabled**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_enabled) property that is inherited by the all trigger interfaces.</span></span>

## <a name="requirements"></a><span data-ttu-id="111ff-135">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="111ff-135">Requirements</span></span>



| <span data-ttu-id="111ff-136">Condition requise</span><span class="sxs-lookup"><span data-stu-id="111ff-136">Requirement</span></span> | <span data-ttu-id="111ff-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="111ff-137">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="111ff-138">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="111ff-138">Minimum supported client</span></span><br/> | <span data-ttu-id="111ff-139">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="111ff-139">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="111ff-140">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="111ff-140">Minimum supported server</span></span><br/> | <span data-ttu-id="111ff-141">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="111ff-141">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="111ff-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="111ff-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="111ff-143">Éléments de schéma Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="111ff-143">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="111ff-144">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="111ff-144">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





