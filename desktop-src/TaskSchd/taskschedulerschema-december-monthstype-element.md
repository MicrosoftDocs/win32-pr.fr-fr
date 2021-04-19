---
title: Élément de décembre (monthsType)
description: Spécifie que la tâche s’exécute en décembre.
ms.assetid: 42f3cfb2-8e82-46a0-b3ef-42e83d329124
keywords:
- Planificateur de tâches de l’élément de décembre
topic_type:
- apiref
api_name:
- December
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5c907262fe67a0529917d085583465eb97f94c73
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106512615"
---
# <a name="december-monthstype-element"></a><span data-ttu-id="1ad30-104">Élément de décembre (monthsType)</span><span class="sxs-lookup"><span data-stu-id="1ad30-104">December (monthsType) Element</span></span>

<span data-ttu-id="1ad30-105">Spécifie que la tâche s’exécute en décembre.</span><span class="sxs-lookup"><span data-stu-id="1ad30-105">Specifies that the task runs in December.</span></span>

``` syntax
<xs:element name="December">
    <xs:complexType />
</xs:element>
```

<span data-ttu-id="1ad30-106">L’élément **décembre** est défini par le type complexe [**monthsType**](taskschedulerschema-monthstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="1ad30-106">The **December** element is defined by the [**monthsType**](taskschedulerschema-monthstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="1ad30-107">Élément parent</span><span class="sxs-lookup"><span data-stu-id="1ad30-107">Parent element</span></span>



| <span data-ttu-id="1ad30-108">Élément</span><span class="sxs-lookup"><span data-stu-id="1ad30-108">Element</span></span>                                                                                                          | <span data-ttu-id="1ad30-109">Dérivé de</span><span class="sxs-lookup"><span data-stu-id="1ad30-109">Derived from</span></span>                                                     | <span data-ttu-id="1ad30-110">Description</span><span class="sxs-lookup"><span data-stu-id="1ad30-110">Description</span></span>                                                                                                |
|------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1ad30-111">**Mois (monthlyDayOfWeekScheduleType)**</span><span class="sxs-lookup"><span data-stu-id="1ad30-111">**Months (monthlyDayOfWeekScheduleType)**</span></span>](taskschedulerschema-months-monthlydayofweekscheduletype-element.md) | [<span data-ttu-id="1ad30-112">**monthsType**</span><span class="sxs-lookup"><span data-stu-id="1ad30-112">**monthsType**</span></span>](taskschedulerschema-monthstype-complextype.md) | <span data-ttu-id="1ad30-113">Spécifie les mois de l’année pendant laquelle la tâche s’exécute pour une planification mensuelle de jour de semaine.</span><span class="sxs-lookup"><span data-stu-id="1ad30-113">Specifies the months of the year during which the task runs for a monthly day-of-week schedule.</span></span><br/> |
| [<span data-ttu-id="1ad30-114">**Mois (monthlyScheduleType)**</span><span class="sxs-lookup"><span data-stu-id="1ad30-114">**Months (monthlyScheduleType)**</span></span>](taskschedulerschema-months-monthlyscheduletype-element.md)                   | [<span data-ttu-id="1ad30-115">**monthsType**</span><span class="sxs-lookup"><span data-stu-id="1ad30-115">**monthsType**</span></span>](taskschedulerschema-monthstype-complextype.md) | <span data-ttu-id="1ad30-116">Spécifie les mois de l’année pendant laquelle la tâche s’exécute pour une planification mensuelle.</span><span class="sxs-lookup"><span data-stu-id="1ad30-116">Specifies the months of the year during which the task runs for a monthly schedule.</span></span><br/>             |



## <a name="examples"></a><span data-ttu-id="1ad30-117">Exemples</span><span class="sxs-lookup"><span data-stu-id="1ad30-117">Examples</span></span>

<span data-ttu-id="1ad30-118">Le code XML suivant définit un calendrier de mois qui exécute la tâche en décembre.</span><span class="sxs-lookup"><span data-stu-id="1ad30-118">The following XML defines a months calendar that runs the task in December.</span></span>


```XML
<Months>
    <December/>
</Months>
```



## <a name="requirements"></a><span data-ttu-id="1ad30-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1ad30-119">Requirements</span></span>



| <span data-ttu-id="1ad30-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1ad30-120">Requirement</span></span> | <span data-ttu-id="1ad30-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="1ad30-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="1ad30-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1ad30-122">Minimum supported client</span></span><br/> | <span data-ttu-id="1ad30-123">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1ad30-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="1ad30-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1ad30-124">Minimum supported server</span></span><br/> | <span data-ttu-id="1ad30-125">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1ad30-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1ad30-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1ad30-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ad30-127">Éléments de schéma Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="1ad30-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="1ad30-128">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="1ad30-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





