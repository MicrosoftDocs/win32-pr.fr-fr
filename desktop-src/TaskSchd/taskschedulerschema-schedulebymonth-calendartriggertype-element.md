---
title: Élément ScheduleByMonth (calendarTriggerType)
description: Spécifie une planification mensuelle.
ms.assetid: 3a23f4d0-bdaf-4f2a-81c6-8652a0849fc8
keywords:
- Élément ScheduleByMonth Planificateur de tâches
topic_type:
- apiref
api_name:
- ScheduleByMonth
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6fda84a1cd4373f7988fa66a5ad70c97dd371d4d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105361"
---
# <a name="schedulebymonth-calendartriggertype-element"></a><span data-ttu-id="5a629-104">Élément ScheduleByMonth (calendarTriggerType)</span><span class="sxs-lookup"><span data-stu-id="5a629-104">ScheduleByMonth (calendarTriggerType) Element</span></span>

<span data-ttu-id="5a629-105">Spécifie une planification mensuelle.</span><span class="sxs-lookup"><span data-stu-id="5a629-105">Specifies a monthly schedule.</span></span> <span data-ttu-id="5a629-106">Par exemple, la tâche commence à 8:00 AM sur des jours spécifiques du mois sur des mois spécifiques.</span><span class="sxs-lookup"><span data-stu-id="5a629-106">For example, the task starts at 8:00 AM on specific days of the month on specific months.</span></span>

``` syntax
<xs:element name="ScheduleByMonth"
    type="monthlyScheduleType"
 />
```

<span data-ttu-id="5a629-107">L’élément **ScheduleByMonth** est défini par le type complexe [**calendarTriggerType**](taskschedulerschema-calendartriggertype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="5a629-107">The **ScheduleByMonth** element is defined by the [**calendarTriggerType**](taskschedulerschema-calendartriggertype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="5a629-108">Élément parent</span><span class="sxs-lookup"><span data-stu-id="5a629-108">Parent element</span></span>



| <span data-ttu-id="5a629-109">Élément</span><span class="sxs-lookup"><span data-stu-id="5a629-109">Element</span></span>                                                                             | <span data-ttu-id="5a629-110">Dérivé de</span><span class="sxs-lookup"><span data-stu-id="5a629-110">Derived from</span></span>                                                                       | <span data-ttu-id="5a629-111">Description</span><span class="sxs-lookup"><span data-stu-id="5a629-111">Description</span></span>                                                                                |
|-------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5a629-112">**CalendarTrigger**</span><span class="sxs-lookup"><span data-stu-id="5a629-112">**CalendarTrigger**</span></span>](taskschedulerschema-calendartrigger-triggergroup-element.md) | [<span data-ttu-id="5a629-113">**calendarTriggerType**</span><span class="sxs-lookup"><span data-stu-id="5a629-113">**calendarTriggerType**</span></span>](taskschedulerschema-calendartriggertype-complextype.md) | <span data-ttu-id="5a629-114">Spécifie un déclencheur quotidien, hebdomadaire, mensuel ou un jour de la semaine (DOW) mensuel.</span><span class="sxs-lookup"><span data-stu-id="5a629-114">Specifies a daily, weekly, monthly, or a monthly day-of-the-week (DOW) trigger.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="5a629-115">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="5a629-115">Child elements</span></span>



| <span data-ttu-id="5a629-116">Élément</span><span class="sxs-lookup"><span data-stu-id="5a629-116">Element</span></span>                                                                                                  | <span data-ttu-id="5a629-117">Type</span><span class="sxs-lookup"><span data-stu-id="5a629-117">Type</span></span>                                                                       | <span data-ttu-id="5a629-118">Description</span><span class="sxs-lookup"><span data-stu-id="5a629-118">Description</span></span>                                                             |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [<span data-ttu-id="5a629-119">**DaysOfMonth (monthlyScheduleType)**</span><span class="sxs-lookup"><span data-stu-id="5a629-119">**DaysOfMonth (monthlyScheduleType)**</span></span>](taskschedulerschema-daysofmonth-monthlyscheduletype-element.md) | [<span data-ttu-id="5a629-120">**daysOfMonthType**</span><span class="sxs-lookup"><span data-stu-id="5a629-120">**daysOfMonthType**</span></span>](taskschedulerschema-daysofmonthtype-complextype.md) | <span data-ttu-id="5a629-121">Spécifie les jours du mois pendant lesquels la tâche est exécutée.</span><span class="sxs-lookup"><span data-stu-id="5a629-121">Specifies the days of the month during which the task runs.</span></span><br/>  |
| [<span data-ttu-id="5a629-122">**Mois (monthlyScheduleType)**</span><span class="sxs-lookup"><span data-stu-id="5a629-122">**Months (monthlyScheduleType)**</span></span>](taskschedulerschema-months-monthlyscheduletype-element.md)           | [<span data-ttu-id="5a629-123">**monthsType**</span><span class="sxs-lookup"><span data-stu-id="5a629-123">**monthsType**</span></span>](taskschedulerschema-monthstype-complextype.md)           | <span data-ttu-id="5a629-124">Spécifie les mois de l’année pendant laquelle la tâche s’exécute.</span><span class="sxs-lookup"><span data-stu-id="5a629-124">Specifies the months of the year during which the task runs.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="5a629-125">Notes</span><span class="sxs-lookup"><span data-stu-id="5a629-125">Remarks</span></span>

<span data-ttu-id="5a629-126">L’heure de début de la tâche est définie par l’élément [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="5a629-126">The time of day that the task is started is set by the [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) element.</span></span>

<span data-ttu-id="5a629-127">Pour le développement de scripts, un déclencheur mensuel est spécifié à l’aide de l’objet [**MonthlyTrigger**](monthlytrigger.md) .</span><span class="sxs-lookup"><span data-stu-id="5a629-127">For script development, a monthly trigger is specified using the [**MonthlyTrigger**](monthlytrigger.md) object.</span></span>

<span data-ttu-id="5a629-128">Pour le développement C++, un déclencheur mensuel est spécifié à l’aide de l’interface [**IMonthlyTrigger**](/windows/desktop/api/taskschd/nn-taskschd-imonthlytrigger) .</span><span class="sxs-lookup"><span data-stu-id="5a629-128">For C++ development, a monthly trigger is specified using the [**IMonthlyTrigger**](/windows/desktop/api/taskschd/nn-taskschd-imonthlytrigger) interface.</span></span>

<span data-ttu-id="5a629-129">Les éléments enfants répertoriés ci-dessous sont définis par les types d’éléments complexes [**monthlyScheduleType**](taskschedulerschema-monthlyscheduletype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="5a629-129">The child elements listed below are defined by the [**monthlyScheduleType**](taskschedulerschema-monthlyscheduletype-complextype.md) complex element types.</span></span>

## <a name="examples"></a><span data-ttu-id="5a629-130">Exemples</span><span class="sxs-lookup"><span data-stu-id="5a629-130">Examples</span></span>

<span data-ttu-id="5a629-131">Le code XML suivant définit un déclencheur de calendrier mensuel qui démarre une tâche (à 8:00 AM) le 1er et le quinzième jour de chaque mois de l’année.</span><span class="sxs-lookup"><span data-stu-id="5a629-131">The following XML defines a monthly calendar trigger that starts a task ( at 8:00 AM) on the 1st and 15th day of every month of the year.</span></span>


```XML
<CalendarTrigger>
    <StartBoundary>2005-01-01T08:00:00</StartBoundary>
    <EndBounadry>2007-01-01T00:00:00</EndBoundary>
    <ScheduleByMonth>
        <DaysOfMonth>
            <Day>1</Day>
            <Day>15</Day>
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
        </Months>
    </ScheduleByMonth>
</CalendarTrigger>
```



## <a name="requirements"></a><span data-ttu-id="5a629-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5a629-132">Requirements</span></span>



| <span data-ttu-id="5a629-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5a629-133">Requirement</span></span> | <span data-ttu-id="5a629-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="5a629-134">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="5a629-135">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5a629-135">Minimum supported client</span></span><br/> | <span data-ttu-id="5a629-136">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5a629-136">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="5a629-137">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5a629-137">Minimum supported server</span></span><br/> | <span data-ttu-id="5a629-138">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5a629-138">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5a629-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5a629-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a629-140">Éléments de schéma Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="5a629-140">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="5a629-141">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="5a629-141">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





