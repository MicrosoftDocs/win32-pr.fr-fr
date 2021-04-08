---
title: Méthode ibackgroundcopyjob méthode Cancel (Deliveryoptimization. h)
description: Supprime le travail de la file d’attente de transfert et supprime les fichiers temporaires associés du client (Téléchargements) et le serveur (chargements).
ms.assetid: DC502DC2-1335-476F-A1B8-FDB6BA595FF1
keywords:
- Cancel, méthode
- Cancel, méthode, méthode ibackgroundcopyjob, interface
- Interface méthode ibackgroundcopyjob, méthode Cancel
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.Cancel
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f72cdcea82ef7db30de141af295bb74594a7a630
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843457"
---
# <a name="ibackgroundcopyjobcancel-method"></a><span data-ttu-id="0f6d8-106">Méthode ibackgroundcopyjob :: Cancel, méthode</span><span class="sxs-lookup"><span data-stu-id="0f6d8-106">IBackgroundCopyJob::Cancel method</span></span>

<span data-ttu-id="0f6d8-107">Supprime le travail de la file d’attente de transfert et supprime les fichiers temporaires associés du client (Téléchargements) et le serveur (chargements).</span><span class="sxs-lookup"><span data-stu-id="0f6d8-107">Deletes the job from the transfer queue and removes related temporary files from the client (downloads) and server (uploads).</span></span>

## <a name="syntax"></a><span data-ttu-id="0f6d8-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0f6d8-108">Syntax</span></span>


```C++
HRESULT Cancel();
```



## <a name="parameters"></a><span data-ttu-id="0f6d8-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0f6d8-109">Parameters</span></span>

<span data-ttu-id="0f6d8-110">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="0f6d8-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0f6d8-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0f6d8-111">Return value</span></span>

<span data-ttu-id="0f6d8-112">Cette méthode retourne les valeurs **HRESULT** suivantes, ainsi que d’autres.</span><span class="sxs-lookup"><span data-stu-id="0f6d8-112">This method returns the following **HRESULT** values, as well as others.</span></span>



| <span data-ttu-id="0f6d8-113">Code de retour</span><span class="sxs-lookup"><span data-stu-id="0f6d8-113">Return code</span></span>                                                                                          | <span data-ttu-id="0f6d8-114">Description</span><span class="sxs-lookup"><span data-stu-id="0f6d8-114">Description</span></span>                                                                                              |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="0f6d8-115"><dt>S_OK \* \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="0f6d8-115"><dt>\*\*\*\*S_OK\*\*\*\*</dt></span></span> </dl>             | <span data-ttu-id="0f6d8-116">La tâche a été annulée avec succès.</span><span class="sxs-lookup"><span data-stu-id="0f6d8-116">Job was successfully canceled.</span></span><br/>                                                                |
| <dl> <span data-ttu-id="0f6d8-117"><dt>**DO_E_INVALID_STATE**</dt></span><span class="sxs-lookup"><span data-stu-id="0f6d8-117"><dt>**DO_E_INVALID_STATE**</dt></span></span> </dl> | <span data-ttu-id="0f6d8-118">Impossible d’annuler un travail dont l’État est BG_JOB_STATE_CANCELLED ou BG_JOB_STATE_ACKNOWLEDGED.</span><span class="sxs-lookup"><span data-stu-id="0f6d8-118">Cannot cancel a job whose state is BG_JOB_STATE_CANCELLED or BG_JOB_STATE_ACKNOWLEDGED.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="0f6d8-119">Notes</span><span class="sxs-lookup"><span data-stu-id="0f6d8-119">Remarks</span></span>

<span data-ttu-id="0f6d8-120">Vous pouvez annuler un travail à tout moment ; Toutefois, le travail ne peut pas être récupéré une fois qu’il a été annulé.</span><span class="sxs-lookup"><span data-stu-id="0f6d8-120">You can cancel a job at any time; however, the job cannot be recovered after it is canceled.</span></span>

## <a name="requirements"></a><span data-ttu-id="0f6d8-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0f6d8-121">Requirements</span></span>



| <span data-ttu-id="0f6d8-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0f6d8-122">Requirement</span></span> | <span data-ttu-id="0f6d8-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="0f6d8-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0f6d8-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0f6d8-124">Minimum supported client</span></span><br/> | <span data-ttu-id="0f6d8-125">Applications de bureau Windows 10, version 1709 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0f6d8-125">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="0f6d8-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0f6d8-126">Minimum supported server</span></span><br/> | <span data-ttu-id="0f6d8-127">Windows Server, version 1709, \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0f6d8-127">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="0f6d8-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="0f6d8-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="0f6d8-129"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="0f6d8-129"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="0f6d8-130">MIDL</span><span class="sxs-lookup"><span data-stu-id="0f6d8-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="0f6d8-131"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="0f6d8-131"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="0f6d8-132">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="0f6d8-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="0f6d8-133"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0f6d8-133"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="0f6d8-134">DLL</span><span class="sxs-lookup"><span data-stu-id="0f6d8-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0f6d8-135"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0f6d8-135"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="0f6d8-136">IID</span><span class="sxs-lookup"><span data-stu-id="0f6d8-136">IID</span></span><br/>                      | <span data-ttu-id="0f6d8-137">IID_IBackgroundCopyJob est défini en tant que 37668D37-507E-4160-9316-26306D150B12</span><span class="sxs-lookup"><span data-stu-id="0f6d8-137">IID_IBackgroundCopyJob is defined as 37668D37-507E-4160-9316-26306D150B12</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="0f6d8-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0f6d8-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f6d8-139">**Méthode ibackgroundcopyjob**</span><span class="sxs-lookup"><span data-stu-id="0f6d8-139">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> <dt>

[<span data-ttu-id="0f6d8-140">**Méthode ibackgroundcopyjob :: complet**</span><span class="sxs-lookup"><span data-stu-id="0f6d8-140">**IBackgroundCopyJob::Complete**</span></span>](ibackgroundcopyjob-complete.md)
</dt> <dt>

[<span data-ttu-id="0f6d8-141">**Méthode ibackgroundcopyjob :: Resume**</span><span class="sxs-lookup"><span data-stu-id="0f6d8-141">**IBackgroundCopyJob::Resume**</span></span>](ibackgroundcopyjob-resume.md)
</dt> <dt>

[<span data-ttu-id="0f6d8-142">**Méthode ibackgroundcopyjob :: suspend**</span><span class="sxs-lookup"><span data-stu-id="0f6d8-142">**IBackgroundCopyJob::Suspend**</span></span>](ibackgroundcopyjob-suspend.md)
</dt> </dl>

 

 





