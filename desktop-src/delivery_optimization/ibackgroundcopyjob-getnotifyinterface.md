---
title: Méthode méthode ibackgroundcopyjob GetNotifyInterface (Deliveryoptimization. h)
description: Récupère le pointeur d’interface vers votre implémentation de l’interface IBackgroundCopyCallback.
ms.assetid: 1AA50C03-AC84-4AA9-8EC3-3FBA865C70C0
keywords:
- Méthode GetNotifyInterface
- Méthode GetNotifyInterface, interface méthode ibackgroundcopyjob
- Interface méthode ibackgroundcopyjob, méthode GetNotifyInterface
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.GetNotifyInterface
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6586a90de5783ceb24e5a7677f699a9cf6dfa60c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106509134"
---
# <a name="ibackgroundcopyjobgetnotifyinterface-method"></a><span data-ttu-id="16b3b-106">Méthode ibackgroundcopyjob :: GetNotifyInterface, méthode</span><span class="sxs-lookup"><span data-stu-id="16b3b-106">IBackgroundCopyJob::GetNotifyInterface method</span></span>

<span data-ttu-id="16b3b-107">Récupère le pointeur d’interface vers votre implémentation de l’interface [**IBackgroundCopyCallback**](ibackgroundcopycallback.md) .</span><span class="sxs-lookup"><span data-stu-id="16b3b-107">Retrieves the interface pointer to your implementation of the [**IBackgroundCopyCallback**](ibackgroundcopycallback.md) interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="16b3b-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="16b3b-108">Syntax</span></span>


```C++
HRESULT GetNotifyInterface(
  [out] IUnknown **ppNotifyInterface
);
```



## <a name="parameters"></a><span data-ttu-id="16b3b-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="16b3b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="16b3b-110">*ppNotifyInterface* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="16b3b-110">*ppNotifyInterface* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="16b3b-111">Pointeur d’interface vers votre implémentation de l’interface [**IBackgroundCopyCallback**](ibackgroundcopycallback.md) .</span><span class="sxs-lookup"><span data-stu-id="16b3b-111">Interface pointer to your implementation of the [**IBackgroundCopyCallback**](ibackgroundcopycallback.md) interface.</span></span> <span data-ttu-id="16b3b-112">Lorsque vous avez terminé, libérez *ppNotifyInterface*.</span><span class="sxs-lookup"><span data-stu-id="16b3b-112">When done, release *ppNotifyInterface*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="16b3b-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="16b3b-113">Return value</span></span>

<span data-ttu-id="16b3b-114">Cette méthode retourne les valeurs **HRESULT** suivantes, ainsi que d’autres.</span><span class="sxs-lookup"><span data-stu-id="16b3b-114">This method returns the following **HRESULT** values, as well as others.</span></span>



| <span data-ttu-id="16b3b-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="16b3b-115">Return code</span></span>                                                                              | <span data-ttu-id="16b3b-116">Description</span><span class="sxs-lookup"><span data-stu-id="16b3b-116">Description</span></span>                                                           |
|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <dl> <span data-ttu-id="16b3b-117"><dt>S_OK \* \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="16b3b-117"><dt>\*\*\*\*S_OK\*\*\*\*</dt></span></span> </dl> | <span data-ttu-id="16b3b-118">Le pointeur d’interface de notification a été correctement récupéré.</span><span class="sxs-lookup"><span data-stu-id="16b3b-118">Notification interface pointer was successfully retrieved.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="16b3b-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="16b3b-119">Requirements</span></span>



| <span data-ttu-id="16b3b-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="16b3b-120">Requirement</span></span> | <span data-ttu-id="16b3b-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="16b3b-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="16b3b-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="16b3b-122">Minimum supported client</span></span><br/> | <span data-ttu-id="16b3b-123">Applications de bureau Windows 10, version 1709 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="16b3b-123">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="16b3b-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="16b3b-124">Minimum supported server</span></span><br/> | <span data-ttu-id="16b3b-125">Windows Server, version 1709, \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="16b3b-125">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="16b3b-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="16b3b-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="16b3b-127"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="16b3b-127"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="16b3b-128">MIDL</span><span class="sxs-lookup"><span data-stu-id="16b3b-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="16b3b-129"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="16b3b-129"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="16b3b-130">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="16b3b-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="16b3b-131"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="16b3b-131"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="16b3b-132">DLL</span><span class="sxs-lookup"><span data-stu-id="16b3b-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="16b3b-133"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="16b3b-133"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="16b3b-134">IID</span><span class="sxs-lookup"><span data-stu-id="16b3b-134">IID</span></span><br/>                      | <span data-ttu-id="16b3b-135">IID_IBackgroundCopyJob est défini en tant que 37668D37-507E-4160-9316-26306D150B12</span><span class="sxs-lookup"><span data-stu-id="16b3b-135">IID_IBackgroundCopyJob is defined as 37668D37-507E-4160-9316-26306D150B12</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="16b3b-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="16b3b-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16b3b-137">**Méthode ibackgroundcopyjob**</span><span class="sxs-lookup"><span data-stu-id="16b3b-137">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> <dt>

[<span data-ttu-id="16b3b-138">**IBackgroundCopyCallback**</span><span class="sxs-lookup"><span data-stu-id="16b3b-138">**IBackgroundCopyCallback**</span></span>](ibackgroundcopycallback.md)
</dt> <dt>

[<span data-ttu-id="16b3b-139">**Méthode ibackgroundcopyjob :: GetNotifyFlags**</span><span class="sxs-lookup"><span data-stu-id="16b3b-139">**IBackgroundCopyJob::GetNotifyFlags**</span></span>](ibackgroundcopyjob-getnotifyflags.md)
</dt> <dt>

[<span data-ttu-id="16b3b-140">**Méthode ibackgroundcopyjob :: SetNotifyInterface**</span><span class="sxs-lookup"><span data-stu-id="16b3b-140">**IBackgroundCopyJob::SetNotifyInterface**</span></span>](ibackgroundcopyjob-setnotifyinterface.md)
</dt> </dl>

 

 





