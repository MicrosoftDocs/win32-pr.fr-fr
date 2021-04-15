---
title: Élément Monday (daysOfWeekType)
description: Spécifie que la tâche est exécutée le lundi.
ms.assetid: 2b7ce0c1-c635-47d0-b482-5c93c0028c92
keywords:
- Monday, élément Planificateur de tâches
topic_type:
- apiref
api_name:
- Monday
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3967db32a6ccd536e2e389e84de4eec05b333634
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466274"
---
# <a name="monday-daysofweektype-element"></a><span data-ttu-id="7bff9-104">Élément Monday (daysOfWeekType)</span><span class="sxs-lookup"><span data-stu-id="7bff9-104">Monday (daysOfWeekType) Element</span></span>

<span data-ttu-id="7bff9-105">Spécifie que la tâche est exécutée le lundi.</span><span class="sxs-lookup"><span data-stu-id="7bff9-105">Specifies that the task runs on Monday.</span></span>

``` syntax
<xs:element name="Monday">
    <xs:complexType />
</xs:element>
```

<span data-ttu-id="7bff9-106">L’élément **Monday** est défini par le type complexe [**weeklyScheduleType**](taskschedulerschema-weeklyscheduletype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="7bff9-106">The **Monday** element is defined by the [**weeklyScheduleType**](taskschedulerschema-weeklyscheduletype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="7bff9-107">Élément parent</span><span class="sxs-lookup"><span data-stu-id="7bff9-107">Parent element</span></span>



| <span data-ttu-id="7bff9-108">Élément</span><span class="sxs-lookup"><span data-stu-id="7bff9-108">Element</span></span>                                                                                                                  | <span data-ttu-id="7bff9-109">Dérivé de</span><span class="sxs-lookup"><span data-stu-id="7bff9-109">Derived from</span></span>                                                             | <span data-ttu-id="7bff9-110">Description</span><span class="sxs-lookup"><span data-stu-id="7bff9-110">Description</span></span>                                                                                          |
|--------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7bff9-111">**DaysOfWeek (monthlyDayOfWeekScheduleType)**</span><span class="sxs-lookup"><span data-stu-id="7bff9-111">**DaysOfWeek (monthlyDayOfWeekScheduleType)**</span></span>](taskschedulerschema-daysofweek-monthlydayofweekscheduletype-element.md) | [<span data-ttu-id="7bff9-112">**daysOfWeekType**</span><span class="sxs-lookup"><span data-stu-id="7bff9-112">**daysOfWeekType**</span></span>](taskschedulerschema-daysofweektype-complextype.md) | <span data-ttu-id="7bff9-113">Spécifie les jours de la semaine pendant lesquels la tâche s’exécute pour une planification mensuelle de jour de semaine.</span><span class="sxs-lookup"><span data-stu-id="7bff9-113">Specifies the days of the week in which the task runs for a monthly day-of-week schedule.</span></span><br/> |
| [<span data-ttu-id="7bff9-114">**DaysOfWeek (weeklyScheduleType)**</span><span class="sxs-lookup"><span data-stu-id="7bff9-114">**DaysOfWeek (weeklyScheduleType)**</span></span>](taskschedulerschema-daysofweek-weeklyscheduletype-element.md)                     | [<span data-ttu-id="7bff9-115">**daysOfWeekType**</span><span class="sxs-lookup"><span data-stu-id="7bff9-115">**daysOfWeekType**</span></span>](taskschedulerschema-daysofweektype-complextype.md) | <span data-ttu-id="7bff9-116">Spécifie les jours de la semaine pendant lesquels la tâche s’exécute pour une planification hebdomadaire.</span><span class="sxs-lookup"><span data-stu-id="7bff9-116">Specifies the days of the week in which the task runs for a weekly schedule.</span></span><br/>              |



## <a name="examples"></a><span data-ttu-id="7bff9-117">Exemples</span><span class="sxs-lookup"><span data-stu-id="7bff9-117">Examples</span></span>

<span data-ttu-id="7bff9-118">Le code XML suivant définit un calendrier de jour de semaine qui démarre une tâche le lundi.</span><span class="sxs-lookup"><span data-stu-id="7bff9-118">The following XML defines a day of week calendar that starts a task on Monday.</span></span>


```XML
<DaysOfWeek>
    <Monday/>
</DaysOfWeek>
```



## <a name="requirements"></a><span data-ttu-id="7bff9-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7bff9-119">Requirements</span></span>



| <span data-ttu-id="7bff9-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7bff9-120">Requirement</span></span> | <span data-ttu-id="7bff9-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="7bff9-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="7bff9-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7bff9-122">Minimum supported client</span></span><br/> | <span data-ttu-id="7bff9-123">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7bff9-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="7bff9-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7bff9-124">Minimum supported server</span></span><br/> | <span data-ttu-id="7bff9-125">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7bff9-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7bff9-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7bff9-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7bff9-127">Éléments de schéma Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="7bff9-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="7bff9-128">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="7bff9-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





