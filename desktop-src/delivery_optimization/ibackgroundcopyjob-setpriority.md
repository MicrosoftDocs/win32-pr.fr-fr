---
title: Méthode ibackgroundcopyjob SetPriority, méthode (Deliveryoptimization. h)
description: Spécifie le niveau de priorité de votre travail. Le niveau de priorité détermine le moment où votre travail est traité par rapport à d’autres travaux dans la file d’attente de transfert.
ms.assetid: DC943093-CA1D-4840-B7AC-29710764D4E5
keywords:
- SetPriority, méthode
- SetPriority, méthode, interface méthode ibackgroundcopyjob
- Interface méthode ibackgroundcopyjob, méthode SetPriority
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.SetPriority
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6fb6407c5d693a2c6e75f8aaf8f7a0544d08cdec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741716"
---
# <a name="ibackgroundcopyjobsetpriority-method"></a><span data-ttu-id="5832b-107">Méthode ibackgroundcopyjob :: SetPriority, méthode</span><span class="sxs-lookup"><span data-stu-id="5832b-107">IBackgroundCopyJob::SetPriority method</span></span>

<span data-ttu-id="5832b-108">Spécifie le niveau de priorité de votre travail.</span><span class="sxs-lookup"><span data-stu-id="5832b-108">Specifies the priority level of your job.</span></span> <span data-ttu-id="5832b-109">Le niveau de priorité détermine le moment où votre travail est traité par rapport à d’autres travaux dans la file d’attente de transfert.</span><span class="sxs-lookup"><span data-stu-id="5832b-109">The priority level determines when your job is processed relative to other jobs in the transfer queue.</span></span>

## <a name="syntax"></a><span data-ttu-id="5832b-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5832b-110">Syntax</span></span>


```C++
HRESULT SetPriority(
  [in] BG_JOB_PRIORITY Priority
);
```



## <a name="parameters"></a><span data-ttu-id="5832b-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5832b-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5832b-112">*Priorité* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5832b-112">*Priority* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5832b-113">Spécifie le niveau de priorité de votre travail par rapport à d’autres travaux dans la file d’attente de transfert.</span><span class="sxs-lookup"><span data-stu-id="5832b-113">Specifies the priority level of your job relative to other jobs in the transfer queue.</span></span> <span data-ttu-id="5832b-114">La valeur par défaut est BG_JOB_PRIORITY_NORMAL.</span><span class="sxs-lookup"><span data-stu-id="5832b-114">The default is BG_JOB_PRIORITY_NORMAL.</span></span> <span data-ttu-id="5832b-115">Pour obtenir la liste des niveaux de priorité, consultez l’énumération [**BG_JOB_PRIORITY**](bg-job-priority-.md) .</span><span class="sxs-lookup"><span data-stu-id="5832b-115">For a list of priority levels, see the [**BG_JOB_PRIORITY**](bg-job-priority-.md) enumeration.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5832b-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5832b-116">Return value</span></span>

<span data-ttu-id="5832b-117">Cette méthode retourne les valeurs **HRESULT** suivantes, ainsi que d’autres.</span><span class="sxs-lookup"><span data-stu-id="5832b-117">This method returns the following **HRESULT** values, as well as others.</span></span>



| <span data-ttu-id="5832b-118">Code de retour</span><span class="sxs-lookup"><span data-stu-id="5832b-118">Return code</span></span>                                                                              | <span data-ttu-id="5832b-119">Description</span><span class="sxs-lookup"><span data-stu-id="5832b-119">Description</span></span>                                   |
|------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <span data-ttu-id="5832b-120"><dt>S_OK \* \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="5832b-120"><dt>\*\*\*\*S_OK\*\*\*\*</dt></span></span> </dl> | <span data-ttu-id="5832b-121">La priorité du travail a été correctement définie.</span><span class="sxs-lookup"><span data-stu-id="5832b-121">Job priority was successfully set.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="5832b-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5832b-122">Requirements</span></span>



| <span data-ttu-id="5832b-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5832b-123">Requirement</span></span> | <span data-ttu-id="5832b-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="5832b-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5832b-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5832b-125">Minimum supported client</span></span><br/> | <span data-ttu-id="5832b-126">Applications de bureau Windows 10, version 1709 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5832b-126">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="5832b-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5832b-127">Minimum supported server</span></span><br/> | <span data-ttu-id="5832b-128">Windows Server, version 1709, \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5832b-128">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="5832b-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="5832b-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="5832b-130"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="5832b-130"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="5832b-131">MIDL</span><span class="sxs-lookup"><span data-stu-id="5832b-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="5832b-132"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="5832b-132"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="5832b-133">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="5832b-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="5832b-134"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5832b-134"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="5832b-135">DLL</span><span class="sxs-lookup"><span data-stu-id="5832b-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5832b-136"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5832b-136"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="5832b-137">IID</span><span class="sxs-lookup"><span data-stu-id="5832b-137">IID</span></span><br/>                      | <span data-ttu-id="5832b-138">IID_IBackgroundCopyJob est défini en tant que 37668D37-507E-4160-9316-26306D150B12</span><span class="sxs-lookup"><span data-stu-id="5832b-138">IID_IBackgroundCopyJob is defined as 37668D37-507E-4160-9316-26306D150B12</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="5832b-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5832b-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5832b-140">**Méthode ibackgroundcopyjob**</span><span class="sxs-lookup"><span data-stu-id="5832b-140">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> <dt>

[<span data-ttu-id="5832b-141">**BG_JOB_PRIORITY**</span><span class="sxs-lookup"><span data-stu-id="5832b-141">**BG_JOB_PRIORITY**</span></span>](bg-job-priority-.md)
</dt> <dt>

[<span data-ttu-id="5832b-142">**Méthode ibackgroundcopyjob :: getPriority,**</span><span class="sxs-lookup"><span data-stu-id="5832b-142">**IBackgroundCopyJob::GetPriority**</span></span>](ibackgroundcopyjob-getpriority.md)
</dt> </dl>

 

 





