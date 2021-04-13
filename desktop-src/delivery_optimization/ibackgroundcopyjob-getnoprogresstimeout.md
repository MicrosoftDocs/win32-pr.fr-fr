---
title: Méthode méthode ibackgroundcopyjob GetNoProgressTimeout (Deliveryoptimization. h)
description: Récupère la durée pendant laquelle le service tente de transférer le fichier après qu’une condition d’erreur temporaire se produit. En cas de progression, la minuterie est réinitialisée.
ms.assetid: 3C31A15B-62EF-4807-8EC3-78BAEA3E23AE
keywords:
- Méthode GetNoProgressTimeout
- Méthode GetNoProgressTimeout, interface méthode ibackgroundcopyjob
- Interface méthode ibackgroundcopyjob, méthode GetNoProgressTimeout
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.GetNoProgressTimeout
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3ccd236c17612aa03a28e07a08d087454f8db6f3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465519"
---
# <a name="ibackgroundcopyjobgetnoprogresstimeout-method"></a><span data-ttu-id="2d4e5-107">Méthode ibackgroundcopyjob :: GetNoProgressTimeout, méthode</span><span class="sxs-lookup"><span data-stu-id="2d4e5-107">IBackgroundCopyJob::GetNoProgressTimeout method</span></span>

<span data-ttu-id="2d4e5-108">Récupère la durée pendant laquelle le service tente de transférer le fichier après qu’une condition d’erreur temporaire se produit.</span><span class="sxs-lookup"><span data-stu-id="2d4e5-108">Retrieves the length of time that the service tries to transfer the file after a transient error condition occurs.</span></span> <span data-ttu-id="2d4e5-109">En cas de progression, la minuterie est réinitialisée.</span><span class="sxs-lookup"><span data-stu-id="2d4e5-109">If there is progress, the timer is reset.</span></span>

## <a name="syntax"></a><span data-ttu-id="2d4e5-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2d4e5-110">Syntax</span></span>


```C++
HRESULT GetNoProgressTimeout(
  [in] ULONG *pRetryPeriod
);
```



## <a name="parameters"></a><span data-ttu-id="2d4e5-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2d4e5-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2d4e5-112">*pRetryPeriod* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2d4e5-112">*pRetryPeriod* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2d4e5-113">Durée, en secondes, pendant laquelle le service tente de transférer le fichier après qu’une erreur temporaire se produit.</span><span class="sxs-lookup"><span data-stu-id="2d4e5-113">Length of time, in seconds, that the service tries to transfer the file after a transient error occurs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2d4e5-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2d4e5-114">Return value</span></span>

<span data-ttu-id="2d4e5-115">Cette méthode retourne les valeurs **HRESULT** suivantes, ainsi que d’autres.</span><span class="sxs-lookup"><span data-stu-id="2d4e5-115">This method returns the following **HRESULT** values, as well as others.</span></span>



| <span data-ttu-id="2d4e5-116">Code de retour</span><span class="sxs-lookup"><span data-stu-id="2d4e5-116">Return code</span></span>                                                                              | <span data-ttu-id="2d4e5-117">Description</span><span class="sxs-lookup"><span data-stu-id="2d4e5-117">Description</span></span>                                     |
|------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="2d4e5-118"><dt>S_OK \* \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="2d4e5-118"><dt>\*\*\*\*S_OK\*\*\*\*</dt></span></span> </dl> | <span data-ttu-id="2d4e5-119">Le délai d’attente a été correctement récupéré.</span><span class="sxs-lookup"><span data-stu-id="2d4e5-119">Time-out was successfully retrieved.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="2d4e5-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2d4e5-120">Requirements</span></span>



| <span data-ttu-id="2d4e5-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2d4e5-121">Requirement</span></span> | <span data-ttu-id="2d4e5-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="2d4e5-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2d4e5-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2d4e5-123">Minimum supported client</span></span><br/> | <span data-ttu-id="2d4e5-124">Applications de bureau Windows 10, version 1709 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2d4e5-124">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="2d4e5-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2d4e5-125">Minimum supported server</span></span><br/> | <span data-ttu-id="2d4e5-126">Windows Server, version 1709, \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2d4e5-126">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="2d4e5-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="2d4e5-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="2d4e5-128"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="2d4e5-128"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="2d4e5-129">MIDL</span><span class="sxs-lookup"><span data-stu-id="2d4e5-129">IDL</span></span><br/>                      | <dl> <span data-ttu-id="2d4e5-130"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="2d4e5-130"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="2d4e5-131">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="2d4e5-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="2d4e5-132"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2d4e5-132"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="2d4e5-133">DLL</span><span class="sxs-lookup"><span data-stu-id="2d4e5-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2d4e5-134"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2d4e5-134"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="2d4e5-135">IID</span><span class="sxs-lookup"><span data-stu-id="2d4e5-135">IID</span></span><br/>                      | <span data-ttu-id="2d4e5-136">IID_IBackgroundCopyJob est défini en tant que 37668D37-507E-4160-9316-26306D150B12</span><span class="sxs-lookup"><span data-stu-id="2d4e5-136">IID_IBackgroundCopyJob is defined as 37668D37-507E-4160-9316-26306D150B12</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="2d4e5-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2d4e5-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d4e5-138">**Méthode ibackgroundcopyjob**</span><span class="sxs-lookup"><span data-stu-id="2d4e5-138">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> <dt>

[<span data-ttu-id="2d4e5-139">**Méthode ibackgroundcopyjob :: SetNoProgressTimeout**</span><span class="sxs-lookup"><span data-stu-id="2d4e5-139">**IBackgroundCopyJob::SetNoProgressTimeout**</span></span>](ibackgroundcopyjob-setnoprogresstimeout.md)
</dt> </dl>

 

 





