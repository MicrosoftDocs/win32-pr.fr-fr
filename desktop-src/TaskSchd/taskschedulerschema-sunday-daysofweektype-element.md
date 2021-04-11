---
title: Sunday (daysOfWeekType) (élément)
description: Spécifie que la tâche est exécutée le dimanche.
ms.assetid: 856db869-2273-4bb8-88c8-c126bb16c87b
keywords:
- Sunday, élément Planificateur de tâches
topic_type:
- apiref
api_name:
- Sunday
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 40efba31b392da5959853feeb1cae567cee25cc7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105352"
---
# <a name="sunday-daysofweektype-element"></a><span data-ttu-id="aae64-104">Sunday (daysOfWeekType) (élément)</span><span class="sxs-lookup"><span data-stu-id="aae64-104">Sunday (daysOfWeekType) Element</span></span>

<span data-ttu-id="aae64-105">Spécifie que la tâche est exécutée le dimanche.</span><span class="sxs-lookup"><span data-stu-id="aae64-105">Specifies that the task runs on Sunday.</span></span>

``` syntax
<xs:element name="Sunday">
    <xs:complexType />
</xs:element>
```

<span data-ttu-id="aae64-106">L’élément **Sunday** est défini par le type complexe [**daysOfWeekType**](taskschedulerschema-daysofweektype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="aae64-106">The **Sunday** element is defined by the [**daysOfWeekType**](taskschedulerschema-daysofweektype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="aae64-107">Élément parent</span><span class="sxs-lookup"><span data-stu-id="aae64-107">Parent element</span></span>



| <span data-ttu-id="aae64-108">Élément</span><span class="sxs-lookup"><span data-stu-id="aae64-108">Element</span></span>                                                                                                                  | <span data-ttu-id="aae64-109">Dérivé de</span><span class="sxs-lookup"><span data-stu-id="aae64-109">Derived from</span></span>                                                             | <span data-ttu-id="aae64-110">Description</span><span class="sxs-lookup"><span data-stu-id="aae64-110">Description</span></span>                                                                                          |
|--------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="aae64-111">**DaysOfWeek (monthlyDayOfWeekScheduleType)**</span><span class="sxs-lookup"><span data-stu-id="aae64-111">**DaysOfWeek (monthlyDayOfWeekScheduleType)**</span></span>](taskschedulerschema-daysofweek-monthlydayofweekscheduletype-element.md) | [<span data-ttu-id="aae64-112">**daysOfWeekType**</span><span class="sxs-lookup"><span data-stu-id="aae64-112">**daysOfWeekType**</span></span>](taskschedulerschema-daysofweektype-complextype.md) | <span data-ttu-id="aae64-113">Spécifie les jours de la semaine pendant lesquels la tâche s’exécute pour une planification mensuelle de jour de semaine.</span><span class="sxs-lookup"><span data-stu-id="aae64-113">Specifies the days of the week in which the task runs for a monthly day-of-week schedule.</span></span><br/> |
| [<span data-ttu-id="aae64-114">**DaysOfWeek (weeklyScheduleType)**</span><span class="sxs-lookup"><span data-stu-id="aae64-114">**DaysOfWeek (weeklyScheduleType)**</span></span>](taskschedulerschema-daysofweek-weeklyscheduletype-element.md)                     | [<span data-ttu-id="aae64-115">**daysOfWeekType**</span><span class="sxs-lookup"><span data-stu-id="aae64-115">**daysOfWeekType**</span></span>](taskschedulerschema-daysofweektype-complextype.md) | <span data-ttu-id="aae64-116">Spécifie les jours de la semaine pendant lesquels la tâche s’exécute pour une planification hebdomadaire.</span><span class="sxs-lookup"><span data-stu-id="aae64-116">Specifies the days of the week in which the task runs for a weekly schedule.</span></span><br/>              |



## <a name="examples"></a><span data-ttu-id="aae64-117">Exemples</span><span class="sxs-lookup"><span data-stu-id="aae64-117">Examples</span></span>

<span data-ttu-id="aae64-118">Le code XML suivant définit un calendrier de jour de semaine qui démarre une tâche le dimanche.</span><span class="sxs-lookup"><span data-stu-id="aae64-118">The following XML defines a day of week calendar that starts a task on Sunday.</span></span>


```XML
<DaysOfWeek>
    <Sunday/>
</DaysOfWeek>
```



## <a name="requirements"></a><span data-ttu-id="aae64-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="aae64-119">Requirements</span></span>



| <span data-ttu-id="aae64-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="aae64-120">Requirement</span></span> | <span data-ttu-id="aae64-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="aae64-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="aae64-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="aae64-122">Minimum supported client</span></span><br/> | <span data-ttu-id="aae64-123">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="aae64-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="aae64-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="aae64-124">Minimum supported server</span></span><br/> | <span data-ttu-id="aae64-125">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="aae64-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="aae64-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="aae64-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aae64-127">Éléments de schéma Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="aae64-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="aae64-128">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="aae64-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





