---
title: Semaines (élément monthlyDayOfWeekScheduleType)
description: Spécifie les semaines du mois où la tâche est exécutée.
ms.assetid: c126d1e2-6e60-4067-9fc2-86c9522cce5d
keywords:
- Planificateur de tâches de l’élément weeks
topic_type:
- apiref
api_name:
- Weeks
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2e032b936353d2c89a84b5da684f681ea3c2b6d3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743309"
---
# <a name="weeks-monthlydayofweekscheduletype-element"></a><span data-ttu-id="bce92-104">Semaines (élément monthlyDayOfWeekScheduleType)</span><span class="sxs-lookup"><span data-stu-id="bce92-104">Weeks (monthlyDayOfWeekScheduleType) Element</span></span>

<span data-ttu-id="bce92-105">Spécifie les semaines du mois où la tâche est exécutée.</span><span class="sxs-lookup"><span data-stu-id="bce92-105">Specifies the weeks of the month in which the task is run.</span></span>

``` syntax
<xs:element name="Weeks"
    type="weeksType"
 />
```

<span data-ttu-id="bce92-106">L’élément **weeks** est défini par le type complexe [**monthlyDayOfWeekScheduleType**](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="bce92-106">The **Weeks** element is defined by the [**monthlyDayOfWeekScheduleType**](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="bce92-107">Élément parent</span><span class="sxs-lookup"><span data-stu-id="bce92-107">Parent element</span></span>



| <span data-ttu-id="bce92-108">Élément</span><span class="sxs-lookup"><span data-stu-id="bce92-108">Element</span></span>                                                                                                      | <span data-ttu-id="bce92-109">Dérivé de</span><span class="sxs-lookup"><span data-stu-id="bce92-109">Derived from</span></span>                                                                                         | <span data-ttu-id="bce92-110">Description</span><span class="sxs-lookup"><span data-stu-id="bce92-110">Description</span></span>                                                                         |
|--------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| [<span data-ttu-id="bce92-111">**ScheduleByMonthDayOfWeek**</span><span class="sxs-lookup"><span data-stu-id="bce92-111">**ScheduleByMonthDayOfWeek**</span></span>](taskschedulerschema-schedulebymonthdayofweek-calendartriggertype-element.md) | [<span data-ttu-id="bce92-112">**monthlyDayOfWeekScheduleType**</span><span class="sxs-lookup"><span data-stu-id="bce92-112">**monthlyDayOfWeekScheduleType**</span></span>](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) | <span data-ttu-id="bce92-113">Spécifie un déclencheur qui démarre un travail sur une planification de jour de semaine mensuelle.</span><span class="sxs-lookup"><span data-stu-id="bce92-113">Specifies a trigger that starts a job on a monthly day-of-week schedule.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="bce92-114">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="bce92-114">Child elements</span></span>



| <span data-ttu-id="bce92-115">Élément</span><span class="sxs-lookup"><span data-stu-id="bce92-115">Element</span></span>                                                    | <span data-ttu-id="bce92-116">Type</span><span class="sxs-lookup"><span data-stu-id="bce92-116">Type</span></span>                                                        | <span data-ttu-id="bce92-117">Description</span><span class="sxs-lookup"><span data-stu-id="bce92-117">Description</span></span>                                        |
|------------------------------------------------------------|-------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="bce92-118">**Week**</span><span class="sxs-lookup"><span data-stu-id="bce92-118">**Week**</span></span>](taskschedulerschema-week-weekstype-element.md) | [<span data-ttu-id="bce92-119">**weekType**</span><span class="sxs-lookup"><span data-stu-id="bce92-119">**weekType**</span></span>](taskschedulerschema-weektype-simpletype.md) | <span data-ttu-id="bce92-120">Spécifie une semaine spécifique du mois.</span><span class="sxs-lookup"><span data-stu-id="bce92-120">Specifies a specific week of the month.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="bce92-121">Notes</span><span class="sxs-lookup"><span data-stu-id="bce92-121">Remarks</span></span>

<span data-ttu-id="bce92-122">Pour le développement de scripts, les semaines du mois sont spécifiées à l’aide de la propriété [**MonthlyDOWTrigger. WeeksOfMonth**](monthlydowtrigger-weeksofmonth.md) .</span><span class="sxs-lookup"><span data-stu-id="bce92-122">For scripting development, the weeks of the month are specified using the [**MonthlyDOWTrigger.WeeksOfMonth**](monthlydowtrigger-weeksofmonth.md) property.</span></span>

<span data-ttu-id="bce92-123">Pour le développement C++, les semaines du mois sont spécifiées à l’aide de la propriété [**IMonthlyDOWTrigger :: WeeksOfMonth**](/windows/desktop/api/taskschd/nf-taskschd-imonthlydowtrigger-get_weeksofmonth) .</span><span class="sxs-lookup"><span data-stu-id="bce92-123">For C++ development, the weeks of the month are specified using the [**IMonthlyDOWTrigger::WeeksOfMonth**](/windows/desktop/api/taskschd/nf-taskschd-imonthlydowtrigger-get_weeksofmonth) property.</span></span>

<span data-ttu-id="bce92-124">Lorsque vous spécifiez les semaines du mois, utilisez 1-4 pour spécifier les quatre premières semaines du mois ou utilisez la chaîne « Last » pour indiquer la dernière semaine, quelle que soit la semaine.</span><span class="sxs-lookup"><span data-stu-id="bce92-124">When specifying the weeks of the month, use 1-4 to specify the first four weeks of the month or use the string "Last" to indicate the last week regardless of which week it is.</span></span>

## <a name="examples"></a><span data-ttu-id="bce92-125">Exemples</span><span class="sxs-lookup"><span data-stu-id="bce92-125">Examples</span></span>

<span data-ttu-id="bce92-126">Le code XML suivant définit un calendrier mensuel de jour de semaine qui démarre la tâche le lundi de la première semaine pour chaque mois de l’année.</span><span class="sxs-lookup"><span data-stu-id="bce92-126">The following XML defines a monthly day-of-week calendar that starts the task on Monday of the first week for each month of the year.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="bce92-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bce92-127">Requirements</span></span>



| <span data-ttu-id="bce92-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bce92-128">Requirement</span></span> | <span data-ttu-id="bce92-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="bce92-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="bce92-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bce92-130">Minimum supported client</span></span><br/> | <span data-ttu-id="bce92-131">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bce92-131">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="bce92-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bce92-132">Minimum supported server</span></span><br/> | <span data-ttu-id="bce92-133">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bce92-133">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="bce92-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bce92-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bce92-135">Éléments de schéma Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="bce92-135">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="bce92-136">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="bce92-136">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





