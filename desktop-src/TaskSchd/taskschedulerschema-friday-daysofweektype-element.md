---
title: Élément Friday (daysOfWeekType)
description: Spécifie que la tâche est exécutée le vendredi.
ms.assetid: bff85911-d354-4954-8c69-7b6f2ca312d3
keywords:
- Friday, élément Planificateur de tâches
topic_type:
- apiref
api_name:
- Friday
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 951142e7e925ea71ef1f833be4421351aaea3b35
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105223"
---
# <a name="friday-daysofweektype-element"></a><span data-ttu-id="b3d60-104">Élément Friday (daysOfWeekType)</span><span class="sxs-lookup"><span data-stu-id="b3d60-104">Friday (daysOfWeekType) Element</span></span>

<span data-ttu-id="b3d60-105">Spécifie que la tâche est exécutée le vendredi.</span><span class="sxs-lookup"><span data-stu-id="b3d60-105">Specifies that the task runs on Friday.</span></span>

``` syntax
<xs:element name="Friday">
    <xs:complexType />
</xs:element>
```

<span data-ttu-id="b3d60-106">L’élément **Friday** est défini par le type complexe [**daysOfWeekType**](taskschedulerschema-daysofweektype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="b3d60-106">The **Friday** element is defined by the [**daysOfWeekType**](taskschedulerschema-daysofweektype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="b3d60-107">Élément parent</span><span class="sxs-lookup"><span data-stu-id="b3d60-107">Parent element</span></span>



| <span data-ttu-id="b3d60-108">Élément</span><span class="sxs-lookup"><span data-stu-id="b3d60-108">Element</span></span>                                                                                                                  | <span data-ttu-id="b3d60-109">Dérivé de</span><span class="sxs-lookup"><span data-stu-id="b3d60-109">Derived from</span></span>                                                             | <span data-ttu-id="b3d60-110">Description</span><span class="sxs-lookup"><span data-stu-id="b3d60-110">Description</span></span>                                                                                          |
|--------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b3d60-111">**DaysOfWeek (monthlyDayOfWeekScheduleType)**</span><span class="sxs-lookup"><span data-stu-id="b3d60-111">**DaysOfWeek (monthlyDayOfWeekScheduleType)**</span></span>](taskschedulerschema-daysofweek-monthlydayofweekscheduletype-element.md) | [<span data-ttu-id="b3d60-112">**daysOfWeekType**</span><span class="sxs-lookup"><span data-stu-id="b3d60-112">**daysOfWeekType**</span></span>](taskschedulerschema-daysofweektype-complextype.md) | <span data-ttu-id="b3d60-113">Spécifie les jours de la semaine pendant lesquels la tâche s’exécute pour une planification mensuelle de jour de semaine.</span><span class="sxs-lookup"><span data-stu-id="b3d60-113">Specifies the days of the week in which the task runs for a monthly day-of-week schedule.</span></span><br/> |
| [<span data-ttu-id="b3d60-114">**DaysOfWeek (weeklyScheduleType)**</span><span class="sxs-lookup"><span data-stu-id="b3d60-114">**DaysOfWeek (weeklyScheduleType)**</span></span>](taskschedulerschema-daysofweek-weeklyscheduletype-element.md)                     | [<span data-ttu-id="b3d60-115">**daysOfWeekType**</span><span class="sxs-lookup"><span data-stu-id="b3d60-115">**daysOfWeekType**</span></span>](taskschedulerschema-daysofweektype-complextype.md) | <span data-ttu-id="b3d60-116">Spécifie les jours de la semaine pendant lesquels la tâche s’exécute pour une planification hebdomadaire.</span><span class="sxs-lookup"><span data-stu-id="b3d60-116">Specifies the days of the week in which the task runs for a weekly schedule.</span></span><br/>              |



## <a name="examples"></a><span data-ttu-id="b3d60-117">Exemples</span><span class="sxs-lookup"><span data-stu-id="b3d60-117">Examples</span></span>

<span data-ttu-id="b3d60-118">Le code XML suivant définit un calendrier de jour de semaine qui démarre une tâche le vendredi.</span><span class="sxs-lookup"><span data-stu-id="b3d60-118">The following XML defines a day of week calendar that starts a task on Friday.</span></span>


```XML
<DaysOfWeek>
    <Friday/>
</DaysOfWeek>
```



## <a name="requirements"></a><span data-ttu-id="b3d60-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b3d60-119">Requirements</span></span>



| <span data-ttu-id="b3d60-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b3d60-120">Requirement</span></span> | <span data-ttu-id="b3d60-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="b3d60-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="b3d60-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b3d60-122">Minimum supported client</span></span><br/> | <span data-ttu-id="b3d60-123">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b3d60-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="b3d60-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b3d60-124">Minimum supported server</span></span><br/> | <span data-ttu-id="b3d60-125">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b3d60-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b3d60-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b3d60-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3d60-127">Éléments de schéma Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="b3d60-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="b3d60-128">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="b3d60-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





