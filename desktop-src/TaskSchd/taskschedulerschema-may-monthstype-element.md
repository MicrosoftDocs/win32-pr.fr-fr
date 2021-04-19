---
title: Élément mai (monthsType)
description: Spécifie que la tâche s’exécute en mai.
ms.assetid: 1fcc3eb7-6500-4ba3-b146-14d169d9b445
keywords:
- Élément de mai Planificateur de tâches
topic_type:
- apiref
api_name:
- May
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d3f0c107124aa2c87672f63a469857f3795e13c4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106512825"
---
# <a name="may-monthstype-element"></a><span data-ttu-id="c2206-104">Élément mai (monthsType)</span><span class="sxs-lookup"><span data-stu-id="c2206-104">May (monthsType) Element</span></span>

<span data-ttu-id="c2206-105">Spécifie que la tâche s’exécute en mai.</span><span class="sxs-lookup"><span data-stu-id="c2206-105">Specifies that the task runs in May.</span></span>

``` syntax
<xs:element name="May">
    <xs:complexType />
</xs:element>
```

<span data-ttu-id="c2206-106">L’élément **peut être** défini par le type complexe [**monthsType**](taskschedulerschema-monthstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="c2206-106">The **May** element is defined by the [**monthsType**](taskschedulerschema-monthstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="c2206-107">Élément parent</span><span class="sxs-lookup"><span data-stu-id="c2206-107">Parent element</span></span>



| <span data-ttu-id="c2206-108">Élément</span><span class="sxs-lookup"><span data-stu-id="c2206-108">Element</span></span>                                                                                                          | <span data-ttu-id="c2206-109">Dérivé de</span><span class="sxs-lookup"><span data-stu-id="c2206-109">Derived from</span></span>                                                     | <span data-ttu-id="c2206-110">Description</span><span class="sxs-lookup"><span data-stu-id="c2206-110">Description</span></span>                                                                                                |
|------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c2206-111">**Mois (monthlyDayOfWeekScheduleType)**</span><span class="sxs-lookup"><span data-stu-id="c2206-111">**Months (monthlyDayOfWeekScheduleType)**</span></span>](taskschedulerschema-months-monthlydayofweekscheduletype-element.md) | [<span data-ttu-id="c2206-112">**monthsType**</span><span class="sxs-lookup"><span data-stu-id="c2206-112">**monthsType**</span></span>](taskschedulerschema-monthstype-complextype.md) | <span data-ttu-id="c2206-113">Spécifie les mois de l’année pendant laquelle la tâche s’exécute pour une planification mensuelle de jour de semaine.</span><span class="sxs-lookup"><span data-stu-id="c2206-113">Specifies the months of the year during which the task runs for a monthly day-of-week schedule.</span></span><br/> |
| [<span data-ttu-id="c2206-114">**Mois (monthlyScheduleType)**</span><span class="sxs-lookup"><span data-stu-id="c2206-114">**Months (monthlyScheduleType)**</span></span>](taskschedulerschema-months-monthlyscheduletype-element.md)                   | [<span data-ttu-id="c2206-115">**monthsType**</span><span class="sxs-lookup"><span data-stu-id="c2206-115">**monthsType**</span></span>](taskschedulerschema-monthstype-complextype.md) | <span data-ttu-id="c2206-116">Spécifie les mois de l’année pendant laquelle la tâche s’exécute pour une planification mensuelle.</span><span class="sxs-lookup"><span data-stu-id="c2206-116">Specifies the months of the year during which the task runs for a monthly schedule.</span></span><br/>             |



## <a name="examples"></a><span data-ttu-id="c2206-117">Exemples</span><span class="sxs-lookup"><span data-stu-id="c2206-117">Examples</span></span>

<span data-ttu-id="c2206-118">Le code XML suivant définit un calendrier de mois qui exécute la tâche dans mai.</span><span class="sxs-lookup"><span data-stu-id="c2206-118">The following XML defines a months calendar that runs the task in May.</span></span>


```XML
<Months>
    <May/>
</Months>
```



## <a name="requirements"></a><span data-ttu-id="c2206-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c2206-119">Requirements</span></span>



| <span data-ttu-id="c2206-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c2206-120">Requirement</span></span> | <span data-ttu-id="c2206-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="c2206-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="c2206-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c2206-122">Minimum supported client</span></span><br/> | <span data-ttu-id="c2206-123">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c2206-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="c2206-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c2206-124">Minimum supported server</span></span><br/> | <span data-ttu-id="c2206-125">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c2206-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c2206-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c2206-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2206-127">Éléments de schéma Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="c2206-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="c2206-128">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="c2206-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





