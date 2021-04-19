---
title: WeeklyTrigger. WeeksInterval, propriété
description: Pour les scripts, obtient ou définit l’intervalle entre les semaines de la planification.
ms.assetid: 7992dee2-1725-4325-9fe9-eaff84fa5adc
keywords:
- Planificateur de tâches de la propriété WeeksInterval
- Planificateur de tâches de la propriété WeeksInterval, objet WeeklyTrigger
- Planificateur de tâches objet WeeklyTrigger, propriété WeeksInterval
topic_type:
- apiref
api_name:
- WeeklyTrigger.WeeksInterval
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4668b68d0b3f83e096284db35df799a63eb677b8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106509510"
---
# <a name="weeklytriggerweeksinterval-property"></a><span data-ttu-id="12195-106">WeeklyTrigger. WeeksInterval, propriété</span><span class="sxs-lookup"><span data-stu-id="12195-106">WeeklyTrigger.WeeksInterval property</span></span>

<span data-ttu-id="12195-107">Pour les scripts, obtient ou définit l’intervalle entre les semaines de la planification.</span><span class="sxs-lookup"><span data-stu-id="12195-107">For scripting, gets or sets the interval between the weeks in the schedule.</span></span>

## <a name="syntax"></a><span data-ttu-id="12195-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="12195-108">Syntax</span></span>


```VB
WeeklyTrigger.WeeksInterval As short
```



## <a name="property-value"></a><span data-ttu-id="12195-109">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="12195-109">Property value</span></span>

<span data-ttu-id="12195-110">Intervalle entre les semaines de la planification.</span><span class="sxs-lookup"><span data-stu-id="12195-110">The interval between the weeks in the schedule.</span></span>

## <a name="remarks"></a><span data-ttu-id="12195-111">Notes</span><span class="sxs-lookup"><span data-stu-id="12195-111">Remarks</span></span>

<span data-ttu-id="12195-112">Un intervalle de 1 produit une planification hebdomadaire.</span><span class="sxs-lookup"><span data-stu-id="12195-112">An interval of 1 produces a weekly schedule.</span></span> <span data-ttu-id="12195-113">Un intervalle de 2 produit une planification chaque semaine.</span><span class="sxs-lookup"><span data-stu-id="12195-113">An interval of 2 produces an every-other week schedule.</span></span>

<span data-ttu-id="12195-114">Lors de la lecture ou de l’écriture de vos propres données XML pour une tâche, l’intervalle d’une planification hebdomadaire est spécifié à l’aide de l’élément [**WeeksInterval**](taskschedulerschema-weeksinterval-weeklyscheduletype-element.md) du schéma planificateur de tâches.</span><span class="sxs-lookup"><span data-stu-id="12195-114">When reading or writing your own XML for a task, the interval for a weekly schedule is specified using the [**WeeksInterval**](taskschedulerschema-weeksinterval-weeklyscheduletype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="12195-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="12195-115">Requirements</span></span>



| <span data-ttu-id="12195-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="12195-116">Requirement</span></span> | <span data-ttu-id="12195-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="12195-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="12195-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="12195-118">Minimum supported client</span></span><br/> | <span data-ttu-id="12195-119">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="12195-119">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="12195-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="12195-120">Minimum supported server</span></span><br/> | <span data-ttu-id="12195-121">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="12195-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="12195-122">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="12195-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="12195-123"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="12195-123"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="12195-124">DLL</span><span class="sxs-lookup"><span data-stu-id="12195-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="12195-125"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="12195-125"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="12195-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="12195-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12195-127">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="12195-127">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





