---
title: Tuesday (daysOfWeekType) (élément)
description: Spécifie que la tâche est exécutée le mardi.
ms.assetid: 588608e9-33f9-405d-8b4b-35f11ab403db
keywords:
- Tuesday, élément Planificateur de tâches
topic_type:
- apiref
api_name:
- Tuesday
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5ed48803d0cad5dae409202869c600e7e7a60643
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106511185"
---
# <a name="tuesday-daysofweektype-element"></a><span data-ttu-id="ebf65-104">Tuesday (daysOfWeekType) (élément)</span><span class="sxs-lookup"><span data-stu-id="ebf65-104">Tuesday (daysOfWeekType) Element</span></span>

<span data-ttu-id="ebf65-105">Spécifie que la tâche est exécutée le mardi.</span><span class="sxs-lookup"><span data-stu-id="ebf65-105">Specifies that the task runs on Tuesday.</span></span>

``` syntax
<xs:element name="Tuesday">
    <xs:complexType />
</xs:element>
```

<span data-ttu-id="ebf65-106">L’élément **Tuesday** est défini par le type complexe [**daysOfWeekType**](taskschedulerschema-daysofweektype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="ebf65-106">The **Tuesday** element is defined by the [**daysOfWeekType**](taskschedulerschema-daysofweektype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="ebf65-107">Élément parent</span><span class="sxs-lookup"><span data-stu-id="ebf65-107">Parent element</span></span>



| <span data-ttu-id="ebf65-108">Élément</span><span class="sxs-lookup"><span data-stu-id="ebf65-108">Element</span></span>                                                                                                                  | <span data-ttu-id="ebf65-109">Dérivé de</span><span class="sxs-lookup"><span data-stu-id="ebf65-109">Derived from</span></span>                                                             | <span data-ttu-id="ebf65-110">Description</span><span class="sxs-lookup"><span data-stu-id="ebf65-110">Description</span></span>                                                                                          |
|--------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ebf65-111">**DaysOfWeek (monthlyDayOfWeekScheduleType)**</span><span class="sxs-lookup"><span data-stu-id="ebf65-111">**DaysOfWeek (monthlyDayOfWeekScheduleType)**</span></span>](taskschedulerschema-daysofweek-monthlydayofweekscheduletype-element.md) | [<span data-ttu-id="ebf65-112">**daysOfWeekType**</span><span class="sxs-lookup"><span data-stu-id="ebf65-112">**daysOfWeekType**</span></span>](taskschedulerschema-daysofweektype-complextype.md) | <span data-ttu-id="ebf65-113">Spécifie les jours de la semaine pendant lesquels la tâche s’exécute pour une planification mensuelle de jour de semaine.</span><span class="sxs-lookup"><span data-stu-id="ebf65-113">Specifies the days of the week in which the task runs for a monthly day-of-week schedule.</span></span><br/> |
| [<span data-ttu-id="ebf65-114">**DaysOfWeek (weeklyScheduleType)**</span><span class="sxs-lookup"><span data-stu-id="ebf65-114">**DaysOfWeek (weeklyScheduleType)**</span></span>](taskschedulerschema-daysofweek-weeklyscheduletype-element.md)                     | [<span data-ttu-id="ebf65-115">**daysOfWeekType**</span><span class="sxs-lookup"><span data-stu-id="ebf65-115">**daysOfWeekType**</span></span>](taskschedulerschema-daysofweektype-complextype.md) | <span data-ttu-id="ebf65-116">Spécifie les jours de la semaine pendant lesquels la tâche s’exécute pour une planification hebdomadaire.</span><span class="sxs-lookup"><span data-stu-id="ebf65-116">Specifies the days of the week in which the task runs for a weekly schedule.</span></span><br/>              |



## <a name="examples"></a><span data-ttu-id="ebf65-117">Exemples</span><span class="sxs-lookup"><span data-stu-id="ebf65-117">Examples</span></span>

<span data-ttu-id="ebf65-118">Le code XML suivant définit un calendrier de jour de semaine qui démarre une tâche le mardi.</span><span class="sxs-lookup"><span data-stu-id="ebf65-118">The following XML defines a day of week calendar that starts a task on Tuesday.</span></span>


```XML
<DaysOfWeek>
    <Tuesday/>
</DaysOfWeek>
```



## <a name="requirements"></a><span data-ttu-id="ebf65-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ebf65-119">Requirements</span></span>



| <span data-ttu-id="ebf65-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ebf65-120">Requirement</span></span> | <span data-ttu-id="ebf65-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="ebf65-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="ebf65-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ebf65-122">Minimum supported client</span></span><br/> | <span data-ttu-id="ebf65-123">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ebf65-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="ebf65-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ebf65-124">Minimum supported server</span></span><br/> | <span data-ttu-id="ebf65-125">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ebf65-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ebf65-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ebf65-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ebf65-127">Éléments de schéma Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="ebf65-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="ebf65-128">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="ebf65-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





