---
title: Méthode ibackgroundcopyjob suspend, méthode (Deliveryoptimization. h)
description: Interrompt un travail. Les nouveaux travaux, les travaux en erreur et les travaux qui ont terminé le transfert des fichiers sont automatiquement suspendus.
ms.assetid: 23EED354-A3AC-4865-8C06-ADA097851F96
keywords:
- Suspend, méthode
- Suspend, méthode, méthode ibackgroundcopyjob, interface
- Interface méthode ibackgroundcopyjob, méthode suspend
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.Suspend
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: dd4464a04f87a7759e9b51974eef2188ba1d0c2a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384655"
---
# <a name="ibackgroundcopyjobsuspend-method"></a><span data-ttu-id="2db11-107">Méthode ibackgroundcopyjob :: suspend, méthode</span><span class="sxs-lookup"><span data-stu-id="2db11-107">IBackgroundCopyJob::Suspend method</span></span>

<span data-ttu-id="2db11-108">Interrompt un travail.</span><span class="sxs-lookup"><span data-stu-id="2db11-108">Suspends a job.</span></span> <span data-ttu-id="2db11-109">Les nouveaux travaux, les travaux en erreur et les travaux qui ont terminé le transfert des fichiers sont automatiquement suspendus.</span><span class="sxs-lookup"><span data-stu-id="2db11-109">New jobs, jobs that are in error, and jobs that have finished transferring files are automatically suspended.</span></span>

## <a name="syntax"></a><span data-ttu-id="2db11-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2db11-110">Syntax</span></span>


```C++
HRESULT Suspend();
```



## <a name="parameters"></a><span data-ttu-id="2db11-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2db11-111">Parameters</span></span>

<span data-ttu-id="2db11-112">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="2db11-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="2db11-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2db11-113">Return value</span></span>

<span data-ttu-id="2db11-114">Cette méthode retourne les valeurs **HRESULT** suivantes, ainsi que d’autres.</span><span class="sxs-lookup"><span data-stu-id="2db11-114">This method returns the following **HRESULT** values, as well as others.</span></span>



| <span data-ttu-id="2db11-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="2db11-115">Return code</span></span>                                                                                          | <span data-ttu-id="2db11-116">Description</span><span class="sxs-lookup"><span data-stu-id="2db11-116">Description</span></span>                                                                                          |
|------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="2db11-117"><dt>S_OK \* \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="2db11-117"><dt>\*\*\*\*S_OK\*\*\*\*</dt></span></span> </dl>             | <span data-ttu-id="2db11-118">La tâche a été suspendue.</span><span class="sxs-lookup"><span data-stu-id="2db11-118">Successfully suspended the job.</span></span><br/>                                                           |
| <dl> <span data-ttu-id="2db11-119"><dt>**DO_E_INVALID_STATE**</dt></span><span class="sxs-lookup"><span data-stu-id="2db11-119"><dt>**DO_E_INVALID_STATE**</dt></span></span> </dl> | <span data-ttu-id="2db11-120">L’état du travail ne peut pas être BG_JOB_STATE_CANCELLED ou BG_JOB_STATE_ACKNOWLEDGED.</span><span class="sxs-lookup"><span data-stu-id="2db11-120">The state of the job cannot be BG_JOB_STATE_CANCELLED or BG_JOB_STATE_ACKNOWLEDGED.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="2db11-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2db11-121">Requirements</span></span>



| <span data-ttu-id="2db11-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2db11-122">Requirement</span></span> | <span data-ttu-id="2db11-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="2db11-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2db11-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2db11-124">Minimum supported client</span></span><br/> | <span data-ttu-id="2db11-125">Applications de bureau Windows 10, version 1709 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2db11-125">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="2db11-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2db11-126">Minimum supported server</span></span><br/> | <span data-ttu-id="2db11-127">Windows Server, version 1709, \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2db11-127">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="2db11-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="2db11-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="2db11-129"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="2db11-129"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="2db11-130">MIDL</span><span class="sxs-lookup"><span data-stu-id="2db11-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="2db11-131"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="2db11-131"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="2db11-132">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="2db11-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="2db11-133"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2db11-133"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="2db11-134">DLL</span><span class="sxs-lookup"><span data-stu-id="2db11-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2db11-135"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2db11-135"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="2db11-136">IID</span><span class="sxs-lookup"><span data-stu-id="2db11-136">IID</span></span><br/>                      | <span data-ttu-id="2db11-137">IID_IBackgroundCopyJob est défini en tant que 37668D37-507E-4160-9316-26306D150B12</span><span class="sxs-lookup"><span data-stu-id="2db11-137">IID_IBackgroundCopyJob is defined as 37668D37-507E-4160-9316-26306D150B12</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="2db11-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2db11-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2db11-139">**Méthode ibackgroundcopyjob**</span><span class="sxs-lookup"><span data-stu-id="2db11-139">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> <dt>

[<span data-ttu-id="2db11-140">**Méthode ibackgroundcopyjob :: Cancel**</span><span class="sxs-lookup"><span data-stu-id="2db11-140">**IBackgroundCopyJob::Cancel**</span></span>](ibackgroundcopyjob-cancel.md)
</dt> <dt>

[<span data-ttu-id="2db11-141">**Méthode ibackgroundcopyjob :: Resume**</span><span class="sxs-lookup"><span data-stu-id="2db11-141">**IBackgroundCopyJob::Resume**</span></span>](ibackgroundcopyjob-resume.md)
</dt> </dl>

 

 





