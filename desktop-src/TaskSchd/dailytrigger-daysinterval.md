---
title: DailyTrigger. DaysInterval, propriété
description: Pour les scripts, obtient ou définit l’intervalle entre les jours de la planification.
ms.assetid: 13e9f6fd-62ee-4b19-8b3d-a6808e146340
keywords:
- Planificateur de tâches de la propriété DaysInterval
- Planificateur de tâches de la propriété DaysInterval, objet DailyTrigger
- Planificateur de tâches objet DailyTrigger, propriété DaysInterval
topic_type:
- apiref
api_name:
- DailyTrigger.DaysInterval
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6499f3b900fe10b2a2527c2e2ee675cca3151204
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508666"
---
# <a name="dailytriggerdaysinterval-property"></a><span data-ttu-id="b5474-106">DailyTrigger. DaysInterval, propriété</span><span class="sxs-lookup"><span data-stu-id="b5474-106">DailyTrigger.DaysInterval property</span></span>

<span data-ttu-id="b5474-107">Pour les scripts, obtient ou définit l’intervalle entre les jours de la planification.</span><span class="sxs-lookup"><span data-stu-id="b5474-107">For scripting, gets or sets the interval between the days in the schedule.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5474-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b5474-108">Syntax</span></span>


```VB
DailyTrigger.DaysInterval As short
```



## <a name="property-value"></a><span data-ttu-id="b5474-109">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="b5474-109">Property value</span></span>

<span data-ttu-id="b5474-110">Intervalle entre les jours de la planification.</span><span class="sxs-lookup"><span data-stu-id="b5474-110">The interval between the days in the schedule.</span></span>

## <a name="remarks"></a><span data-ttu-id="b5474-111">Notes</span><span class="sxs-lookup"><span data-stu-id="b5474-111">Remarks</span></span>

<span data-ttu-id="b5474-112">Un intervalle de 1 produit une planification quotidienne.</span><span class="sxs-lookup"><span data-stu-id="b5474-112">An interval of 1 produces a daily schedule.</span></span> <span data-ttu-id="b5474-113">Un intervalle de 2 produit une planification tous les jours.</span><span class="sxs-lookup"><span data-stu-id="b5474-113">An interval of 2 produces an every-other day schedule.</span></span>

<span data-ttu-id="b5474-114">Lors de la lecture ou de l’écriture de vos propres données XML pour une tâche, l’intervalle d’une planification quotidienne est spécifié à l’aide de l’élément [**DaysInterval**](taskschedulerschema-daysinterval-dailyscheduletype-element.md) du schéma planificateur de tâches.</span><span class="sxs-lookup"><span data-stu-id="b5474-114">When reading or writing your own XML for a task, the interval for a daily schedule is specified using the [**DaysInterval**](taskschedulerschema-daysinterval-dailyscheduletype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="b5474-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b5474-115">Requirements</span></span>



| <span data-ttu-id="b5474-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b5474-116">Requirement</span></span> | <span data-ttu-id="b5474-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="b5474-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b5474-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b5474-118">Minimum supported client</span></span><br/> | <span data-ttu-id="b5474-119">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b5474-119">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="b5474-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b5474-120">Minimum supported server</span></span><br/> | <span data-ttu-id="b5474-121">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b5474-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b5474-122">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="b5474-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="b5474-123"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="b5474-123"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="b5474-124">DLL</span><span class="sxs-lookup"><span data-stu-id="b5474-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b5474-125"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b5474-125"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b5474-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b5474-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5474-127">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="b5474-127">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="b5474-128">**DailyTrigger**</span><span class="sxs-lookup"><span data-stu-id="b5474-128">**DailyTrigger**</span></span>](dailytrigger.md)
</dt> </dl>

 

 





