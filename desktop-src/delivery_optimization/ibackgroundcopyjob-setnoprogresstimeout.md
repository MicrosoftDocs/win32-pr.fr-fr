---
title: Méthode méthode ibackgroundcopyjob SetNoProgressTimeout (Deliveryoptimization. h)
description: Définit la durée pendant laquelle l’optimisation de la remise (DO) tente de transférer le fichier après qu’une condition d’erreur temporaire se produit. En cas de progression, la minuterie est réinitialisée.
ms.assetid: DC86F74F-8429-4D78-B425-CAF19867B05E
keywords:
- Méthode SetNoProgressTimeout
- Méthode SetNoProgressTimeout, interface méthode ibackgroundcopyjob
- Interface méthode ibackgroundcopyjob, méthode SetNoProgressTimeout
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.SetNoProgressTimeout
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 276c8c44d2b2b034543aae25361c5f5c94046f5d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032926"
---
# <a name="ibackgroundcopyjobsetnoprogresstimeout-method"></a><span data-ttu-id="79513-107">Méthode ibackgroundcopyjob :: SetNoProgressTimeout, méthode</span><span class="sxs-lookup"><span data-stu-id="79513-107">IBackgroundCopyJob::SetNoProgressTimeout method</span></span>

<span data-ttu-id="79513-108">Définit la durée pendant laquelle l’optimisation de la remise (DO) tente de transférer le fichier après qu’une condition d’erreur temporaire se produit.</span><span class="sxs-lookup"><span data-stu-id="79513-108">Sets the length of time that Delivery Optimization (DO) tries to transfer the file after a transient error condition occurs.</span></span> <span data-ttu-id="79513-109">En cas de progression, la minuterie est réinitialisée.</span><span class="sxs-lookup"><span data-stu-id="79513-109">If there is progress, the timer is reset.</span></span>

## <a name="syntax"></a><span data-ttu-id="79513-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="79513-110">Syntax</span></span>


```C++
HRESULT SetNoProgressTimeout(
  [in] ULONG RetryPeriod
);
```



## <a name="parameters"></a><span data-ttu-id="79513-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="79513-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="79513-112">*RetryPeriod* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="79513-112">*RetryPeriod* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="79513-113">Durée, en secondes, pendant laquelle tente de transférer le fichier après qu’aucune progression n’a été effectuée.</span><span class="sxs-lookup"><span data-stu-id="79513-113">Length of time, in seconds, that DO tries to transfer the file after there has been no progress made.</span></span> <span data-ttu-id="79513-114">La période de nouvelle tentative par défaut pour un travail à priorité élevée est de 3600 secondes (1 heure) et, pour une tâche basse priorité, 86400 secondes (24 heures).</span><span class="sxs-lookup"><span data-stu-id="79513-114">The default retry period for high priority job is 3600 seconds (1 hour) and for low priority job is 86400 seconds (24 hours).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="79513-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="79513-115">Return value</span></span>

<span data-ttu-id="79513-116">Cette méthode retourne les valeurs **HRESULT** suivantes, ainsi que d’autres.</span><span class="sxs-lookup"><span data-stu-id="79513-116">This method returns the following **HRESULT** values, as well as others.</span></span>



| <span data-ttu-id="79513-117">Code de retour</span><span class="sxs-lookup"><span data-stu-id="79513-117">Return code</span></span>                                                                                          | <span data-ttu-id="79513-118">Description</span><span class="sxs-lookup"><span data-stu-id="79513-118">Description</span></span>                                                                                          |
|------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="79513-119"><dt>S_OK \* \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="79513-119"><dt>\*\*\*\*S_OK\*\*\*\*</dt></span></span> </dl>             | <span data-ttu-id="79513-120">Période de nouvelle tentative définie avec succès.</span><span class="sxs-lookup"><span data-stu-id="79513-120">Retry period successfully set.</span></span><br/>                                                            |
| <dl> <span data-ttu-id="79513-121"><dt>**DO_E_INVALID_STATE**</dt></span><span class="sxs-lookup"><span data-stu-id="79513-121"><dt>**DO_E_INVALID_STATE**</dt></span></span> </dl> | <span data-ttu-id="79513-122">L’état du travail ne peut pas être BG_JOB_STATE_CANCELLED ou BG_JOB_STATE_ACKNOWLEDGED.</span><span class="sxs-lookup"><span data-stu-id="79513-122">The state of the job cannot be BG_JOB_STATE_CANCELLED or BG_JOB_STATE_ACKNOWLEDGED.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="79513-123">Notes</span><span class="sxs-lookup"><span data-stu-id="79513-123">Remarks</span></span>

<span data-ttu-id="79513-124">Si ne progresse pas pendant la période de nouvelle tentative, il déplace l’état du travail de BG_JOB_STATE_TRANSIENT_ERROR à BG_JOB_STATE_ERROR.</span><span class="sxs-lookup"><span data-stu-id="79513-124">If DO does not make progress during the retry period, it moves the state of the job from BG_JOB_STATE_TRANSIENT_ERROR to BG_JOB_STATE_ERROR.</span></span> <span data-ttu-id="79513-125">Si vous demandez une notification d’erreur, appelle votre rappel [**JobError**](https://www.bing.com/search?q=**JobError**) .</span><span class="sxs-lookup"><span data-stu-id="79513-125">If you request error notification, DO then calls your [**JobError**](https://www.bing.com/search?q=**JobError**) callback.</span></span>

## <a name="requirements"></a><span data-ttu-id="79513-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="79513-126">Requirements</span></span>



| <span data-ttu-id="79513-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="79513-127">Requirement</span></span> | <span data-ttu-id="79513-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="79513-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="79513-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="79513-129">Minimum supported client</span></span><br/> | <span data-ttu-id="79513-130">Applications de bureau Windows 10, version 1709 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="79513-130">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="79513-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="79513-131">Minimum supported server</span></span><br/> | <span data-ttu-id="79513-132">Windows Server, version 1709, \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="79513-132">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="79513-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="79513-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="79513-134"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="79513-134"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="79513-135">MIDL</span><span class="sxs-lookup"><span data-stu-id="79513-135">IDL</span></span><br/>                      | <dl> <span data-ttu-id="79513-136"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="79513-136"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="79513-137">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="79513-137">Library</span></span><br/>                  | <dl> <span data-ttu-id="79513-138"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="79513-138"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="79513-139">DLL</span><span class="sxs-lookup"><span data-stu-id="79513-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="79513-140"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="79513-140"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="79513-141">IID</span><span class="sxs-lookup"><span data-stu-id="79513-141">IID</span></span><br/>                      | <span data-ttu-id="79513-142">IID_IBackgroundCopyJob est défini en tant que 37668D37-507E-4160-9316-26306D150B12</span><span class="sxs-lookup"><span data-stu-id="79513-142">IID_IBackgroundCopyJob is defined as 37668D37-507E-4160-9316-26306D150B12</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="79513-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="79513-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79513-144">**Méthode ibackgroundcopyjob**</span><span class="sxs-lookup"><span data-stu-id="79513-144">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> <dt>

[<span data-ttu-id="79513-145">**Méthode ibackgroundcopyjob :: GetNoProgressTimeout**</span><span class="sxs-lookup"><span data-stu-id="79513-145">**IBackgroundCopyJob::GetNoProgressTimeout**</span></span>](ibackgroundcopyjob-getnoprogresstimeout.md)
</dt> </dl>

 

 





