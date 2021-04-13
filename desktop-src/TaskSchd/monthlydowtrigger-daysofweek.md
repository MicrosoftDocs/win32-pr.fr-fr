---
title: MonthlyDOWTrigger. DaysOfWeek, propriété
description: Pour les scripts, obtient ou définit les jours de la semaine pendant lesquels la tâche est exécutée.
ms.assetid: dd9b2463-69a1-4e77-a8f7-26b186d3d02d
keywords:
- DaysOfWeek, propriété Planificateur de tâches
- DaysOfWeek, propriété Planificateur de tâches, objet MonthlyDOWTrigger
- Objet MonthlyDOWTrigger Planificateur de tâches, DaysOfWeek, propriété
topic_type:
- apiref
api_name:
- MonthlyDOWTrigger.DaysOfWeek
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15344650dabdec2bcbacf91397b37b97ce3f0772
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466442"
---
# <a name="monthlydowtriggerdaysofweek-property"></a><span data-ttu-id="2b2cc-106">MonthlyDOWTrigger. DaysOfWeek, propriété</span><span class="sxs-lookup"><span data-stu-id="2b2cc-106">MonthlyDOWTrigger.DaysOfWeek property</span></span>

<span data-ttu-id="2b2cc-107">Pour les scripts, obtient ou définit les jours de la semaine pendant lesquels la tâche est exécutée.</span><span class="sxs-lookup"><span data-stu-id="2b2cc-107">For scripting, gets or sets the days of the week during which the task runs.</span></span>

## <a name="syntax"></a><span data-ttu-id="2b2cc-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2b2cc-108">Syntax</span></span>


```VB
MonthlyDOWTrigger.DaysOfWeek As short
```



## <a name="property-value"></a><span data-ttu-id="2b2cc-109">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="2b2cc-109">Property value</span></span>

<span data-ttu-id="2b2cc-110">Un masque de bits qui indique les jours de la semaine pendant lesquels la tâche s’exécute.</span><span class="sxs-lookup"><span data-stu-id="2b2cc-110">A bitwise mask that indicates the days of the week during which the task runs.</span></span>

## <a name="remarks"></a><span data-ttu-id="2b2cc-111">Notes</span><span class="sxs-lookup"><span data-stu-id="2b2cc-111">Remarks</span></span>

<span data-ttu-id="2b2cc-112">Le tableau suivant montre le mappage du masque de bits utilisé par cette propriété.</span><span class="sxs-lookup"><span data-stu-id="2b2cc-112">The following table shows the mapping of the bitwise mask used by this property.</span></span>



| <span data-ttu-id="2b2cc-113">Jour de la semaine</span><span class="sxs-lookup"><span data-stu-id="2b2cc-113">Day of Week</span></span> | <span data-ttu-id="2b2cc-114">Valeur hexadécimale</span><span class="sxs-lookup"><span data-stu-id="2b2cc-114">Hex Value</span></span> | <span data-ttu-id="2b2cc-115">Valeur décimale</span><span class="sxs-lookup"><span data-stu-id="2b2cc-115">Decimal Value</span></span> |
|-------------|-----------|---------------|
| <span data-ttu-id="2b2cc-116">Dimanche</span><span class="sxs-lookup"><span data-stu-id="2b2cc-116">Sunday</span></span>      | <span data-ttu-id="2b2cc-117">0x01</span><span class="sxs-lookup"><span data-stu-id="2b2cc-117">0x01</span></span>      | <span data-ttu-id="2b2cc-118">1</span><span class="sxs-lookup"><span data-stu-id="2b2cc-118">1</span></span>             |
| <span data-ttu-id="2b2cc-119">Lundi</span><span class="sxs-lookup"><span data-stu-id="2b2cc-119">Monday</span></span>      | <span data-ttu-id="2b2cc-120">0x02</span><span class="sxs-lookup"><span data-stu-id="2b2cc-120">0x02</span></span>      | <span data-ttu-id="2b2cc-121">2</span><span class="sxs-lookup"><span data-stu-id="2b2cc-121">2</span></span>             |
| <span data-ttu-id="2b2cc-122">Mardi</span><span class="sxs-lookup"><span data-stu-id="2b2cc-122">Tuesday</span></span>     | <span data-ttu-id="2b2cc-123">0x04</span><span class="sxs-lookup"><span data-stu-id="2b2cc-123">0x04</span></span>      | <span data-ttu-id="2b2cc-124">4</span><span class="sxs-lookup"><span data-stu-id="2b2cc-124">4</span></span>             |
| <span data-ttu-id="2b2cc-125">Mercredi</span><span class="sxs-lookup"><span data-stu-id="2b2cc-125">Wednesday</span></span>   | <span data-ttu-id="2b2cc-126">0x08</span><span class="sxs-lookup"><span data-stu-id="2b2cc-126">0x08</span></span>      | <span data-ttu-id="2b2cc-127">8</span><span class="sxs-lookup"><span data-stu-id="2b2cc-127">8</span></span>             |
| <span data-ttu-id="2b2cc-128">Thursday</span><span class="sxs-lookup"><span data-stu-id="2b2cc-128">Thursday</span></span>    | <span data-ttu-id="2b2cc-129">0x10</span><span class="sxs-lookup"><span data-stu-id="2b2cc-129">0x10</span></span>      | <span data-ttu-id="2b2cc-130">16</span><span class="sxs-lookup"><span data-stu-id="2b2cc-130">16</span></span>            |
| <span data-ttu-id="2b2cc-131">Vendredi</span><span class="sxs-lookup"><span data-stu-id="2b2cc-131">Friday</span></span>      | <span data-ttu-id="2b2cc-132">0x20</span><span class="sxs-lookup"><span data-stu-id="2b2cc-132">0x20</span></span>      | <span data-ttu-id="2b2cc-133">32</span><span class="sxs-lookup"><span data-stu-id="2b2cc-133">32</span></span>            |
| <span data-ttu-id="2b2cc-134">Samedi</span><span class="sxs-lookup"><span data-stu-id="2b2cc-134">Saturday</span></span>    | <span data-ttu-id="2b2cc-135">0x40</span><span class="sxs-lookup"><span data-stu-id="2b2cc-135">0x40</span></span>      | <span data-ttu-id="2b2cc-136">64</span><span class="sxs-lookup"><span data-stu-id="2b2cc-136">64</span></span>            |



 

<span data-ttu-id="2b2cc-137">Lors de la lecture ou de l’écriture de données XML pour une tâche, les jours de la semaine d’un calendrier de jour de semaine mensuel sont spécifiés par l’élément [**DaysOfWeek**](taskschedulerschema-daysofweek-monthlydayofweekscheduletype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="2b2cc-137">When reading or writing XML for a task, the days of the week of a monthly day-of-week calendar are specified by the [**DaysOfWeek**](taskschedulerschema-daysofweek-monthlydayofweekscheduletype-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="2b2cc-138">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2b2cc-138">Requirements</span></span>



| <span data-ttu-id="2b2cc-139">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2b2cc-139">Requirement</span></span> | <span data-ttu-id="2b2cc-140">Valeur</span><span class="sxs-lookup"><span data-stu-id="2b2cc-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2b2cc-141">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2b2cc-141">Minimum supported client</span></span><br/> | <span data-ttu-id="2b2cc-142">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2b2cc-142">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="2b2cc-143">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2b2cc-143">Minimum supported server</span></span><br/> | <span data-ttu-id="2b2cc-144">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2b2cc-144">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="2b2cc-145">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="2b2cc-145">Type library</span></span><br/>             | <dl> <span data-ttu-id="2b2cc-146"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="2b2cc-146"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="2b2cc-147">DLL</span><span class="sxs-lookup"><span data-stu-id="2b2cc-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2b2cc-148"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2b2cc-148"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2b2cc-149">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2b2cc-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b2cc-150">**MonthlyDOWTrigger**</span><span class="sxs-lookup"><span data-stu-id="2b2cc-150">**MonthlyDOWTrigger**</span></span>](monthlydowtrigger.md)
</dt> <dt>

[<span data-ttu-id="2b2cc-151">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="2b2cc-151">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





