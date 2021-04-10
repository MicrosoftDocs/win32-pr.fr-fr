---
title: MonthlyTrigger. MonthsOfYear, propriété
description: Pour les scripts, obtient ou définit les mois de l’année pendant laquelle la tâche s’exécute. | MonthlyTrigger. MonthsOfYear, propriété
ms.assetid: cf26a815-7f4f-4b7a-8db8-a4bd9b77cf49
keywords:
- Planificateur de tâches de la propriété MonthsOfYear
- Planificateur de tâches de la propriété MonthsOfYear, objet MonthlyTrigger
- Planificateur de tâches objet MonthlyTrigger, propriété MonthsOfYear
topic_type:
- apiref
api_name:
- MonthlyTrigger.MonthsOfYear
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5683fb1c85e470ca7c82b069929de0351ea7cffe
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "103869878"
---
# <a name="monthlytriggermonthsofyear-property"></a><span data-ttu-id="d7bc8-107">MonthlyTrigger. MonthsOfYear, propriété</span><span class="sxs-lookup"><span data-stu-id="d7bc8-107">MonthlyTrigger.MonthsOfYear property</span></span>

<span data-ttu-id="d7bc8-108">Pour les scripts, obtient ou définit les mois de l’année pendant laquelle la tâche s’exécute.</span><span class="sxs-lookup"><span data-stu-id="d7bc8-108">For scripting, gets or sets the months of the year during which the task runs.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7bc8-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d7bc8-109">Syntax</span></span>


```VB
MonthlyTrigger.MonthsOfYear As short
```



## <a name="property-value"></a><span data-ttu-id="d7bc8-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="d7bc8-110">Property value</span></span>

<span data-ttu-id="d7bc8-111">Un masque de bits qui indique les mois de l’année pendant laquelle la tâche s’exécute.</span><span class="sxs-lookup"><span data-stu-id="d7bc8-111">A bitwise mask that indicates the months of the year during which the task runs.</span></span>

## <a name="remarks"></a><span data-ttu-id="d7bc8-112">Notes</span><span class="sxs-lookup"><span data-stu-id="d7bc8-112">Remarks</span></span>

<span data-ttu-id="d7bc8-113">Le tableau suivant montre le mappage du masque de bits utilisé par cette propriété.</span><span class="sxs-lookup"><span data-stu-id="d7bc8-113">The following table shows the mapping of the bitwise mask that is used by this property.</span></span>



| <span data-ttu-id="d7bc8-114">Month</span><span class="sxs-lookup"><span data-stu-id="d7bc8-114">Month</span></span>     | <span data-ttu-id="d7bc8-115">Valeur hexadécimale</span><span class="sxs-lookup"><span data-stu-id="d7bc8-115">Hex value</span></span> | <span data-ttu-id="d7bc8-116">Valeur décimale</span><span class="sxs-lookup"><span data-stu-id="d7bc8-116">Decimal value</span></span> |
|-----------|-----------|---------------|
| <span data-ttu-id="d7bc8-117">Janvier</span><span class="sxs-lookup"><span data-stu-id="d7bc8-117">January</span></span>   | <span data-ttu-id="d7bc8-118">0X01</span><span class="sxs-lookup"><span data-stu-id="d7bc8-118">0X01</span></span>      | <span data-ttu-id="d7bc8-119">1</span><span class="sxs-lookup"><span data-stu-id="d7bc8-119">1</span></span>             |
| <span data-ttu-id="d7bc8-120">February</span><span class="sxs-lookup"><span data-stu-id="d7bc8-120">February</span></span>  | <span data-ttu-id="d7bc8-121">0x02</span><span class="sxs-lookup"><span data-stu-id="d7bc8-121">0x02</span></span>      | <span data-ttu-id="d7bc8-122">2</span><span class="sxs-lookup"><span data-stu-id="d7bc8-122">2</span></span>             |
| <span data-ttu-id="d7bc8-123">Mars</span><span class="sxs-lookup"><span data-stu-id="d7bc8-123">March</span></span>     | <span data-ttu-id="d7bc8-124">0X04</span><span class="sxs-lookup"><span data-stu-id="d7bc8-124">0X04</span></span>      | <span data-ttu-id="d7bc8-125">4</span><span class="sxs-lookup"><span data-stu-id="d7bc8-125">4</span></span>             |
| <span data-ttu-id="d7bc8-126">avril</span><span class="sxs-lookup"><span data-stu-id="d7bc8-126">April</span></span>     | <span data-ttu-id="d7bc8-127">0X08</span><span class="sxs-lookup"><span data-stu-id="d7bc8-127">0X08</span></span>      | <span data-ttu-id="d7bc8-128">8</span><span class="sxs-lookup"><span data-stu-id="d7bc8-128">8</span></span>             |
| <span data-ttu-id="d7bc8-129">Mai</span><span class="sxs-lookup"><span data-stu-id="d7bc8-129">May</span></span>       | <span data-ttu-id="d7bc8-130">0X10</span><span class="sxs-lookup"><span data-stu-id="d7bc8-130">0X10</span></span>      | <span data-ttu-id="d7bc8-131">16</span><span class="sxs-lookup"><span data-stu-id="d7bc8-131">16</span></span>            |
| <span data-ttu-id="d7bc8-132">June</span><span class="sxs-lookup"><span data-stu-id="d7bc8-132">June</span></span>      | <span data-ttu-id="d7bc8-133">0X20</span><span class="sxs-lookup"><span data-stu-id="d7bc8-133">0X20</span></span>      | <span data-ttu-id="d7bc8-134">32</span><span class="sxs-lookup"><span data-stu-id="d7bc8-134">32</span></span>            |
| <span data-ttu-id="d7bc8-135">Juillet</span><span class="sxs-lookup"><span data-stu-id="d7bc8-135">July</span></span>      | <span data-ttu-id="d7bc8-136">0x40</span><span class="sxs-lookup"><span data-stu-id="d7bc8-136">0x40</span></span>      | <span data-ttu-id="d7bc8-137">64</span><span class="sxs-lookup"><span data-stu-id="d7bc8-137">64</span></span>            |
| <span data-ttu-id="d7bc8-138">Août</span><span class="sxs-lookup"><span data-stu-id="d7bc8-138">August</span></span>    | <span data-ttu-id="d7bc8-139">0X80</span><span class="sxs-lookup"><span data-stu-id="d7bc8-139">0X80</span></span>      | <span data-ttu-id="d7bc8-140">128</span><span class="sxs-lookup"><span data-stu-id="d7bc8-140">128</span></span>           |
| <span data-ttu-id="d7bc8-141">Septembre</span><span class="sxs-lookup"><span data-stu-id="d7bc8-141">September</span></span> | <span data-ttu-id="d7bc8-142">0X100</span><span class="sxs-lookup"><span data-stu-id="d7bc8-142">0X100</span></span>     | <span data-ttu-id="d7bc8-143">256</span><span class="sxs-lookup"><span data-stu-id="d7bc8-143">256</span></span>           |
| <span data-ttu-id="d7bc8-144">Octobre</span><span class="sxs-lookup"><span data-stu-id="d7bc8-144">October</span></span>   | <span data-ttu-id="d7bc8-145">0X200</span><span class="sxs-lookup"><span data-stu-id="d7bc8-145">0X200</span></span>     | <span data-ttu-id="d7bc8-146">512</span><span class="sxs-lookup"><span data-stu-id="d7bc8-146">512</span></span>           |
| <span data-ttu-id="d7bc8-147">Novembre</span><span class="sxs-lookup"><span data-stu-id="d7bc8-147">November</span></span>  | <span data-ttu-id="d7bc8-148">0X400</span><span class="sxs-lookup"><span data-stu-id="d7bc8-148">0X400</span></span>     | <span data-ttu-id="d7bc8-149">1 024</span><span class="sxs-lookup"><span data-stu-id="d7bc8-149">1024</span></span>          |
| <span data-ttu-id="d7bc8-150">Décembre</span><span class="sxs-lookup"><span data-stu-id="d7bc8-150">December</span></span>  | <span data-ttu-id="d7bc8-151">0X800</span><span class="sxs-lookup"><span data-stu-id="d7bc8-151">0X800</span></span>     | <span data-ttu-id="d7bc8-152">2 048</span><span class="sxs-lookup"><span data-stu-id="d7bc8-152">2048</span></span>          |



 

<span data-ttu-id="d7bc8-153">Lors de la lecture ou de l’écriture de votre propre XML pour une tâche, les mois de l’année sont spécifiés à l’aide de l’élément [**months**](taskschedulerschema-months-monthlyscheduletype-element.md) du schéma planificateur de tâches.</span><span class="sxs-lookup"><span data-stu-id="d7bc8-153">When reading or writing your own XML for a task, the months of the year are specified using the [**Months**](taskschedulerschema-months-monthlyscheduletype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="d7bc8-154">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d7bc8-154">Requirements</span></span>



| <span data-ttu-id="d7bc8-155">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d7bc8-155">Requirement</span></span> | <span data-ttu-id="d7bc8-156">Valeur</span><span class="sxs-lookup"><span data-stu-id="d7bc8-156">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d7bc8-157">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d7bc8-157">Minimum supported client</span></span><br/> | <span data-ttu-id="d7bc8-158">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d7bc8-158">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="d7bc8-159">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d7bc8-159">Minimum supported server</span></span><br/> | <span data-ttu-id="d7bc8-160">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d7bc8-160">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d7bc8-161">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="d7bc8-161">Type library</span></span><br/>             | <dl> <span data-ttu-id="d7bc8-162"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="d7bc8-162"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="d7bc8-163">DLL</span><span class="sxs-lookup"><span data-stu-id="d7bc8-163">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d7bc8-164"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d7bc8-164"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d7bc8-165">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d7bc8-165">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7bc8-166">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="d7bc8-166">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="d7bc8-167">**MonthlyTrigger**</span><span class="sxs-lookup"><span data-stu-id="d7bc8-167">**MonthlyTrigger**</span></span>](monthlytrigger.md)
</dt> </dl>

 

 





