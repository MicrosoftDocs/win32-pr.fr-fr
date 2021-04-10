---
title: MonthlyTrigger. DaysOfMonth, propriété
description: Pour les scripts, obtient ou définit les jours du mois pendant lesquels la tâche s’exécute.
ms.assetid: 4da80d0f-ae0c-4e56-b51b-6ee6ab309d7c
keywords:
- Planificateur de tâches de la propriété DaysOfMonth
- Planificateur de tâches de la propriété DaysOfMonth, objet MonthlyTrigger
- Planificateur de tâches objet MonthlyTrigger, propriété DaysOfMonth
topic_type:
- apiref
api_name:
- MonthlyTrigger.DaysOfMonth
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81a3bd671266cfbe459218367fadf20fd52f94a7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104359"
---
# <a name="monthlytriggerdaysofmonth-property"></a><span data-ttu-id="fc8bb-106">MonthlyTrigger. DaysOfMonth, propriété</span><span class="sxs-lookup"><span data-stu-id="fc8bb-106">MonthlyTrigger.DaysOfMonth property</span></span>

<span data-ttu-id="fc8bb-107">Pour les scripts, obtient ou définit les jours du mois pendant lesquels la tâche s’exécute.</span><span class="sxs-lookup"><span data-stu-id="fc8bb-107">For scripting, gets or sets the days of the month during which the task runs.</span></span>

## <a name="syntax"></a><span data-ttu-id="fc8bb-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fc8bb-108">Syntax</span></span>


```VB
MonthlyTrigger.DaysOfMonth As long
```



## <a name="property-value"></a><span data-ttu-id="fc8bb-109">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="fc8bb-109">Property value</span></span>

<span data-ttu-id="fc8bb-110">Un masque de bits qui indique les jours du mois pendant lesquels la tâche s’exécute.</span><span class="sxs-lookup"><span data-stu-id="fc8bb-110">A bitwise mask that indicates the days of the month during which the task runs.</span></span>

## <a name="remarks"></a><span data-ttu-id="fc8bb-111">Notes</span><span class="sxs-lookup"><span data-stu-id="fc8bb-111">Remarks</span></span>



| <span data-ttu-id="fc8bb-112">Jour du mois</span><span class="sxs-lookup"><span data-stu-id="fc8bb-112">Day of month</span></span> | <span data-ttu-id="fc8bb-113">Valeur hexadécimale</span><span class="sxs-lookup"><span data-stu-id="fc8bb-113">Hex value</span></span>  | <span data-ttu-id="fc8bb-114">Valeur décimale</span><span class="sxs-lookup"><span data-stu-id="fc8bb-114">Decimal value</span></span> |
|--------------|------------|---------------|
| <span data-ttu-id="fc8bb-115">1</span><span class="sxs-lookup"><span data-stu-id="fc8bb-115">1</span></span>            | <span data-ttu-id="fc8bb-116">0x01</span><span class="sxs-lookup"><span data-stu-id="fc8bb-116">0x01</span></span>       | <span data-ttu-id="fc8bb-117">1</span><span class="sxs-lookup"><span data-stu-id="fc8bb-117">1</span></span>             |
| <span data-ttu-id="fc8bb-118">2</span><span class="sxs-lookup"><span data-stu-id="fc8bb-118">2</span></span>            | <span data-ttu-id="fc8bb-119">0x02</span><span class="sxs-lookup"><span data-stu-id="fc8bb-119">0x02</span></span>       | <span data-ttu-id="fc8bb-120">2</span><span class="sxs-lookup"><span data-stu-id="fc8bb-120">2</span></span>             |
| <span data-ttu-id="fc8bb-121">3</span><span class="sxs-lookup"><span data-stu-id="fc8bb-121">3</span></span>            | <span data-ttu-id="fc8bb-122">0x04</span><span class="sxs-lookup"><span data-stu-id="fc8bb-122">0x04</span></span>       | <span data-ttu-id="fc8bb-123">4</span><span class="sxs-lookup"><span data-stu-id="fc8bb-123">4</span></span>             |
| <span data-ttu-id="fc8bb-124">4</span><span class="sxs-lookup"><span data-stu-id="fc8bb-124">4</span></span>            | <span data-ttu-id="fc8bb-125">0x08</span><span class="sxs-lookup"><span data-stu-id="fc8bb-125">0x08</span></span>       | <span data-ttu-id="fc8bb-126">8</span><span class="sxs-lookup"><span data-stu-id="fc8bb-126">8</span></span>             |
| <span data-ttu-id="fc8bb-127">5</span><span class="sxs-lookup"><span data-stu-id="fc8bb-127">5</span></span>            | <span data-ttu-id="fc8bb-128">0x10</span><span class="sxs-lookup"><span data-stu-id="fc8bb-128">0x10</span></span>       | <span data-ttu-id="fc8bb-129">16</span><span class="sxs-lookup"><span data-stu-id="fc8bb-129">16</span></span>            |
| <span data-ttu-id="fc8bb-130">6</span><span class="sxs-lookup"><span data-stu-id="fc8bb-130">6</span></span>            | <span data-ttu-id="fc8bb-131">0x20</span><span class="sxs-lookup"><span data-stu-id="fc8bb-131">0x20</span></span>       | <span data-ttu-id="fc8bb-132">32</span><span class="sxs-lookup"><span data-stu-id="fc8bb-132">32</span></span>            |
| <span data-ttu-id="fc8bb-133">7</span><span class="sxs-lookup"><span data-stu-id="fc8bb-133">7</span></span>            | <span data-ttu-id="fc8bb-134">0x40</span><span class="sxs-lookup"><span data-stu-id="fc8bb-134">0x40</span></span>       | <span data-ttu-id="fc8bb-135">64</span><span class="sxs-lookup"><span data-stu-id="fc8bb-135">64</span></span>            |
| <span data-ttu-id="fc8bb-136">8</span><span class="sxs-lookup"><span data-stu-id="fc8bb-136">8</span></span>            | <span data-ttu-id="fc8bb-137">0x80</span><span class="sxs-lookup"><span data-stu-id="fc8bb-137">0x80</span></span>       | <span data-ttu-id="fc8bb-138">128</span><span class="sxs-lookup"><span data-stu-id="fc8bb-138">128</span></span>           |
| <span data-ttu-id="fc8bb-139">9</span><span class="sxs-lookup"><span data-stu-id="fc8bb-139">9</span></span>            | <span data-ttu-id="fc8bb-140">0x100</span><span class="sxs-lookup"><span data-stu-id="fc8bb-140">0x100</span></span>      | <span data-ttu-id="fc8bb-141">256</span><span class="sxs-lookup"><span data-stu-id="fc8bb-141">256</span></span>           |
| <span data-ttu-id="fc8bb-142">10</span><span class="sxs-lookup"><span data-stu-id="fc8bb-142">10</span></span>           | <span data-ttu-id="fc8bb-143">0x200</span><span class="sxs-lookup"><span data-stu-id="fc8bb-143">0x200</span></span>      | <span data-ttu-id="fc8bb-144">512</span><span class="sxs-lookup"><span data-stu-id="fc8bb-144">512</span></span>           |
| <span data-ttu-id="fc8bb-145">11</span><span class="sxs-lookup"><span data-stu-id="fc8bb-145">11</span></span>           | <span data-ttu-id="fc8bb-146">0x400</span><span class="sxs-lookup"><span data-stu-id="fc8bb-146">0x400</span></span>      | <span data-ttu-id="fc8bb-147">1 024</span><span class="sxs-lookup"><span data-stu-id="fc8bb-147">1024</span></span>          |
| <span data-ttu-id="fc8bb-148">12</span><span class="sxs-lookup"><span data-stu-id="fc8bb-148">12</span></span>           | <span data-ttu-id="fc8bb-149">0x800</span><span class="sxs-lookup"><span data-stu-id="fc8bb-149">0x800</span></span>      | <span data-ttu-id="fc8bb-150">2 048</span><span class="sxs-lookup"><span data-stu-id="fc8bb-150">2048</span></span>          |
| <span data-ttu-id="fc8bb-151">13</span><span class="sxs-lookup"><span data-stu-id="fc8bb-151">13</span></span>           | <span data-ttu-id="fc8bb-152">0x1000</span><span class="sxs-lookup"><span data-stu-id="fc8bb-152">0x1000</span></span>     | <span data-ttu-id="fc8bb-153">4096</span><span class="sxs-lookup"><span data-stu-id="fc8bb-153">4096</span></span>          |
| <span data-ttu-id="fc8bb-154">14</span><span class="sxs-lookup"><span data-stu-id="fc8bb-154">14</span></span>           | <span data-ttu-id="fc8bb-155">0x2000</span><span class="sxs-lookup"><span data-stu-id="fc8bb-155">0x2000</span></span>     | <span data-ttu-id="fc8bb-156">8 192</span><span class="sxs-lookup"><span data-stu-id="fc8bb-156">8192</span></span>          |
| <span data-ttu-id="fc8bb-157">15</span><span class="sxs-lookup"><span data-stu-id="fc8bb-157">15</span></span>           | <span data-ttu-id="fc8bb-158">0x4000</span><span class="sxs-lookup"><span data-stu-id="fc8bb-158">0x4000</span></span>     | <span data-ttu-id="fc8bb-159">16384</span><span class="sxs-lookup"><span data-stu-id="fc8bb-159">16384</span></span>         |
| <span data-ttu-id="fc8bb-160">16</span><span class="sxs-lookup"><span data-stu-id="fc8bb-160">16</span></span>           | <span data-ttu-id="fc8bb-161">0x8000</span><span class="sxs-lookup"><span data-stu-id="fc8bb-161">0x8000</span></span>     | <span data-ttu-id="fc8bb-162">32 768</span><span class="sxs-lookup"><span data-stu-id="fc8bb-162">32768</span></span>         |
| <span data-ttu-id="fc8bb-163">17</span><span class="sxs-lookup"><span data-stu-id="fc8bb-163">17</span></span>           | <span data-ttu-id="fc8bb-164">0x10000</span><span class="sxs-lookup"><span data-stu-id="fc8bb-164">0x10000</span></span>    | <span data-ttu-id="fc8bb-165">65536</span><span class="sxs-lookup"><span data-stu-id="fc8bb-165">65536</span></span>         |
| <span data-ttu-id="fc8bb-166">18</span><span class="sxs-lookup"><span data-stu-id="fc8bb-166">18</span></span>           | <span data-ttu-id="fc8bb-167">0x20000</span><span class="sxs-lookup"><span data-stu-id="fc8bb-167">0x20000</span></span>    | <span data-ttu-id="fc8bb-168">131 072</span><span class="sxs-lookup"><span data-stu-id="fc8bb-168">131072</span></span>        |
| <span data-ttu-id="fc8bb-169">19</span><span class="sxs-lookup"><span data-stu-id="fc8bb-169">19</span></span>           | <span data-ttu-id="fc8bb-170">0x40000</span><span class="sxs-lookup"><span data-stu-id="fc8bb-170">0x40000</span></span>    | <span data-ttu-id="fc8bb-171">262 144</span><span class="sxs-lookup"><span data-stu-id="fc8bb-171">262144</span></span>        |
| <span data-ttu-id="fc8bb-172">20</span><span class="sxs-lookup"><span data-stu-id="fc8bb-172">20</span></span>           | <span data-ttu-id="fc8bb-173">0x80000</span><span class="sxs-lookup"><span data-stu-id="fc8bb-173">0x80000</span></span>    | <span data-ttu-id="fc8bb-174">524 288</span><span class="sxs-lookup"><span data-stu-id="fc8bb-174">524288</span></span>        |
| <span data-ttu-id="fc8bb-175">21</span><span class="sxs-lookup"><span data-stu-id="fc8bb-175">21</span></span>           | <span data-ttu-id="fc8bb-176">0x100000</span><span class="sxs-lookup"><span data-stu-id="fc8bb-176">0x100000</span></span>   | <span data-ttu-id="fc8bb-177">1 048 576</span><span class="sxs-lookup"><span data-stu-id="fc8bb-177">1048576</span></span>       |
| <span data-ttu-id="fc8bb-178">22</span><span class="sxs-lookup"><span data-stu-id="fc8bb-178">22</span></span>           | <span data-ttu-id="fc8bb-179">0x200000</span><span class="sxs-lookup"><span data-stu-id="fc8bb-179">0x200000</span></span>   | <span data-ttu-id="fc8bb-180">2 097 152</span><span class="sxs-lookup"><span data-stu-id="fc8bb-180">2097152</span></span>       |
| <span data-ttu-id="fc8bb-181">23</span><span class="sxs-lookup"><span data-stu-id="fc8bb-181">23</span></span>           | <span data-ttu-id="fc8bb-182">0x400000</span><span class="sxs-lookup"><span data-stu-id="fc8bb-182">0x400000</span></span>   | <span data-ttu-id="fc8bb-183">4 194 304</span><span class="sxs-lookup"><span data-stu-id="fc8bb-183">4194304</span></span>       |
| <span data-ttu-id="fc8bb-184">24</span><span class="sxs-lookup"><span data-stu-id="fc8bb-184">24</span></span>           | <span data-ttu-id="fc8bb-185">0x800000</span><span class="sxs-lookup"><span data-stu-id="fc8bb-185">0x800000</span></span>   | <span data-ttu-id="fc8bb-186">8388608</span><span class="sxs-lookup"><span data-stu-id="fc8bb-186">8388608</span></span>       |
| <span data-ttu-id="fc8bb-187">25</span><span class="sxs-lookup"><span data-stu-id="fc8bb-187">25</span></span>           | <span data-ttu-id="fc8bb-188">0x1000000</span><span class="sxs-lookup"><span data-stu-id="fc8bb-188">0x1000000</span></span>  | <span data-ttu-id="fc8bb-189">16 777 216</span><span class="sxs-lookup"><span data-stu-id="fc8bb-189">16777216</span></span>      |
| <span data-ttu-id="fc8bb-190">26</span><span class="sxs-lookup"><span data-stu-id="fc8bb-190">26</span></span>           | <span data-ttu-id="fc8bb-191">0x2000000</span><span class="sxs-lookup"><span data-stu-id="fc8bb-191">0x2000000</span></span>  | <span data-ttu-id="fc8bb-192">33554432</span><span class="sxs-lookup"><span data-stu-id="fc8bb-192">33554432</span></span>      |
| <span data-ttu-id="fc8bb-193">27</span><span class="sxs-lookup"><span data-stu-id="fc8bb-193">27</span></span>           | <span data-ttu-id="fc8bb-194">0x4000000</span><span class="sxs-lookup"><span data-stu-id="fc8bb-194">0x4000000</span></span>  | <span data-ttu-id="fc8bb-195">67108864</span><span class="sxs-lookup"><span data-stu-id="fc8bb-195">67108864</span></span>      |
| <span data-ttu-id="fc8bb-196">28</span><span class="sxs-lookup"><span data-stu-id="fc8bb-196">28</span></span>           | <span data-ttu-id="fc8bb-197">0x8000000</span><span class="sxs-lookup"><span data-stu-id="fc8bb-197">0x8000000</span></span>  | <span data-ttu-id="fc8bb-198">134217728</span><span class="sxs-lookup"><span data-stu-id="fc8bb-198">134217728</span></span>     |
| <span data-ttu-id="fc8bb-199">29</span><span class="sxs-lookup"><span data-stu-id="fc8bb-199">29</span></span>           | <span data-ttu-id="fc8bb-200">0x10000000</span><span class="sxs-lookup"><span data-stu-id="fc8bb-200">0x10000000</span></span> | <span data-ttu-id="fc8bb-201">268435456</span><span class="sxs-lookup"><span data-stu-id="fc8bb-201">268435456</span></span>     |
| <span data-ttu-id="fc8bb-202">30</span><span class="sxs-lookup"><span data-stu-id="fc8bb-202">30</span></span>           | <span data-ttu-id="fc8bb-203">0x20000000</span><span class="sxs-lookup"><span data-stu-id="fc8bb-203">0x20000000</span></span> | <span data-ttu-id="fc8bb-204">536870912</span><span class="sxs-lookup"><span data-stu-id="fc8bb-204">536870912</span></span>     |
| <span data-ttu-id="fc8bb-205">31</span><span class="sxs-lookup"><span data-stu-id="fc8bb-205">31</span></span>           | <span data-ttu-id="fc8bb-206">0x40000000</span><span class="sxs-lookup"><span data-stu-id="fc8bb-206">0x40000000</span></span> | <span data-ttu-id="fc8bb-207">1073741824</span><span class="sxs-lookup"><span data-stu-id="fc8bb-207">1073741824</span></span>    |
| <span data-ttu-id="fc8bb-208">Dernier</span><span class="sxs-lookup"><span data-stu-id="fc8bb-208">Last</span></span>         | <span data-ttu-id="fc8bb-209">0x80000000</span><span class="sxs-lookup"><span data-stu-id="fc8bb-209">0x80000000</span></span> | <span data-ttu-id="fc8bb-210">2147483648</span><span class="sxs-lookup"><span data-stu-id="fc8bb-210">2147483648</span></span>    |



 

<span data-ttu-id="fc8bb-211">Lors de la lecture ou de l’écriture de vos propres données XML pour une tâche, les jours du mois sont spécifiés à l’aide de l’élément [**DaysOfMonth**](taskschedulerschema-daysofmonth-monthlyscheduletype-element.md) du schéma planificateur de tâches.</span><span class="sxs-lookup"><span data-stu-id="fc8bb-211">When reading or writing your own XML for a task, the days of the month are specified using the [**DaysOfMonth**](taskschedulerschema-daysofmonth-monthlyscheduletype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="fc8bb-212">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fc8bb-212">Requirements</span></span>



| <span data-ttu-id="fc8bb-213">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fc8bb-213">Requirement</span></span> | <span data-ttu-id="fc8bb-214">Valeur</span><span class="sxs-lookup"><span data-stu-id="fc8bb-214">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fc8bb-215">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fc8bb-215">Minimum supported client</span></span><br/> | <span data-ttu-id="fc8bb-216">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fc8bb-216">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="fc8bb-217">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fc8bb-217">Minimum supported server</span></span><br/> | <span data-ttu-id="fc8bb-218">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fc8bb-218">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="fc8bb-219">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="fc8bb-219">Type library</span></span><br/>             | <dl> <span data-ttu-id="fc8bb-220"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="fc8bb-220"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="fc8bb-221">DLL</span><span class="sxs-lookup"><span data-stu-id="fc8bb-221">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fc8bb-222"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fc8bb-222"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fc8bb-223">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fc8bb-223">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc8bb-224">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="fc8bb-224">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="fc8bb-225">**MonthlyTrigger**</span><span class="sxs-lookup"><span data-stu-id="fc8bb-225">**MonthlyTrigger**</span></span>](monthlytrigger.md)
</dt> </dl>

 

 





