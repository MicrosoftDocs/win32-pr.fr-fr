---
title: WeeklyTrigger. DaysOfWeek, propriété
description: Pour les scripts, obtient ou définit les jours de la semaine où la tâche est exécutée.
ms.assetid: 79f279d4-d6d2-428b-bbed-226e4eaaefb6
keywords:
- DaysOfWeek, propriété Planificateur de tâches
- DaysOfWeek, propriété Planificateur de tâches, objet WeeklyTrigger
- Objet WeeklyTrigger Planificateur de tâches, DaysOfWeek, propriété
topic_type:
- apiref
api_name:
- WeeklyTrigger.DaysOfWeek
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7f0a27ef031e7baf46d2d3c0e33c23fb505c7ee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104519257"
---
# <a name="weeklytriggerdaysofweek-property"></a><span data-ttu-id="144dc-106">WeeklyTrigger. DaysOfWeek, propriété</span><span class="sxs-lookup"><span data-stu-id="144dc-106">WeeklyTrigger.DaysOfWeek property</span></span>

<span data-ttu-id="144dc-107">Pour les scripts, obtient ou définit les jours de la semaine où la tâche est exécutée.</span><span class="sxs-lookup"><span data-stu-id="144dc-107">For scripting, gets or sets the days of the week on which the task runs.</span></span>

## <a name="syntax"></a><span data-ttu-id="144dc-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="144dc-108">Syntax</span></span>


```VB
WeeklyTrigger.DaysOfWeek As short
```



## <a name="property-value"></a><span data-ttu-id="144dc-109">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="144dc-109">Property value</span></span>

<span data-ttu-id="144dc-110">Un masque de bits qui indique les jours de la semaine où la tâche est exécutée.</span><span class="sxs-lookup"><span data-stu-id="144dc-110">A bitwise mask that indicates the days of the week on which the task runs.</span></span>

## <a name="remarks"></a><span data-ttu-id="144dc-111">Notes</span><span class="sxs-lookup"><span data-stu-id="144dc-111">Remarks</span></span>

<span data-ttu-id="144dc-112">Le tableau suivant montre le mappage du masque de bits utilisé par cette propriété.</span><span class="sxs-lookup"><span data-stu-id="144dc-112">The following table shows the mapping of the bitwise mask used by this property.</span></span>



| <span data-ttu-id="144dc-113">Month</span><span class="sxs-lookup"><span data-stu-id="144dc-113">Month</span></span>     | <span data-ttu-id="144dc-114">Valeur hexadécimale</span><span class="sxs-lookup"><span data-stu-id="144dc-114">Hex value</span></span> | <span data-ttu-id="144dc-115">Valeur décimale</span><span class="sxs-lookup"><span data-stu-id="144dc-115">Decimal value</span></span> |
|-----------|-----------|---------------|
| <span data-ttu-id="144dc-116">Dimanche</span><span class="sxs-lookup"><span data-stu-id="144dc-116">Sunday</span></span>    | <span data-ttu-id="144dc-117">0X01</span><span class="sxs-lookup"><span data-stu-id="144dc-117">0X01</span></span>      | <span data-ttu-id="144dc-118">1</span><span class="sxs-lookup"><span data-stu-id="144dc-118">1</span></span>             |
| <span data-ttu-id="144dc-119">Lundi</span><span class="sxs-lookup"><span data-stu-id="144dc-119">Monday</span></span>    | <span data-ttu-id="144dc-120">0x02</span><span class="sxs-lookup"><span data-stu-id="144dc-120">0x02</span></span>      | <span data-ttu-id="144dc-121">2</span><span class="sxs-lookup"><span data-stu-id="144dc-121">2</span></span>             |
| <span data-ttu-id="144dc-122">Mardi</span><span class="sxs-lookup"><span data-stu-id="144dc-122">Tuesday</span></span>   | <span data-ttu-id="144dc-123">0X04</span><span class="sxs-lookup"><span data-stu-id="144dc-123">0X04</span></span>      | <span data-ttu-id="144dc-124">4</span><span class="sxs-lookup"><span data-stu-id="144dc-124">4</span></span>             |
| <span data-ttu-id="144dc-125">Mercredi</span><span class="sxs-lookup"><span data-stu-id="144dc-125">Wednesday</span></span> | <span data-ttu-id="144dc-126">0X08</span><span class="sxs-lookup"><span data-stu-id="144dc-126">0X08</span></span>      | <span data-ttu-id="144dc-127">8</span><span class="sxs-lookup"><span data-stu-id="144dc-127">8</span></span>             |
| <span data-ttu-id="144dc-128">Thursday</span><span class="sxs-lookup"><span data-stu-id="144dc-128">Thursday</span></span>  | <span data-ttu-id="144dc-129">0X10</span><span class="sxs-lookup"><span data-stu-id="144dc-129">0X10</span></span>      | <span data-ttu-id="144dc-130">16</span><span class="sxs-lookup"><span data-stu-id="144dc-130">16</span></span>            |
| <span data-ttu-id="144dc-131">Vendredi</span><span class="sxs-lookup"><span data-stu-id="144dc-131">Friday</span></span>    | <span data-ttu-id="144dc-132">0x20</span><span class="sxs-lookup"><span data-stu-id="144dc-132">0x20</span></span>      | <span data-ttu-id="144dc-133">32</span><span class="sxs-lookup"><span data-stu-id="144dc-133">32</span></span>            |
| <span data-ttu-id="144dc-134">Samedi</span><span class="sxs-lookup"><span data-stu-id="144dc-134">Saturday</span></span>  | <span data-ttu-id="144dc-135">0X40</span><span class="sxs-lookup"><span data-stu-id="144dc-135">0X40</span></span>      | <span data-ttu-id="144dc-136">64</span><span class="sxs-lookup"><span data-stu-id="144dc-136">64</span></span>            |



 

<span data-ttu-id="144dc-137">Lors de la lecture ou de l’écriture de vos propres données XML pour une tâche, les jours de la semaine sont spécifiés à l’aide de l’élément [**DaysOfWeek**](taskschedulerschema-daysofweek-weeklyscheduletype-element.md) du schéma planificateur de tâches.</span><span class="sxs-lookup"><span data-stu-id="144dc-137">When reading or writing your own XML for a task, the days of the week are specified using the [**DaysOfWeek**](taskschedulerschema-daysofweek-weeklyscheduletype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="144dc-138">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="144dc-138">Requirements</span></span>



| <span data-ttu-id="144dc-139">Condition requise</span><span class="sxs-lookup"><span data-stu-id="144dc-139">Requirement</span></span> | <span data-ttu-id="144dc-140">Valeur</span><span class="sxs-lookup"><span data-stu-id="144dc-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="144dc-141">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="144dc-141">Minimum supported client</span></span><br/> | <span data-ttu-id="144dc-142">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="144dc-142">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="144dc-143">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="144dc-143">Minimum supported server</span></span><br/> | <span data-ttu-id="144dc-144">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="144dc-144">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="144dc-145">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="144dc-145">Type library</span></span><br/>             | <dl> <span data-ttu-id="144dc-146"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="144dc-146"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="144dc-147">DLL</span><span class="sxs-lookup"><span data-stu-id="144dc-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="144dc-148"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="144dc-148"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="144dc-149">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="144dc-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="144dc-150">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="144dc-150">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





