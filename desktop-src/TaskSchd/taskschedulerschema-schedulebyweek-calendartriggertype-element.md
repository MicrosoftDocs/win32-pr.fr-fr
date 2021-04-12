---
title: Élément ScheduleByWeek (calendarTriggerType)
description: Spécifie une planification hebdomadaire.
ms.assetid: d2c33e76-0564-4b3c-ab86-e7bca667fa4f
keywords:
- déclencheur hebdomadaire Planificateur de tâches, élément XML
- Élément ScheduleByWeek Planificateur de tâches
topic_type:
- apiref
api_name:
- ScheduleByWeek
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2d5ab62a0c39c4c1d0102edcdb96d310e9315820
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104385183"
---
# <a name="schedulebyweek-calendartriggertype-element"></a><span data-ttu-id="c40a9-105">Élément ScheduleByWeek (calendarTriggerType)</span><span class="sxs-lookup"><span data-stu-id="c40a9-105">ScheduleByWeek (calendarTriggerType) Element</span></span>

<span data-ttu-id="c40a9-106">Spécifie une planification hebdomadaire.</span><span class="sxs-lookup"><span data-stu-id="c40a9-106">Specifies a weekly schedule.</span></span> <span data-ttu-id="c40a9-107">Par exemple, la tâche commence à 8:00 AM un jour spécifique de la semaine chaque semaine ou un jour spécifique de la semaine chaque semaine.</span><span class="sxs-lookup"><span data-stu-id="c40a9-107">For example, the task starts at 8:00 AM on a specific day of the week every week or on a specific day of the week every other week.</span></span>

``` syntax
<xs:element name="ScheduleByWeek"
    type="weeklyScheduleType"
 />
```

<span data-ttu-id="c40a9-108">L’élément **ScheduleByWeek** est défini par le type complexe [**calendarTriggerType**](taskschedulerschema-calendartriggertype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="c40a9-108">The **ScheduleByWeek** element is defined by the [**calendarTriggerType**](taskschedulerschema-calendartriggertype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="c40a9-109">Élément parent</span><span class="sxs-lookup"><span data-stu-id="c40a9-109">Parent element</span></span>



| <span data-ttu-id="c40a9-110">Élément</span><span class="sxs-lookup"><span data-stu-id="c40a9-110">Element</span></span>                                                                             | <span data-ttu-id="c40a9-111">Dérivé de</span><span class="sxs-lookup"><span data-stu-id="c40a9-111">Derived from</span></span>                                                                       | <span data-ttu-id="c40a9-112">Description</span><span class="sxs-lookup"><span data-stu-id="c40a9-112">Description</span></span>                                                                                |
|-------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c40a9-113">**CalendarTrigger**</span><span class="sxs-lookup"><span data-stu-id="c40a9-113">**CalendarTrigger**</span></span>](taskschedulerschema-calendartrigger-triggergroup-element.md) | [<span data-ttu-id="c40a9-114">**calendarTriggerType**</span><span class="sxs-lookup"><span data-stu-id="c40a9-114">**calendarTriggerType**</span></span>](taskschedulerschema-calendartriggertype-complextype.md) | <span data-ttu-id="c40a9-115">Spécifie un déclencheur quotidien, hebdomadaire, mensuel ou un jour de la semaine (DOW) mensuel.</span><span class="sxs-lookup"><span data-stu-id="c40a9-115">Specifies a daily, weekly, monthly, or a monthly day-of-the-week (DOW) trigger.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="c40a9-116">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="c40a9-116">Child elements</span></span>



| <span data-ttu-id="c40a9-117">Élément</span><span class="sxs-lookup"><span data-stu-id="c40a9-117">Element</span></span>                                                                               | <span data-ttu-id="c40a9-118">Type</span><span class="sxs-lookup"><span data-stu-id="c40a9-118">Type</span></span>                                                                     | <span data-ttu-id="c40a9-119">Description</span><span class="sxs-lookup"><span data-stu-id="c40a9-119">Description</span></span>                                                          |
|---------------------------------------------------------------------------------------|--------------------------------------------------------------------------|----------------------------------------------------------------------|
| [<span data-ttu-id="c40a9-120">**DaysOfWeek**</span><span class="sxs-lookup"><span data-stu-id="c40a9-120">**DaysOfWeek**</span></span>](taskschedulerschema-daysofweek-weeklyscheduletype-element.md)       | [<span data-ttu-id="c40a9-121">**daysOfWeekType**</span><span class="sxs-lookup"><span data-stu-id="c40a9-121">**daysOfWeekType**</span></span>](taskschedulerschema-daysofweektype-complextype.md) | <span data-ttu-id="c40a9-122">Spécifie les jours de la semaine d’exécution de la tâche.</span><span class="sxs-lookup"><span data-stu-id="c40a9-122">Specifies the days of the week in which the task runs.</span></span><br/>    |
| [<span data-ttu-id="c40a9-123">**WeeksInterval**</span><span class="sxs-lookup"><span data-stu-id="c40a9-123">**WeeksInterval**</span></span>](taskschedulerschema-weeksinterval-weeklyscheduletype-element.md) | <span data-ttu-id="c40a9-124">unsignedByte</span><span class="sxs-lookup"><span data-stu-id="c40a9-124">unsignedByte</span></span>                                                             | <span data-ttu-id="c40a9-125">Spécifie l’intervalle entre les semaines de la planification.</span><span class="sxs-lookup"><span data-stu-id="c40a9-125">Specifies the interval between the weeks in the schedule.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="c40a9-126">Notes</span><span class="sxs-lookup"><span data-stu-id="c40a9-126">Remarks</span></span>

<span data-ttu-id="c40a9-127">Les éléments enfants répertoriés ci-dessus sont définis par les types d’éléments complexes [**weeklyScheduleType**](taskschedulerschema-weeklyscheduletype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="c40a9-127">The child elements listed above are defined by the [**weeklyScheduleType**](taskschedulerschema-weeklyscheduletype-complextype.md) complex element types.</span></span>

<span data-ttu-id="c40a9-128">L’heure de début de la tâche est définie par l’élément [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="c40a9-128">The time of day that the task is started is set by the [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) element.</span></span>

<span data-ttu-id="c40a9-129">Pour le développement de script, un déclencheur hebdomadaire est spécifié à l’aide de l’objet [**WeeklyTrigger**](weeklytrigger.md) .</span><span class="sxs-lookup"><span data-stu-id="c40a9-129">For scripting development, a weekly trigger is specified using the [**WeeklyTrigger**](weeklytrigger.md) object.</span></span>

<span data-ttu-id="c40a9-130">Pour le développement C++, un déclencheur hebdomadaire est spécifié à l’aide de l’interface [**IWeeklyTrigger**](/windows/desktop/api/taskschd/nn-taskschd-iweeklytrigger) .</span><span class="sxs-lookup"><span data-stu-id="c40a9-130">For C++ development, a weekly trigger is specified using the [**IWeeklyTrigger**](/windows/desktop/api/taskschd/nn-taskschd-iweeklytrigger) interface.</span></span>

## <a name="examples"></a><span data-ttu-id="c40a9-131">Exemples</span><span class="sxs-lookup"><span data-stu-id="c40a9-131">Examples</span></span>

<span data-ttu-id="c40a9-132">Le code XML suivant définit un déclencheur de calendrier hebdomadaire qui démarre une tâche du lundi au vendredi (à 8:00 AM) chaque semaine.</span><span class="sxs-lookup"><span data-stu-id="c40a9-132">The following XML defines a weekly calendar trigger that starts a task Monday through Friday (at 8:00 AM) every week.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="c40a9-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c40a9-133">Requirements</span></span>



| <span data-ttu-id="c40a9-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c40a9-134">Requirement</span></span> | <span data-ttu-id="c40a9-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="c40a9-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="c40a9-136">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c40a9-136">Minimum supported client</span></span><br/> | <span data-ttu-id="c40a9-137">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c40a9-137">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="c40a9-138">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c40a9-138">Minimum supported server</span></span><br/> | <span data-ttu-id="c40a9-139">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c40a9-139">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c40a9-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c40a9-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c40a9-141">Éléments de schéma Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="c40a9-141">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="c40a9-142">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="c40a9-142">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





