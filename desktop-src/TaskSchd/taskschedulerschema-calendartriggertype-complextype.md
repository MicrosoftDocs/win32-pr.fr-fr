---
title: Type complexe calendarTriggerType
description: Définit les éléments enfants et les informations de séquencement pour les éléments de calendrier.
ms.assetid: bf0d964e-aff2-4807-b086-c504f8963663
keywords:
- Planificateur de tâches de type complexe calendarTriggerType
topic_type:
- apiref
api_name:
- calendarTriggerType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6f45434fa68b6300157a29318ba257f43bac5992
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106512176"
---
# <a name="calendartriggertype-complex-type"></a><span data-ttu-id="36ea8-104">Type complexe calendarTriggerType</span><span class="sxs-lookup"><span data-stu-id="36ea8-104">calendarTriggerType Complex Type</span></span>

<span data-ttu-id="36ea8-105">Définit les éléments enfants et les informations de séquencement pour les éléments de calendrier.</span><span class="sxs-lookup"><span data-stu-id="36ea8-105">Defines the child elements and sequencing information for calendar elements.</span></span>

``` syntax
<xs:complexType name="calendarTriggerType">
    <xs:complexContent>
        <xs:extension
            base="triggerBaseType"
        >
            <xs:sequence>
                <xs:element name="RandomDelay"
                    type="duration"
                    default="PT0M"
                    minOccurs="0"
                 />
                <xs:choice>
                    <xs:element name="ScheduleByDay"
                        type="dailyScheduleType"
                     />
                    <xs:element name="ScheduleByWeek"
                        type="weeklyScheduleType"
                     />
                    <xs:element name="ScheduleByMonth"
                        type="monthlyScheduleType"
                     />
                    <xs:element name="ScheduleByMonthDayOfWeek"
                        type="monthlyDayOfWeekScheduleType"
                     />
                </xs:choice>
            </xs:sequence>
        </xs:extension>
    </xs:complexContent>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="36ea8-106">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="36ea8-106">Child elements</span></span>



| <span data-ttu-id="36ea8-107">Élément</span><span class="sxs-lookup"><span data-stu-id="36ea8-107">Element</span></span>                                                                                                      | <span data-ttu-id="36ea8-108">Type</span><span class="sxs-lookup"><span data-stu-id="36ea8-108">Type</span></span>                                                                                                 | <span data-ttu-id="36ea8-109">Description</span><span class="sxs-lookup"><span data-stu-id="36ea8-109">Description</span></span>                                                                                                                                                                                                                               |
|--------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="36ea8-110">**RandomDelay**</span><span class="sxs-lookup"><span data-stu-id="36ea8-110">**RandomDelay**</span></span>](taskschedulerschema-randomdelay-calendartriggertype-element.md)                           | <span data-ttu-id="36ea8-111">duration</span><span class="sxs-lookup"><span data-stu-id="36ea8-111">duration</span></span>                                                                                             | <span data-ttu-id="36ea8-112">Contient le délai d’attente ajouté de manière aléatoire à l’heure de début du déclencheur.</span><span class="sxs-lookup"><span data-stu-id="36ea8-112">Contains the delay time that is randomly added to the start time of the trigger.</span></span> <span data-ttu-id="36ea8-113">Le format de cette chaîne est P <days> DT <hours> H <minutes> M <seconds> S (par exemple, P2DT5S est un délai de 2 jours, 5 secondes).</span><span class="sxs-lookup"><span data-stu-id="36ea8-113">The format for this string is P<days>DT<hours>H<minutes>M<seconds>S (for example, P2DT5S is a 2 day, 5 second delay).</span></span><br/> |
| [<span data-ttu-id="36ea8-114">**ScheduleByDay**</span><span class="sxs-lookup"><span data-stu-id="36ea8-114">**ScheduleByDay**</span></span>](taskschedulerschema-schedulebyday-calendartriggertype-element.md)                       | [<span data-ttu-id="36ea8-115">**dailyScheduleType**</span><span class="sxs-lookup"><span data-stu-id="36ea8-115">**dailyScheduleType**</span></span>](taskschedulerschema-dailyscheduletype-complextype.md)                       | <span data-ttu-id="36ea8-116">Spécifie une planification quotidienne.</span><span class="sxs-lookup"><span data-stu-id="36ea8-116">Specifies a daily schedule.</span></span> <span data-ttu-id="36ea8-117">Par exemple, la tâche démarre tous les jours, tous les jours, tous les trois jours, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="36ea8-117">For example, the task starts every day, every-other day, every third day, and so on.</span></span><br/>                                                                                                               |
| [<span data-ttu-id="36ea8-118">**ScheduleByMonth**</span><span class="sxs-lookup"><span data-stu-id="36ea8-118">**ScheduleByMonth**</span></span>](taskschedulerschema-schedulebymonth-calendartriggertype-element.md)                   | [<span data-ttu-id="36ea8-119">**monthlyScheduleType**</span><span class="sxs-lookup"><span data-stu-id="36ea8-119">**monthlyScheduleType**</span></span>](taskschedulerschema-monthlyscheduletype-complextype.md)                   | <span data-ttu-id="36ea8-120">Spécifie une planification mensuelle.</span><span class="sxs-lookup"><span data-stu-id="36ea8-120">Specifies a monthly schedule.</span></span> <span data-ttu-id="36ea8-121">Par exemple, la tâche commence à 8:00 AM sur des jours spécifiques du mois sur des mois spécifiques.</span><span class="sxs-lookup"><span data-stu-id="36ea8-121">For example, the task starts at 8:00 AM on specific days of the month on specific months.</span></span> <br/>                                                                                                       |
| [<span data-ttu-id="36ea8-122">**ScheduleByMonthDayOfWeek**</span><span class="sxs-lookup"><span data-stu-id="36ea8-122">**ScheduleByMonthDayOfWeek**</span></span>](taskschedulerschema-schedulebymonthdayofweek-calendartriggertype-element.md) | [<span data-ttu-id="36ea8-123">**monthlyDayOfWeekScheduleType**</span><span class="sxs-lookup"><span data-stu-id="36ea8-123">**monthlyDayOfWeekScheduleType**</span></span>](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) | <span data-ttu-id="36ea8-124">Spécifie un déclencheur qui démarre un travail sur une planification de jour de semaine mensuelle.</span><span class="sxs-lookup"><span data-stu-id="36ea8-124">Specifies a trigger that starts a job on a monthly day-of-week schedule.</span></span> <span data-ttu-id="36ea8-125">Par exemple, la tâche démarre des jours spécifiques de la semaine, des semaines du mois et des mois de l’année.</span><span class="sxs-lookup"><span data-stu-id="36ea8-125">For example, the task starts on specific days of the week, weeks of the month, and months of the year.</span></span> <br/>                                               |
| [<span data-ttu-id="36ea8-126">**ScheduleByWeek**</span><span class="sxs-lookup"><span data-stu-id="36ea8-126">**ScheduleByWeek**</span></span>](taskschedulerschema-schedulebyweek-calendartriggertype-element.md)                     | [<span data-ttu-id="36ea8-127">**weeklyScheduleType**</span><span class="sxs-lookup"><span data-stu-id="36ea8-127">**weeklyScheduleType**</span></span>](taskschedulerschema-weeklyscheduletype-complextype.md)                     | <span data-ttu-id="36ea8-128">Spécifie une planification hebdomadaire.</span><span class="sxs-lookup"><span data-stu-id="36ea8-128">Specifies a weekly schedule.</span></span> <span data-ttu-id="36ea8-129">Par exemple, la tâche commence à 8:00 AM un jour spécifique de la semaine chaque semaine ou un jour spécifique de la semaine chaque semaine.</span><span class="sxs-lookup"><span data-stu-id="36ea8-129">For example, the task starts at 8:00 AM on a specific day of the week every week or on a specific day of the week every other week.</span></span> <br/>                                                              |



## <a name="remarks"></a><span data-ttu-id="36ea8-130">Notes</span><span class="sxs-lookup"><span data-stu-id="36ea8-130">Remarks</span></span>

<span data-ttu-id="36ea8-131">En plus de l’élément enfant défini ici, l’élément [**CalendarTrigger**](taskschedulerschema-calendartrigger-triggergroup-element.md) utilise également les éléments enfants définis par le type complexe [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="36ea8-131">In addition to the child element defined here, the [**CalendarTrigger**](taskschedulerschema-calendartrigger-triggergroup-element.md) element also uses the child elements defined by the [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="36ea8-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="36ea8-132">Requirements</span></span>



| <span data-ttu-id="36ea8-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="36ea8-133">Requirement</span></span> | <span data-ttu-id="36ea8-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="36ea8-134">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="36ea8-135">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="36ea8-135">Minimum supported client</span></span><br/> | <span data-ttu-id="36ea8-136">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="36ea8-136">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="36ea8-137">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="36ea8-137">Minimum supported server</span></span><br/> | <span data-ttu-id="36ea8-138">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="36ea8-138">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="36ea8-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="36ea8-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36ea8-140">Types complexes de schéma Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="36ea8-140">Task Scheduler Schema Complex Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="36ea8-141">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="36ea8-141">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





