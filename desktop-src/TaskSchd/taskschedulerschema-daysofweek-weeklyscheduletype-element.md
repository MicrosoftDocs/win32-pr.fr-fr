---
title: DaysOfWeek (weeklyScheduleType) (élément)
description: Spécifie les jours de la semaine d’exécution de la tâche. | DaysOfWeek (weeklyScheduleType) (élément)
ms.assetid: 86555681-2324-4095-9eab-fdef40e0acba
keywords:
- DaysOfWeek, élément Planificateur de tâches
topic_type:
- apiref
api_name:
- DaysOfWeek
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3a2b310feb49f3141d1f7f08c4552305f9ffc3ea
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106532404"
---
# <a name="daysofweek-weeklyscheduletype-element"></a><span data-ttu-id="26323-105">DaysOfWeek (weeklyScheduleType) (élément)</span><span class="sxs-lookup"><span data-stu-id="26323-105">DaysOfWeek (weeklyScheduleType) Element</span></span>

<span data-ttu-id="26323-106">Spécifie les jours de la semaine d’exécution de la tâche.</span><span class="sxs-lookup"><span data-stu-id="26323-106">Specifies the days of the week in which the task runs.</span></span>

``` syntax
<xs:element name="DaysOfWeek"
    type="daysOfWeekType"
 />
```

<span data-ttu-id="26323-107">L’élément **DaysOfWeek** est défini par le type complexe [**weeklyScheduleType**](taskschedulerschema-weeklyscheduletype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="26323-107">The **DaysOfWeek** element is defined by the [**weeklyScheduleType**](taskschedulerschema-weeklyscheduletype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="26323-108">Élément parent</span><span class="sxs-lookup"><span data-stu-id="26323-108">Parent element</span></span>



| <span data-ttu-id="26323-109">Élément</span><span class="sxs-lookup"><span data-stu-id="26323-109">Element</span></span>                                                                                  | <span data-ttu-id="26323-110">Dérivé de</span><span class="sxs-lookup"><span data-stu-id="26323-110">Derived from</span></span>                                                                     | <span data-ttu-id="26323-111">Description</span><span class="sxs-lookup"><span data-stu-id="26323-111">Description</span></span>                             |
|------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|-----------------------------------------|
| [<span data-ttu-id="26323-112">**ScheduleByWeek**</span><span class="sxs-lookup"><span data-stu-id="26323-112">**ScheduleByWeek**</span></span>](taskschedulerschema-schedulebyweek-calendartriggertype-element.md) | [<span data-ttu-id="26323-113">**weeklyScheduleType**</span><span class="sxs-lookup"><span data-stu-id="26323-113">**weeklyScheduleType**</span></span>](taskschedulerschema-weeklyscheduletype-complextype.md) | <span data-ttu-id="26323-114">Spécifie une planification hebdomadaire.</span><span class="sxs-lookup"><span data-stu-id="26323-114">Specifies a weekly schedule.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="26323-115">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="26323-115">Child elements</span></span>



| <span data-ttu-id="26323-116">Élément</span><span class="sxs-lookup"><span data-stu-id="26323-116">Element</span></span>                                                                   | <span data-ttu-id="26323-117">Type</span><span class="sxs-lookup"><span data-stu-id="26323-117">Type</span></span> | <span data-ttu-id="26323-118">Description</span><span class="sxs-lookup"><span data-stu-id="26323-118">Description</span></span>                                           |
|---------------------------------------------------------------------------|------|-------------------------------------------------------|
| [<span data-ttu-id="26323-119">**Vendredi**</span><span class="sxs-lookup"><span data-stu-id="26323-119">**Friday**</span></span>](taskschedulerschema-friday-daysofweektype-element.md)       |      | <span data-ttu-id="26323-120">Spécifie que la tâche est exécutée le vendredi.</span><span class="sxs-lookup"><span data-stu-id="26323-120">Specifies that the task runs on Friday.</span></span><br/>    |
| [<span data-ttu-id="26323-121">**Monday**</span><span class="sxs-lookup"><span data-stu-id="26323-121">**Monday**</span></span>](taskschedulerschema-monday-daysofweektype-element.md)       |      | <span data-ttu-id="26323-122">Spécifie que la tâche est exécutée le lundi.</span><span class="sxs-lookup"><span data-stu-id="26323-122">Specifies that the task runs on Monday.</span></span><br/>    |
| [<span data-ttu-id="26323-123">**Samedi**</span><span class="sxs-lookup"><span data-stu-id="26323-123">**Saturday**</span></span>](taskschedulerschema-saturday-daysofweektype-element.md)   |      | <span data-ttu-id="26323-124">Spécifie que la tâche est exécutée le samedi.</span><span class="sxs-lookup"><span data-stu-id="26323-124">Specifies that the task runs on Saturday.</span></span><br/>  |
| [<span data-ttu-id="26323-125">**Dimanche**</span><span class="sxs-lookup"><span data-stu-id="26323-125">**Sunday**</span></span>](taskschedulerschema-sunday-daysofweektype-element.md)       |      | <span data-ttu-id="26323-126">Spécifie que la tâche est exécutée le dimanche.</span><span class="sxs-lookup"><span data-stu-id="26323-126">Specifies that the task runs on Sunday.</span></span><br/>    |
| [<span data-ttu-id="26323-127">**Thursday**</span><span class="sxs-lookup"><span data-stu-id="26323-127">**Thursday**</span></span>](taskschedulerschema-thursday-daysofweektype-element.md)   |      | <span data-ttu-id="26323-128">Spécifie que la tâche est exécutée le jeudi.</span><span class="sxs-lookup"><span data-stu-id="26323-128">Specifies that the task runs on Thursday.</span></span><br/>  |
| [<span data-ttu-id="26323-129">**Mardi**</span><span class="sxs-lookup"><span data-stu-id="26323-129">**Tuesday**</span></span>](taskschedulerschema-tuesday-daysofweektype-element.md)     |      | <span data-ttu-id="26323-130">Spécifie que la tâche est exécutée le mardi.</span><span class="sxs-lookup"><span data-stu-id="26323-130">Specifies that the task runs on Tuesday.</span></span><br/>   |
| [<span data-ttu-id="26323-131">**Mercredi**</span><span class="sxs-lookup"><span data-stu-id="26323-131">**Wednesday**</span></span>](taskschedulerschema-wednesday-daysofweektype-element.md) |      | <span data-ttu-id="26323-132">Spécifie que la tâche est exécutée le mercredi.</span><span class="sxs-lookup"><span data-stu-id="26323-132">Specifies that the task runs on Wednesday.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="26323-133">Notes</span><span class="sxs-lookup"><span data-stu-id="26323-133">Remarks</span></span>

<span data-ttu-id="26323-134">Les éléments enfants précédents sont définis par le type complexe [**daysOfWeekType**](taskschedulerschema-daysofweektype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="26323-134">The previous child elements are defined by the [**daysOfWeekType**](taskschedulerschema-daysofweektype-complextype.md) complex type.</span></span>

<span data-ttu-id="26323-135">Pour le développement de script, l’intervalle hebdomadaire est spécifié à l’aide de la propriété [**WeeklyTrigger. WeeksInterval**](weeklytrigger-weeksinterval.md) .</span><span class="sxs-lookup"><span data-stu-id="26323-135">For scripting development, the weekly interval is specified using the [**WeeklyTrigger.WeeksInterval**](weeklytrigger-weeksinterval.md) property.</span></span>

<span data-ttu-id="26323-136">Pour le développement C++, l’intervalle hebdomadaire est spécifié à l’aide de la propriété [**IWeeklyTrigger :: WeeksInterval**](/windows/desktop/api/taskschd/nf-taskschd-iweeklytrigger-get_weeksinterval) .</span><span class="sxs-lookup"><span data-stu-id="26323-136">For C++ development, the weekly interval is specified using the [**IWeeklyTrigger::WeeksInterval**](/windows/desktop/api/taskschd/nf-taskschd-iweeklytrigger-get_weeksinterval) property.</span></span>

## <a name="examples"></a><span data-ttu-id="26323-137">Exemples</span><span class="sxs-lookup"><span data-stu-id="26323-137">Examples</span></span>

<span data-ttu-id="26323-138">Le code XML suivant définit un déclencheur de calendrier quotidien qui démarre une tâche du lundi au vendredi (à 8:00 AM) chaque semaine.</span><span class="sxs-lookup"><span data-stu-id="26323-138">The following XML defines a daily calendar trigger that starts a task Monday through Friday ( at 8:00 AM) every week.</span></span>


```XML
<CalendarTrigger>
    <StartBoundary>2005-01-01T08:00:00</StartBoundary>
    <EndBounadry>2007-01-01T00:00:00</EndBoundary>
    <ScheduleByWeek>
        <WeeksInterval>1</WeeksInterval>
        <DaysOfWeek>
            <Monday/>
            <Tuesday/>
            <Wednesday/>
            <Thurday/>
            <Friday/>
        </DaysOfWeek>
    </ScheduleByWeek>
</CalendarTrigger>
```



<span data-ttu-id="26323-139">Pour obtenir un exemple complet du code XML d’une tâche qui utilise un déclencheur hebdomadaire, consultez [exemple de déclencheur hebdomadaire (XML)](weekly-trigger-example--xml-.md).</span><span class="sxs-lookup"><span data-stu-id="26323-139">For a complete example of the XML for a task that uses a weekly trigger, see [Weekly Trigger Example (XML)](weekly-trigger-example--xml-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="26323-140">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="26323-140">Requirements</span></span>



| <span data-ttu-id="26323-141">Condition requise</span><span class="sxs-lookup"><span data-stu-id="26323-141">Requirement</span></span> | <span data-ttu-id="26323-142">Valeur</span><span class="sxs-lookup"><span data-stu-id="26323-142">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="26323-143">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="26323-143">Minimum supported client</span></span><br/> | <span data-ttu-id="26323-144">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="26323-144">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="26323-145">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="26323-145">Minimum supported server</span></span><br/> | <span data-ttu-id="26323-146">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="26323-146">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="26323-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="26323-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26323-148">Éléments de schéma Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="26323-148">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="26323-149">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="26323-149">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





