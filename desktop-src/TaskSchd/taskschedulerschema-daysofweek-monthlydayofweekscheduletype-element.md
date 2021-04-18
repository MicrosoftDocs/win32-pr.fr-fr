---
title: DaysOfWeek (monthlyDayOfWeekScheduleType) (élément)
description: Spécifie les jours de la semaine d’exécution de la tâche. | DaysOfWeek (monthlyDayOfWeekScheduleType) (élément)
ms.assetid: d84f0019-1369-465f-9054-0fb5a83cad6d
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
ms.openlocfilehash: 3867e08dd001a035a3ab25da056f75c1e73eeeef
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106523156"
---
# <a name="daysofweek-monthlydayofweekscheduletype-element"></a><span data-ttu-id="e4e12-105">DaysOfWeek (monthlyDayOfWeekScheduleType) (élément)</span><span class="sxs-lookup"><span data-stu-id="e4e12-105">DaysOfWeek (monthlyDayOfWeekScheduleType) Element</span></span>

<span data-ttu-id="e4e12-106">Spécifie les jours de la semaine d’exécution de la tâche.</span><span class="sxs-lookup"><span data-stu-id="e4e12-106">Specifies the days of the week in which the task runs.</span></span>

``` syntax
<xs:element name="DaysOfWeek"
    type="daysOfWeekType"
 />
```

<span data-ttu-id="e4e12-107">L’élément **DaysOfWeek** est défini par le type complexe [**monthlyDayOfWeekScheduleType**](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="e4e12-107">The **DaysOfWeek** element is defined by the [**monthlyDayOfWeekScheduleType**](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="e4e12-108">Élément parent</span><span class="sxs-lookup"><span data-stu-id="e4e12-108">Parent element</span></span>



| <span data-ttu-id="e4e12-109">Élément</span><span class="sxs-lookup"><span data-stu-id="e4e12-109">Element</span></span>                                                                                                      | <span data-ttu-id="e4e12-110">Dérivé de</span><span class="sxs-lookup"><span data-stu-id="e4e12-110">Derived from</span></span>                                                                                         | <span data-ttu-id="e4e12-111">Description</span><span class="sxs-lookup"><span data-stu-id="e4e12-111">Description</span></span>                                                                          |
|--------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [<span data-ttu-id="e4e12-112">**ScheduleByMonthDayOfWeek**</span><span class="sxs-lookup"><span data-stu-id="e4e12-112">**ScheduleByMonthDayOfWeek**</span></span>](taskschedulerschema-schedulebymonthdayofweek-calendartriggertype-element.md) | [<span data-ttu-id="e4e12-113">**monthlyDayOfWeekScheduleType**</span><span class="sxs-lookup"><span data-stu-id="e4e12-113">**monthlyDayOfWeekScheduleType**</span></span>](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) | <span data-ttu-id="e4e12-114">Spécifie un déclencheur qui démarre un travail pour une planification mensuelle de jour de semaine.</span><span class="sxs-lookup"><span data-stu-id="e4e12-114">Specifies a trigger that starts a job for a monthly day-of-week schedule.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="e4e12-115">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="e4e12-115">Child elements</span></span>



| <span data-ttu-id="e4e12-116">Élément</span><span class="sxs-lookup"><span data-stu-id="e4e12-116">Element</span></span>                                                                   | <span data-ttu-id="e4e12-117">Type</span><span class="sxs-lookup"><span data-stu-id="e4e12-117">Type</span></span> | <span data-ttu-id="e4e12-118">Description</span><span class="sxs-lookup"><span data-stu-id="e4e12-118">Description</span></span>                                           |
|---------------------------------------------------------------------------|------|-------------------------------------------------------|
| [<span data-ttu-id="e4e12-119">**Vendredi**</span><span class="sxs-lookup"><span data-stu-id="e4e12-119">**Friday**</span></span>](taskschedulerschema-friday-daysofweektype-element.md)       |      | <span data-ttu-id="e4e12-120">Spécifie que la tâche est exécutée le vendredi.</span><span class="sxs-lookup"><span data-stu-id="e4e12-120">Specifies that the task runs on Friday.</span></span><br/>    |
| [<span data-ttu-id="e4e12-121">**Monday**</span><span class="sxs-lookup"><span data-stu-id="e4e12-121">**Monday**</span></span>](taskschedulerschema-monday-daysofweektype-element.md)       |      | <span data-ttu-id="e4e12-122">Spécifie que la tâche est exécutée le lundi.</span><span class="sxs-lookup"><span data-stu-id="e4e12-122">Specifies that the task runs on Monday.</span></span><br/>    |
| [<span data-ttu-id="e4e12-123">**Samedi**</span><span class="sxs-lookup"><span data-stu-id="e4e12-123">**Saturday**</span></span>](taskschedulerschema-saturday-daysofweektype-element.md)   |      | <span data-ttu-id="e4e12-124">Spécifie que la tâche est exécutée le samedi.</span><span class="sxs-lookup"><span data-stu-id="e4e12-124">Specifies that the task runs on Saturday.</span></span><br/>  |
| [<span data-ttu-id="e4e12-125">**Dimanche**</span><span class="sxs-lookup"><span data-stu-id="e4e12-125">**Sunday**</span></span>](taskschedulerschema-sunday-daysofweektype-element.md)       |      | <span data-ttu-id="e4e12-126">Spécifie que la tâche est exécutée le dimanche.</span><span class="sxs-lookup"><span data-stu-id="e4e12-126">Specifies that the task runs on Sunday.</span></span><br/>    |
| [<span data-ttu-id="e4e12-127">**Thursday**</span><span class="sxs-lookup"><span data-stu-id="e4e12-127">**Thursday**</span></span>](taskschedulerschema-thursday-daysofweektype-element.md)   |      | <span data-ttu-id="e4e12-128">Spécifie que la tâche est exécutée le jeudi.</span><span class="sxs-lookup"><span data-stu-id="e4e12-128">Specifies that the task runs on Thursday.</span></span><br/>  |
| [<span data-ttu-id="e4e12-129">**Mardi**</span><span class="sxs-lookup"><span data-stu-id="e4e12-129">**Tuesday**</span></span>](taskschedulerschema-tuesday-daysofweektype-element.md)     |      | <span data-ttu-id="e4e12-130">Spécifie que la tâche est exécutée le mardi.</span><span class="sxs-lookup"><span data-stu-id="e4e12-130">Specifies that the task runs on Tuesday.</span></span><br/>   |
| [<span data-ttu-id="e4e12-131">**Mercredi**</span><span class="sxs-lookup"><span data-stu-id="e4e12-131">**Wednesday**</span></span>](taskschedulerschema-wednesday-daysofweektype-element.md) |      | <span data-ttu-id="e4e12-132">Spécifie que la tâche est exécutée le mercredi.</span><span class="sxs-lookup"><span data-stu-id="e4e12-132">Specifies that the task runs on Wednesday.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="e4e12-133">Notes</span><span class="sxs-lookup"><span data-stu-id="e4e12-133">Remarks</span></span>

<span data-ttu-id="e4e12-134">Pour le développement de scripts, les jours de la semaine pour un calendrier mensuel de jour de la semaine sont spécifiés à l’aide de la propriété [**MonthlyDOWTrigger. DaysOfWeek**](monthlydowtrigger-daysofweek.md) .</span><span class="sxs-lookup"><span data-stu-id="e4e12-134">For scripting development, the days of the week for a monthly day-of-week calendar are specified using the [**MonthlyDOWTrigger.DaysOfWeek**](monthlydowtrigger-daysofweek.md) property.</span></span>

<span data-ttu-id="e4e12-135">Pour le développement C++, les jours de la semaine pour un calendrier mensuel de jour de semaine sont spécifiés à l’aide de la propriété [**IMonthlyDOWTrigger ::D aysofweek**](/windows/desktop/api/taskschd/nf-taskschd-imonthlydowtrigger-get_daysofweek) .</span><span class="sxs-lookup"><span data-stu-id="e4e12-135">For C++ development, the days of the week for a monthly day-of-week calendar are specified using the [**IMonthlyDOWTrigger::DaysOfWeek**](/windows/desktop/api/taskschd/nf-taskschd-imonthlydowtrigger-get_daysofweek) property.</span></span>

<span data-ttu-id="e4e12-136">Les éléments enfants ci-dessus sont définis par le type complexe [**daysOfWeekType**](taskschedulerschema-daysofweektype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="e4e12-136">The child elements above are defined by the [**daysOfWeekType**](taskschedulerschema-daysofweektype-complextype.md) complex type.</span></span>

## <a name="examples"></a><span data-ttu-id="e4e12-137">Exemples</span><span class="sxs-lookup"><span data-stu-id="e4e12-137">Examples</span></span>

<span data-ttu-id="e4e12-138">Le code XML suivant définit un calendrier mensuel de jour de semaine qui démarre la tâche le lundi de la première semaine pour chaque mois de l’année.</span><span class="sxs-lookup"><span data-stu-id="e4e12-138">The following XML defines a monthly day-of-week calendar that starts the task on Monday of the first week for each month of the year.</span></span>


```XML
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
```



## <a name="requirements"></a><span data-ttu-id="e4e12-139">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e4e12-139">Requirements</span></span>



| <span data-ttu-id="e4e12-140">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e4e12-140">Requirement</span></span> | <span data-ttu-id="e4e12-141">Valeur</span><span class="sxs-lookup"><span data-stu-id="e4e12-141">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="e4e12-142">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e4e12-142">Minimum supported client</span></span><br/> | <span data-ttu-id="e4e12-143">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e4e12-143">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="e4e12-144">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e4e12-144">Minimum supported server</span></span><br/> | <span data-ttu-id="e4e12-145">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e4e12-145">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e4e12-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e4e12-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4e12-147">Éléments de schéma Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="e4e12-147">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="e4e12-148">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="e4e12-148">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





