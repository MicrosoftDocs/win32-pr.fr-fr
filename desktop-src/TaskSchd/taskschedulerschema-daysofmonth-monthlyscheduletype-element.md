---
title: Élément DaysOfMonth (monthlyScheduleType)
description: Spécifie les jours du mois pendant lesquels la tâche est exécutée.
ms.assetid: 62f28f44-b3d8-414e-80d4-f4d8bd3c4527
keywords:
- Élément DaysOfMonth Planificateur de tâches
topic_type:
- apiref
api_name:
- DaysOfMonth
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 38c2106f8d612ee27dc1297023a59b531fa9548d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106513834"
---
# <a name="daysofmonth-monthlyscheduletype-element"></a><span data-ttu-id="1c097-104">Élément DaysOfMonth (monthlyScheduleType)</span><span class="sxs-lookup"><span data-stu-id="1c097-104">DaysOfMonth (monthlyScheduleType) Element</span></span>

<span data-ttu-id="1c097-105">Spécifie les jours du mois pendant lesquels la tâche est exécutée.</span><span class="sxs-lookup"><span data-stu-id="1c097-105">Specifies the days of the month during which the task runs.</span></span>

``` syntax
<xs:element name="DaysOfMonth"
    type="daysOfMonthType"
 />
```

<span data-ttu-id="1c097-106">L’élément **DaysOfMonth** est défini par le type complexe [**monthlyScheduleType**](taskschedulerschema-monthlyscheduletype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="1c097-106">The **DaysOfMonth** element is defined by the [**monthlyScheduleType**](taskschedulerschema-monthlyscheduletype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="1c097-107">Élément parent</span><span class="sxs-lookup"><span data-stu-id="1c097-107">Parent element</span></span>



| <span data-ttu-id="1c097-108">Élément</span><span class="sxs-lookup"><span data-stu-id="1c097-108">Element</span></span>                                                                                    | <span data-ttu-id="1c097-109">Dérivé de</span><span class="sxs-lookup"><span data-stu-id="1c097-109">Derived from</span></span>                                                                                         | <span data-ttu-id="1c097-110">Description</span><span class="sxs-lookup"><span data-stu-id="1c097-110">Description</span></span>                                                                          |
|--------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [<span data-ttu-id="1c097-111">**ScheduleByMonth**</span><span class="sxs-lookup"><span data-stu-id="1c097-111">**ScheduleByMonth**</span></span>](taskschedulerschema-schedulebymonth-calendartriggertype-element.md) | [<span data-ttu-id="1c097-112">**monthlyDayOfWeekScheduleType**</span><span class="sxs-lookup"><span data-stu-id="1c097-112">**monthlyDayOfWeekScheduleType**</span></span>](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) | <span data-ttu-id="1c097-113">Spécifie un déclencheur qui démarre un travail pour une planification mensuelle de jour de semaine.</span><span class="sxs-lookup"><span data-stu-id="1c097-113">Specifies a trigger that starts a job for a monthly day-of-week schedule.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="1c097-114">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="1c097-114">Child elements</span></span>



| <span data-ttu-id="1c097-115">Élément</span><span class="sxs-lookup"><span data-stu-id="1c097-115">Element</span></span>                                                        | <span data-ttu-id="1c097-116">Type</span><span class="sxs-lookup"><span data-stu-id="1c097-116">Type</span></span>                                                                    | <span data-ttu-id="1c097-117">Description</span><span class="sxs-lookup"><span data-stu-id="1c097-117">Description</span></span>                                                         |
|----------------------------------------------------------------|-------------------------------------------------------------------------|---------------------------------------------------------------------|
| [<span data-ttu-id="1c097-118">**Temps**</span><span class="sxs-lookup"><span data-stu-id="1c097-118">**Day**</span></span>](taskschedulerschema-day-daysofmonthtype-element.md) | [<span data-ttu-id="1c097-119">**dayOfMonthType**</span><span class="sxs-lookup"><span data-stu-id="1c097-119">**dayOfMonthType**</span></span>](taskschedulerschema-dayofmonthtype-simpletype.md) | <span data-ttu-id="1c097-120">Spécifie un jour du mois pendant lequel la tâche s’exécute.</span><span class="sxs-lookup"><span data-stu-id="1c097-120">Specifies a day of the month during which the task runs.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="1c097-121">Notes</span><span class="sxs-lookup"><span data-stu-id="1c097-121">Remarks</span></span>

<span data-ttu-id="1c097-122">Pour le développement de scripts, les jours du mois pour la planification sont spécifiés à l’aide de la propriété [**MonthlyTrigger. DaysOfMonth**](monthlytrigger-daysofmonth.md) .</span><span class="sxs-lookup"><span data-stu-id="1c097-122">For script development, the days of the month for the schedule are specified using the [**MonthlyTrigger.DaysOfMonth**](monthlytrigger-daysofmonth.md) property.</span></span>

<span data-ttu-id="1c097-123">Pour le développement C++, les jours du mois pour la planification sont spécifiés à l’aide de la propriété [**IMonthlyTrigger ::D aysofmonth**](/windows/desktop/api/taskschd/nf-taskschd-imonthlytrigger-get_daysofmonth) .</span><span class="sxs-lookup"><span data-stu-id="1c097-123">For C++ development, the days of the month for the schedule are specified using the [**IMonthlyTrigger::DaysOfMonth**](/windows/desktop/api/taskschd/nf-taskschd-imonthlytrigger-get_daysofmonth) property.</span></span>

<span data-ttu-id="1c097-124">L’élément enfant doit être répété pour chaque jour du mois où la tâche doit être exécutée.</span><span class="sxs-lookup"><span data-stu-id="1c097-124">The child element must be repeated for each day of the month the task is to run.</span></span>

## <a name="examples"></a><span data-ttu-id="1c097-125">Exemples</span><span class="sxs-lookup"><span data-stu-id="1c097-125">Examples</span></span>

<span data-ttu-id="1c097-126">Le code XML suivant définit un déclencheur de calendrier mensuel qui démarre une tâche (à 8:30 AM) le 1er jour de chaque mois.</span><span class="sxs-lookup"><span data-stu-id="1c097-126">The following XML defines a monthly calendar trigger that starts a task (at 8:30 AM) on the 1st day of every month.</span></span>


```XML
<CalendarTrigger>
    <StartBoundary>2005-01-01T08:00:00</StartBoundary>
    <EndBounadry>2007-01-01T00:00:00</EndBoundary>
    <ScheduleByMonth>
        <DaysOfMonth>
            <Day>1</Day>  
        </DaysOfMonth>
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
    </ScheduleByMonth>
</CalendarTrigger>
```



## <a name="requirements"></a><span data-ttu-id="1c097-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1c097-127">Requirements</span></span>



| <span data-ttu-id="1c097-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1c097-128">Requirement</span></span> | <span data-ttu-id="1c097-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="1c097-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="1c097-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1c097-130">Minimum supported client</span></span><br/> | <span data-ttu-id="1c097-131">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1c097-131">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="1c097-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1c097-132">Minimum supported server</span></span><br/> | <span data-ttu-id="1c097-133">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1c097-133">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1c097-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1c097-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c097-135">Éléments de schéma Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="1c097-135">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="1c097-136">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="1c097-136">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





