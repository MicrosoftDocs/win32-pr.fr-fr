---
title: Mercredi (daysOfWeekType) (élément)
description: Spécifie que la tâche est exécutée le mercredi.
ms.assetid: 6d4f52e2-4390-4f9d-bab8-813bd0851582
keywords:
- Mercredi, élément Planificateur de tâches
topic_type:
- apiref
api_name:
- Wednesday
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3f9d8c60cb7cea818cc0b096e99e97e8f1490d47
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509045"
---
# <a name="wednesday-daysofweektype-element"></a><span data-ttu-id="5fa91-104">Mercredi (daysOfWeekType) (élément)</span><span class="sxs-lookup"><span data-stu-id="5fa91-104">Wednesday (daysOfWeekType) Element</span></span>

<span data-ttu-id="5fa91-105">Spécifie que la tâche est exécutée le mercredi.</span><span class="sxs-lookup"><span data-stu-id="5fa91-105">Specifies that the task runs on Wednesday.</span></span>

``` syntax
<xs:element name="Wednesday">
    <xs:complexType />
</xs:element>
```

<span data-ttu-id="5fa91-106">L’élément **mercredi** est défini par le type complexe [**daysOfWeekType**](taskschedulerschema-daysofweektype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="5fa91-106">The **Wednesday** element is defined by the [**daysOfWeekType**](taskschedulerschema-daysofweektype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="5fa91-107">Élément parent</span><span class="sxs-lookup"><span data-stu-id="5fa91-107">Parent element</span></span>



| <span data-ttu-id="5fa91-108">Élément</span><span class="sxs-lookup"><span data-stu-id="5fa91-108">Element</span></span>                                                                                                                  | <span data-ttu-id="5fa91-109">Dérivé de</span><span class="sxs-lookup"><span data-stu-id="5fa91-109">Derived from</span></span>                                                             | <span data-ttu-id="5fa91-110">Description</span><span class="sxs-lookup"><span data-stu-id="5fa91-110">Description</span></span>                                                                                          |
|--------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5fa91-111">**DaysOfWeek (monthlyDayOfWeekScheduleType)**</span><span class="sxs-lookup"><span data-stu-id="5fa91-111">**DaysOfWeek (monthlyDayOfWeekScheduleType)**</span></span>](taskschedulerschema-daysofweek-monthlydayofweekscheduletype-element.md) | [<span data-ttu-id="5fa91-112">**daysOfWeekType**</span><span class="sxs-lookup"><span data-stu-id="5fa91-112">**daysOfWeekType**</span></span>](taskschedulerschema-daysofweektype-complextype.md) | <span data-ttu-id="5fa91-113">Spécifie les jours de la semaine pendant lesquels la tâche s’exécute pour une planification mensuelle de jour de semaine.</span><span class="sxs-lookup"><span data-stu-id="5fa91-113">Specifies the days of the week in which the task runs for a monthly day-of-week schedule.</span></span><br/> |
| [<span data-ttu-id="5fa91-114">**DaysOfWeek (weeklyScheduleType)**</span><span class="sxs-lookup"><span data-stu-id="5fa91-114">**DaysOfWeek (weeklyScheduleType)**</span></span>](taskschedulerschema-daysofweek-weeklyscheduletype-element.md)                     | [<span data-ttu-id="5fa91-115">**daysOfWeekType**</span><span class="sxs-lookup"><span data-stu-id="5fa91-115">**daysOfWeekType**</span></span>](taskschedulerschema-daysofweektype-complextype.md) | <span data-ttu-id="5fa91-116">Spécifie les jours de la semaine pendant lesquels la tâche s’exécute pour une planification hebdomadaire.</span><span class="sxs-lookup"><span data-stu-id="5fa91-116">Specifies the days of the week in which the task runs for a weekly schedule.</span></span><br/>              |



## <a name="examples"></a><span data-ttu-id="5fa91-117">Exemples</span><span class="sxs-lookup"><span data-stu-id="5fa91-117">Examples</span></span>

<span data-ttu-id="5fa91-118">Le code XML suivant définit un calendrier de jour de semaine qui démarre une tâche le mercredi.</span><span class="sxs-lookup"><span data-stu-id="5fa91-118">The following XML defines a day of week calendar that starts a task on Wednesday.</span></span>


```XML
<DaysOfWeek>
    <Wednesday/>
</DaysOfWeek>
```



## <a name="requirements"></a><span data-ttu-id="5fa91-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5fa91-119">Requirements</span></span>



| <span data-ttu-id="5fa91-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5fa91-120">Requirement</span></span> | <span data-ttu-id="5fa91-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="5fa91-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="5fa91-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5fa91-122">Minimum supported client</span></span><br/> | <span data-ttu-id="5fa91-123">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5fa91-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="5fa91-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5fa91-124">Minimum supported server</span></span><br/> | <span data-ttu-id="5fa91-125">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5fa91-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5fa91-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5fa91-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5fa91-127">Éléments de schéma Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="5fa91-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="5fa91-128">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="5fa91-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





