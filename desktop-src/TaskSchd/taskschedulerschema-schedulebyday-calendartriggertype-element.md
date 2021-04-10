---
title: Élément ScheduleByDay (calendarTriggerType)
description: Spécifie une planification quotidienne.
ms.assetid: 5a6097ce-a855-4b08-84c5-71f06343805e
keywords:
- déclencheur quotidien Planificateur de tâches, élément XML
- Élément ScheduleByDay Planificateur de tâches
topic_type:
- apiref
api_name:
- ScheduleByDay
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 614777ede63605dc7ed6936bda952c6071bda371
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942618"
---
# <a name="schedulebyday-calendartriggertype-element"></a><span data-ttu-id="d42b8-105">Élément ScheduleByDay (calendarTriggerType)</span><span class="sxs-lookup"><span data-stu-id="d42b8-105">ScheduleByDay (calendarTriggerType) Element</span></span>

<span data-ttu-id="d42b8-106">Spécifie une planification quotidienne.</span><span class="sxs-lookup"><span data-stu-id="d42b8-106">Specifies a daily schedule.</span></span> <span data-ttu-id="d42b8-107">Par exemple, la tâche commence à 8:00 AM tous les jours, tous les jours, tous les trois jours, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="d42b8-107">For example, the task starts at 8:00 AM every day, every-other day, every third day, and so on.</span></span>

``` syntax
<xs:element name="ScheduleByDay"
    type="dailyScheduleType"
 />
```

<span data-ttu-id="d42b8-108">L’élément **ScheduleByDay** est défini par le type complexe [**calendarTriggerType**](taskschedulerschema-calendartriggertype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="d42b8-108">The **ScheduleByDay** element is defined by the [**calendarTriggerType**](taskschedulerschema-calendartriggertype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="d42b8-109">Élément parent</span><span class="sxs-lookup"><span data-stu-id="d42b8-109">Parent element</span></span>



| <span data-ttu-id="d42b8-110">Élément</span><span class="sxs-lookup"><span data-stu-id="d42b8-110">Element</span></span>                                                                             | <span data-ttu-id="d42b8-111">Dérivé de</span><span class="sxs-lookup"><span data-stu-id="d42b8-111">Derived from</span></span>                                                                       | <span data-ttu-id="d42b8-112">Description</span><span class="sxs-lookup"><span data-stu-id="d42b8-112">Description</span></span>                                                                                |
|-------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d42b8-113">**CalendarTrigger**</span><span class="sxs-lookup"><span data-stu-id="d42b8-113">**CalendarTrigger**</span></span>](taskschedulerschema-calendartrigger-triggergroup-element.md) | [<span data-ttu-id="d42b8-114">**calendarTriggerType**</span><span class="sxs-lookup"><span data-stu-id="d42b8-114">**calendarTriggerType**</span></span>](taskschedulerschema-calendartriggertype-complextype.md) | <span data-ttu-id="d42b8-115">Spécifie un déclencheur quotidien, hebdomadaire, mensuel ou un jour de la semaine (DOW) mensuel.</span><span class="sxs-lookup"><span data-stu-id="d42b8-115">Specifies a daily, weekly, monthly, or a monthly day-of-the-week (DOW) trigger.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="d42b8-116">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="d42b8-116">Child elements</span></span>



| <span data-ttu-id="d42b8-117">Élément</span><span class="sxs-lookup"><span data-stu-id="d42b8-117">Element</span></span>                                                                            | <span data-ttu-id="d42b8-118">Type</span><span class="sxs-lookup"><span data-stu-id="d42b8-118">Type</span></span>             | <span data-ttu-id="d42b8-119">Description</span><span class="sxs-lookup"><span data-stu-id="d42b8-119">Description</span></span>                                                         |
|------------------------------------------------------------------------------------|------------------|---------------------------------------------------------------------|
| [<span data-ttu-id="d42b8-120">**DaysInterval**</span><span class="sxs-lookup"><span data-stu-id="d42b8-120">**DaysInterval**</span></span>](taskschedulerschema-daysinterval-dailyscheduletype-element.md) | <span data-ttu-id="d42b8-121">**unsignedByte**</span><span class="sxs-lookup"><span data-stu-id="d42b8-121">**unsignedByte**</span></span> | <span data-ttu-id="d42b8-122">Spécifie l’intervalle entre les jours de la planification.</span><span class="sxs-lookup"><span data-stu-id="d42b8-122">Specifies the interval between the days in the schedule.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="d42b8-123">Notes</span><span class="sxs-lookup"><span data-stu-id="d42b8-123">Remarks</span></span>

<span data-ttu-id="d42b8-124">L’élément enfant listé précédemment est défini par les types d’éléments complexes [**dailyScheduleType**](taskschedulerschema-dailyscheduletype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="d42b8-124">The child element listed previously is defined by the [**dailyScheduleType**](taskschedulerschema-dailyscheduletype-complextype.md) complex element types.</span></span>

<span data-ttu-id="d42b8-125">L’heure de début de la tâche est définie par l’élément [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="d42b8-125">The time of day that the task is started is set by the [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) element.</span></span>

<span data-ttu-id="d42b8-126">Pour le développement de script, un déclencheur quotidien est spécifié à l’aide de l’objet [**DailyTrigger**](weeklytrigger.md) .</span><span class="sxs-lookup"><span data-stu-id="d42b8-126">For scripting development, a daily trigger is specified using the [**DailyTrigger**](weeklytrigger.md) object.</span></span>

<span data-ttu-id="d42b8-127">Pour le développement C++, un déclencheur quotidien est spécifié à l’aide de l’interface [**IDailyTrigger**](/windows/desktop/api/taskschd/nn-taskschd-idailytrigger) .</span><span class="sxs-lookup"><span data-stu-id="d42b8-127">For C++ development, a daily trigger is specified using the [**IDailyTrigger**](/windows/desktop/api/taskschd/nn-taskschd-idailytrigger) interface.</span></span>

## <a name="examples"></a><span data-ttu-id="d42b8-128">Exemples</span><span class="sxs-lookup"><span data-stu-id="d42b8-128">Examples</span></span>

<span data-ttu-id="d42b8-129">Le code XML suivant définit un déclencheur de calendrier quotidien qui démarre la tâche tous les jours.</span><span class="sxs-lookup"><span data-stu-id="d42b8-129">The following XML defines a daily calendar trigger that starts the task every day.</span></span>


```XML
<CalendarTrigger>
    <StartBoundary>2005-01-01T00:00:00</StartBoundary>
    <EndBounadry>2007-01-01T00:00:00</EndBoundary>
    <ScheduleByDay>
        <DaysInterval>1</DaysInterval>
    </ScheduleByDay>
</CalendarTrigger>
```



<span data-ttu-id="d42b8-130">Pour obtenir un exemple complet du code XML d’une tâche qui spécifie une planification quotidienne, consultez [exemple de déclencheur quotidien (XML)](daily-trigger-example--xml-.md).</span><span class="sxs-lookup"><span data-stu-id="d42b8-130">For a complete example of the XML for a task that specifies a daily schedule, see [Daily Trigger Example (XML)](daily-trigger-example--xml-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d42b8-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d42b8-131">Requirements</span></span>



| <span data-ttu-id="d42b8-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d42b8-132">Requirement</span></span> | <span data-ttu-id="d42b8-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="d42b8-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="d42b8-134">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d42b8-134">Minimum supported client</span></span><br/> | <span data-ttu-id="d42b8-135">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d42b8-135">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="d42b8-136">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d42b8-136">Minimum supported server</span></span><br/> | <span data-ttu-id="d42b8-137">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d42b8-137">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d42b8-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d42b8-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d42b8-139">Éléments de schéma Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="d42b8-139">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="d42b8-140">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="d42b8-140">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





