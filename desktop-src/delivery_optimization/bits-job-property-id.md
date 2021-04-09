---
title: Énumération BITS_JOB_PROPERTY_ID (Deliveryoptimization. h)
description: L’énumération BITS_JOB_PROPERTY_ID spécifie l’ID de la propriété pour le travail DO. Cette énumération est utilisée dans l’Union BITS_JOB_PROPERTY_VALUE pour déterminer le type de valeur contenu dans l’Union.
ms.assetid: B0F3C6C2-474F-4FD8-990A-770FAA993550
keywords:
- Énumération BITS_JOB_PROPERTY_ID
topic_type:
- apiref
api_name:
- BITS_JOB_PROPERTY_ID
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cd1d00d4dc12b27c1c80b0e18bb095641a56e322
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740317"
---
# <a name="bits_job_property_id-enumeration"></a><span data-ttu-id="785dc-105">Énumération BITS_JOB_PROPERTY_ID</span><span class="sxs-lookup"><span data-stu-id="785dc-105">BITS_JOB_PROPERTY_ID enumeration</span></span>

<span data-ttu-id="785dc-106">L’énumération **BITS_JOB_PROPERTY_ID** spécifie l’ID de la propriété pour le travail do.</span><span class="sxs-lookup"><span data-stu-id="785dc-106">The **BITS_JOB_PROPERTY_ID** enumeration specifies the ID of the property for the DO job.</span></span> <span data-ttu-id="785dc-107">Cette énumération est utilisée dans l’Union [**BITS_JOB_PROPERTY_VALUE**](bits-job-property-value-.md) pour déterminer le type de valeur contenu dans l’Union.</span><span class="sxs-lookup"><span data-stu-id="785dc-107">This enumeration is used in the [**BITS_JOB_PROPERTY_VALUE**](bits-job-property-value-.md) union to determine the type of value contained in the union.</span></span>

## <a name="syntax"></a><span data-ttu-id="785dc-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="785dc-108">Syntax</span></span>


```C++
typedef enum  { 
  BITS_JOB_PROPERTY_ID_COST_FLAGS                     = 1,
  BITS_JOB_PROPERTY_NOTIFICATION_CLSID                = 2,
  BITS_JOB_PROPERTY_DYNAMIC_CONTENT                   = 3,
  BITS_JOB_PROPERTY_HIGH_PERFORMANCE                  = 4,
  BITS_JOB_PROPERTY_MAX_DOWNLOAD_SIZE                 = 5,
  BITS_JOB_PROPERTY_USE_STORED_CREDENTIALS            = 7,
  BITS_JOB_PROPERTY_MINIMUM_NOTIFICATION_INTERVAL_MS  = 9,
  BITS_JOB_PROPERTY_ON_DEMAND_MODE                    = 10
} BITS_JOB_PROPERTY_ID;
```



## <a name="constants"></a><span data-ttu-id="785dc-109">Constantes</span><span class="sxs-lookup"><span data-stu-id="785dc-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="785dc-110"><span id="BITS_JOB_PROPERTY_ID_COST_FLAGS"></span><span id="bits_job_property_id_cost_flags"></span>**BITS_JOB_PROPERTY_ID_COST_FLAGS**</span><span class="sxs-lookup"><span data-stu-id="785dc-110"><span id="BITS_JOB_PROPERTY_ID_COST_FLAGS"></span><span id="bits_job_property_id_cost_flags"></span>**BITS_JOB_PROPERTY_ID_COST_FLAGS**</span></span>
</dt> <dd>

<span data-ttu-id="785dc-111">ID utilisé pour [contrôler le comportement de transfert](https://www.bing.com/search?q=control+transfer+behavior) sur des réseaux cellulaires et/ou similaires.</span><span class="sxs-lookup"><span data-stu-id="785dc-111">The ID that is used to [control transfer behavior](https://www.bing.com/search?q=control+transfer+behavior) over cellular and/or similar networks.</span></span> <span data-ttu-id="785dc-112">Cette propriété peut être modifiée lorsqu’un transfert est en cours, les nouveaux indicateurs de coût prennent effet immédiatement.</span><span class="sxs-lookup"><span data-stu-id="785dc-112">This property may be changed while a transfer is ongoing   the new cost flags will take effect immediately.</span></span>

<span data-ttu-id="785dc-113">Cette propriété utilise le champ **Dword** **BITS_JOB_PROPERTY_VALUE** s.</span><span class="sxs-lookup"><span data-stu-id="785dc-113">This property uses the **BITS_JOB_PROPERTY_VALUE** s **Dword** field.</span></span>

</dd> <dt>

<span data-ttu-id="785dc-114"><span id="BITS_JOB_PROPERTY_NOTIFICATION_CLSID"></span><span id="bits_job_property_notification_clsid"></span>**BITS_JOB_PROPERTY_NOTIFICATION_CLSID**</span><span class="sxs-lookup"><span data-stu-id="785dc-114"><span id="BITS_JOB_PROPERTY_NOTIFICATION_CLSID"></span><span id="bits_job_property_notification_clsid"></span>**BITS_JOB_PROPERTY_NOTIFICATION_CLSID**</span></span>
</dt> <dd>

<span data-ttu-id="785dc-115">ID utilisé pour [inscrire un rappel com](https://www.bing.com/search?q=register+a+COM+callback) par CLSID pour recevoir des notifications sur la progression et l’achèvement d’un travail do.</span><span class="sxs-lookup"><span data-stu-id="785dc-115">The ID that is used to [register a COM callback](https://www.bing.com/search?q=register+a+COM+callback) by CLSID to receive notifications about the progress and completion of a DO job.</span></span> <span data-ttu-id="785dc-116">Le CLSID doit faire référence à une classe associée à un serveur COM hors processus inscrit.</span><span class="sxs-lookup"><span data-stu-id="785dc-116">The CLSID must refer to a class associated with a registered out-of-process COM server.</span></span> <span data-ttu-id="785dc-117">Elle peut également être définie sur **GUID_NULL** pour effacer un CLSID de notification précédemment défini.</span><span class="sxs-lookup"><span data-stu-id="785dc-117">It may also be set to **GUID_NULL** to clear a previously set notification CLSID.</span></span>

<span data-ttu-id="785dc-118">Cette propriété utilise le champ **CLsID** **BITS_JOB_PROPERTY_VALUE** .</span><span class="sxs-lookup"><span data-stu-id="785dc-118">This property uses the **BITS_JOB_PROPERTY_VALUE** s **CLsID** field.</span></span>

</dd> <dt>

<span data-ttu-id="785dc-119"><span id="BITS_JOB_PROPERTY_DYNAMIC_CONTENT"></span><span id="bits_job_property_dynamic_content"></span>**BITS_JOB_PROPERTY_DYNAMIC_CONTENT**</span><span class="sxs-lookup"><span data-stu-id="785dc-119"><span id="BITS_JOB_PROPERTY_DYNAMIC_CONTENT"></span><span id="bits_job_property_dynamic_content"></span>**BITS_JOB_PROPERTY_DYNAMIC_CONTENT**</span></span>
</dt> <dd>

<span data-ttu-id="785dc-120">Non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="785dc-120">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="785dc-121"><span id="BITS_JOB_PROPERTY_HIGH_PERFORMANCE"></span><span id="bits_job_property_high_performance"></span>**BITS_JOB_PROPERTY_HIGH_PERFORMANCE**</span><span class="sxs-lookup"><span data-stu-id="785dc-121"><span id="BITS_JOB_PROPERTY_HIGH_PERFORMANCE"></span><span id="bits_job_property_high_performance"></span>**BITS_JOB_PROPERTY_HIGH_PERFORMANCE**</span></span>
</dt> <dd>

<span data-ttu-id="785dc-122">Non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="785dc-122">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="785dc-123"><span id="BITS_JOB_PROPERTY_MAX_DOWNLOAD_SIZE"></span><span id="bits_job_property_max_download_size"></span>**BITS_JOB_PROPERTY_MAX_DOWNLOAD_SIZE**</span><span class="sxs-lookup"><span data-stu-id="785dc-123"><span id="BITS_JOB_PROPERTY_MAX_DOWNLOAD_SIZE"></span><span id="bits_job_property_max_download_size"></span>**BITS_JOB_PROPERTY_MAX_DOWNLOAD_SIZE**</span></span>
</dt> <dd>

<span data-ttu-id="785dc-124">Non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="785dc-124">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="785dc-125"><span id="BITS_JOB_PROPERTY_USE_STORED_CREDENTIALS"></span><span id="bits_job_property_use_stored_credentials"></span>**BITS_JOB_PROPERTY_USE_STORED_CREDENTIALS**</span><span class="sxs-lookup"><span data-stu-id="785dc-125"><span id="BITS_JOB_PROPERTY_USE_STORED_CREDENTIALS"></span><span id="bits_job_property_use_stored_credentials"></span>**BITS_JOB_PROPERTY_USE_STORED_CREDENTIALS**</span></span>
</dt> <dd>

<span data-ttu-id="785dc-126">Non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="785dc-126">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="785dc-127"><span id="BITS_JOB_PROPERTY_MINIMUM_NOTIFICATION_INTERVAL_MS"></span><span id="bits_job_property_minimum_notification_interval_ms"></span>**BITS_JOB_PROPERTY_MINIMUM_NOTIFICATION_INTERVAL_MS**</span><span class="sxs-lookup"><span data-stu-id="785dc-127"><span id="BITS_JOB_PROPERTY_MINIMUM_NOTIFICATION_INTERVAL_MS"></span><span id="bits_job_property_minimum_notification_interval_ms"></span>**BITS_JOB_PROPERTY_MINIMUM_NOTIFICATION_INTERVAL_MS**</span></span>
</dt> <dd>

<span data-ttu-id="785dc-128">Non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="785dc-128">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="785dc-129"><span id="BITS_JOB_PROPERTY_ON_DEMAND_MODE"></span><span id="bits_job_property_on_demand_mode"></span>**BITS_JOB_PROPERTY_ON_DEMAND_MODE**</span><span class="sxs-lookup"><span data-stu-id="785dc-129"><span id="BITS_JOB_PROPERTY_ON_DEMAND_MODE"></span><span id="bits_job_property_on_demand_mode"></span>**BITS_JOB_PROPERTY_ON_DEMAND_MODE**</span></span>
</dt> <dd>

<span data-ttu-id="785dc-130">Non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="785dc-130">Not supported.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="785dc-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="785dc-131">Requirements</span></span>



| <span data-ttu-id="785dc-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="785dc-132">Requirement</span></span> | <span data-ttu-id="785dc-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="785dc-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="785dc-134">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="785dc-134">Minimum supported client</span></span><br/> | <span data-ttu-id="785dc-135">Applications de bureau Windows 10, version 1709 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="785dc-135">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="785dc-136">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="785dc-136">Minimum supported server</span></span><br/> | <span data-ttu-id="785dc-137">Windows Server, version 1709, \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="785dc-137">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="785dc-138">En-tête</span><span class="sxs-lookup"><span data-stu-id="785dc-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="785dc-139"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="785dc-139"><dt>Deliveryoptimization.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="785dc-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="785dc-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="785dc-141">**BITS_JOB_PROPERTY_ID**</span><span class="sxs-lookup"><span data-stu-id="785dc-141">**BITS_JOB_PROPERTY_ID**</span></span>](bits-job-property-id.md)
</dt> <dt>

[<span data-ttu-id="785dc-142">**BITS_JOB_PROPERTY_VALUE**</span><span class="sxs-lookup"><span data-stu-id="785dc-142">**BITS_JOB_PROPERTY_VALUE**</span></span>](bits-job-property-value-.md)
</dt> <dt>

[<span data-ttu-id="785dc-143">**BITS_JOB_TRANSFER_POLICY**</span><span class="sxs-lookup"><span data-stu-id="785dc-143">**BITS_JOB_TRANSFER_POLICY**</span></span>](bits-job-transfer-policy-.md)
</dt> <dt>

[<span data-ttu-id="785dc-144">**IBackgroundCopyJob5 :: SetProperty**</span><span class="sxs-lookup"><span data-stu-id="785dc-144">**IBackgroundCopyJob5::SetProperty**</span></span>](ibackgroundcopyjob5-setproperty.md)
</dt> <dt>

[<span data-ttu-id="785dc-145">**IBackgroundCopyJob5 :: GetProperty**</span><span class="sxs-lookup"><span data-stu-id="785dc-145">**IBackgroundCopyJob5::GetProperty**</span></span>](ibackgroundcopyjob5-getproperty.md)
</dt> </dl>

 

 





