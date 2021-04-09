---
title: Méthode ibackgroundcopyjob, méthode de reprise (Deliveryoptimization. h)
description: Active un nouveau travail ou redémarre un travail qui a été suspendu.
ms.assetid: B745BDA6-36B9-41FD-9737-61D14150A9E4
keywords:
- Resume, méthode
- Resume, méthode, interface méthode ibackgroundcopyjob
- Interface méthode ibackgroundcopyjob, méthode Resume
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.Resume
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f87f5b5347785810d84331ce56f240cd1f016383
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103241"
---
# <a name="ibackgroundcopyjobresume-method"></a><span data-ttu-id="a5bd4-106">Méthode ibackgroundcopyjob :: Resume, méthode</span><span class="sxs-lookup"><span data-stu-id="a5bd4-106">IBackgroundCopyJob::Resume method</span></span>

<span data-ttu-id="a5bd4-107">Active un nouveau travail ou redémarre un travail qui a été suspendu.</span><span class="sxs-lookup"><span data-stu-id="a5bd4-107">Activates a new job or restarts a job that has been suspended.</span></span>

## <a name="syntax"></a><span data-ttu-id="a5bd4-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a5bd4-108">Syntax</span></span>


```C++
HRESULT Resume();
```



## <a name="parameters"></a><span data-ttu-id="a5bd4-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a5bd4-109">Parameters</span></span>

<span data-ttu-id="a5bd4-110">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="a5bd4-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a5bd4-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a5bd4-111">Return value</span></span>

<span data-ttu-id="a5bd4-112">Cette méthode retourne les valeurs **HRESULT** suivantes, ainsi que d’autres.</span><span class="sxs-lookup"><span data-stu-id="a5bd4-112">This method returns the following **HRESULT** values, as well as others.</span></span>



| <span data-ttu-id="a5bd4-113">Code de retour</span><span class="sxs-lookup"><span data-stu-id="a5bd4-113">Return code</span></span>                                                                                          | <span data-ttu-id="a5bd4-114">Description</span><span class="sxs-lookup"><span data-stu-id="a5bd4-114">Description</span></span>                                                                                          |
|------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="a5bd4-115"><dt>S_OK \* \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="a5bd4-115"><dt>\*\*\*\*S_OK\*\*\*\*</dt></span></span> </dl>             | <span data-ttu-id="a5bd4-116">Le travail a été redémarré avec succès.</span><span class="sxs-lookup"><span data-stu-id="a5bd4-116">Job was successfully restarted.</span></span><br/>                                                           |
| <dl> <span data-ttu-id="a5bd4-117"><dt>**DO_E_EMPTY**</dt></span><span class="sxs-lookup"><span data-stu-id="a5bd4-117"><dt>**DO_E_EMPTY**</dt></span></span> </dl>          | <span data-ttu-id="a5bd4-118">Aucun fichier à transférer.</span><span class="sxs-lookup"><span data-stu-id="a5bd4-118">There are no files to transfer.</span></span><br/>                                                           |
| <dl> <span data-ttu-id="a5bd4-119"><dt>**DO_E_INVALID_STATE**</dt></span><span class="sxs-lookup"><span data-stu-id="a5bd4-119"><dt>**DO_E_INVALID_STATE**</dt></span></span> </dl> | <span data-ttu-id="a5bd4-120">L’état du travail ne peut pas être BG_JOB_STATE_CANCELLED ou BG_JOB_STATE_ACKNOWLEDGED.</span><span class="sxs-lookup"><span data-stu-id="a5bd4-120">The state of the job cannot be BG_JOB_STATE_CANCELLED or BG_JOB_STATE_ACKNOWLEDGED.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="a5bd4-121">Notes</span><span class="sxs-lookup"><span data-stu-id="a5bd4-121">Remarks</span></span>

<span data-ttu-id="a5bd4-122">Lorsque vous créez un travail, le travail est initialement suspendu.</span><span class="sxs-lookup"><span data-stu-id="a5bd4-122">When you create a job, the job is initially suspended.</span></span> <span data-ttu-id="a5bd4-123">L’appel de la méthode **Resume** déplace le travail vers l’État Transfering.</span><span class="sxs-lookup"><span data-stu-id="a5bd4-123">Calling **Resume** moves the job to the Transferring state.</span></span> <span data-ttu-id="a5bd4-124">Notez que le travail doit contenir un ou plusieurs fichiers avant d’appeler cette méthode.</span><span class="sxs-lookup"><span data-stu-id="a5bd4-124">Note that the job must contain one or more files before calling this method.</span></span>

<span data-ttu-id="a5bd4-125">Si un travail qui se trouve dans l’État BG_JOB_STATE_TRANSIENT_ERROR ou BG_JOB_STATE_ERROR, appelez la méthode **Resume** pour redémarrer le travail après avoir corrigé l’erreur.</span><span class="sxs-lookup"><span data-stu-id="a5bd4-125">If a job that is in the BG_JOB_STATE_TRANSIENT_ERROR or BG_JOB_STATE_ERROR state, call the **Resume** method to restart the job after you fix the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="a5bd4-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a5bd4-126">Requirements</span></span>



| <span data-ttu-id="a5bd4-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a5bd4-127">Requirement</span></span> | <span data-ttu-id="a5bd4-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="a5bd4-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a5bd4-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a5bd4-129">Minimum supported client</span></span><br/> | <span data-ttu-id="a5bd4-130">Applications de bureau Windows 10, version 1709 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a5bd4-130">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="a5bd4-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a5bd4-131">Minimum supported server</span></span><br/> | <span data-ttu-id="a5bd4-132">Windows Server, version 1709, \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a5bd4-132">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="a5bd4-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="a5bd4-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="a5bd4-134"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="a5bd4-134"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="a5bd4-135">MIDL</span><span class="sxs-lookup"><span data-stu-id="a5bd4-135">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a5bd4-136"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="a5bd4-136"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="a5bd4-137">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="a5bd4-137">Library</span></span><br/>                  | <dl> <span data-ttu-id="a5bd4-138"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a5bd4-138"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="a5bd4-139">DLL</span><span class="sxs-lookup"><span data-stu-id="a5bd4-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a5bd4-140"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a5bd4-140"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="a5bd4-141">IID</span><span class="sxs-lookup"><span data-stu-id="a5bd4-141">IID</span></span><br/>                      | <span data-ttu-id="a5bd4-142">IID_IBackgroundCopyJob est défini en tant que 37668D37-507E-4160-9316-26306D150B12</span><span class="sxs-lookup"><span data-stu-id="a5bd4-142">IID_IBackgroundCopyJob is defined as 37668D37-507E-4160-9316-26306D150B12</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="a5bd4-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a5bd4-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5bd4-144">**Méthode ibackgroundcopyjob**</span><span class="sxs-lookup"><span data-stu-id="a5bd4-144">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> <dt>

[<span data-ttu-id="a5bd4-145">**Méthode ibackgroundcopyjob :: Cancel**</span><span class="sxs-lookup"><span data-stu-id="a5bd4-145">**IBackgroundCopyJob::Cancel**</span></span>](ibackgroundcopyjob-cancel.md)
</dt> <dt>

[<span data-ttu-id="a5bd4-146">**Méthode ibackgroundcopyjob :: suspend**</span><span class="sxs-lookup"><span data-stu-id="a5bd4-146">**IBackgroundCopyJob::Suspend**</span></span>](ibackgroundcopyjob-suspend.md)
</dt> </dl>

 

 





