---
title: Élément ScheduleByMonthDayOfWeek (calendarTriggerType)
description: Spécifie une planification mensuelle du jour de la semaine.
ms.assetid: 7ff17bea-fa26-40c4-90fa-d94a3690e464
keywords:
- Élément ScheduleByMonthDayOfWeek Planificateur de tâches
topic_type:
- apiref
api_name:
- ScheduleByMonthDayOfWeek
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3e92d6ad530466a2238c8239c9e262f85ae361d2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742892"
---
# <a name="schedulebymonthdayofweek-calendartriggertype-element"></a><span data-ttu-id="a08ff-104">Élément ScheduleByMonthDayOfWeek (calendarTriggerType)</span><span class="sxs-lookup"><span data-stu-id="a08ff-104">ScheduleByMonthDayOfWeek (calendarTriggerType) Element</span></span>

<span data-ttu-id="a08ff-105">Spécifie une planification mensuelle du jour de la semaine.</span><span class="sxs-lookup"><span data-stu-id="a08ff-105">Specifies a monthly day-of-week schedule.</span></span> <span data-ttu-id="a08ff-106">Par exemple, la tâche démarre des jours spécifiques de la semaine, des semaines du mois et des mois de l’année.</span><span class="sxs-lookup"><span data-stu-id="a08ff-106">For example, the task starts on specific days of the week, weeks of the month, and months of the year.</span></span>

``` syntax
<xs:element name="ScheduleByMonthDayOfWeek"
    type="monthlyDayOfWeekScheduleType"
 />
```

<span data-ttu-id="a08ff-107">L’élément **ScheduleByMonthDayOfWeek** est défini par le type complexe [**monthlyDayOfWeekScheduleType**](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="a08ff-107">The **ScheduleByMonthDayOfWeek** element is defined by the [**monthlyDayOfWeekScheduleType**](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="a08ff-108">Élément parent</span><span class="sxs-lookup"><span data-stu-id="a08ff-108">Parent element</span></span>



| <span data-ttu-id="a08ff-109">Élément</span><span class="sxs-lookup"><span data-stu-id="a08ff-109">Element</span></span>                                                                             | <span data-ttu-id="a08ff-110">Dérivé de</span><span class="sxs-lookup"><span data-stu-id="a08ff-110">Derived from</span></span>                                                                       | <span data-ttu-id="a08ff-111">Description</span><span class="sxs-lookup"><span data-stu-id="a08ff-111">Description</span></span>                                                                                |
|-------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a08ff-112">**CalendarTrigger**</span><span class="sxs-lookup"><span data-stu-id="a08ff-112">**CalendarTrigger**</span></span>](taskschedulerschema-calendartrigger-triggergroup-element.md) | [<span data-ttu-id="a08ff-113">**calendarTriggerType**</span><span class="sxs-lookup"><span data-stu-id="a08ff-113">**calendarTriggerType**</span></span>](taskschedulerschema-calendartriggertype-complextype.md) | <span data-ttu-id="a08ff-114">Spécifie un déclencheur quotidien, hebdomadaire, mensuel ou un jour de la semaine (DOW) mensuel.</span><span class="sxs-lookup"><span data-stu-id="a08ff-114">Specifies a daily, weekly, monthly, or a monthly day-of-the-week (DOW) trigger.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="a08ff-115">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="a08ff-115">Child elements</span></span>



| <span data-ttu-id="a08ff-116">Élément</span><span class="sxs-lookup"><span data-stu-id="a08ff-116">Element</span></span>                                                                                   | <span data-ttu-id="a08ff-117">Type</span><span class="sxs-lookup"><span data-stu-id="a08ff-117">Type</span></span>                                                                     | <span data-ttu-id="a08ff-118">Description</span><span class="sxs-lookup"><span data-stu-id="a08ff-118">Description</span></span>                                                             |
|-------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [<span data-ttu-id="a08ff-119">**DaysOfWeek**</span><span class="sxs-lookup"><span data-stu-id="a08ff-119">**DaysOfWeek**</span></span>](taskschedulerschema-daysofweek-monthlydayofweekscheduletype-element.md) | [<span data-ttu-id="a08ff-120">**daysOfWeekType**</span><span class="sxs-lookup"><span data-stu-id="a08ff-120">**daysOfWeekType**</span></span>](taskschedulerschema-daysofweektype-complextype.md) | <span data-ttu-id="a08ff-121">Spécifie les jours de la semaine d’exécution de la tâche.</span><span class="sxs-lookup"><span data-stu-id="a08ff-121">Specifies the days of the week in which the task runs.</span></span><br/>       |
| [<span data-ttu-id="a08ff-122">**Suivent**</span><span class="sxs-lookup"><span data-stu-id="a08ff-122">**Months**</span></span>](taskschedulerschema-months-monthlydayofweekscheduletype-element.md)         | [<span data-ttu-id="a08ff-123">**monthsType**</span><span class="sxs-lookup"><span data-stu-id="a08ff-123">**monthsType**</span></span>](taskschedulerschema-monthstype-complextype.md)         | <span data-ttu-id="a08ff-124">Spécifie les mois de l’année pendant laquelle la tâche s’exécute.</span><span class="sxs-lookup"><span data-stu-id="a08ff-124">Specifies the months of the year during which the task runs.</span></span><br/> |
| [<span data-ttu-id="a08ff-125">**Semaines**</span><span class="sxs-lookup"><span data-stu-id="a08ff-125">**Weeks**</span></span>](taskschedulerschema-weeks-monthlydayofweekscheduletype-element.md)           | <span data-ttu-id="a08ff-126">unsignedByte</span><span class="sxs-lookup"><span data-stu-id="a08ff-126">unsignedByte</span></span>                                                             | <span data-ttu-id="a08ff-127">Spécifie l’intervalle entre les semaines de la planification.</span><span class="sxs-lookup"><span data-stu-id="a08ff-127">Specifies the interval between the weeks in the schedule.</span></span><br/>    |



## <a name="remarks"></a><span data-ttu-id="a08ff-128">Notes</span><span class="sxs-lookup"><span data-stu-id="a08ff-128">Remarks</span></span>

<span data-ttu-id="a08ff-129">L’heure de début de la tâche est définie par l’élément [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="a08ff-129">The time of day that the task is started is set by the [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) element.</span></span>

<span data-ttu-id="a08ff-130">Pour le développement de scripts, un déclencheur de jour de semaine mensuel est spécifié à l’aide de l’objet [**MonthlyDOWTrigger**](monthlydowtrigger.md) .</span><span class="sxs-lookup"><span data-stu-id="a08ff-130">For scripting development, a monthly day-of-week trigger is specified using the [**MonthlyDOWTrigger**](monthlydowtrigger.md) object.</span></span>

<span data-ttu-id="a08ff-131">Pour le développement C++, un déclencheur de jour de semaine mensuel est spécifié à l’aide de l’interface [**IMonthlyDOWTrigger**](/windows/desktop/api/taskschd/nn-taskschd-imonthlydowtrigger) .</span><span class="sxs-lookup"><span data-stu-id="a08ff-131">For C++ development, a monthly day-of-week trigger is specified using the [**IMonthlyDOWTrigger**](/windows/desktop/api/taskschd/nn-taskschd-imonthlydowtrigger) interface.</span></span>

<span data-ttu-id="a08ff-132">Les éléments enfants répertoriés ci-dessus sont définis par les types d’éléments complexes [**monthlyDayOfWeekScheduleType**](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="a08ff-132">The child elements listed above are defined by the [**monthlyDayOfWeekScheduleType**](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) complex element types.</span></span>

## <a name="examples"></a><span data-ttu-id="a08ff-133">Exemples</span><span class="sxs-lookup"><span data-stu-id="a08ff-133">Examples</span></span>

<span data-ttu-id="a08ff-134">Le code XML suivant définit un déclencheur de calendrier de jour de semaine mensuel qui démarre une tâche (à 8:00 AM) le lundi de la première semaine pour chaque mois de l’année.</span><span class="sxs-lookup"><span data-stu-id="a08ff-134">The following XML defines a monthly day of week calendar trigger that starts a task ( at 8:00 AM) on Monday of the first week for each month of the year.</span></span>


```XML
<CalendarTrigger>
    <StartBoundary>2005-01-01T08:00:00</StartBoundary>
    <EndBounadry>2007-01-01T00:00:00</EndBoundary>
    <ScheduleByMonthDayOfWeek>
        <Weeks>
            <Week>1</Week>
        </Weeks>
        <DaysOfWeek>
            <Monday/>
        </DaysOfWeek>
        <Months>
            <January/>
            <February/>
            <March/>
            <April/>
            <May/>
            <June/>
            <July/>
            <August/>
            <September/>
            <October/>
            <November/>
            <December/>
        <Months>
    </ScheduleByMonthDayOfWeek>
</CalendarTrigger>
```



## <a name="requirements"></a><span data-ttu-id="a08ff-135">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a08ff-135">Requirements</span></span>



| <span data-ttu-id="a08ff-136">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a08ff-136">Requirement</span></span> | <span data-ttu-id="a08ff-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="a08ff-137">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="a08ff-138">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a08ff-138">Minimum supported client</span></span><br/> | <span data-ttu-id="a08ff-139">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a08ff-139">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="a08ff-140">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a08ff-140">Minimum supported server</span></span><br/> | <span data-ttu-id="a08ff-141">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a08ff-141">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a08ff-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a08ff-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a08ff-143">Éléments de schéma Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="a08ff-143">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="a08ff-144">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="a08ff-144">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





