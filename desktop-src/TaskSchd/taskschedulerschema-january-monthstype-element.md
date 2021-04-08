---
title: Élément de janvier (monthsType)
description: Spécifie que la tâche s’exécute en janvier.
ms.assetid: 3a0dde08-f2de-4ff4-9c5a-4368ff7a0e2c
keywords:
- Planificateur de tâches de l’élément de janvier
topic_type:
- apiref
api_name:
- January
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e72967f0fb6addb70af1792ffabf0457b1d20c29
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740444"
---
# <a name="january-monthstype-element"></a><span data-ttu-id="c0417-104">Élément de janvier (monthsType)</span><span class="sxs-lookup"><span data-stu-id="c0417-104">January (monthsType) Element</span></span>

<span data-ttu-id="c0417-105">Spécifie que la tâche s’exécute en janvier.</span><span class="sxs-lookup"><span data-stu-id="c0417-105">Specifies that the task runs in January.</span></span>

``` syntax
<xs:element name="January">
    <xs:complexType />
</xs:element>
```

<span data-ttu-id="c0417-106">L’élément de **janvier** est défini par le type complexe [**monthsType**](taskschedulerschema-monthstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="c0417-106">The **January** element is defined by the [**monthsType**](taskschedulerschema-monthstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="c0417-107">Élément parent</span><span class="sxs-lookup"><span data-stu-id="c0417-107">Parent element</span></span>



| <span data-ttu-id="c0417-108">Élément</span><span class="sxs-lookup"><span data-stu-id="c0417-108">Element</span></span>                                                                                                          | <span data-ttu-id="c0417-109">Dérivé de</span><span class="sxs-lookup"><span data-stu-id="c0417-109">Derived from</span></span>                                                     | <span data-ttu-id="c0417-110">Description</span><span class="sxs-lookup"><span data-stu-id="c0417-110">Description</span></span>                                                                                                |
|------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c0417-111">**Mois (monthlyDayOfWeekScheduleType)**</span><span class="sxs-lookup"><span data-stu-id="c0417-111">**Months (monthlyDayOfWeekScheduleType)**</span></span>](taskschedulerschema-months-monthlydayofweekscheduletype-element.md) | [<span data-ttu-id="c0417-112">**monthsType**</span><span class="sxs-lookup"><span data-stu-id="c0417-112">**monthsType**</span></span>](taskschedulerschema-monthstype-complextype.md) | <span data-ttu-id="c0417-113">Spécifie les mois de l’année pendant laquelle la tâche s’exécute pour une planification mensuelle de jour de semaine.</span><span class="sxs-lookup"><span data-stu-id="c0417-113">Specifies the months of the year during which the task runs for a monthly day-of-week schedule.</span></span><br/> |
| [<span data-ttu-id="c0417-114">**Mois (monthlyScheduleType)**</span><span class="sxs-lookup"><span data-stu-id="c0417-114">**Months (monthlyScheduleType)**</span></span>](taskschedulerschema-months-monthlyscheduletype-element.md)                   | [<span data-ttu-id="c0417-115">**monthsType**</span><span class="sxs-lookup"><span data-stu-id="c0417-115">**monthsType**</span></span>](taskschedulerschema-monthstype-complextype.md) | <span data-ttu-id="c0417-116">Spécifie les mois de l’année pendant laquelle la tâche s’exécute pour une planification mensuelle.</span><span class="sxs-lookup"><span data-stu-id="c0417-116">Specifies the months of the year during which the task runs for a monthly schedule.</span></span><br/>             |



## <a name="examples"></a><span data-ttu-id="c0417-117">Exemples</span><span class="sxs-lookup"><span data-stu-id="c0417-117">Examples</span></span>

<span data-ttu-id="c0417-118">Le code XML suivant définit un calendrier de mois qui exécute la tâche en janvier.</span><span class="sxs-lookup"><span data-stu-id="c0417-118">The following XML defines a months calendar that runs the task in January.</span></span>


```XML
<Months>
    <January/>
</Months>
```



## <a name="requirements"></a><span data-ttu-id="c0417-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c0417-119">Requirements</span></span>



| <span data-ttu-id="c0417-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c0417-120">Requirement</span></span> | <span data-ttu-id="c0417-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="c0417-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="c0417-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c0417-122">Minimum supported client</span></span><br/> | <span data-ttu-id="c0417-123">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c0417-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="c0417-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c0417-124">Minimum supported server</span></span><br/> | <span data-ttu-id="c0417-125">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c0417-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c0417-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c0417-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0417-127">Éléments de schéma Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="c0417-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="c0417-128">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="c0417-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





