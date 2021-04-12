---
title: Élément months (monthlyDayOfWeekScheduleType)
description: Spécifie les mois de l’année pendant laquelle la tâche s’exécute pour une planification mensuelle de jour de semaine.
ms.assetid: 420fa7f4-7106-483e-9b3b-d1ba51f25222
keywords:
- Mois, élément Planificateur de tâches
topic_type:
- apiref
api_name:
- Months
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 76f13a5823e0154519dbdb093dd03ea36bbe77b5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384223"
---
# <a name="months-monthlydayofweekscheduletype-element"></a><span data-ttu-id="80d8b-104">Élément months (monthlyDayOfWeekScheduleType)</span><span class="sxs-lookup"><span data-stu-id="80d8b-104">Months (monthlyDayOfWeekScheduleType) Element</span></span>

<span data-ttu-id="80d8b-105">Spécifie les mois de l’année pendant laquelle la tâche s’exécute pour une planification mensuelle de jour de semaine.</span><span class="sxs-lookup"><span data-stu-id="80d8b-105">Specifies the months of the year during which the task runs for a monthly day-of-week schedule.</span></span>

``` syntax
<xs:element name="Months"
    type="monthsType"
 />
```

<span data-ttu-id="80d8b-106">L’élément **months** est défini par le type complexe [**monthlyDayOfWeekScheduleType**](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="80d8b-106">The **Months** element is defined by the [**monthlyDayOfWeekScheduleType**](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="80d8b-107">Élément parent</span><span class="sxs-lookup"><span data-stu-id="80d8b-107">Parent element</span></span>



| <span data-ttu-id="80d8b-108">Élément</span><span class="sxs-lookup"><span data-stu-id="80d8b-108">Element</span></span>                                                                                                                            | <span data-ttu-id="80d8b-109">Dérivé de</span><span class="sxs-lookup"><span data-stu-id="80d8b-109">Derived from</span></span>                                                                                         | <span data-ttu-id="80d8b-110">Description</span><span class="sxs-lookup"><span data-stu-id="80d8b-110">Description</span></span>                                                                          |
|------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [<span data-ttu-id="80d8b-111">**ScheduleByMonthDayOfWeek (calendarTriggerType)**</span><span class="sxs-lookup"><span data-stu-id="80d8b-111">**ScheduleByMonthDayOfWeek (calendarTriggerType)**</span></span>](taskschedulerschema-schedulebymonthdayofweek-calendartriggertype-element.md) | [<span data-ttu-id="80d8b-112">**monthlyDayOfWeekScheduleType**</span><span class="sxs-lookup"><span data-stu-id="80d8b-112">**monthlyDayOfWeekScheduleType**</span></span>](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) | <span data-ttu-id="80d8b-113">Spécifie un déclencheur qui démarre un travail pour une planification mensuelle de jour de semaine.</span><span class="sxs-lookup"><span data-stu-id="80d8b-113">Specifies a trigger that starts a job for a monthly day-of-week schedule.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="80d8b-114">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="80d8b-114">Child elements</span></span>



| <span data-ttu-id="80d8b-115">Élément</span><span class="sxs-lookup"><span data-stu-id="80d8b-115">Element</span></span>                                                               | <span data-ttu-id="80d8b-116">Type</span><span class="sxs-lookup"><span data-stu-id="80d8b-116">Type</span></span> | <span data-ttu-id="80d8b-117">Description</span><span class="sxs-lookup"><span data-stu-id="80d8b-117">Description</span></span>                                           |
|-----------------------------------------------------------------------|------|-------------------------------------------------------|
| [<span data-ttu-id="80d8b-118">**Avril**</span><span class="sxs-lookup"><span data-stu-id="80d8b-118">**April**</span></span>](taskschedulerschema-april-monthstype-element.md)         |      | <span data-ttu-id="80d8b-119">Spécifie que la tâche s’exécute en avril.</span><span class="sxs-lookup"><span data-stu-id="80d8b-119">Specifies that the task runs in April.</span></span><br/>     |
| [<span data-ttu-id="80d8b-120">**Août**</span><span class="sxs-lookup"><span data-stu-id="80d8b-120">**August**</span></span>](taskschedulerschema-august-monthstype-element.md)       |      | <span data-ttu-id="80d8b-121">Spécifie que la tâche s’exécute en août.</span><span class="sxs-lookup"><span data-stu-id="80d8b-121">Specifies that the task runs in August.</span></span><br/>    |
| [<span data-ttu-id="80d8b-122">**Décembre**</span><span class="sxs-lookup"><span data-stu-id="80d8b-122">**December**</span></span>](taskschedulerschema-december-monthstype-element.md)   |      | <span data-ttu-id="80d8b-123">Spécifie que la tâche s’exécute en décembre.</span><span class="sxs-lookup"><span data-stu-id="80d8b-123">Specifies that the task runs in December.</span></span><br/>  |
| [<span data-ttu-id="80d8b-124">**February**</span><span class="sxs-lookup"><span data-stu-id="80d8b-124">**February**</span></span>](taskschedulerschema-february-monthstype-element.md)   |      | <span data-ttu-id="80d8b-125">Spécifie que la tâche s’exécute en février.</span><span class="sxs-lookup"><span data-stu-id="80d8b-125">Specifies that the task runs in February.</span></span><br/>  |
| [<span data-ttu-id="80d8b-126">**Janvier**</span><span class="sxs-lookup"><span data-stu-id="80d8b-126">**January**</span></span>](taskschedulerschema-january-monthstype-element.md)     |      | <span data-ttu-id="80d8b-127">Spécifie que la tâche s’exécute en janvier.</span><span class="sxs-lookup"><span data-stu-id="80d8b-127">Specifies that the task runs in January.</span></span><br/>   |
| [<span data-ttu-id="80d8b-128">**Juillet**</span><span class="sxs-lookup"><span data-stu-id="80d8b-128">**July**</span></span>](taskschedulerschema-july-monthstype-element.md)           |      | <span data-ttu-id="80d8b-129">Spécifie que la tâche s’exécute en juillet.</span><span class="sxs-lookup"><span data-stu-id="80d8b-129">Specifies that the task runs in July.</span></span><br/>      |
| [<span data-ttu-id="80d8b-130">**June**</span><span class="sxs-lookup"><span data-stu-id="80d8b-130">**June**</span></span>](taskschedulerschema-june-monthstype-element.md)           |      | <span data-ttu-id="80d8b-131">Spécifie que la tâche s’exécute en juin.</span><span class="sxs-lookup"><span data-stu-id="80d8b-131">Specifies that the task runs in June.</span></span><br/>      |
| [<span data-ttu-id="80d8b-132">**Mars**</span><span class="sxs-lookup"><span data-stu-id="80d8b-132">**March**</span></span>](taskschedulerschema-march-monthstype-element.md)         |      | <span data-ttu-id="80d8b-133">Spécifie que la tâche s’exécute en mars.</span><span class="sxs-lookup"><span data-stu-id="80d8b-133">Specifies that the task runs in March.</span></span><br/>     |
| [<span data-ttu-id="80d8b-134">**Mai**</span><span class="sxs-lookup"><span data-stu-id="80d8b-134">**May**</span></span>](taskschedulerschema-may-monthstype-element.md)             |      | <span data-ttu-id="80d8b-135">Spécifie que la tâche s’exécute en mai.</span><span class="sxs-lookup"><span data-stu-id="80d8b-135">Specifies that the task runs in May.</span></span><br/>       |
| [<span data-ttu-id="80d8b-136">**Novembre**</span><span class="sxs-lookup"><span data-stu-id="80d8b-136">**November**</span></span>](taskschedulerschema-november-monthstype-element.md)   |      | <span data-ttu-id="80d8b-137">Spécifie que la tâche s’exécute en novembre.</span><span class="sxs-lookup"><span data-stu-id="80d8b-137">Specifies that the task runs in November.</span></span><br/>  |
| [<span data-ttu-id="80d8b-138">**Octobre**</span><span class="sxs-lookup"><span data-stu-id="80d8b-138">**October**</span></span>](taskschedulerschema-october-monthstype-element.md)     |      | <span data-ttu-id="80d8b-139">Spécifie que la tâche s’exécute en octobre.</span><span class="sxs-lookup"><span data-stu-id="80d8b-139">Specifies that the task runs in October.</span></span><br/>   |
| [<span data-ttu-id="80d8b-140">**Septembre**</span><span class="sxs-lookup"><span data-stu-id="80d8b-140">**September**</span></span>](taskschedulerschema-september-monthstype-element.md) |      | <span data-ttu-id="80d8b-141">Spécifie que la tâche s’exécute en septembre.</span><span class="sxs-lookup"><span data-stu-id="80d8b-141">Specifies that the task runs in September.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="80d8b-142">Notes</span><span class="sxs-lookup"><span data-stu-id="80d8b-142">Remarks</span></span>

<span data-ttu-id="80d8b-143">Pour le développement de scripts, les mois d’une année pour une planification de jour de semaine mensuelle sont spécifiés à l’aide de la propriété [**MonthlyDOWTrigger. MonthsOfYear**](monthlydowtrigger-monthsofyear.md) .</span><span class="sxs-lookup"><span data-stu-id="80d8b-143">For scripting development, the months of a year for a monthly day-of-week schedule are specified using the [**MonthlyDOWTrigger.MonthsOfYear**](monthlydowtrigger-monthsofyear.md) property.</span></span>

<span data-ttu-id="80d8b-144">Pour le développement C++, les mois d’une année pour une planification de jour de semaine mensuelle sont spécifiés à l’aide de la propriété [**IMonthlyDOWTrigger :: MonthsOfYear**](/windows/desktop/api/taskschd/nf-taskschd-imonthlydowtrigger-get_monthsofyear) .</span><span class="sxs-lookup"><span data-stu-id="80d8b-144">For C++ development, the months of a year for a monthly day-of-week schedule are specified using the [**IMonthlyDOWTrigger::MonthsOfYear**](/windows/desktop/api/taskschd/nf-taskschd-imonthlydowtrigger-get_monthsofyear) property.</span></span>

<span data-ttu-id="80d8b-145">Les éléments enfants ci-dessus sont définis par le type complexe [**monthsType**](taskschedulerschema-monthstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="80d8b-145">The child elements above are defined by the [**monthsType**](taskschedulerschema-monthstype-complextype.md) complex type.</span></span>

## <a name="examples"></a><span data-ttu-id="80d8b-146">Exemples</span><span class="sxs-lookup"><span data-stu-id="80d8b-146">Examples</span></span>

<span data-ttu-id="80d8b-147">Le code XML suivant définit un calendrier mensuel de jour de semaine qui démarre la tâche le lundi de la première semaine pour chaque mois de l’année.</span><span class="sxs-lookup"><span data-stu-id="80d8b-147">The following XML defines a monthly day-of-week calendar that starts the task on Monday of the first week for each month of the year.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="80d8b-148">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="80d8b-148">Requirements</span></span>



| <span data-ttu-id="80d8b-149">Condition requise</span><span class="sxs-lookup"><span data-stu-id="80d8b-149">Requirement</span></span> | <span data-ttu-id="80d8b-150">Valeur</span><span class="sxs-lookup"><span data-stu-id="80d8b-150">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="80d8b-151">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="80d8b-151">Minimum supported client</span></span><br/> | <span data-ttu-id="80d8b-152">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="80d8b-152">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="80d8b-153">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="80d8b-153">Minimum supported server</span></span><br/> | <span data-ttu-id="80d8b-154">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="80d8b-154">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="80d8b-155">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="80d8b-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80d8b-156">Éléments de schéma Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="80d8b-156">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="80d8b-157">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="80d8b-157">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





