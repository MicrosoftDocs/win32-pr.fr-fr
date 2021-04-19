---
title: Élément week (weeksType)
description: Spécifie une semaine spécifique du mois.
ms.assetid: 0cec07da-e9e7-43ef-9f54-48d00114ba1f
keywords:
- Élément week Planificateur de tâches
topic_type:
- apiref
api_name:
- Week
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0487aa07e1f1132c998b6cb2ba0f518a9db57ce2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106515086"
---
# <a name="week-weekstype-element"></a><span data-ttu-id="352a9-104">Élément week (weeksType)</span><span class="sxs-lookup"><span data-stu-id="352a9-104">Week (weeksType) Element</span></span>

<span data-ttu-id="352a9-105">Spécifie une semaine spécifique du mois.</span><span class="sxs-lookup"><span data-stu-id="352a9-105">Specifies a specific week of the month.</span></span>

``` syntax
<xs:element name="Week"
    type="weekType"
 />
```

<span data-ttu-id="352a9-106">L’élément **week** est défini par le type complexe [**weeksType**](taskschedulerschema-weekstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="352a9-106">The **Week** element is defined by the [**weeksType**](taskschedulerschema-weekstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="352a9-107">Élément parent</span><span class="sxs-lookup"><span data-stu-id="352a9-107">Parent element</span></span>



| <span data-ttu-id="352a9-108">Élément</span><span class="sxs-lookup"><span data-stu-id="352a9-108">Element</span></span>                                                                                                        | <span data-ttu-id="352a9-109">Dérivé de</span><span class="sxs-lookup"><span data-stu-id="352a9-109">Derived from</span></span>                                                   | <span data-ttu-id="352a9-110">Description</span><span class="sxs-lookup"><span data-stu-id="352a9-110">Description</span></span>                                                           |
|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|-----------------------------------------------------------------------|
| [<span data-ttu-id="352a9-111">**Semaines (monthlyDayOfWeekScheduleType)**</span><span class="sxs-lookup"><span data-stu-id="352a9-111">**Weeks (monthlyDayOfWeekScheduleType)**</span></span>](taskschedulerschema-weeks-monthlydayofweekscheduletype-element.md) | [<span data-ttu-id="352a9-112">**weeksType**</span><span class="sxs-lookup"><span data-stu-id="352a9-112">**weeksType**</span></span>](taskschedulerschema-weekstype-complextype.md) | <span data-ttu-id="352a9-113">Spécifie les semaines du mois où la tâche est exécutée.</span><span class="sxs-lookup"><span data-stu-id="352a9-113">Specifies the weeks of the month in which the task is run.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="352a9-114">Notes</span><span class="sxs-lookup"><span data-stu-id="352a9-114">Remarks</span></span>

<span data-ttu-id="352a9-115">Lorsque vous spécifiez les semaines du mois, utilisez les nombres 1-4 pour les quatre premières semaines du mois ou utilisez la chaîne « Last » pour indiquer la semaine dernière du mois.</span><span class="sxs-lookup"><span data-stu-id="352a9-115">When specifying the weeks of the month, use the numbers 1-4 for the first four weeks of the month or use the string "Last" to indicate that last week of the month.</span></span>

## <a name="requirements"></a><span data-ttu-id="352a9-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="352a9-116">Requirements</span></span>



| <span data-ttu-id="352a9-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="352a9-117">Requirement</span></span> | <span data-ttu-id="352a9-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="352a9-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="352a9-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="352a9-119">Minimum supported client</span></span><br/> | <span data-ttu-id="352a9-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="352a9-120">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="352a9-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="352a9-121">Minimum supported server</span></span><br/> | <span data-ttu-id="352a9-122">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="352a9-122">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="352a9-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="352a9-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="352a9-124">Éléments de schéma Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="352a9-124">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="352a9-125">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="352a9-125">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





