---
title: Élément CalendarTrigger (triggerGroup)
description: Spécifie un déclencheur quotidien, hebdomadaire, mensuel ou un jour de la semaine (DOW) mensuel.
ms.assetid: 9b9218bf-222c-4ece-8b37-5c5d8b765015
keywords:
- Planificateur de tâches de déclencheur de calendrier, élément XML
- Élément CalendarTrigger Planificateur de tâches
topic_type:
- apiref
api_name:
- CalendarTrigger
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 02c061d8821dffa82eca8756ab26acadc6bb9281
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510338"
---
# <a name="calendartrigger-triggergroup-element"></a><span data-ttu-id="eb72d-105">Élément CalendarTrigger (triggerGroup)</span><span class="sxs-lookup"><span data-stu-id="eb72d-105">CalendarTrigger (triggerGroup) Element</span></span>

<span data-ttu-id="eb72d-106">Spécifie un déclencheur quotidien, hebdomadaire, mensuel ou un jour de la semaine (DOW) mensuel.</span><span class="sxs-lookup"><span data-stu-id="eb72d-106">Specifies a daily, weekly, monthly, or a monthly day-of-the-week (DOW) trigger.</span></span>

``` syntax
<xs:element name="CalendarTrigger"
    type="calendarTriggerType"
 />
```

<span data-ttu-id="eb72d-107">L’élément **CalendarTrigger** est défini par le type complexe [**calendarTriggerType**](taskschedulerschema-calendartriggertype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="eb72d-107">The **CalendarTrigger** element is defined by the [**calendarTriggerType**](taskschedulerschema-calendartriggertype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="eb72d-108">Élément parent</span><span class="sxs-lookup"><span data-stu-id="eb72d-108">Parent element</span></span>



| <span data-ttu-id="eb72d-109">Élément</span><span class="sxs-lookup"><span data-stu-id="eb72d-109">Element</span></span>                                                           | <span data-ttu-id="eb72d-110">Dérivé de</span><span class="sxs-lookup"><span data-stu-id="eb72d-110">Derived from</span></span>                                                         | <span data-ttu-id="eb72d-111">Description</span><span class="sxs-lookup"><span data-stu-id="eb72d-111">Description</span></span>                                            |
|-------------------------------------------------------------------|----------------------------------------------------------------------|--------------------------------------------------------|
| [<span data-ttu-id="eb72d-112">**Déclencheurs**</span><span class="sxs-lookup"><span data-stu-id="eb72d-112">**Triggers**</span></span>](taskschedulerschema-triggers-tasktype-element.md) | [<span data-ttu-id="eb72d-113">**triggersType**</span><span class="sxs-lookup"><span data-stu-id="eb72d-113">**triggersType**</span></span>](taskschedulerschema-triggerstype-complextype.md) | <span data-ttu-id="eb72d-114">Spécifie les déclencheurs qui démarrent la tâche.</span><span class="sxs-lookup"><span data-stu-id="eb72d-114">Specifies the triggers that start the task.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="eb72d-115">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="eb72d-115">Child elements</span></span>



| <span data-ttu-id="eb72d-116">Élément</span><span class="sxs-lookup"><span data-stu-id="eb72d-116">Element</span></span>                                                                                                                            | <span data-ttu-id="eb72d-117">Type</span><span class="sxs-lookup"><span data-stu-id="eb72d-117">Type</span></span>                                                                                                 | <span data-ttu-id="eb72d-118">Description</span><span class="sxs-lookup"><span data-stu-id="eb72d-118">Description</span></span>                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="eb72d-119">**Activé (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="eb72d-119">**Enabled (triggerBaseType)**</span></span>](taskschedulerschema-enabled-triggerbasetype-element.md)                                           | <span data-ttu-id="eb72d-120">boolean</span><span class="sxs-lookup"><span data-stu-id="eb72d-120">boolean</span></span>                                                                                              | <span data-ttu-id="eb72d-121">Spécifie que le déclencheur est activé.</span><span class="sxs-lookup"><span data-stu-id="eb72d-121">Specifies that the trigger is enabled.</span></span><br/>                                                                                  |
| [<span data-ttu-id="eb72d-122">**EndBoundary (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="eb72d-122">**EndBoundary (triggerBaseType)**</span></span>](taskschedulerschema-endboundary-triggerbasetype-element.md)                                   | <span data-ttu-id="eb72d-123">dateTime</span><span class="sxs-lookup"><span data-stu-id="eb72d-123">dateTime</span></span>                                                                                             | <span data-ttu-id="eb72d-124">Spécifie la date et l’heure de désactivation du déclencheur.</span><span class="sxs-lookup"><span data-stu-id="eb72d-124">Specifies the date and time when the trigger is deactivated.</span></span> <span data-ttu-id="eb72d-125">Le déclencheur ne peut pas démarrer la tâche une fois qu’elle est désactivée.</span><span class="sxs-lookup"><span data-stu-id="eb72d-125">The trigger cannot start the task after it is deactivated.</span></span><br/> |
| [<span data-ttu-id="eb72d-126">**ExecutionTimeLimit (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="eb72d-126">**ExecutionTimeLimit (triggerBaseType)**</span></span>](taskschedulerschema-executiontimelimit-triggerbasetype-element.md)                     | <span data-ttu-id="eb72d-127">duration</span><span class="sxs-lookup"><span data-stu-id="eb72d-127">duration</span></span>                                                                                             | <span data-ttu-id="eb72d-128">Spécifie la durée maximale pendant laquelle la tâche peut être démarrée par le déclencheur.</span><span class="sxs-lookup"><span data-stu-id="eb72d-128">Specifies the maximum amount of time in which the task can be started by the trigger.</span></span><br/>                                   |
| [<span data-ttu-id="eb72d-129">**Répétition (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="eb72d-129">**Repetition (triggerBaseType)**</span></span>](taskschedulerschema-repetition-triggerbasetype-element.md)                                     | [<span data-ttu-id="eb72d-130">**repetitionType**</span><span class="sxs-lookup"><span data-stu-id="eb72d-130">**repetitionType**</span></span>](taskschedulerschema-repetitiontype-complextype.md)                             | <span data-ttu-id="eb72d-131">Spécifie la fréquence d’exécution de la tâche et la durée de répétition du modèle de répétition après le démarrage de la tâche.</span><span class="sxs-lookup"><span data-stu-id="eb72d-131">Specifies how often the task is run and how long the repetition pattern is repeated after the task is started.</span></span><br/>          |
| [<span data-ttu-id="eb72d-132">**ScheduleByDay (calendarTriggerType)**</span><span class="sxs-lookup"><span data-stu-id="eb72d-132">**ScheduleByDay (calendarTriggerType)**</span></span>](taskschedulerschema-schedulebyday-calendartriggertype-element.md)                       | [<span data-ttu-id="eb72d-133">**dailyScheduleType**</span><span class="sxs-lookup"><span data-stu-id="eb72d-133">**dailyScheduleType**</span></span>](taskschedulerschema-dailyscheduletype-complextype.md)                       | <span data-ttu-id="eb72d-134">Spécifie une planification quotidienne.</span><span class="sxs-lookup"><span data-stu-id="eb72d-134">Specifies a daily schedule.</span></span><br/>                                                                                             |
| [<span data-ttu-id="eb72d-135">**ScheduleByMonth (calendarTriggerType)**</span><span class="sxs-lookup"><span data-stu-id="eb72d-135">**ScheduleByMonth (calendarTriggerType)**</span></span>](taskschedulerschema-schedulebymonth-calendartriggertype-element.md)                   | [<span data-ttu-id="eb72d-136">**monthlyScheduleType**</span><span class="sxs-lookup"><span data-stu-id="eb72d-136">**monthlyScheduleType**</span></span>](taskschedulerschema-monthlyscheduletype-complextype.md)                   | <span data-ttu-id="eb72d-137">Spécifie une planification mensuelle.</span><span class="sxs-lookup"><span data-stu-id="eb72d-137">Specifies a monthly schedule.</span></span><br/>                                                                                           |
| [<span data-ttu-id="eb72d-138">**ScheduleByMonthDayOfWeek (calendarTriggerType)**</span><span class="sxs-lookup"><span data-stu-id="eb72d-138">**ScheduleByMonthDayOfWeek (calendarTriggerType)**</span></span>](taskschedulerschema-schedulebymonthdayofweek-calendartriggertype-element.md) | [<span data-ttu-id="eb72d-139">**monthlyDayOfWeekScheduleType**</span><span class="sxs-lookup"><span data-stu-id="eb72d-139">**monthlyDayOfWeekScheduleType**</span></span>](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) | <span data-ttu-id="eb72d-140">Spécifie un déclencheur qui démarre un travail sur une planification de jour de semaine mensuelle.</span><span class="sxs-lookup"><span data-stu-id="eb72d-140">Specifies a trigger that starts a job on a monthly day-of-week schedule.</span></span><br/>                                                |
| [<span data-ttu-id="eb72d-141">**ScheduleByWeek (calendarTriggerType)**</span><span class="sxs-lookup"><span data-stu-id="eb72d-141">**ScheduleByWeek (calendarTriggerType)**</span></span>](taskschedulerschema-schedulebyweek-calendartriggertype-element.md)                     | [<span data-ttu-id="eb72d-142">**weeklyScheduleType**</span><span class="sxs-lookup"><span data-stu-id="eb72d-142">**weeklyScheduleType**</span></span>](taskschedulerschema-weeklyscheduletype-complextype.md)                     | <span data-ttu-id="eb72d-143">Spécifie une planification hebdomadaire.</span><span class="sxs-lookup"><span data-stu-id="eb72d-143">Specifies a weekly schedule.</span></span><br/>                                                                                            |
| [<span data-ttu-id="eb72d-144">**StartBoundary (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="eb72d-144">**StartBoundary (triggerBaseType)**</span></span>](taskschedulerschema-startboundary-triggerbasetype-element.md)                               | <span data-ttu-id="eb72d-145">dateTime</span><span class="sxs-lookup"><span data-stu-id="eb72d-145">dateTime</span></span>                                                                                             | <span data-ttu-id="eb72d-146">Spécifie la date et l’heure d’activation du déclencheur.</span><span class="sxs-lookup"><span data-stu-id="eb72d-146">Specifies the date and time when the trigger is activated.</span></span> <span data-ttu-id="eb72d-147">Cet élément est obligatoire.</span><span class="sxs-lookup"><span data-stu-id="eb72d-147">This element is required.</span></span><br/>                                    |



## <a name="attributes"></a><span data-ttu-id="eb72d-148">Attributs</span><span class="sxs-lookup"><span data-stu-id="eb72d-148">Attributes</span></span>



| <span data-ttu-id="eb72d-149">Nom</span><span class="sxs-lookup"><span data-stu-id="eb72d-149">Name</span></span> | <span data-ttu-id="eb72d-150">Type</span><span class="sxs-lookup"><span data-stu-id="eb72d-150">Type</span></span> | <span data-ttu-id="eb72d-151">Description</span><span class="sxs-lookup"><span data-stu-id="eb72d-151">Description</span></span>                               |
|------|------|-------------------------------------------|
| <span data-ttu-id="eb72d-152">Id</span><span class="sxs-lookup"><span data-stu-id="eb72d-152">Id</span></span>   | <span data-ttu-id="eb72d-153">id</span><span class="sxs-lookup"><span data-stu-id="eb72d-153">ID</span></span>   | <span data-ttu-id="eb72d-154">Identificateur du déclencheur.</span><span class="sxs-lookup"><span data-stu-id="eb72d-154">The identifier of the trigger.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="eb72d-155">Notes</span><span class="sxs-lookup"><span data-stu-id="eb72d-155">Remarks</span></span>

<span data-ttu-id="eb72d-156">L’élément [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) est un élément requis pour les déclencheurs de temps et de calendrier ([**timetrigger**](taskschedulerschema-timetrigger-triggergroup-element.md) et **CalendarTrigger**).</span><span class="sxs-lookup"><span data-stu-id="eb72d-156">The [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) element is a required element for time and calendar triggers ([**TimeTrigger**](taskschedulerschema-timetrigger-triggergroup-element.md) and **CalendarTrigger**).</span></span>

<span data-ttu-id="eb72d-157">Les éléments enfants répertoriés ci-dessus sont définis par les types d’éléments complexes [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) et [**calendarTriggerType**](taskschedulerschema-calendartriggertype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="eb72d-157">The child elements listed above are defined by the [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) and [**calendarTriggerType**](taskschedulerschema-calendartriggertype-complextype.md) complex element types.</span></span>

<span data-ttu-id="eb72d-158">Pour le développement de scripts, les déclencheurs de calendrier sont spécifiés à l’aide de l’un des objets suivants.</span><span class="sxs-lookup"><span data-stu-id="eb72d-158">For script development, calendar triggers are specified using one of the following objects.</span></span>

-   [<span data-ttu-id="eb72d-159">**DailyTrigger**</span><span class="sxs-lookup"><span data-stu-id="eb72d-159">**DailyTrigger**</span></span>](dailytrigger.md)
-   [<span data-ttu-id="eb72d-160">**WeeklyTrigger**</span><span class="sxs-lookup"><span data-stu-id="eb72d-160">**WeeklyTrigger**</span></span>](weeklytrigger.md)
-   [<span data-ttu-id="eb72d-161">**MonthlyTrigger**</span><span class="sxs-lookup"><span data-stu-id="eb72d-161">**MonthlyTrigger**</span></span>](monthlytrigger.md)
-   [<span data-ttu-id="eb72d-162">**MonthlyDOWTrigger**</span><span class="sxs-lookup"><span data-stu-id="eb72d-162">**MonthlyDOWTrigger**</span></span>](monthlydowtrigger.md)

<span data-ttu-id="eb72d-163">Pour le développement C++, les déclencheurs de calendrier sont spécifiés à l’aide de l’une des interfaces suivantes.</span><span class="sxs-lookup"><span data-stu-id="eb72d-163">For C++ development, calendar triggers are specified using one of the following interfaces.</span></span>

-   [<span data-ttu-id="eb72d-164">**IDailyTrigger**</span><span class="sxs-lookup"><span data-stu-id="eb72d-164">**IDailyTrigger**</span></span>](/windows/desktop/api/taskschd/nn-taskschd-idailytrigger)
-   [<span data-ttu-id="eb72d-165">**IWeeklyTrigger**</span><span class="sxs-lookup"><span data-stu-id="eb72d-165">**IWeeklyTrigger**</span></span>](/windows/desktop/api/taskschd/nn-taskschd-iweeklytrigger)
-   [<span data-ttu-id="eb72d-166">**IMonthlyTrigger**</span><span class="sxs-lookup"><span data-stu-id="eb72d-166">**IMonthlyTrigger**</span></span>](/windows/desktop/api/taskschd/nn-taskschd-imonthlytrigger)
-   [<span data-ttu-id="eb72d-167">**IMonthlyDOWTrigger**</span><span class="sxs-lookup"><span data-stu-id="eb72d-167">**IMonthlyDOWTrigger**</span></span>](/windows/desktop/api/taskschd/nn-taskschd-imonthlydowtrigger)

## <a name="examples"></a><span data-ttu-id="eb72d-168">Exemples</span><span class="sxs-lookup"><span data-stu-id="eb72d-168">Examples</span></span>

<span data-ttu-id="eb72d-169">Pour obtenir un exemple complet du code XML d’une tâche qui spécifie un déclencheur de calendrier, consultez [exemple de déclencheur quotidien (XML)](daily-trigger-example--xml-.md).</span><span class="sxs-lookup"><span data-stu-id="eb72d-169">For a complete example of the XML for a task that specifies a calendar trigger, see [Daily Trigger Example (XML)](daily-trigger-example--xml-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="eb72d-170">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="eb72d-170">Requirements</span></span>



| <span data-ttu-id="eb72d-171">Condition requise</span><span class="sxs-lookup"><span data-stu-id="eb72d-171">Requirement</span></span> | <span data-ttu-id="eb72d-172">Valeur</span><span class="sxs-lookup"><span data-stu-id="eb72d-172">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="eb72d-173">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="eb72d-173">Minimum supported client</span></span><br/> | <span data-ttu-id="eb72d-174">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="eb72d-174">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="eb72d-175">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="eb72d-175">Minimum supported server</span></span><br/> | <span data-ttu-id="eb72d-176">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="eb72d-176">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="eb72d-177">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="eb72d-177">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb72d-178">Éléments de schéma Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="eb72d-178">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="eb72d-179">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="eb72d-179">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





