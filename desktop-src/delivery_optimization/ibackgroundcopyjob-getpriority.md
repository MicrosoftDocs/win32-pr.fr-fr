---
title: Méthode méthode ibackgroundcopyjob getPriority, (Deliveryoptimization. h)
description: Récupère le niveau de priorité du travail. Le niveau de priorité détermine le moment où le travail est traité par rapport à d’autres travaux dans la file d’attente de transfert.
ms.assetid: 2F778B35-8DBB-4540-88C2-A2E18EBB0D89
keywords:
- Méthode getPriority,
- Méthode getPriority,, interface méthode ibackgroundcopyjob
- Interface méthode ibackgroundcopyjob, méthode getPriority,
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.GetPriority
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7ae9a865045ee1264a0598a3d3c1db8cc3c3b8bc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106511154"
---
# <a name="ibackgroundcopyjobgetpriority-method"></a><span data-ttu-id="b0016-107">Méthode ibackgroundcopyjob :: getPriority,, méthode</span><span class="sxs-lookup"><span data-stu-id="b0016-107">IBackgroundCopyJob::GetPriority method</span></span>

<span data-ttu-id="b0016-108">Récupère le niveau de priorité du travail.</span><span class="sxs-lookup"><span data-stu-id="b0016-108">Retrieves the priority level for the job.</span></span> <span data-ttu-id="b0016-109">Le niveau de priorité détermine le moment où le travail est traité par rapport à d’autres travaux dans la file d’attente de transfert.</span><span class="sxs-lookup"><span data-stu-id="b0016-109">The priority level determines when the job is processed relative to other jobs in the transfer queue.</span></span>

## <a name="syntax"></a><span data-ttu-id="b0016-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b0016-110">Syntax</span></span>


```C++
HRESULT GetPriority(
  [out] BG_JOB_PRIORITY *pPriority
);
```



## <a name="parameters"></a><span data-ttu-id="b0016-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b0016-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b0016-112">*pPriority* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="b0016-112">*pPriority* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b0016-113">Priorité du travail par rapport aux autres travaux dans la file d’attente de transfert.</span><span class="sxs-lookup"><span data-stu-id="b0016-113">Priority of the job relative to other jobs in the transfer queue.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b0016-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b0016-114">Return value</span></span>

<span data-ttu-id="b0016-115">Cette méthode retourne les valeurs **HRESULT** suivantes, ainsi que d’autres.</span><span class="sxs-lookup"><span data-stu-id="b0016-115">This method returns the following **HRESULT** values, as well as others.</span></span>



| <span data-ttu-id="b0016-116">Code de retour</span><span class="sxs-lookup"><span data-stu-id="b0016-116">Return code</span></span>                                                                              | <span data-ttu-id="b0016-117">Description</span><span class="sxs-lookup"><span data-stu-id="b0016-117">Description</span></span>                                           |
|------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <dl> <span data-ttu-id="b0016-118"><dt>S_OK \* \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="b0016-118"><dt>\*\*\*\*S_OK\*\*\*\*</dt></span></span> </dl> | <span data-ttu-id="b0016-119">Le niveau de priorité a été récupéré avec succès.</span><span class="sxs-lookup"><span data-stu-id="b0016-119">Priority level was successfully retrieved.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="b0016-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b0016-120">Requirements</span></span>



| <span data-ttu-id="b0016-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b0016-121">Requirement</span></span> | <span data-ttu-id="b0016-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="b0016-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b0016-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b0016-123">Minimum supported client</span></span><br/> | <span data-ttu-id="b0016-124">Applications de bureau Windows 10, version 1709 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b0016-124">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="b0016-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b0016-125">Minimum supported server</span></span><br/> | <span data-ttu-id="b0016-126">Windows Server, version 1709, \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b0016-126">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="b0016-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="b0016-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="b0016-128"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="b0016-128"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="b0016-129">MIDL</span><span class="sxs-lookup"><span data-stu-id="b0016-129">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b0016-130"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="b0016-130"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="b0016-131">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="b0016-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="b0016-132"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b0016-132"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="b0016-133">DLL</span><span class="sxs-lookup"><span data-stu-id="b0016-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b0016-134"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b0016-134"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="b0016-135">IID</span><span class="sxs-lookup"><span data-stu-id="b0016-135">IID</span></span><br/>                      | <span data-ttu-id="b0016-136">IID_IBackgroundCopyJob est défini en tant que 37668D37-507E-4160-9316-26306D150B12</span><span class="sxs-lookup"><span data-stu-id="b0016-136">IID_IBackgroundCopyJob is defined as 37668D37-507E-4160-9316-26306D150B12</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="b0016-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b0016-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0016-138">**Méthode ibackgroundcopyjob**</span><span class="sxs-lookup"><span data-stu-id="b0016-138">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> <dt>

[<span data-ttu-id="b0016-139">**Méthode ibackgroundcopyjob :: SetPriority**</span><span class="sxs-lookup"><span data-stu-id="b0016-139">**IBackgroundCopyJob::SetPriority**</span></span>](ibackgroundcopyjob-setpriority.md)
</dt> </dl>

 

 





