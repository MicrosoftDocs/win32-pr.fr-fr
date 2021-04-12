---
title: Méthode méthode ibackgroundcopyjob GetNotifyFlags (Deliveryoptimization. h)
description: Récupère les indicateurs de notification d’événement pour le travail.
ms.assetid: 95ADC97F-63DC-4EB6-B85C-7BCC79238C12
keywords:
- Méthode GetNotifyFlags
- Méthode GetNotifyFlags, interface méthode ibackgroundcopyjob
- Interface méthode ibackgroundcopyjob, méthode GetNotifyFlags
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.GetNotifyFlags
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e104857725849dfeb899b449ea055bc3cdb046bd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317246"
---
# <a name="ibackgroundcopyjobgetnotifyflags-method"></a><span data-ttu-id="18f2f-106">Méthode ibackgroundcopyjob :: GetNotifyFlags, méthode</span><span class="sxs-lookup"><span data-stu-id="18f2f-106">IBackgroundCopyJob::GetNotifyFlags method</span></span>

<span data-ttu-id="18f2f-107">Récupère les indicateurs de notification d’événement pour le travail.</span><span class="sxs-lookup"><span data-stu-id="18f2f-107">Retrieves the event notification flags for the job.</span></span>

## <a name="syntax"></a><span data-ttu-id="18f2f-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="18f2f-108">Syntax</span></span>


```C++
HRESULT GetNotifyFlags(
  [out] ULONG *pNotifyFlags
);
```



## <a name="parameters"></a><span data-ttu-id="18f2f-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="18f2f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="18f2f-110">*pNotifyFlags* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="18f2f-110">*pNotifyFlags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="18f2f-111">Identifie les événements que votre application reçoit.</span><span class="sxs-lookup"><span data-stu-id="18f2f-111">Identifies the events that your application receives.</span></span> <span data-ttu-id="18f2f-112">Le tableau suivant répertorie les valeurs de l’indicateur de notification d’événement.</span><span class="sxs-lookup"><span data-stu-id="18f2f-112">The following table lists the event notification flag values.</span></span>



| <span data-ttu-id="18f2f-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="18f2f-113">Value</span></span>                                                                                                                                                                                                  | <span data-ttu-id="18f2f-114">Signification</span><span class="sxs-lookup"><span data-stu-id="18f2f-114">Meaning</span></span>                                                                        |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| <span id="BG_NOTIFY_JOB_TRANSFERRED"></span><span id="bg_notify_job_transferred"></span><dl> <span data-ttu-id="18f2f-115"><dt>**BG_NOTIFY_JOB_TRANSFERRED**</dt></span><span class="sxs-lookup"><span data-stu-id="18f2f-115"><dt>**BG_NOTIFY_JOB_TRANSFERRED**</dt></span></span> </dl>    | <span data-ttu-id="18f2f-116">Tous les fichiers du travail ont été transférés.</span><span class="sxs-lookup"><span data-stu-id="18f2f-116">All of the files in the job have been transferred.</span></span><br/>                  |
| <span id="BG_NOTIFY_JOB_ERROR"></span><span id="bg_notify_job_error"></span><dl> <span data-ttu-id="18f2f-117"><dt>**BG_NOTIFY_JOB_ERROR**</dt></span><span class="sxs-lookup"><span data-stu-id="18f2f-117"><dt>**BG_NOTIFY_JOB_ERROR**</dt></span></span> </dl>                      | <span data-ttu-id="18f2f-118">Une erreur s’est produite.</span><span class="sxs-lookup"><span data-stu-id="18f2f-118">An error has occurred.</span></span><br/>                                              |
| <span id="BG_NOTIFY_DISABLE"></span><span id="bg_notify_disable"></span><dl> <span data-ttu-id="18f2f-119"><dt>**BG_NOTIFY_DISABLE**</dt></span><span class="sxs-lookup"><span data-stu-id="18f2f-119"><dt>**BG_NOTIFY_DISABLE**</dt></span></span> </dl>                             | <span data-ttu-id="18f2f-120">La notification d’événements est désactivée.</span><span class="sxs-lookup"><span data-stu-id="18f2f-120">Event notification is disabled.</span></span> <span data-ttu-id="18f2f-121">Si cette option est définie, ignore les autres indicateurs.</span><span class="sxs-lookup"><span data-stu-id="18f2f-121">If set, DO ignores the other flags.</span></span><br/> |
| <span id="BG_NOTIFY_JOB_MODIFICATION"></span><span id="bg_notify_job_modification"></span><dl> <span data-ttu-id="18f2f-122"><dt>**BG_NOTIFY_JOB_MODIFICATION**</dt></span><span class="sxs-lookup"><span data-stu-id="18f2f-122"><dt>**BG_NOTIFY_JOB_MODIFICATION**</dt></span></span> </dl> | <span data-ttu-id="18f2f-123">La tâche a été modifiée.</span><span class="sxs-lookup"><span data-stu-id="18f2f-123">The job has been modified.</span></span><br/>                                          |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="18f2f-124">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="18f2f-124">Return value</span></span>

<span data-ttu-id="18f2f-125">Cette méthode retourne les valeurs **HRESULT** suivantes, ainsi que d’autres.</span><span class="sxs-lookup"><span data-stu-id="18f2f-125">This method returns the following **HRESULT** values, as well as others.</span></span>



| <span data-ttu-id="18f2f-126">Code de retour</span><span class="sxs-lookup"><span data-stu-id="18f2f-126">Return code</span></span>                                                                              | <span data-ttu-id="18f2f-127">Description</span><span class="sxs-lookup"><span data-stu-id="18f2f-127">Description</span></span>                                                |
|------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <dl> <span data-ttu-id="18f2f-128"><dt>S_OK \* \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="18f2f-128"><dt>\*\*\*\*S_OK\*\*\*\*</dt></span></span> </dl> | <span data-ttu-id="18f2f-129">Les indicateurs de notification d’événement ont été correctement récupérés.</span><span class="sxs-lookup"><span data-stu-id="18f2f-129">Event notify flags were successfully retrieved.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="18f2f-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="18f2f-130">Requirements</span></span>



| <span data-ttu-id="18f2f-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="18f2f-131">Requirement</span></span> | <span data-ttu-id="18f2f-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="18f2f-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="18f2f-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="18f2f-133">Minimum supported client</span></span><br/> | <span data-ttu-id="18f2f-134">Applications de bureau Windows 10, version 1709 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="18f2f-134">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="18f2f-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="18f2f-135">Minimum supported server</span></span><br/> | <span data-ttu-id="18f2f-136">Windows Server, version 1709, \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="18f2f-136">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="18f2f-137">En-tête</span><span class="sxs-lookup"><span data-stu-id="18f2f-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="18f2f-138"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="18f2f-138"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="18f2f-139">MIDL</span><span class="sxs-lookup"><span data-stu-id="18f2f-139">IDL</span></span><br/>                      | <dl> <span data-ttu-id="18f2f-140"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="18f2f-140"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="18f2f-141">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="18f2f-141">Library</span></span><br/>                  | <dl> <span data-ttu-id="18f2f-142"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="18f2f-142"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="18f2f-143">DLL</span><span class="sxs-lookup"><span data-stu-id="18f2f-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="18f2f-144"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="18f2f-144"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="18f2f-145">IID</span><span class="sxs-lookup"><span data-stu-id="18f2f-145">IID</span></span><br/>                      | <span data-ttu-id="18f2f-146">IID_IBackgroundCopyJob est défini en tant que 37668D37-507E-4160-9316-26306D150B12</span><span class="sxs-lookup"><span data-stu-id="18f2f-146">IID_IBackgroundCopyJob is defined as 37668D37-507E-4160-9316-26306D150B12</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="18f2f-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="18f2f-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18f2f-148">**Méthode ibackgroundcopyjob**</span><span class="sxs-lookup"><span data-stu-id="18f2f-148">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> <dt>

[<span data-ttu-id="18f2f-149">**IBackgroundCopyCallback**</span><span class="sxs-lookup"><span data-stu-id="18f2f-149">**IBackgroundCopyCallback**</span></span>](ibackgroundcopycallback.md)
</dt> <dt>

[<span data-ttu-id="18f2f-150">**Méthode ibackgroundcopyjob :: GetNotifyInterface**</span><span class="sxs-lookup"><span data-stu-id="18f2f-150">**IBackgroundCopyJob::GetNotifyInterface**</span></span>](ibackgroundcopyjob-getnotifyinterface.md)
</dt> <dt>

[<span data-ttu-id="18f2f-151">**Méthode ibackgroundcopyjob :: SetNotifyFlags**</span><span class="sxs-lookup"><span data-stu-id="18f2f-151">**IBackgroundCopyJob::SetNotifyFlags**</span></span>](ibackgroundcopyjob-setnotifyflags.md)
</dt> </dl>

 

 





