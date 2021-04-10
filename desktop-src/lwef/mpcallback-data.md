---
title: Structure MPCALLBACK_DATA (MpClient. h)
description: Données passées à la fonction de rappel.
ms.assetid: EA8E6C1E-F80B-4247-B073-C78D49A354CF
keywords:
- Fonctionnalités d’environnement Windows héritées de la structure MPCALLBACK_DATA
- PMPCALLBACK_DATA des fonctionnalités d’environnement Windows héritées du pointeur de structure
topic_type:
- apiref
api_name:
- MPCALLBACK_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9741ca479eeb9770a3ae8c2aedbc51a8a2643033
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103568"
---
# <a name="mpcallback_data-structure"></a><span data-ttu-id="a10bb-105">\_Structure de données MPCALLBACK</span><span class="sxs-lookup"><span data-stu-id="a10bb-105">MPCALLBACK\_DATA structure</span></span>

<span data-ttu-id="a10bb-106">Données passées à la fonction de rappel.</span><span class="sxs-lookup"><span data-stu-id="a10bb-106">Data passed to the callback function.</span></span>

## <a name="syntax"></a><span data-ttu-id="a10bb-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a10bb-107">Syntax</span></span>


```C++
typedef struct tagMPCALLBACK_DATA {
  MPNOTIFY        Notify;
  HRESULT         hResult;
  ULARGE_INTEGER  TimeStamp;
  MPCALLBACK_TYPE Type;
  union {
    PMPSTATUS_DATA         pStatusData;
    PMPSCAN_DATA           pScanData;
    PMPCLEAN_DATA          pCleanData;
    PMPCLEAN_PRECHECK_DATA pPrecheckData;
    PMPTHREAT_DATA         pThreatData;
    PMPSIGUPDATE_DATA      pSigUpdateData;
    PMPSAMPLE_DATA         pSampleData;
    PMPRESERVED_DATA       pReservedData;
    PMPCONFIGURATION_DATA  pConfigurationData;
    PMPFASTPATH_DATA       pFastPathData;
    PMPEXPIRATION_DATA     pExpirationData;
    PMPNIS_PRIVATE_DATA    pNISPrivateData;
    PMPHEALTH_DATA         pHealthData;
    PMPENDOFLIFE_DATA      pEndOfLifeData;
    PMPMALWARETOAST_DATA   pMalwareToastData;
  } Data;
} MPCALLBACK_DATA, *PMPCALLBACK_DATA;
```



## <a name="members"></a><span data-ttu-id="a10bb-108">Membres</span><span class="sxs-lookup"><span data-stu-id="a10bb-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="a10bb-109">**Notifier**</span><span class="sxs-lookup"><span data-stu-id="a10bb-109">**Notify**</span></span>
</dt> <dd>

<span data-ttu-id="a10bb-110">Type : **[ **MPNOTIFY**](mpnotify.md)**</span><span class="sxs-lookup"><span data-stu-id="a10bb-110">Type: **[**MPNOTIFY**](mpnotify.md)**</span></span>

</dd> <dd>

<span data-ttu-id="a10bb-111">Notification de modification au rapport.</span><span class="sxs-lookup"><span data-stu-id="a10bb-111">Change notification to report.</span></span>

</dd> <dt>

<span data-ttu-id="a10bb-112">**Signé**</span><span class="sxs-lookup"><span data-stu-id="a10bb-112">**hResult**</span></span>
</dt> <dd>

<span data-ttu-id="a10bb-113">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="a10bb-113">Type: **HRESULT**</span></span>

</dd> <dd>

<span data-ttu-id="a10bb-114">Code d’erreur, en cas de défaillance interne.</span><span class="sxs-lookup"><span data-stu-id="a10bb-114">Error code, in case of an internal failure.</span></span>

</dd> <dt>

<span data-ttu-id="a10bb-115">**Confirmé**</span><span class="sxs-lookup"><span data-stu-id="a10bb-115">**TimeStamp**</span></span>
</dt> <dd>

<span data-ttu-id="a10bb-116">Type : **\_ entier ULARGE**</span><span class="sxs-lookup"><span data-stu-id="a10bb-116">Type: **ULARGE\_INTEGER**</span></span>

</dd> <dd>

<span data-ttu-id="a10bb-117">Horodatage actuel.</span><span class="sxs-lookup"><span data-stu-id="a10bb-117">Current timestamp.</span></span>

</dd> <dt>

<span data-ttu-id="a10bb-118">**Type**</span><span class="sxs-lookup"><span data-stu-id="a10bb-118">**Type**</span></span>
</dt> <dd>

<span data-ttu-id="a10bb-119">Type : **[ **MPCALLBACK \_**](mpcallback-type.md)**</span><span class="sxs-lookup"><span data-stu-id="a10bb-119">Type: **[**MPCALLBACK\_TYPE**](mpcallback-type.md)**</span></span>

</dd> <dd>

<span data-ttu-id="a10bb-120">Type de données spécial de rappel.</span><span class="sxs-lookup"><span data-stu-id="a10bb-120">Callback special data type.</span></span>

</dd> <dt>

<span data-ttu-id="a10bb-121">**Données**</span><span class="sxs-lookup"><span data-stu-id="a10bb-121">**Data**</span></span>
</dt> <dd>

<span data-ttu-id="a10bb-122">Données spéciales de rappel.</span><span class="sxs-lookup"><span data-stu-id="a10bb-122">Callback special data.</span></span> <span data-ttu-id="a10bb-123">Le pointeur vers la structure appropriée dépend de la valeur de **type**.</span><span class="sxs-lookup"><span data-stu-id="a10bb-123">The pointer to the appropriate structure depends on the value of **Type**.</span></span>

<dl> <dt>

<span data-ttu-id="a10bb-124">**pStatusData**</span><span class="sxs-lookup"><span data-stu-id="a10bb-124">**pStatusData**</span></span>
</dt> <dd>

<span data-ttu-id="a10bb-125">Type : **\_ données PMPSTATUS**</span><span class="sxs-lookup"><span data-stu-id="a10bb-125">Type: **PMPSTATUS\_DATA**</span></span>

</dd> <dd>

<span data-ttu-id="a10bb-126">Lorsque le **type**  ==  **MPCALLBACK est \_ Status**.</span><span class="sxs-lookup"><span data-stu-id="a10bb-126">When **Type** == **MPCALLBACK\_STATUS**.</span></span> <span data-ttu-id="a10bb-127">Consultez [**\_ données MPSTATUS**](mpstatus-data.md).</span><span class="sxs-lookup"><span data-stu-id="a10bb-127">See [**MPSTATUS\_DATA**](mpstatus-data.md).</span></span>

</dd> <dt>

<span data-ttu-id="a10bb-128">**pScanData**</span><span class="sxs-lookup"><span data-stu-id="a10bb-128">**pScanData**</span></span>
</dt> <dd>

<span data-ttu-id="a10bb-129">Type : **\_ données PMPSCAN**</span><span class="sxs-lookup"><span data-stu-id="a10bb-129">Type: **PMPSCAN\_DATA**</span></span>

</dd> <dd>

<span data-ttu-id="a10bb-130">Lorsque le **type**  ==  **MPCALLBACK \_ Scan**.</span><span class="sxs-lookup"><span data-stu-id="a10bb-130">When **Type** == **MPCALLBACK\_SCAN**.</span></span> <span data-ttu-id="a10bb-131">Consultez [**\_ données MPSCAN**](mpscan-data.md).</span><span class="sxs-lookup"><span data-stu-id="a10bb-131">See [**MPSCAN\_DATA**](mpscan-data.md).</span></span>

</dd> <dt>

<span data-ttu-id="a10bb-132">**pCleanData**</span><span class="sxs-lookup"><span data-stu-id="a10bb-132">**pCleanData**</span></span>
</dt> <dd>

<span data-ttu-id="a10bb-133">Type : **\_ données PMPCLEAN**</span><span class="sxs-lookup"><span data-stu-id="a10bb-133">Type: **PMPCLEAN\_DATA**</span></span>

</dd> <dd>

<span data-ttu-id="a10bb-134">Lorsque le **type**  ==  **MPCALLBACK \_ Clean**.</span><span class="sxs-lookup"><span data-stu-id="a10bb-134">When **Type** == **MPCALLBACK\_CLEAN**.</span></span> <span data-ttu-id="a10bb-135">Consultez [**\_ données MPCLEAN**](mpclean-data.md).</span><span class="sxs-lookup"><span data-stu-id="a10bb-135">See [**MPCLEAN\_DATA**](mpclean-data.md).</span></span>

</dd> <dt>

<span data-ttu-id="a10bb-136">**pPrecheckData**</span><span class="sxs-lookup"><span data-stu-id="a10bb-136">**pPrecheckData**</span></span>
</dt> <dd>

<span data-ttu-id="a10bb-137">Type : **PMPCLEAN \_ prévérifier les \_ données**</span><span class="sxs-lookup"><span data-stu-id="a10bb-137">Type: **PMPCLEAN\_PRECHECK\_DATA**</span></span>

</dd> <dd>

<span data-ttu-id="a10bb-138">Quand le **type** est  ==  **MPCALLBACK \_ précheck**.</span><span class="sxs-lookup"><span data-stu-id="a10bb-138">When **Type** == **MPCALLBACK\_PRECHECK**.</span></span> <span data-ttu-id="a10bb-139">Consultez [**MPCLEAN \_ prévérifier les \_ données**](mpclean-precheck-data.md).</span><span class="sxs-lookup"><span data-stu-id="a10bb-139">See [**MPCLEAN\_PRECHECK\_DATA**](mpclean-precheck-data.md).</span></span>

</dd> <dt>

<span data-ttu-id="a10bb-140">**pThreatData**</span><span class="sxs-lookup"><span data-stu-id="a10bb-140">**pThreatData**</span></span>
</dt> <dd>

<span data-ttu-id="a10bb-141">Type : **\_ données PMPTHREAT**</span><span class="sxs-lookup"><span data-stu-id="a10bb-141">Type: **PMPTHREAT\_DATA**</span></span>

</dd> <dd>

<span data-ttu-id="a10bb-142">Lorsque le **type**  ==  **MPCALLBACK \_ menace**.</span><span class="sxs-lookup"><span data-stu-id="a10bb-142">When **Type** == **MPCALLBACK\_THREAT**.</span></span> <span data-ttu-id="a10bb-143">Consultez [**\_ données MPTHREAT**](mpthreat-data.md).</span><span class="sxs-lookup"><span data-stu-id="a10bb-143">See [**MPTHREAT\_DATA**](mpthreat-data.md).</span></span>

</dd> <dt>

<span data-ttu-id="a10bb-144">**pSigUpdateData**</span><span class="sxs-lookup"><span data-stu-id="a10bb-144">**pSigUpdateData**</span></span>
</dt> <dd>

<span data-ttu-id="a10bb-145">Type : **\_ données PMPSIGUPDATE**</span><span class="sxs-lookup"><span data-stu-id="a10bb-145">Type: **PMPSIGUPDATE\_DATA**</span></span>

</dd> <dd>

<span data-ttu-id="a10bb-146">Lorsque le **type** est  ==  **MPCALLBACK \_ SIGUPDATE**.</span><span class="sxs-lookup"><span data-stu-id="a10bb-146">When **Type** == **MPCALLBACK\_SIGUPDATE**.</span></span> <span data-ttu-id="a10bb-147">Consultez [**\_ données MPSIGUPDATE**](mpsigupdate-data.md).</span><span class="sxs-lookup"><span data-stu-id="a10bb-147">See [**MPSIGUPDATE\_DATA**](mpsigupdate-data.md).</span></span>

</dd> <dt>

<span data-ttu-id="a10bb-148">**pSampleData**</span><span class="sxs-lookup"><span data-stu-id="a10bb-148">**pSampleData**</span></span>
</dt> <dd>

<span data-ttu-id="a10bb-149">Type : **\_ données PMPSAMPLE**</span><span class="sxs-lookup"><span data-stu-id="a10bb-149">Type: **PMPSAMPLE\_DATA**</span></span>

</dd> <dd>

<span data-ttu-id="a10bb-150">Lorsque **type**  ==  **MPCALLBACK \_ Sample**.</span><span class="sxs-lookup"><span data-stu-id="a10bb-150">When **Type** == **MPCALLBACK\_SAMPLE**.</span></span> <span data-ttu-id="a10bb-151">Consultez [**\_ données MPSAMPLE**](mpsample-data.md).</span><span class="sxs-lookup"><span data-stu-id="a10bb-151">See [**MPSAMPLE\_DATA**](mpsample-data.md).</span></span>

</dd> <dt>

<span data-ttu-id="a10bb-152">**pReservedData**</span><span class="sxs-lookup"><span data-stu-id="a10bb-152">**pReservedData**</span></span>
</dt> <dd>

<span data-ttu-id="a10bb-153">Type : **\_ données PMPRESERVED**</span><span class="sxs-lookup"><span data-stu-id="a10bb-153">Type: **PMPRESERVED\_DATA**</span></span>

</dd> <dd>

<span data-ttu-id="a10bb-154">Lorsque le **type**  ==  **MPCALLBACK est \_ réservé**.</span><span class="sxs-lookup"><span data-stu-id="a10bb-154">When **Type** == **MPCALLBACK\_RESERVED**.</span></span> <span data-ttu-id="a10bb-155">Consultez [**\_ données MPRESERVED**](mpreserved-data.md).</span><span class="sxs-lookup"><span data-stu-id="a10bb-155">See [**MPRESERVED\_DATA**](mpreserved-data.md).</span></span>

</dd> <dt>

<span data-ttu-id="a10bb-156">**pConfigurationData**</span><span class="sxs-lookup"><span data-stu-id="a10bb-156">**pConfigurationData**</span></span>
</dt> <dd>

<span data-ttu-id="a10bb-157">Type : **\_ données PMPCONFIGURATION**</span><span class="sxs-lookup"><span data-stu-id="a10bb-157">Type: **PMPCONFIGURATION\_DATA**</span></span>

</dd> <dd>

<span data-ttu-id="a10bb-158">Lorsque le **type** est  ==  **\_ \_ notification de configuration MPCALLBACK**.</span><span class="sxs-lookup"><span data-stu-id="a10bb-158">When **Type** == **MPCALLBACK\_CONFIGURATION\_NOTIFICATION**.</span></span> <span data-ttu-id="a10bb-159">Consultez [**\_ données MPCONFIGURATION**](mpconfiguration-data.md).</span><span class="sxs-lookup"><span data-stu-id="a10bb-159">See [**MPCONFIGURATION\_DATA**](mpconfiguration-data.md).</span></span>

</dd> <dt>

<span data-ttu-id="a10bb-160">**pFastPathData**</span><span class="sxs-lookup"><span data-stu-id="a10bb-160">**pFastPathData**</span></span>
</dt> <dd>

<span data-ttu-id="a10bb-161">Type : **\_ données PMPFASTPATH**</span><span class="sxs-lookup"><span data-stu-id="a10bb-161">Type: **PMPFASTPATH\_DATA**</span></span>

</dd> <dd>

<span data-ttu-id="a10bb-162">Lorsque le **type** est  ==  **MPCALLBACK \_ FASTPATH**.</span><span class="sxs-lookup"><span data-stu-id="a10bb-162">When **Type** == **MPCALLBACK\_FASTPATH**.</span></span> <span data-ttu-id="a10bb-163">Consultez [**\_ données MPFASTPATH**](mpfastpath-data.md).</span><span class="sxs-lookup"><span data-stu-id="a10bb-163">See [**MPFASTPATH\_DATA**](mpfastpath-data.md).</span></span>

</dd> <dt>

<span data-ttu-id="a10bb-164">**pExpirationData**</span><span class="sxs-lookup"><span data-stu-id="a10bb-164">**pExpirationData**</span></span>
</dt> <dd>

<span data-ttu-id="a10bb-165">Type : **\_ données PMPEXPIRATION**</span><span class="sxs-lookup"><span data-stu-id="a10bb-165">Type: **PMPEXPIRATION\_DATA**</span></span>

</dd> <dd>

<span data-ttu-id="a10bb-166">Lorsque **tapez**  ==  **MPCALLBACK \_ \_ expiration du produit**.</span><span class="sxs-lookup"><span data-stu-id="a10bb-166">When **Type** == **MPCALLBACK\_PRODUCT\_EXPIRATION**.</span></span> <span data-ttu-id="a10bb-167">Consultez [**\_ données MPEXPIRATION**](mpexpiration-data.md).</span><span class="sxs-lookup"><span data-stu-id="a10bb-167">See [**MPEXPIRATION\_DATA**](mpexpiration-data.md).</span></span>

</dd> <dt>

<span data-ttu-id="a10bb-168">**pNISPrivateData**</span><span class="sxs-lookup"><span data-stu-id="a10bb-168">**pNISPrivateData**</span></span>
</dt> <dd>

<span data-ttu-id="a10bb-169">Type : **PMPNIS \_ Private \_ Data**</span><span class="sxs-lookup"><span data-stu-id="a10bb-169">Type: **PMPNIS\_PRIVATE\_DATA**</span></span>

</dd> <dd>

<span data-ttu-id="a10bb-170">Lorsque **tapez**  ==  **MPCALLBACK \_ NIS \_ Private**.</span><span class="sxs-lookup"><span data-stu-id="a10bb-170">When **Type** == **MPCALLBACK\_NIS\_PRIVATE**.</span></span> <span data-ttu-id="a10bb-171">Consultez [**MPNIS \_ Private \_ Data**](mpnis-private-data.md).</span><span class="sxs-lookup"><span data-stu-id="a10bb-171">See [**MPNIS\_PRIVATE\_DATA**](mpnis-private-data.md).</span></span>

</dd> <dt>

<span data-ttu-id="a10bb-172">**pHealthData**</span><span class="sxs-lookup"><span data-stu-id="a10bb-172">**pHealthData**</span></span>
</dt> <dd>

<span data-ttu-id="a10bb-173">Type : **\_ données PMPHEALTH**</span><span class="sxs-lookup"><span data-stu-id="a10bb-173">Type: **PMPHEALTH\_DATA**</span></span>

</dd> <dd>

<span data-ttu-id="a10bb-174">Lorsque le **type**  ==  **MPCALLBACK \_ Health**.</span><span class="sxs-lookup"><span data-stu-id="a10bb-174">When **Type** == **MPCALLBACK\_HEALTH**.</span></span> <span data-ttu-id="a10bb-175">Consultez [**\_ données MPHEALTH**](mphealth-data.md).</span><span class="sxs-lookup"><span data-stu-id="a10bb-175">See [**MPHEALTH\_DATA**](mphealth-data.md).</span></span>

</dd> <dt>

<span data-ttu-id="a10bb-176">**pEndOfLifeData**</span><span class="sxs-lookup"><span data-stu-id="a10bb-176">**pEndOfLifeData**</span></span>
</dt> <dd>

<span data-ttu-id="a10bb-177">Type : **\_ données PMPENDOFLIFE**</span><span class="sxs-lookup"><span data-stu-id="a10bb-177">Type: **PMPENDOFLIFE\_DATA**</span></span>

</dd> <dd>

<span data-ttu-id="a10bb-178">Lorsque le **type** est  ==  **MPCALLBACK \_ ENDOFLIFE**.</span><span class="sxs-lookup"><span data-stu-id="a10bb-178">When **Type** == **MPCALLBACK\_ENDOFLIFE**.</span></span> <span data-ttu-id="a10bb-179">Consultez [**\_ données MPENDOFLIFE**](mpendoflife-data.md).</span><span class="sxs-lookup"><span data-stu-id="a10bb-179">See [**MPENDOFLIFE\_DATA**](mpendoflife-data.md).</span></span>

</dd> <dt>

<span data-ttu-id="a10bb-180">**pMalwareToastData**</span><span class="sxs-lookup"><span data-stu-id="a10bb-180">**pMalwareToastData**</span></span>
</dt> <dd>

<span data-ttu-id="a10bb-181">Type : **\_ données PMPMALWARETOAST**</span><span class="sxs-lookup"><span data-stu-id="a10bb-181">Type: **PMPMALWARETOAST\_DATA**</span></span>

</dd> <dd>

<span data-ttu-id="a10bb-182">Lorsque le **type** est  ==  **MPCALLBACK \_ MALWARETOAST**.</span><span class="sxs-lookup"><span data-stu-id="a10bb-182">When **Type** == **MPCALLBACK\_MALWARETOAST**.</span></span> <span data-ttu-id="a10bb-183">Consultez [**\_ données MPMALWARETOAST**](mpmalwaretoast-data.md).</span><span class="sxs-lookup"><span data-stu-id="a10bb-183">See [**MPMALWARETOAST\_DATA**](mpmalwaretoast-data.md).</span></span>

</dd> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a10bb-184">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a10bb-184">Requirements</span></span>



| <span data-ttu-id="a10bb-185">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a10bb-185">Requirement</span></span> | <span data-ttu-id="a10bb-186">Valeur</span><span class="sxs-lookup"><span data-stu-id="a10bb-186">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a10bb-187">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a10bb-187">Minimum supported client</span></span><br/> | <span data-ttu-id="a10bb-188">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a10bb-188">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="a10bb-189">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a10bb-189">Minimum supported server</span></span><br/> | <span data-ttu-id="a10bb-190">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a10bb-190">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a10bb-191">En-tête</span><span class="sxs-lookup"><span data-stu-id="a10bb-191">Header</span></span><br/>                   | <dl> <span data-ttu-id="a10bb-192"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="a10bb-192"><dt>MpClient.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a10bb-193">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a10bb-193">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a10bb-194">**\_type MPCALLBACK**</span><span class="sxs-lookup"><span data-stu-id="a10bb-194">**MPCALLBACK\_TYPE**</span></span>](mpcallback-type.md)
</dt> <dt>

[<span data-ttu-id="a10bb-195">**\_données MPCLEAN**</span><span class="sxs-lookup"><span data-stu-id="a10bb-195">**MPCLEAN\_DATA**</span></span>](mpclean-data.md)
</dt> <dt>

[<span data-ttu-id="a10bb-196">**MPCLEAN les données de la \_ PRÉvérification \_**</span><span class="sxs-lookup"><span data-stu-id="a10bb-196">**MPCLEAN\_PRECHECK\_DATA**</span></span>](mpclean-precheck-data.md)
</dt> <dt>

[<span data-ttu-id="a10bb-197">**\_données MPCONFIGURATION**</span><span class="sxs-lookup"><span data-stu-id="a10bb-197">**MPCONFIGURATION\_DATA**</span></span>](mpconfiguration-data.md)
</dt> <dt>

[<span data-ttu-id="a10bb-198">**\_données MPENDOFLIFE**</span><span class="sxs-lookup"><span data-stu-id="a10bb-198">**MPENDOFLIFE\_DATA**</span></span>](mpendoflife-data.md)
</dt> <dt>

[<span data-ttu-id="a10bb-199">**\_données MPEXPIRATION**</span><span class="sxs-lookup"><span data-stu-id="a10bb-199">**MPEXPIRATION\_DATA**</span></span>](mpexpiration-data.md)
</dt> <dt>

[<span data-ttu-id="a10bb-200">**\_données MPFASTPATH**</span><span class="sxs-lookup"><span data-stu-id="a10bb-200">**MPFASTPATH\_DATA**</span></span>](mpfastpath-data.md)
</dt> <dt>

[<span data-ttu-id="a10bb-201">**\_données MPHEALTH**</span><span class="sxs-lookup"><span data-stu-id="a10bb-201">**MPHEALTH\_DATA**</span></span>](mphealth-data.md)
</dt> <dt>

[<span data-ttu-id="a10bb-202">**\_données MPMALWARETOAST**</span><span class="sxs-lookup"><span data-stu-id="a10bb-202">**MPMALWARETOAST\_DATA**</span></span>](mpmalwaretoast-data.md)
</dt> <dt>

[<span data-ttu-id="a10bb-203">**\_données privées \_ MPNIS**</span><span class="sxs-lookup"><span data-stu-id="a10bb-203">**MPNIS\_PRIVATE\_DATA**</span></span>](mpnis-private-data.md)
</dt> <dt>

[<span data-ttu-id="a10bb-204">**MPNOTIFY**</span><span class="sxs-lookup"><span data-stu-id="a10bb-204">**MPNOTIFY**</span></span>](mpnotify.md)
</dt> <dt>

[<span data-ttu-id="a10bb-205">**\_données MPRESERVED**</span><span class="sxs-lookup"><span data-stu-id="a10bb-205">**MPRESERVED\_DATA**</span></span>](mpreserved-data.md)
</dt> <dt>

[<span data-ttu-id="a10bb-206">**\_données MPSAMPLE**</span><span class="sxs-lookup"><span data-stu-id="a10bb-206">**MPSAMPLE\_DATA**</span></span>](mpsample-data.md)
</dt> <dt>

[<span data-ttu-id="a10bb-207">**\_données MPSCAN**</span><span class="sxs-lookup"><span data-stu-id="a10bb-207">**MPSCAN\_DATA**</span></span>](mpscan-data.md)
</dt> <dt>

[<span data-ttu-id="a10bb-208">**\_données MPSIGUPDATE**</span><span class="sxs-lookup"><span data-stu-id="a10bb-208">**MPSIGUPDATE\_DATA**</span></span>](mpsigupdate-data.md)
</dt> <dt>

[<span data-ttu-id="a10bb-209">**\_données MPSTATUS**</span><span class="sxs-lookup"><span data-stu-id="a10bb-209">**MPSTATUS\_DATA**</span></span>](mpstatus-data.md)
</dt> <dt>

[<span data-ttu-id="a10bb-210">**\_données MPTHREAT**</span><span class="sxs-lookup"><span data-stu-id="a10bb-210">**MPTHREAT\_DATA**</span></span>](mpthreat-data.md)
</dt> </dl>

 

 





