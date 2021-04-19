---
description: Le qualificateur abPerfRawData contient la valeur entière pour le type de compteur de la propriété pour les propriétés des \_ classes Win32. CookingType contient les constantes pour les types de formule de propriété dans les \_ classes PerfFormattedData Win32.
ms.assetid: aa79fcdb-503f-4928-b2b7-f07baeaf9fb5
ms.tgt_platform: multiple
title: Qualificateur de l’identificateur de la
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CounterType
api_type:
- NA
api_location: ''
ms.openlocfilehash: 883ee7aa2f230756d62294d46e6402fe7f962d4e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517010"
---
# <a name="countertype-qualifier"></a><span data-ttu-id="9ec71-104">Qualificateur de l’identificateur de la</span><span class="sxs-lookup"><span data-stu-id="9ec71-104">CounterType Qualifier</span></span>

<span data-ttu-id="9ec71-105">Le **qualificateur abPerfRawData contient la valeur** entière pour le type de compteur de la propriété pour les propriétés des classes [**Win32 \_**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) .</span><span class="sxs-lookup"><span data-stu-id="9ec71-105">The **CounterType** qualifier contains the integer value for the property counter type for properties in [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) classes.</span></span> <span data-ttu-id="9ec71-106">**CookingType** contient les constantes pour les types de formule de propriété dans les classes [**\_ PerfFormattedData Win32**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) .</span><span class="sxs-lookup"><span data-stu-id="9ec71-106">The **CookingType** contains the constants for property formula types in [**Win32\_PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) classes.</span></span>

<span data-ttu-id="9ec71-107">Pour plus d’informations et une répartition des types de compteurs par fonction, consultez [types de compteurs](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10)).</span><span class="sxs-lookup"><span data-stu-id="9ec71-107">For more information and a breakdown of counter types by function, see [Counter Types](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10)).</span></span>



| <span data-ttu-id="9ec71-108">CounterType</span><span class="sxs-lookup"><span data-stu-id="9ec71-108">CounterType</span></span> | <span data-ttu-id="9ec71-109">CookingType</span><span class="sxs-lookup"><span data-stu-id="9ec71-109">CookingType</span></span>                              |
|-------------|------------------------------------------|
| <span data-ttu-id="9ec71-110">0</span><span class="sxs-lookup"><span data-stu-id="9ec71-110">0</span></span>           | <span data-ttu-id="9ec71-111">compteur de performances \_ \_ RAWCOUNT \_ Hex</span><span class="sxs-lookup"><span data-stu-id="9ec71-111">PERF\_COUNTER\_RAWCOUNT\_HEX</span></span>             |
| <span data-ttu-id="9ec71-112">256</span><span class="sxs-lookup"><span data-stu-id="9ec71-112">256</span></span>         | <span data-ttu-id="9ec71-113">compteur de performances \_ \_ grand \_ RAWCOUNT \_ Hex hex</span><span class="sxs-lookup"><span data-stu-id="9ec71-113">PERF\_COUNTER\_LARGE\_RAWCOUNT\_HEX</span></span>      |
| <span data-ttu-id="9ec71-114">2816</span><span class="sxs-lookup"><span data-stu-id="9ec71-114">2816</span></span>        | <span data-ttu-id="9ec71-115">\_texte du compteur de performances \_</span><span class="sxs-lookup"><span data-stu-id="9ec71-115">PERF\_COUNTER\_TEXT</span></span>                      |
| <span data-ttu-id="9ec71-116">65536</span><span class="sxs-lookup"><span data-stu-id="9ec71-116">65536</span></span>       | <span data-ttu-id="9ec71-117">compteur de performances \_ \_ RAWCOUNT</span><span class="sxs-lookup"><span data-stu-id="9ec71-117">PERF\_COUNTER\_RAWCOUNT</span></span>                  |
| <span data-ttu-id="9ec71-118">65792</span><span class="sxs-lookup"><span data-stu-id="9ec71-118">65792</span></span>       | <span data-ttu-id="9ec71-119">compteur de performances- \_ \_ grand \_ RAWCOUNT</span><span class="sxs-lookup"><span data-stu-id="9ec71-119">PERF\_COUNTER\_LARGE\_RAWCOUNT</span></span>           |
| <span data-ttu-id="9ec71-120">73728</span><span class="sxs-lookup"><span data-stu-id="9ec71-120">73728</span></span>       | <span data-ttu-id="9ec71-121">PERF \_ double \_ brut</span><span class="sxs-lookup"><span data-stu-id="9ec71-121">PERF\_DOUBLE\_RAW</span></span>                        |
| <span data-ttu-id="9ec71-122">4195328</span><span class="sxs-lookup"><span data-stu-id="9ec71-122">4195328</span></span>     | <span data-ttu-id="9ec71-123">\_delta du compteur de performances \_</span><span class="sxs-lookup"><span data-stu-id="9ec71-123">PERF\_COUNTER\_DELTA</span></span>                     |
| <span data-ttu-id="9ec71-124">4195584</span><span class="sxs-lookup"><span data-stu-id="9ec71-124">4195584</span></span>     | <span data-ttu-id="9ec71-125">compteur de performances- \_ \_ \_ Delta important</span><span class="sxs-lookup"><span data-stu-id="9ec71-125">PERF\_COUNTER\_LARGE\_DELTA</span></span>              |
| <span data-ttu-id="9ec71-126">4260864</span><span class="sxs-lookup"><span data-stu-id="9ec71-126">4260864</span></span>     | <span data-ttu-id="9ec71-127">\_compteur d’exemples perf \_</span><span class="sxs-lookup"><span data-stu-id="9ec71-127">PERF\_SAMPLE\_COUNTER</span></span>                    |
| <span data-ttu-id="9ec71-128">4523008</span><span class="sxs-lookup"><span data-stu-id="9ec71-128">4523008</span></span>     | <span data-ttu-id="9ec71-129">\_type de \_ QUEUELEN du compteur de performances \_</span><span class="sxs-lookup"><span data-stu-id="9ec71-129">PERF\_COUNTER\_QUEUELEN\_TYPE</span></span>            |
| <span data-ttu-id="9ec71-130">4523264</span><span class="sxs-lookup"><span data-stu-id="9ec71-130">4523264</span></span>     | <span data-ttu-id="9ec71-131">TYPE de QUEUELEN de compteur de performances \_ \_ élevé \_ \_</span><span class="sxs-lookup"><span data-stu-id="9ec71-131">PERF\_COUNTER\_LARGE\_QUEUELEN\_TYPE</span></span>     |
| <span data-ttu-id="9ec71-132">5571840</span><span class="sxs-lookup"><span data-stu-id="9ec71-132">5571840</span></span>     | <span data-ttu-id="9ec71-133">TYPE de QUEUELEN de compteur de performances \_ \_ 100 NS \_ \_</span><span class="sxs-lookup"><span data-stu-id="9ec71-133">PERF\_COUNTER\_100NS\_QUEUELEN\_TYPE</span></span>     |
| <span data-ttu-id="9ec71-134">6620416</span><span class="sxs-lookup"><span data-stu-id="9ec71-134">6620416</span></span>     | <span data-ttu-id="9ec71-135">TYPE de QUEUELEN du compteur de performance \_ \_ obj \_ Time \_ \_</span><span class="sxs-lookup"><span data-stu-id="9ec71-135">PERF\_COUNTER\_OBJ\_TIME\_QUEUELEN\_TYPE</span></span> |
| <span data-ttu-id="9ec71-136">272696320</span><span class="sxs-lookup"><span data-stu-id="9ec71-136">272696320</span></span>   | <span data-ttu-id="9ec71-137">\_compteur de compteur de performances \_</span><span class="sxs-lookup"><span data-stu-id="9ec71-137">PERF\_COUNTER\_COUNTER</span></span>                   |
| <span data-ttu-id="9ec71-138">272696576</span><span class="sxs-lookup"><span data-stu-id="9ec71-138">272696576</span></span>   | <span data-ttu-id="9ec71-139">nombre de compteurs de performances \_ \_ en bloc \_</span><span class="sxs-lookup"><span data-stu-id="9ec71-139">PERF\_COUNTER\_BULK\_COUNT</span></span>               |
| <span data-ttu-id="9ec71-140">537003008</span><span class="sxs-lookup"><span data-stu-id="9ec71-140">537003008</span></span>   | <span data-ttu-id="9ec71-141">FRACTION de performances \_ brutes \_</span><span class="sxs-lookup"><span data-stu-id="9ec71-141">PERF\_RAW\_FRACTION</span></span>                      |
| <span data-ttu-id="9ec71-142">541132032</span><span class="sxs-lookup"><span data-stu-id="9ec71-142">541132032</span></span>   | <span data-ttu-id="9ec71-143">\_minuteur de compteur de performances \_</span><span class="sxs-lookup"><span data-stu-id="9ec71-143">PERF\_COUNTER\_TIMER</span></span>                     |
| <span data-ttu-id="9ec71-144">541525248</span><span class="sxs-lookup"><span data-stu-id="9ec71-144">541525248</span></span>   | <span data-ttu-id="9ec71-145">\_ \_ minuteur système de précision de performance \_</span><span class="sxs-lookup"><span data-stu-id="9ec71-145">PERF\_PRECISION\_SYSTEM\_TIMER</span></span>           |
| <span data-ttu-id="9ec71-146">542180608</span><span class="sxs-lookup"><span data-stu-id="9ec71-146">542180608</span></span>   | <span data-ttu-id="9ec71-147">\_ \_ Minuteur 100NSEC perf</span><span class="sxs-lookup"><span data-stu-id="9ec71-147">PERF\_100NSEC\_TIMER</span></span>                     |
| <span data-ttu-id="9ec71-148">542573824</span><span class="sxs-lookup"><span data-stu-id="9ec71-148">542573824</span></span>   | <span data-ttu-id="9ec71-149">\_ \_ Minuteur de 100 précision de performance \_</span><span class="sxs-lookup"><span data-stu-id="9ec71-149">PERF\_PRECISION\_100NS\_TIMER</span></span>            |
| <span data-ttu-id="9ec71-150">543229184</span><span class="sxs-lookup"><span data-stu-id="9ec71-150">543229184</span></span>   | <span data-ttu-id="9ec71-151">\_ \_ minuteur de temps obj de perf \_</span><span class="sxs-lookup"><span data-stu-id="9ec71-151">PERF\_OBJ\_TIME\_TIMER</span></span>                   |
| <span data-ttu-id="9ec71-152">543622400</span><span class="sxs-lookup"><span data-stu-id="9ec71-152">543622400</span></span>   | <span data-ttu-id="9ec71-153">\_ \_ minuteur d’objet de précision de performance \_</span><span class="sxs-lookup"><span data-stu-id="9ec71-153">PERF\_PRECISION\_OBJECT\_TIMER</span></span>           |
| <span data-ttu-id="9ec71-154">549585920</span><span class="sxs-lookup"><span data-stu-id="9ec71-154">549585920</span></span>   | <span data-ttu-id="9ec71-155">FRACTION de l' \_ exemple perf \_</span><span class="sxs-lookup"><span data-stu-id="9ec71-155">PERF\_SAMPLE\_FRACTION</span></span>                   |
| <span data-ttu-id="9ec71-156">557909248</span><span class="sxs-lookup"><span data-stu-id="9ec71-156">557909248</span></span>   | <span data-ttu-id="9ec71-157">\_ \_ inventaire du compteur de performances \_</span><span class="sxs-lookup"><span data-stu-id="9ec71-157">PERF\_COUNTER\_TIMER\_INV</span></span>                |
| <span data-ttu-id="9ec71-158">558957824</span><span class="sxs-lookup"><span data-stu-id="9ec71-158">558957824</span></span>   | <span data-ttu-id="9ec71-159">PERF \_ 100NSEC \_ minuteur \_ inv</span><span class="sxs-lookup"><span data-stu-id="9ec71-159">PERF\_100NSEC\_TIMER\_INV</span></span>                |
| <span data-ttu-id="9ec71-160">574686464</span><span class="sxs-lookup"><span data-stu-id="9ec71-160">574686464</span></span>   | <span data-ttu-id="9ec71-161">compteur de performances \_ \_ multiple \_ Timer</span><span class="sxs-lookup"><span data-stu-id="9ec71-161">PERF\_COUNTER\_MULTI\_TIMER</span></span>              |
| <span data-ttu-id="9ec71-162">575735040</span><span class="sxs-lookup"><span data-stu-id="9ec71-162">575735040</span></span>   | <span data-ttu-id="9ec71-163">\_ \_ \_ MINUTEur 100NSEC perf</span><span class="sxs-lookup"><span data-stu-id="9ec71-163">PERF\_100NSEC\_MULTI\_TIMER</span></span>              |
| <span data-ttu-id="9ec71-164">591463680</span><span class="sxs-lookup"><span data-stu-id="9ec71-164">591463680</span></span>   | <span data-ttu-id="9ec71-165">compteur de performances ( \_ \_ plusieurs \_ minuteurs) \_ inv</span><span class="sxs-lookup"><span data-stu-id="9ec71-165">PERF\_COUNTER\_MULTI\_TIMER\_INV</span></span>         |
| <span data-ttu-id="9ec71-166">592512256</span><span class="sxs-lookup"><span data-stu-id="9ec71-166">592512256</span></span>   | <span data-ttu-id="9ec71-167">PERF \_ 100NSEC \_ multi- \_ Timer \_</span><span class="sxs-lookup"><span data-stu-id="9ec71-167">PERF\_100NSEC\_MULTI\_TIMER\_INV</span></span>         |
| <span data-ttu-id="9ec71-168">805438464</span><span class="sxs-lookup"><span data-stu-id="9ec71-168">805438464</span></span>   | <span data-ttu-id="9ec71-169">\_minuteur de performance moyen \_</span><span class="sxs-lookup"><span data-stu-id="9ec71-169">PERF\_AVERAGE\_TIMER</span></span>                     |
| <span data-ttu-id="9ec71-170">807666944</span><span class="sxs-lookup"><span data-stu-id="9ec71-170">807666944</span></span>   | <span data-ttu-id="9ec71-171">\_temps écoulé de \_ performance</span><span class="sxs-lookup"><span data-stu-id="9ec71-171">PERF\_ELAPSED\_TIME</span></span>                      |
| <span data-ttu-id="9ec71-172">1073742336</span><span class="sxs-lookup"><span data-stu-id="9ec71-172">1073742336</span></span>  | <span data-ttu-id="9ec71-173">compteur de performances \_ \_ NoData</span><span class="sxs-lookup"><span data-stu-id="9ec71-173">PERF\_COUNTER\_NODATA</span></span>                    |
| <span data-ttu-id="9ec71-174">1073874176</span><span class="sxs-lookup"><span data-stu-id="9ec71-174">1073874176</span></span>  | <span data-ttu-id="9ec71-175">moyenne de performances \_ \_ en bloc</span><span class="sxs-lookup"><span data-stu-id="9ec71-175">PERF\_AVERAGE\_BULK</span></span>                      |
| <span data-ttu-id="9ec71-176">1073939457</span><span class="sxs-lookup"><span data-stu-id="9ec71-176">1073939457</span></span>  | <span data-ttu-id="9ec71-177">\_exemple de \_ base de performances</span><span class="sxs-lookup"><span data-stu-id="9ec71-177">PERF\_SAMPLE\_BASE</span></span>                       |
| <span data-ttu-id="9ec71-178">1073939458</span><span class="sxs-lookup"><span data-stu-id="9ec71-178">1073939458</span></span>  | <span data-ttu-id="9ec71-179">\_base moyenne de performances \_</span><span class="sxs-lookup"><span data-stu-id="9ec71-179">PERF\_AVERAGE\_BASE</span></span>                      |
| <span data-ttu-id="9ec71-180">1073939459</span><span class="sxs-lookup"><span data-stu-id="9ec71-180">1073939459</span></span>  | <span data-ttu-id="9ec71-181">\_base brute de perf. \_</span><span class="sxs-lookup"><span data-stu-id="9ec71-181">PERF\_RAW\_BASE</span></span>                          |
| <span data-ttu-id="9ec71-182">1073939712</span><span class="sxs-lookup"><span data-stu-id="9ec71-182">1073939712</span></span>  | <span data-ttu-id="9ec71-183">\_horodatage de précision de performance \_</span><span class="sxs-lookup"><span data-stu-id="9ec71-183">PERF\_PRECISION\_TIMESTAMP</span></span>               |
| <span data-ttu-id="9ec71-184">1073939715</span><span class="sxs-lookup"><span data-stu-id="9ec71-184">1073939715</span></span>  | <span data-ttu-id="9ec71-185">BASE de performances \_ volumineuse \_ brute \_</span><span class="sxs-lookup"><span data-stu-id="9ec71-185">PERF\_LARGE\_RAW\_BASE</span></span>                   |
| <span data-ttu-id="9ec71-186">1107494144</span><span class="sxs-lookup"><span data-stu-id="9ec71-186">1107494144</span></span>  | <span data-ttu-id="9ec71-187">compteur de performances \_ \_ multi- \_ base</span><span class="sxs-lookup"><span data-stu-id="9ec71-187">PERF\_COUNTER\_MULTI\_BASE</span></span>               |
| <span data-ttu-id="9ec71-188">2147483648</span><span class="sxs-lookup"><span data-stu-id="9ec71-188">2147483648</span></span>  | <span data-ttu-id="9ec71-189">\_type d' \_ histogramme du compteur de performances \_</span><span class="sxs-lookup"><span data-stu-id="9ec71-189">PERF\_COUNTER\_HISTOGRAM\_TYPE</span></span>           |



 

## <a name="requirements"></a><span data-ttu-id="9ec71-190">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9ec71-190">Requirements</span></span>



| <span data-ttu-id="9ec71-191">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9ec71-191">Requirement</span></span> | <span data-ttu-id="9ec71-192">Valeur</span><span class="sxs-lookup"><span data-stu-id="9ec71-192">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="9ec71-193">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9ec71-193">Minimum supported client</span></span><br/> | <span data-ttu-id="9ec71-194">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9ec71-194">Windows Vista</span></span><br/>       |
| <span data-ttu-id="9ec71-195">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9ec71-195">Minimum supported server</span></span><br/> | <span data-ttu-id="9ec71-196">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9ec71-196">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9ec71-197">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9ec71-197">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ec71-198">Qualificateurs spécifiques aux classes de performance WMI</span><span class="sxs-lookup"><span data-stu-id="9ec71-198">Qualifiers Specific to WMI Performance Classes</span></span>](qualifiers-specific-to-wmi-performance-classes.md)
</dt> </dl>

 

