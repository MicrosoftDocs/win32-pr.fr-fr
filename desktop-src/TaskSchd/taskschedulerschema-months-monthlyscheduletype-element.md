---
title: Élément months (monthlyScheduleType)
description: Spécifie les mois de l’année pendant laquelle la tâche s’exécute pour une planification mensuelle.
ms.assetid: 71c9f7ac-01fc-4837-bccf-1869df2bc24e
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
ms.openlocfilehash: 0ed40fd2466f8962f839f39e7addd3b7e1bc33eb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105370"
---
# <a name="months-monthlyscheduletype-element"></a><span data-ttu-id="f336c-104">Élément months (monthlyScheduleType)</span><span class="sxs-lookup"><span data-stu-id="f336c-104">Months (monthlyScheduleType) Element</span></span>

<span data-ttu-id="f336c-105">Spécifie les mois de l’année pendant laquelle la tâche s’exécute pour une planification mensuelle.</span><span class="sxs-lookup"><span data-stu-id="f336c-105">Specifies the months of the year during which the task runs for a monthly schedule.</span></span>

``` syntax
<xs:element name="Months"
    type="monthsType"
 />
```

<span data-ttu-id="f336c-106">L’élément **months** est défini par le type complexe [**monthlyScheduleType**](taskschedulerschema-monthlyscheduletype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="f336c-106">The **Months** element is defined by the [**monthlyScheduleType**](taskschedulerschema-monthlyscheduletype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="f336c-107">Élément parent</span><span class="sxs-lookup"><span data-stu-id="f336c-107">Parent element</span></span>



| <span data-ttu-id="f336c-108">Élément</span><span class="sxs-lookup"><span data-stu-id="f336c-108">Element</span></span>                                                                                    | <span data-ttu-id="f336c-109">Dérivé de</span><span class="sxs-lookup"><span data-stu-id="f336c-109">Derived from</span></span>                                                                       | <span data-ttu-id="f336c-110">Description</span><span class="sxs-lookup"><span data-stu-id="f336c-110">Description</span></span>                               |
|--------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|-------------------------------------------|
| [<span data-ttu-id="f336c-111">**ScheduleByMonth**</span><span class="sxs-lookup"><span data-stu-id="f336c-111">**ScheduleByMonth**</span></span>](taskschedulerschema-schedulebymonth-calendartriggertype-element.md) | [<span data-ttu-id="f336c-112">**monthlyScheduleType**</span><span class="sxs-lookup"><span data-stu-id="f336c-112">**monthlyScheduleType**</span></span>](taskschedulerschema-monthlyscheduletype-complextype.md) | <span data-ttu-id="f336c-113">Spécifie une planification mensuelle.</span><span class="sxs-lookup"><span data-stu-id="f336c-113">Specifies a monthly schedule.</span></span> <br/> |



## <a name="child-elements"></a><span data-ttu-id="f336c-114">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="f336c-114">Child elements</span></span>



| <span data-ttu-id="f336c-115">Élément</span><span class="sxs-lookup"><span data-stu-id="f336c-115">Element</span></span>                                                                            | <span data-ttu-id="f336c-116">Type</span><span class="sxs-lookup"><span data-stu-id="f336c-116">Type</span></span> | <span data-ttu-id="f336c-117">Description</span><span class="sxs-lookup"><span data-stu-id="f336c-117">Description</span></span>                                           |
|------------------------------------------------------------------------------------|------|-------------------------------------------------------|
| [<span data-ttu-id="f336c-118">**Avril (monthsType)**</span><span class="sxs-lookup"><span data-stu-id="f336c-118">**April (monthsType)**</span></span>](taskschedulerschema-april-monthstype-element.md)         |      | <span data-ttu-id="f336c-119">Spécifie que la tâche s’exécute en avril.</span><span class="sxs-lookup"><span data-stu-id="f336c-119">Specifies that the task runs in April.</span></span><br/>     |
| [<span data-ttu-id="f336c-120">**Août (monthsType)**</span><span class="sxs-lookup"><span data-stu-id="f336c-120">**August (monthsType)**</span></span>](taskschedulerschema-august-monthstype-element.md)       |      | <span data-ttu-id="f336c-121">Spécifie que la tâche s’exécute en août.</span><span class="sxs-lookup"><span data-stu-id="f336c-121">Specifies that the task runs in August.</span></span><br/>    |
| [<span data-ttu-id="f336c-122">**Décembre (monthsType)**</span><span class="sxs-lookup"><span data-stu-id="f336c-122">**December (monthsType)**</span></span>](taskschedulerschema-december-monthstype-element.md)   |      | <span data-ttu-id="f336c-123">Spécifie que la tâche s’exécute en décembre.</span><span class="sxs-lookup"><span data-stu-id="f336c-123">Specifies that the task runs in December.</span></span><br/>  |
| [<span data-ttu-id="f336c-124">**Février (monthsType)**</span><span class="sxs-lookup"><span data-stu-id="f336c-124">**February (monthsType)**</span></span>](taskschedulerschema-february-monthstype-element.md)   |      | <span data-ttu-id="f336c-125">Spécifie que la tâche s’exécute en février.</span><span class="sxs-lookup"><span data-stu-id="f336c-125">Specifies that the task runs in February.</span></span><br/>  |
| [<span data-ttu-id="f336c-126">**Janvier (monthsType)**</span><span class="sxs-lookup"><span data-stu-id="f336c-126">**January (monthsType)**</span></span>](taskschedulerschema-january-monthstype-element.md)     |      | <span data-ttu-id="f336c-127">Spécifie que la tâche s’exécute en janvier.</span><span class="sxs-lookup"><span data-stu-id="f336c-127">Specifies that the task runs in January.</span></span><br/>   |
| [<span data-ttu-id="f336c-128">**Juillet (monthsType)**</span><span class="sxs-lookup"><span data-stu-id="f336c-128">**July (monthsType)**</span></span>](taskschedulerschema-july-monthstype-element.md)           |      | <span data-ttu-id="f336c-129">Spécifie que la tâche s’exécute en juillet.</span><span class="sxs-lookup"><span data-stu-id="f336c-129">Specifies that the task runs in July.</span></span><br/>      |
| [<span data-ttu-id="f336c-130">**Juin (monthsType)**</span><span class="sxs-lookup"><span data-stu-id="f336c-130">**June (monthsType)**</span></span>](taskschedulerschema-june-monthstype-element.md)           |      | <span data-ttu-id="f336c-131">Spécifie que la tâche s’exécute en juin.</span><span class="sxs-lookup"><span data-stu-id="f336c-131">Specifies that the task runs in June.</span></span><br/>      |
| [<span data-ttu-id="f336c-132">**Mars (monthsType)**</span><span class="sxs-lookup"><span data-stu-id="f336c-132">**March (monthsType)**</span></span>](taskschedulerschema-march-monthstype-element.md)         |      | <span data-ttu-id="f336c-133">Spécifie que la tâche s’exécute en mars.</span><span class="sxs-lookup"><span data-stu-id="f336c-133">Specifies that the task runs in March.</span></span><br/>     |
| [<span data-ttu-id="f336c-134">**Mai (monthsType)**</span><span class="sxs-lookup"><span data-stu-id="f336c-134">**May (monthsType)**</span></span>](taskschedulerschema-may-monthstype-element.md)             |      | <span data-ttu-id="f336c-135">Spécifie que la tâche s’exécute en mai.</span><span class="sxs-lookup"><span data-stu-id="f336c-135">Specifies that the task runs in May.</span></span><br/>       |
| [<span data-ttu-id="f336c-136">**Novembre (monthsType)**</span><span class="sxs-lookup"><span data-stu-id="f336c-136">**November (monthsType)**</span></span>](taskschedulerschema-november-monthstype-element.md)   |      | <span data-ttu-id="f336c-137">Spécifie que la tâche s’exécute en novembre.</span><span class="sxs-lookup"><span data-stu-id="f336c-137">Specifies that the task runs in November.</span></span><br/>  |
| [<span data-ttu-id="f336c-138">**Octobre (monthsType)**</span><span class="sxs-lookup"><span data-stu-id="f336c-138">**October (monthsType)**</span></span>](taskschedulerschema-october-monthstype-element.md)     |      | <span data-ttu-id="f336c-139">Spécifie que la tâche s’exécute en octobre.</span><span class="sxs-lookup"><span data-stu-id="f336c-139">Specifies that the task runs in October.</span></span><br/>   |
| [<span data-ttu-id="f336c-140">**Septembre (monthsType)**</span><span class="sxs-lookup"><span data-stu-id="f336c-140">**September (monthsType)**</span></span>](taskschedulerschema-september-monthstype-element.md) |      | <span data-ttu-id="f336c-141">Spécifie que la tâche s’exécute en septembre.</span><span class="sxs-lookup"><span data-stu-id="f336c-141">Specifies that the task runs in September.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="f336c-142">Notes</span><span class="sxs-lookup"><span data-stu-id="f336c-142">Remarks</span></span>

<span data-ttu-id="f336c-143">Pour le développement de scripts, les mois de la planification sont spécifiés à l’aide de la propriété [**MonthlyTrigger. MonthsOfYear**](monthlytrigger-monthsofyear.md) .</span><span class="sxs-lookup"><span data-stu-id="f336c-143">For script development, the months of the schedule are specified using the [**MonthlyTrigger.MonthsOfYear**](monthlytrigger-monthsofyear.md) property.</span></span>

<span data-ttu-id="f336c-144">Pour le développement C++, les mois de la planification sont spécifiés à l’aide de la propriété [**IMonthlyTrigger :: MonthsOfYear**](/windows/desktop/api/taskschd/nf-taskschd-imonthlytrigger-get_monthsofyear) .</span><span class="sxs-lookup"><span data-stu-id="f336c-144">For C++ development, the months of the schedule are specified using the [**IMonthlyTrigger::MonthsOfYear**](/windows/desktop/api/taskschd/nf-taskschd-imonthlytrigger-get_monthsofyear) property.</span></span>

## <a name="examples"></a><span data-ttu-id="f336c-145">Exemples</span><span class="sxs-lookup"><span data-stu-id="f336c-145">Examples</span></span>

<span data-ttu-id="f336c-146">Le code XML suivant définit un calendrier mensuel qui démarre la tâche le 1er et le quinzième jour de chaque mois de l’année.</span><span class="sxs-lookup"><span data-stu-id="f336c-146">The following XML defines a monthly calendar that starts the task on the 1st and 15th day of every month of the year.</span></span>


```XML
</ScheduleByMonth>
    <DaysOfMonth>
        <Day>1</Day>
        <Day>15</Day>
    </DaysOfMonth
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
```



## <a name="requirements"></a><span data-ttu-id="f336c-147">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f336c-147">Requirements</span></span>



| <span data-ttu-id="f336c-148">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f336c-148">Requirement</span></span> | <span data-ttu-id="f336c-149">Valeur</span><span class="sxs-lookup"><span data-stu-id="f336c-149">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="f336c-150">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f336c-150">Minimum supported client</span></span><br/> | <span data-ttu-id="f336c-151">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f336c-151">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="f336c-152">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f336c-152">Minimum supported server</span></span><br/> | <span data-ttu-id="f336c-153">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f336c-153">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f336c-154">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f336c-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f336c-155">Éléments de schéma Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="f336c-155">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="f336c-156">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="f336c-156">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





