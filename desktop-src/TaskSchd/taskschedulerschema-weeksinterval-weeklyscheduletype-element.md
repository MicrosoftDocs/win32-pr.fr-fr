---
title: Élément WeeksInterval (weeklyScheduleType)
description: Spécifie l’intervalle entre les semaines de la planification.
ms.assetid: 6cbf1e7e-a695-4012-97fd-fe3360c362c4
keywords:
- Élément WeeksInterval Planificateur de tâches
topic_type:
- apiref
api_name:
- WeeksInterval
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 747ca4b73ff18bdb3e29d8b909d72b8d2367d89b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104385100"
---
# <a name="weeksinterval-weeklyscheduletype-element"></a><span data-ttu-id="2d822-104">Élément WeeksInterval (weeklyScheduleType)</span><span class="sxs-lookup"><span data-stu-id="2d822-104">WeeksInterval (weeklyScheduleType) Element</span></span>

<span data-ttu-id="2d822-105">Spécifie l’intervalle entre les semaines de la planification.</span><span class="sxs-lookup"><span data-stu-id="2d822-105">Specifies the interval between the weeks in the schedule.</span></span>

``` syntax
<xs:element name="WeeksInterval"
    minOccurs="0"
>
    <xs:simpleType>
        <xs:restriction
            base="unsignedByte"
        >
            <xs:minInclusive
                value="1"
             />
            <xs:maxInclusive
                value="52"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="2d822-106">L’élément est défini par le type complexe [**weeklyScheduleType**](taskschedulerschema-weeklyscheduletype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="2d822-106">The element is defined by the [**weeklyScheduleType**](taskschedulerschema-weeklyscheduletype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="2d822-107">Élément parent</span><span class="sxs-lookup"><span data-stu-id="2d822-107">Parent element</span></span>



| <span data-ttu-id="2d822-108">Élément</span><span class="sxs-lookup"><span data-stu-id="2d822-108">Element</span></span>                                                                                  | <span data-ttu-id="2d822-109">Dérivé de</span><span class="sxs-lookup"><span data-stu-id="2d822-109">Derived from</span></span>                                                                     | <span data-ttu-id="2d822-110">Description</span><span class="sxs-lookup"><span data-stu-id="2d822-110">Description</span></span>                             |
|------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|-----------------------------------------|
| [<span data-ttu-id="2d822-111">**ScheduleByWeek**</span><span class="sxs-lookup"><span data-stu-id="2d822-111">**ScheduleByWeek**</span></span>](taskschedulerschema-schedulebyweek-calendartriggertype-element.md) | [<span data-ttu-id="2d822-112">**weeklyScheduleType**</span><span class="sxs-lookup"><span data-stu-id="2d822-112">**weeklyScheduleType**</span></span>](taskschedulerschema-weeklyscheduletype-complextype.md) | <span data-ttu-id="2d822-113">Spécifie une planification hebdomadaire.</span><span class="sxs-lookup"><span data-stu-id="2d822-113">Specifies a weekly schedule.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="2d822-114">Notes</span><span class="sxs-lookup"><span data-stu-id="2d822-114">Remarks</span></span>

<span data-ttu-id="2d822-115">Pour le développement de script, l’intervalle hebdomadaire est spécifié à l’aide de la propriété [**WeeklyTrigger. WeeksInterval**](weeklytrigger-weeksinterval.md) .</span><span class="sxs-lookup"><span data-stu-id="2d822-115">For scripting development, the weekly interval is specified using the [**WeeklyTrigger.WeeksInterval**](weeklytrigger-weeksinterval.md) property.</span></span>

<span data-ttu-id="2d822-116">Pour le développement C++, l’intervalle hebdomadaire est spécifié à l’aide de la propriété [**IWeeklyTrigger :: WeeksInterval**](/windows/desktop/api/taskschd/nf-taskschd-iweeklytrigger-get_weeksinterval) .</span><span class="sxs-lookup"><span data-stu-id="2d822-116">For C++ development, the weekly interval is specified using the [**IWeeklyTrigger::WeeksInterval**](/windows/desktop/api/taskschd/nf-taskschd-iweeklytrigger-get_weeksinterval) property.</span></span>

## <a name="examples"></a><span data-ttu-id="2d822-117">Exemples</span><span class="sxs-lookup"><span data-stu-id="2d822-117">Examples</span></span>

<span data-ttu-id="2d822-118">Le code XML suivant définit un déclencheur de calendrier hebdomadaire qui démarre une tâche du lundi au vendredi (à 8:00 AM) chaque semaine.</span><span class="sxs-lookup"><span data-stu-id="2d822-118">The following XML defines a weekly calendar trigger that starts a task Monday through Friday ( at 8:00 AM) every week.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="2d822-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2d822-119">Requirements</span></span>



| <span data-ttu-id="2d822-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2d822-120">Requirement</span></span> | <span data-ttu-id="2d822-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="2d822-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="2d822-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2d822-122">Minimum supported client</span></span><br/> | <span data-ttu-id="2d822-123">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2d822-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="2d822-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2d822-124">Minimum supported server</span></span><br/> | <span data-ttu-id="2d822-125">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2d822-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2d822-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2d822-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d822-127">Éléments de schéma Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="2d822-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="2d822-128">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="2d822-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





