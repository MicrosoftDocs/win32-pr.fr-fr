---
title: Méthode méthode ibackgroundcopyjob SetNotifyFlags (Deliveryoptimization. h)
description: Spécifie le type de notification d’événement que vous souhaitez recevoir, par exemple les événements de transfert de travaux.
ms.assetid: 19E626A5-6B6E-44E0-BD6F-43F132F32890
keywords:
- Méthode SetNotifyFlags
- Méthode SetNotifyFlags, interface méthode ibackgroundcopyjob
- Interface méthode ibackgroundcopyjob, méthode SetNotifyFlags
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.SetNotifyFlags
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ea754eeafca8f0efdcad5545cfc3a462c8b508cc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508622"
---
# <a name="ibackgroundcopyjobsetnotifyflags-method"></a><span data-ttu-id="5d356-106">Méthode ibackgroundcopyjob :: SetNotifyFlags, méthode</span><span class="sxs-lookup"><span data-stu-id="5d356-106">IBackgroundCopyJob::SetNotifyFlags method</span></span>

<span data-ttu-id="5d356-107">Spécifie le type de notification d’événement que vous souhaitez recevoir, par exemple les événements de transfert de travaux.</span><span class="sxs-lookup"><span data-stu-id="5d356-107">Specifies the type of event notification you want to receive, such as job transferred events.</span></span>

## <a name="syntax"></a><span data-ttu-id="5d356-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5d356-108">Syntax</span></span>


```C++
HRESULT SetNotifyFlags(
  [in] ULONG NotifyFlags
);
```



## <a name="parameters"></a><span data-ttu-id="5d356-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5d356-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5d356-110">*NotifyFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5d356-110">*NotifyFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5d356-111">Définissez un ou plusieurs des indicateurs suivants pour identifier les événements que vous souhaitez recevoir.</span><span class="sxs-lookup"><span data-stu-id="5d356-111">Set one or more of the following flags to identify the events that you want to receive.</span></span>



| <span data-ttu-id="5d356-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="5d356-112">Value</span></span>                                                                                                                                                                                                                                                                                    | <span data-ttu-id="5d356-113">Signification</span><span class="sxs-lookup"><span data-stu-id="5d356-113">Meaning</span></span>                                                                                                                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="BG_NOTIFY_JOB_TRANSFERRED"></span><span id="bg_notify_job_transferred"></span><dl> <span data-ttu-id="5d356-114"><dt>**BG_NOTIFY_JOB_TRANSFERRED**</dt> <dt>0x0001</dt></span><span class="sxs-lookup"><span data-stu-id="5d356-114"><dt>**BG_NOTIFY_JOB_TRANSFERRED**</dt> <dt>0x0001</dt></span></span> </dl>                          | <span data-ttu-id="5d356-115">Tous les fichiers du travail ont été transférés.</span><span class="sxs-lookup"><span data-stu-id="5d356-115">All of the files in the job have been transferred.</span></span><br/>                                                                                                                                                          |
| <span id="BG_NOTIFY_JOB_ERROR"></span><span id="bg_notify_job_error"></span><dl> <span data-ttu-id="5d356-116"><dt>**BG_NOTIFY_JOB_ERROR**</dt> <dt>0x0002</dt></span><span class="sxs-lookup"><span data-stu-id="5d356-116"><dt>**BG_NOTIFY_JOB_ERROR**</dt> <dt>0x0002</dt></span></span> </dl>                                            | <span data-ttu-id="5d356-117">Une erreur s’est produite.</span><span class="sxs-lookup"><span data-stu-id="5d356-117">An error has occurred.</span></span><br/>                                                                                                                                                                                      |
| <span id="BG_NOTIFY_DISABLE"></span><span id="bg_notify_disable"></span><dl> <span data-ttu-id="5d356-118"><dt>**BG_NOTIFY_DISABLE**</dt> <dt>0x0004</dt></span><span class="sxs-lookup"><span data-stu-id="5d356-118"><dt>**BG_NOTIFY_DISABLE**</dt> <dt>0x0004</dt></span></span> </dl>                                                   | <span data-ttu-id="5d356-119">Non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="5d356-119">Not supported.</span></span><br/>                                                                                                                                                                                              |
| <span id="BG_NOTIFY_JOB_MODIFICATION"></span><span id="bg_notify_job_modification"></span><dl> <span data-ttu-id="5d356-120"><dt>**BG_NOTIFY_JOB_MODIFICATION**</dt> <dt>0x0008</dt></span><span class="sxs-lookup"><span data-stu-id="5d356-120"><dt>**BG_NOTIFY_JOB_MODIFICATION**</dt> <dt>0x0008</dt></span></span> </dl>                       | <span data-ttu-id="5d356-121">La tâche a été modifiée.</span><span class="sxs-lookup"><span data-stu-id="5d356-121">The job has been modified.</span></span> <span data-ttu-id="5d356-122">Par exemple, une valeur de propriété a été modifiée, l’état de la tâche a changé ou la progression est effectuée en transférant les fichiers.</span><span class="sxs-lookup"><span data-stu-id="5d356-122">For example, a property value changed, the state of the job changed, or progress is made transferring the files.</span></span> <span data-ttu-id="5d356-123">Cet indicateur est ignoré si la notification de ligne de commande est spécifiée.</span><span class="sxs-lookup"><span data-stu-id="5d356-123">This flag is ignored if command line notification is specified.</span></span><br/> |
| <span id="BG_NOTIFY_FILE_TRANSFERRED"></span><span id="bg_notify_file_transferred"></span><dl> <span data-ttu-id="5d356-124"><dt>**BG_NOTIFY_FILE_TRANSFERRED**</dt> <dt>0x0010</dt></span><span class="sxs-lookup"><span data-stu-id="5d356-124"><dt>**BG_NOTIFY_FILE_TRANSFERRED**</dt> <dt>0x0010</dt></span></span> </dl>                       | <span data-ttu-id="5d356-125">Un fichier du travail a été transféré.</span><span class="sxs-lookup"><span data-stu-id="5d356-125">A file in the job has been transferred.</span></span> <span data-ttu-id="5d356-126">Cet indicateur est ignoré si la notification de ligne de commande est spécifiée.</span><span class="sxs-lookup"><span data-stu-id="5d356-126">This flag is ignored if command line notification is specified.</span></span><br/>                                                                                                     |
| <span id="BG_NOTIFY_FILE_RANGES_TRANSFERRED"></span><span id="bg_notify_file_ranges_transferred"></span><dl> <span data-ttu-id="5d356-127"><dt>**BG_NOTIFY_FILE_RANGES_TRANSFERRED**</dt> <dt>0x0020</dt></span><span class="sxs-lookup"><span data-stu-id="5d356-127"><dt>**BG_NOTIFY_FILE_RANGES_TRANSFERRED**</dt> <dt>0x0020</dt></span></span> </dl> | <span data-ttu-id="5d356-128">Non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="5d356-128">Not supported.</span></span><br/>                                                                                                                                                                                              |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5d356-129">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5d356-129">Return value</span></span>

<span data-ttu-id="5d356-130">Cette méthode retourne les valeurs **HRESULT** suivantes, ainsi que d’autres.</span><span class="sxs-lookup"><span data-stu-id="5d356-130">This method returns the following **HRESULT** values, as well as others.</span></span>



| <span data-ttu-id="5d356-131">Code de retour</span><span class="sxs-lookup"><span data-stu-id="5d356-131">Return code</span></span>                                                                                          | <span data-ttu-id="5d356-132">Description</span><span class="sxs-lookup"><span data-stu-id="5d356-132">Description</span></span>                                                                                          |
|------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="5d356-133"><dt>S_OK \* \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="5d356-133"><dt>\*\*\*\*S_OK\*\*\*\*</dt></span></span> </dl>             | <span data-ttu-id="5d356-134">Le type de notification d’événement a été correctement défini.</span><span class="sxs-lookup"><span data-stu-id="5d356-134">Type of event notification was successfully set.</span></span><br/>                                          |
| <dl> <span data-ttu-id="5d356-135"><dt>**DO_E_INVALID_STATE**</dt></span><span class="sxs-lookup"><span data-stu-id="5d356-135"><dt>**DO_E_INVALID_STATE**</dt></span></span> </dl> | <span data-ttu-id="5d356-136">L’état du travail ne peut pas être BG_JOB_STATE_CANCELLED ou BG_JOB_STATE_ACKNOWLEDGED.</span><span class="sxs-lookup"><span data-stu-id="5d356-136">The state of the job cannot be BG_JOB_STATE_CANCELLED or BG_JOB_STATE_ACKNOWLEDGED.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="5d356-137">Notes</span><span class="sxs-lookup"><span data-stu-id="5d356-137">Remarks</span></span>

<span data-ttu-id="5d356-138">Utilisez la méthode **SetNotifyFlags** conjointement avec [**méthode ibackgroundcopyjob :: SetNotifyInterface**](ibackgroundcopyjob-setnotifyinterface.md).</span><span class="sxs-lookup"><span data-stu-id="5d356-138">Use the **SetNotifyFlags** method in conjunction with the [**IBackgroundCopyJob::SetNotifyInterface**](ibackgroundcopyjob-setnotifyinterface.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5d356-139">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5d356-139">Requirements</span></span>



| <span data-ttu-id="5d356-140">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5d356-140">Requirement</span></span> | <span data-ttu-id="5d356-141">Valeur</span><span class="sxs-lookup"><span data-stu-id="5d356-141">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5d356-142">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5d356-142">Minimum supported client</span></span><br/> | <span data-ttu-id="5d356-143">Applications de bureau Windows 10, version 1709 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5d356-143">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="5d356-144">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5d356-144">Minimum supported server</span></span><br/> | <span data-ttu-id="5d356-145">Windows Server, version 1709, \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5d356-145">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="5d356-146">En-tête</span><span class="sxs-lookup"><span data-stu-id="5d356-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="5d356-147"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="5d356-147"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="5d356-148">MIDL</span><span class="sxs-lookup"><span data-stu-id="5d356-148">IDL</span></span><br/>                      | <dl> <span data-ttu-id="5d356-149"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="5d356-149"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="5d356-150">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="5d356-150">Library</span></span><br/>                  | <dl> <span data-ttu-id="5d356-151"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5d356-151"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="5d356-152">DLL</span><span class="sxs-lookup"><span data-stu-id="5d356-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5d356-153"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5d356-153"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="5d356-154">IID</span><span class="sxs-lookup"><span data-stu-id="5d356-154">IID</span></span><br/>                      | <span data-ttu-id="5d356-155">IID_IBackgroundCopyJob est défini en tant que 37668D37-507E-4160-9316-26306D150B12</span><span class="sxs-lookup"><span data-stu-id="5d356-155">IID_IBackgroundCopyJob is defined as 37668D37-507E-4160-9316-26306D150B12</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="5d356-156">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5d356-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d356-157">**Méthode ibackgroundcopyjob**</span><span class="sxs-lookup"><span data-stu-id="5d356-157">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> <dt>

[<span data-ttu-id="5d356-158">**IBackgroundCopyCallback**</span><span class="sxs-lookup"><span data-stu-id="5d356-158">**IBackgroundCopyCallback**</span></span>](ibackgroundcopycallback.md)
</dt> <dt>

[<span data-ttu-id="5d356-159">**Méthode ibackgroundcopyjob :: GetNotifyFlags**</span><span class="sxs-lookup"><span data-stu-id="5d356-159">**IBackgroundCopyJob::GetNotifyFlags**</span></span>](ibackgroundcopyjob-getnotifyflags.md)
</dt> <dt>

[<span data-ttu-id="5d356-160">**Méthode ibackgroundcopyjob :: SetNotifyInterface**</span><span class="sxs-lookup"><span data-stu-id="5d356-160">**IBackgroundCopyJob::SetNotifyInterface**</span></span>](ibackgroundcopyjob-setnotifyinterface.md)
</dt> </dl>

 

 





