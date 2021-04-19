---
title: Jeudi (daysOfWeekType) (élément)
description: Spécifie que la tâche est exécutée le jeudi.
ms.assetid: 01d0e7e8-7135-4f43-9d8f-b50c002b93bc
keywords:
- Jeudi, élément Planificateur de tâches
topic_type:
- apiref
api_name:
- Thursday
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 12b1fb602411a9e4562a044b044e43de4800f239
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510769"
---
# <a name="thursday-daysofweektype-element"></a><span data-ttu-id="7c86d-104">Jeudi (daysOfWeekType) (élément)</span><span class="sxs-lookup"><span data-stu-id="7c86d-104">Thursday (daysOfWeekType) Element</span></span>

<span data-ttu-id="7c86d-105">Spécifie que la tâche est exécutée le jeudi.</span><span class="sxs-lookup"><span data-stu-id="7c86d-105">Specifies that the task runs on Thursday.</span></span>

``` syntax
<xs:element name="Thursday">
    <xs:complexType />
</xs:element>
```

<span data-ttu-id="7c86d-106">L’élément **Thursday** est défini par le type complexe [**daysOfWeekType**](taskschedulerschema-daysofweektype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="7c86d-106">The **Thursday** element is defined by the [**daysOfWeekType**](taskschedulerschema-daysofweektype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="7c86d-107">Élément parent</span><span class="sxs-lookup"><span data-stu-id="7c86d-107">Parent element</span></span>



| <span data-ttu-id="7c86d-108">Élément</span><span class="sxs-lookup"><span data-stu-id="7c86d-108">Element</span></span>                                                                                                                  | <span data-ttu-id="7c86d-109">Dérivé de</span><span class="sxs-lookup"><span data-stu-id="7c86d-109">Derived from</span></span>                                                             | <span data-ttu-id="7c86d-110">Description</span><span class="sxs-lookup"><span data-stu-id="7c86d-110">Description</span></span>                                                                                          |
|--------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7c86d-111">**DaysOfWeek (monthlyDayOfWeekScheduleType)**</span><span class="sxs-lookup"><span data-stu-id="7c86d-111">**DaysOfWeek (monthlyDayOfWeekScheduleType)**</span></span>](taskschedulerschema-daysofweek-monthlydayofweekscheduletype-element.md) | [<span data-ttu-id="7c86d-112">**daysOfWeekType**</span><span class="sxs-lookup"><span data-stu-id="7c86d-112">**daysOfWeekType**</span></span>](taskschedulerschema-daysofweektype-complextype.md) | <span data-ttu-id="7c86d-113">Spécifie les jours de la semaine pendant lesquels la tâche s’exécute pour une planification mensuelle de jour de semaine.</span><span class="sxs-lookup"><span data-stu-id="7c86d-113">Specifies the days of the week in which the task runs for a monthly day-of-week schedule.</span></span><br/> |
| [<span data-ttu-id="7c86d-114">**DaysOfWeek (weeklyScheduleType)**</span><span class="sxs-lookup"><span data-stu-id="7c86d-114">**DaysOfWeek (weeklyScheduleType)**</span></span>](taskschedulerschema-daysofweek-weeklyscheduletype-element.md)                     | [<span data-ttu-id="7c86d-115">**daysOfWeekType**</span><span class="sxs-lookup"><span data-stu-id="7c86d-115">**daysOfWeekType**</span></span>](taskschedulerschema-daysofweektype-complextype.md) | <span data-ttu-id="7c86d-116">Spécifie les jours de la semaine pendant lesquels la tâche s’exécute pour une planification hebdomadaire.</span><span class="sxs-lookup"><span data-stu-id="7c86d-116">Specifies the days of the week in which the task runs for a weekly schedule.</span></span><br/>              |



## <a name="examples"></a><span data-ttu-id="7c86d-117">Exemples</span><span class="sxs-lookup"><span data-stu-id="7c86d-117">Examples</span></span>

<span data-ttu-id="7c86d-118">Le code XML suivant définit un calendrier de jour de semaine qui démarre une tâche le jeudi.</span><span class="sxs-lookup"><span data-stu-id="7c86d-118">The following XML defines a day of week calendar that starts a task on Thursday.</span></span>


```XML
<DaysOfWeek>
    <Thursday/>
</DaysOfWeek>
```



## <a name="requirements"></a><span data-ttu-id="7c86d-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7c86d-119">Requirements</span></span>



| <span data-ttu-id="7c86d-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7c86d-120">Requirement</span></span> | <span data-ttu-id="7c86d-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="7c86d-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="7c86d-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7c86d-122">Minimum supported client</span></span><br/> | <span data-ttu-id="7c86d-123">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7c86d-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="7c86d-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7c86d-124">Minimum supported server</span></span><br/> | <span data-ttu-id="7c86d-125">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7c86d-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7c86d-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7c86d-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c86d-127">Éléments de schéma Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="7c86d-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="7c86d-128">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="7c86d-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





