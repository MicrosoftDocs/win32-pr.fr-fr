---
title: Élément DaysInterval (dailyScheduleType)
description: Spécifie l’intervalle entre les jours de la planification.
ms.assetid: 495ea1c0-37eb-4b12-8241-bfc6489e33ed
keywords:
- Élément DaysInterval Planificateur de tâches
topic_type:
- apiref
api_name:
- DaysInterval
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 97b50581aa4825b31983a234a5eb47ff7b7b7e06
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941771"
---
# <a name="daysinterval-dailyscheduletype-element"></a><span data-ttu-id="b9c0a-104">Élément DaysInterval (dailyScheduleType)</span><span class="sxs-lookup"><span data-stu-id="b9c0a-104">DaysInterval (dailyScheduleType) Element</span></span>

<span data-ttu-id="b9c0a-105">Spécifie l’intervalle entre les jours de la planification.</span><span class="sxs-lookup"><span data-stu-id="b9c0a-105">Specifies the interval between the days in the schedule.</span></span>

``` syntax
<xs:element name="DaysInterval"
    minOccurs="0"
>
    <xs:simpleType>
        <xs:restriction
            base="unsignedInt"
        >
            <xs:minInclusive
                value="1"
             />
            <xs:maxInclusive
                value="365"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="b9c0a-106">L’élément est défini par le type complexe [**dailyScheduleType**](taskschedulerschema-dailyscheduletype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="b9c0a-106">The element is defined by the [**dailyScheduleType**](taskschedulerschema-dailyscheduletype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="b9c0a-107">Élément parent</span><span class="sxs-lookup"><span data-stu-id="b9c0a-107">Parent element</span></span>



| <span data-ttu-id="b9c0a-108">Élément</span><span class="sxs-lookup"><span data-stu-id="b9c0a-108">Element</span></span>                                                                                | <span data-ttu-id="b9c0a-109">Dérivé de</span><span class="sxs-lookup"><span data-stu-id="b9c0a-109">Derived from</span></span>                                                                   | <span data-ttu-id="b9c0a-110">Description</span><span class="sxs-lookup"><span data-stu-id="b9c0a-110">Description</span></span>                            |
|----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|----------------------------------------|
| [<span data-ttu-id="b9c0a-111">**ScheduleByDay**</span><span class="sxs-lookup"><span data-stu-id="b9c0a-111">**ScheduleByDay**</span></span>](taskschedulerschema-schedulebyday-calendartriggertype-element.md) | [<span data-ttu-id="b9c0a-112">**dailyScheduleType**</span><span class="sxs-lookup"><span data-stu-id="b9c0a-112">**dailyScheduleType**</span></span>](taskschedulerschema-dailyscheduletype-complextype.md) | <span data-ttu-id="b9c0a-113">Spécifie une planification quotidienne.</span><span class="sxs-lookup"><span data-stu-id="b9c0a-113">Specifies a daily schedule.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="b9c0a-114">Notes</span><span class="sxs-lookup"><span data-stu-id="b9c0a-114">Remarks</span></span>

<span data-ttu-id="b9c0a-115">Pour le développement de script, l’intervalle de jours pour un déclencheur quotidien est spécifié par la propriété [**DailyTrigger. DaysInterval**](dailytrigger-daysinterval.md) .</span><span class="sxs-lookup"><span data-stu-id="b9c0a-115">For script development, the days interval for a daily trigger is specified by the [**DailyTrigger.DaysInterval**](dailytrigger-daysinterval.md) property.</span></span>

<span data-ttu-id="b9c0a-116">Pour le développement C++, l’intervalle de jours pour un déclencheur quotidien est spécifié par la propriété [**IDailyTrigger ::D aysinterval**](/windows/desktop/api/taskschd/nf-taskschd-idailytrigger-get_daysinterval) .</span><span class="sxs-lookup"><span data-stu-id="b9c0a-116">For C++ development, the days interval for a daily trigger is specified by the [**IDailyTrigger::DaysInterval**](/windows/desktop/api/taskschd/nf-taskschd-idailytrigger-get_daysinterval) property.</span></span>

## <a name="examples"></a><span data-ttu-id="b9c0a-117">Exemples</span><span class="sxs-lookup"><span data-stu-id="b9c0a-117">Examples</span></span>

<span data-ttu-id="b9c0a-118">Le code XML suivant définit un déclencheur de calendrier quotidien qui démarre la tâche tous les jours.</span><span class="sxs-lookup"><span data-stu-id="b9c0a-118">The following XML defines a daily calendar trigger that starts the task every day.</span></span>


```XML
<CalendarTrigger>
    <StartBoundary>2005-01-01T00:00:00</StartBoundary>
    <EndBounadry>2007-01-01T00:00:00</EndBoundary>
    <ScheduleByDay>
        <DaysInterval>1</DaysInterval>
    </ScheduleByDay>
</CalendarTrigger>
```



<span data-ttu-id="b9c0a-119">Pour obtenir un exemple complet du code XML d’une tâche qui spécifie une planification quotidienne, consultez [exemple de déclencheur quotidien (XML)](daily-trigger-example--xml-.md).</span><span class="sxs-lookup"><span data-stu-id="b9c0a-119">For a complete example of the XML for a task that specifies a daily schedule, see [Daily Trigger Example (XML)](daily-trigger-example--xml-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b9c0a-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b9c0a-120">Requirements</span></span>



| <span data-ttu-id="b9c0a-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b9c0a-121">Requirement</span></span> | <span data-ttu-id="b9c0a-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="b9c0a-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="b9c0a-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b9c0a-123">Minimum supported client</span></span><br/> | <span data-ttu-id="b9c0a-124">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b9c0a-124">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="b9c0a-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b9c0a-125">Minimum supported server</span></span><br/> | <span data-ttu-id="b9c0a-126">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b9c0a-126">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b9c0a-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b9c0a-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9c0a-128">Éléments de schéma Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="b9c0a-128">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="b9c0a-129">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="b9c0a-129">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





