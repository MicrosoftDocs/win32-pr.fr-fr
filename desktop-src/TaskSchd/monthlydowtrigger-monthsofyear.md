---
title: MonthlyDOWTrigger. MonthsOfYear, propriété
description: Pour les scripts, obtient ou définit les mois de l’année pendant laquelle la tâche s’exécute. | MonthlyDOWTrigger. MonthsOfYear, propriété
ms.assetid: 4ab7ab43-9c9b-4cd3-be8f-1989b83e8cf3
keywords:
- Planificateur de tâches de la propriété MonthsOfYear
- Planificateur de tâches de la propriété MonthsOfYear, objet MonthlyDOWTrigger
- Planificateur de tâches objet MonthlyDOWTrigger, propriété MonthsOfYear
topic_type:
- apiref
api_name:
- MonthlyDOWTrigger.MonthsOfYear
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c345cd3de12d7dba3450f62bdb18bfdcee496b13
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "103869978"
---
# <a name="monthlydowtriggermonthsofyear-property"></a><span data-ttu-id="1f6ec-107">MonthlyDOWTrigger. MonthsOfYear, propriété</span><span class="sxs-lookup"><span data-stu-id="1f6ec-107">MonthlyDOWTrigger.MonthsOfYear property</span></span>

<span data-ttu-id="1f6ec-108">Pour les scripts, obtient ou définit les mois de l’année pendant laquelle la tâche s’exécute.</span><span class="sxs-lookup"><span data-stu-id="1f6ec-108">For scripting, gets or sets the months of the year during which the task runs.</span></span>

## <a name="syntax"></a><span data-ttu-id="1f6ec-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1f6ec-109">Syntax</span></span>


```VB
MonthlyDOWTrigger.MonthsOfYear As short
```



## <a name="property-value"></a><span data-ttu-id="1f6ec-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="1f6ec-110">Property value</span></span>

<span data-ttu-id="1f6ec-111">Un masque de bits qui indique les mois de l’année pendant laquelle la tâche s’exécute.</span><span class="sxs-lookup"><span data-stu-id="1f6ec-111">A bitwise mask that indicates the months of the year during which the task runs.</span></span>

## <a name="remarks"></a><span data-ttu-id="1f6ec-112">Notes</span><span class="sxs-lookup"><span data-stu-id="1f6ec-112">Remarks</span></span>

<span data-ttu-id="1f6ec-113">Le tableau suivant montre le mappage du masque de bits utilisé par cette propriété.</span><span class="sxs-lookup"><span data-stu-id="1f6ec-113">The following table shows the mapping of the bitwise mask used by this property.</span></span>



| <span data-ttu-id="1f6ec-114">Month</span><span class="sxs-lookup"><span data-stu-id="1f6ec-114">Month</span></span>     | <span data-ttu-id="1f6ec-115">Valeur hexadécimale</span><span class="sxs-lookup"><span data-stu-id="1f6ec-115">Hex value</span></span> | <span data-ttu-id="1f6ec-116">Valeur décimale</span><span class="sxs-lookup"><span data-stu-id="1f6ec-116">Decimal value</span></span> |
|-----------|-----------|---------------|
| <span data-ttu-id="1f6ec-117">Janvier</span><span class="sxs-lookup"><span data-stu-id="1f6ec-117">January</span></span>   | <span data-ttu-id="1f6ec-118">0X01</span><span class="sxs-lookup"><span data-stu-id="1f6ec-118">0X01</span></span>      | <span data-ttu-id="1f6ec-119">1</span><span class="sxs-lookup"><span data-stu-id="1f6ec-119">1</span></span>             |
| <span data-ttu-id="1f6ec-120">February</span><span class="sxs-lookup"><span data-stu-id="1f6ec-120">February</span></span>  | <span data-ttu-id="1f6ec-121">0x02</span><span class="sxs-lookup"><span data-stu-id="1f6ec-121">0x02</span></span>      | <span data-ttu-id="1f6ec-122">2</span><span class="sxs-lookup"><span data-stu-id="1f6ec-122">2</span></span>             |
| <span data-ttu-id="1f6ec-123">Mars</span><span class="sxs-lookup"><span data-stu-id="1f6ec-123">March</span></span>     | <span data-ttu-id="1f6ec-124">0X04</span><span class="sxs-lookup"><span data-stu-id="1f6ec-124">0X04</span></span>      | <span data-ttu-id="1f6ec-125">4</span><span class="sxs-lookup"><span data-stu-id="1f6ec-125">4</span></span>             |
| <span data-ttu-id="1f6ec-126">avril</span><span class="sxs-lookup"><span data-stu-id="1f6ec-126">April</span></span>     | <span data-ttu-id="1f6ec-127">0X08</span><span class="sxs-lookup"><span data-stu-id="1f6ec-127">0X08</span></span>      | <span data-ttu-id="1f6ec-128">8</span><span class="sxs-lookup"><span data-stu-id="1f6ec-128">8</span></span>             |
| <span data-ttu-id="1f6ec-129">Mai</span><span class="sxs-lookup"><span data-stu-id="1f6ec-129">May</span></span>       | <span data-ttu-id="1f6ec-130">0X10</span><span class="sxs-lookup"><span data-stu-id="1f6ec-130">0X10</span></span>      | <span data-ttu-id="1f6ec-131">16</span><span class="sxs-lookup"><span data-stu-id="1f6ec-131">16</span></span>            |
| <span data-ttu-id="1f6ec-132">June</span><span class="sxs-lookup"><span data-stu-id="1f6ec-132">June</span></span>      | <span data-ttu-id="1f6ec-133">0X20</span><span class="sxs-lookup"><span data-stu-id="1f6ec-133">0X20</span></span>      | <span data-ttu-id="1f6ec-134">32</span><span class="sxs-lookup"><span data-stu-id="1f6ec-134">32</span></span>            |
| <span data-ttu-id="1f6ec-135">Juillet</span><span class="sxs-lookup"><span data-stu-id="1f6ec-135">July</span></span>      | <span data-ttu-id="1f6ec-136">0x40</span><span class="sxs-lookup"><span data-stu-id="1f6ec-136">0x40</span></span>      | <span data-ttu-id="1f6ec-137">64</span><span class="sxs-lookup"><span data-stu-id="1f6ec-137">64</span></span>            |
| <span data-ttu-id="1f6ec-138">Août</span><span class="sxs-lookup"><span data-stu-id="1f6ec-138">August</span></span>    | <span data-ttu-id="1f6ec-139">0X80</span><span class="sxs-lookup"><span data-stu-id="1f6ec-139">0X80</span></span>      | <span data-ttu-id="1f6ec-140">128</span><span class="sxs-lookup"><span data-stu-id="1f6ec-140">128</span></span>           |
| <span data-ttu-id="1f6ec-141">Septembre</span><span class="sxs-lookup"><span data-stu-id="1f6ec-141">September</span></span> | <span data-ttu-id="1f6ec-142">0X100</span><span class="sxs-lookup"><span data-stu-id="1f6ec-142">0X100</span></span>     | <span data-ttu-id="1f6ec-143">256</span><span class="sxs-lookup"><span data-stu-id="1f6ec-143">256</span></span>           |
| <span data-ttu-id="1f6ec-144">Octobre</span><span class="sxs-lookup"><span data-stu-id="1f6ec-144">October</span></span>   | <span data-ttu-id="1f6ec-145">0X200</span><span class="sxs-lookup"><span data-stu-id="1f6ec-145">0X200</span></span>     | <span data-ttu-id="1f6ec-146">512</span><span class="sxs-lookup"><span data-stu-id="1f6ec-146">512</span></span>           |
| <span data-ttu-id="1f6ec-147">Novembre</span><span class="sxs-lookup"><span data-stu-id="1f6ec-147">November</span></span>  | <span data-ttu-id="1f6ec-148">0X400</span><span class="sxs-lookup"><span data-stu-id="1f6ec-148">0X400</span></span>     | <span data-ttu-id="1f6ec-149">1 024</span><span class="sxs-lookup"><span data-stu-id="1f6ec-149">1024</span></span>          |
| <span data-ttu-id="1f6ec-150">Décembre</span><span class="sxs-lookup"><span data-stu-id="1f6ec-150">December</span></span>  | <span data-ttu-id="1f6ec-151">0X800</span><span class="sxs-lookup"><span data-stu-id="1f6ec-151">0X800</span></span>     | <span data-ttu-id="1f6ec-152">2 048</span><span class="sxs-lookup"><span data-stu-id="1f6ec-152">2048</span></span>          |



 

<span data-ttu-id="1f6ec-153">Lors de la lecture ou de l’écriture de données XML pour une tâche, les mois de l’année d’un calendrier de jour de semaine mensuel sont spécifiés par l’élément [**months**](taskschedulerschema-months-monthlydayofweekscheduletype-element.md) du schéma planificateur de tâches.</span><span class="sxs-lookup"><span data-stu-id="1f6ec-153">When reading or writing XML for a task, the months of the year of a monthly day-of-week calendar are specified by the [**Months**](taskschedulerschema-months-monthlydayofweekscheduletype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="1f6ec-154">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1f6ec-154">Requirements</span></span>



| <span data-ttu-id="1f6ec-155">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1f6ec-155">Requirement</span></span> | <span data-ttu-id="1f6ec-156">Valeur</span><span class="sxs-lookup"><span data-stu-id="1f6ec-156">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1f6ec-157">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1f6ec-157">Minimum supported client</span></span><br/> | <span data-ttu-id="1f6ec-158">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1f6ec-158">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="1f6ec-159">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1f6ec-159">Minimum supported server</span></span><br/> | <span data-ttu-id="1f6ec-160">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1f6ec-160">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="1f6ec-161">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="1f6ec-161">Type library</span></span><br/>             | <dl> <span data-ttu-id="1f6ec-162"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="1f6ec-162"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="1f6ec-163">DLL</span><span class="sxs-lookup"><span data-stu-id="1f6ec-163">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1f6ec-164"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1f6ec-164"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1f6ec-165">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1f6ec-165">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f6ec-166">**MonthlyDOWTrigger**</span><span class="sxs-lookup"><span data-stu-id="1f6ec-166">**MonthlyDOWTrigger**</span></span>](monthlydowtrigger.md)
</dt> <dt>

[<span data-ttu-id="1f6ec-167">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="1f6ec-167">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





