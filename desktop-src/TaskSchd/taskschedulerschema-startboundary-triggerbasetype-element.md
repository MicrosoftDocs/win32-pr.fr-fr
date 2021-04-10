---
title: Élément StartBoundary (triggerBaseType)
description: Spécifie la date et l’heure d’activation du déclencheur.
ms.assetid: 95a62ae5-4eba-49df-a25f-0d1181772833
keywords:
- Élément StartBoundary Planificateur de tâches
topic_type:
- apiref
api_name:
- StartBoundary
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8d6adf90de2f3b199f98737996fe732f342787b6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103181"
---
# <a name="startboundary-triggerbasetype-element"></a><span data-ttu-id="9b328-104">Élément StartBoundary (triggerBaseType)</span><span class="sxs-lookup"><span data-stu-id="9b328-104">StartBoundary (triggerBaseType) Element</span></span>

<span data-ttu-id="9b328-105">Spécifie la date et l’heure d’activation du déclencheur.</span><span class="sxs-lookup"><span data-stu-id="9b328-105">Specifies the date and time when the trigger is activated.</span></span>

``` syntax
<xs:element name="StartBoundary"
    type="dateTime"
 />
```

<span data-ttu-id="9b328-106">L’élément **StartBoundary** est défini par le type complexe [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="9b328-106">The **StartBoundary** element is defined by the [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="9b328-107">Élément parent</span><span class="sxs-lookup"><span data-stu-id="9b328-107">Parent element</span></span>



| <span data-ttu-id="9b328-108">Élément</span><span class="sxs-lookup"><span data-stu-id="9b328-108">Element</span></span>                                                                                     | <span data-ttu-id="9b328-109">Dérivé de</span><span class="sxs-lookup"><span data-stu-id="9b328-109">Derived from</span></span>                                                                               | <span data-ttu-id="9b328-110">Description</span><span class="sxs-lookup"><span data-stu-id="9b328-110">Description</span></span>                                                                                  |
|---------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9b328-111">**BootTrigger**</span><span class="sxs-lookup"><span data-stu-id="9b328-111">**BootTrigger**</span></span>](taskschedulerschema-boottrigger-triggergroup-element.md)                 | [<span data-ttu-id="9b328-112">**bootTriggerType**</span><span class="sxs-lookup"><span data-stu-id="9b328-112">**bootTriggerType**</span></span>](taskschedulerschema-boottriggertype-complextype.md)                 | <span data-ttu-id="9b328-113">Spécifie un déclencheur qui démarre une tâche au démarrage du système.</span><span class="sxs-lookup"><span data-stu-id="9b328-113">Specifies a trigger that starts a task when the system is booted.</span></span><br/>                 |
| [<span data-ttu-id="9b328-114">**CalendarTrigger**</span><span class="sxs-lookup"><span data-stu-id="9b328-114">**CalendarTrigger**</span></span>](taskschedulerschema-calendartrigger-triggergroup-element.md)         | [<span data-ttu-id="9b328-115">**calendarTriggerType**</span><span class="sxs-lookup"><span data-stu-id="9b328-115">**calendarTriggerType**</span></span>](taskschedulerschema-calendartriggertype-complextype.md)         | <span data-ttu-id="9b328-116">Spécifie un déclencheur quotidien, hebdomadaire, mensuel ou un jour de la semaine (DOW) mensuel.</span><span class="sxs-lookup"><span data-stu-id="9b328-116">Specifies a daily, weekly, monthly, or a monthly day-of-the-week (DOW) trigger.</span></span><br/>   |
| [<span data-ttu-id="9b328-117">**EventTrigger**</span><span class="sxs-lookup"><span data-stu-id="9b328-117">**EventTrigger**</span></span>](taskschedulerschema-eventtrigger-triggergroup-element.md)               | [<span data-ttu-id="9b328-118">**eventTriggerType**</span><span class="sxs-lookup"><span data-stu-id="9b328-118">**eventTriggerType**</span></span>](taskschedulerschema-eventtriggertype-complextype.md)               | <span data-ttu-id="9b328-119">Spécifie un déclencheur qui démarre une tâche lorsqu’un événement système se produit.</span><span class="sxs-lookup"><span data-stu-id="9b328-119">Specifies a trigger that starts a task when a system event occurs.</span></span><br/>                |
| [<span data-ttu-id="9b328-120">**IdleTrigger**</span><span class="sxs-lookup"><span data-stu-id="9b328-120">**IdleTrigger**</span></span>](taskschedulerschema-idletrigger-triggergroup-element.md)                 | [<span data-ttu-id="9b328-121">**idleTriggerType**</span><span class="sxs-lookup"><span data-stu-id="9b328-121">**idleTriggerType**</span></span>](taskschedulerschema-idletriggertype-complextype.md)                 | <span data-ttu-id="9b328-122">Spécifie un déclencheur qui démarre une tâche lorsque l’ordinateur passe en état d’inactivité.</span><span class="sxs-lookup"><span data-stu-id="9b328-122">Specifies a trigger that starts a task when the computer goes into an idle state.</span></span><br/> |
| [<span data-ttu-id="9b328-123">**LogonTrigger**</span><span class="sxs-lookup"><span data-stu-id="9b328-123">**LogonTrigger**</span></span>](taskschedulerschema-logontrigger-triggergroup-element.md)               | [<span data-ttu-id="9b328-124">**logonTriggerType**</span><span class="sxs-lookup"><span data-stu-id="9b328-124">**logonTriggerType**</span></span>](taskschedulerschema-logontriggertype-complextype.md)               | <span data-ttu-id="9b328-125">Spécifie un déclencheur qui démarre une tâche lorsqu’un utilisateur ouvre une session.</span><span class="sxs-lookup"><span data-stu-id="9b328-125">Specifies a trigger that starts a task when a user logs on.</span></span><br/>                       |
| [<span data-ttu-id="9b328-126">**RegistrationTrigger**</span><span class="sxs-lookup"><span data-stu-id="9b328-126">**RegistrationTrigger**</span></span>](taskschedulerschema-registrationtrigger-triggergroup-element.md) | [<span data-ttu-id="9b328-127">**registrationTriggerType**</span><span class="sxs-lookup"><span data-stu-id="9b328-127">**registrationTriggerType**</span></span>](taskschedulerschema-registrationtriggertype-complextype.md) | <span data-ttu-id="9b328-128">Spécifie un déclencheur qui démarre une tâche lorsque la tâche est inscrite.</span><span class="sxs-lookup"><span data-stu-id="9b328-128">Specifies a trigger that starts a task when the task is registered.</span></span><br/>               |
| [<span data-ttu-id="9b328-129">**TimeTrigger**</span><span class="sxs-lookup"><span data-stu-id="9b328-129">**TimeTrigger**</span></span>](taskschedulerschema-timetrigger-triggergroup-element.md)                 | [<span data-ttu-id="9b328-130">**timeTriggerType**</span><span class="sxs-lookup"><span data-stu-id="9b328-130">**timeTriggerType**</span></span>](taskschedulerschema-timetriggertype-complextype.md)                 | <span data-ttu-id="9b328-131">Spécifie un déclencheur qui démarre une tâche lorsque le déclencheur est activé.</span><span class="sxs-lookup"><span data-stu-id="9b328-131">Specifies a trigger that starts a task when the trigger is activated.</span></span><br/>             |



## <a name="remarks"></a><span data-ttu-id="9b328-132">Notes</span><span class="sxs-lookup"><span data-stu-id="9b328-132">Remarks</span></span>

<span data-ttu-id="9b328-133">L' **<StartBoundary>** élément est un élément requis pour les déclencheurs de temps et de calendrier ( [**<TimeTrigger>**](taskschedulerschema-timetrigger-triggergroup-element.md) et [**<CalendarTrigger>**](taskschedulerschema-calendartrigger-triggergroup-element.md) ).</span><span class="sxs-lookup"><span data-stu-id="9b328-133">The **<StartBoundary>** element is a required element for time and calendar triggers ([**<TimeTrigger>**](taskschedulerschema-timetrigger-triggergroup-element.md) and [**<CalendarTrigger>**](taskschedulerschema-calendartrigger-triggergroup-element.md)).</span></span>

<span data-ttu-id="9b328-134">Pour le développement de script, la limite de fin est spécifiée à l’aide de la propriété [**Trigger. StartBoundary**](trigger-startboundary.md) qui est héritée par tous les objets déclencheurs.</span><span class="sxs-lookup"><span data-stu-id="9b328-134">For scripting development, the end boundary is specified using the [**Trigger.StartBoundary**](trigger-startboundary.md) property that is inherited by the all trigger objects.</span></span>

<span data-ttu-id="9b328-135">Pour le développement C++, la limite de fin est spécifiée à l’aide de la propriété [**ITrigger :: StartBoundary**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_startboundary) qui est héritée par les interfaces de déclencheur All.</span><span class="sxs-lookup"><span data-stu-id="9b328-135">For C++ development, the end boundary is specified using the [**ITrigger::StartBoundary**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_startboundary) property that is inherited by the all trigger interfaces.</span></span>

## <a name="examples"></a><span data-ttu-id="9b328-136">Exemples</span><span class="sxs-lookup"><span data-stu-id="9b328-136">Examples</span></span>

<span data-ttu-id="9b328-137">Le code XML suivant définit un élément de déclencheur de démarrage qui définit une limite de début du 1er janvier 2005:8:00 AM.</span><span class="sxs-lookup"><span data-stu-id="9b328-137">The following XML defines a boot trigger element that defines a start boundary of January 1, 2005: 8:00 AM.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="9b328-138">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9b328-138">Requirements</span></span>



| <span data-ttu-id="9b328-139">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9b328-139">Requirement</span></span> | <span data-ttu-id="9b328-140">Valeur</span><span class="sxs-lookup"><span data-stu-id="9b328-140">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="9b328-141">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9b328-141">Minimum supported client</span></span><br/> | <span data-ttu-id="9b328-142">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9b328-142">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="9b328-143">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9b328-143">Minimum supported server</span></span><br/> | <span data-ttu-id="9b328-144">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9b328-144">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9b328-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9b328-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b328-146">Éléments de schéma Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="9b328-146">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="9b328-147">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="9b328-147">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





