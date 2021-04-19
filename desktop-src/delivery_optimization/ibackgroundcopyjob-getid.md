---
title: Méthode ibackgroundcopyjob GetId, méthode (Deliveryoptimization. h)
description: Récupère l’identificateur utilisé pour identifier le travail dans la file d’attente.
ms.assetid: 05CE5420-22F8-4CFE-BC40-3A29C775854B
keywords:
- GetId (méthode)
- GetId, méthode, interface méthode ibackgroundcopyjob
- Interface méthode ibackgroundcopyjob, méthode GetId
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.GetId
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ade12d72d68b43df7d9ae3d1f33010bb95b7052a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106509922"
---
# <a name="ibackgroundcopyjobgetid-method"></a><span data-ttu-id="57121-106">Méthode ibackgroundcopyjob :: GetId, méthode</span><span class="sxs-lookup"><span data-stu-id="57121-106">IBackgroundCopyJob::GetId method</span></span>

<span data-ttu-id="57121-107">Récupère l’identificateur utilisé pour identifier le travail dans la file d’attente.</span><span class="sxs-lookup"><span data-stu-id="57121-107">Retrieves the identifier used to identify the job in the queue.</span></span>

## <a name="syntax"></a><span data-ttu-id="57121-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="57121-108">Syntax</span></span>


```C++
HRESULT GetId(
  [out] GUID *pJobID
);
```



## <a name="parameters"></a><span data-ttu-id="57121-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="57121-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="57121-110">*pJobID* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="57121-110">*pJobID* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="57121-111">GUID qui identifie le travail dans la file d’attente DO.</span><span class="sxs-lookup"><span data-stu-id="57121-111">GUID that identifies the job within the DO queue.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="57121-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="57121-112">Return value</span></span>

<span data-ttu-id="57121-113">Cette méthode retourne **S_OK** en cas de réussite ou une des valeurs com **HRESULT** standard en cas d’erreur.</span><span class="sxs-lookup"><span data-stu-id="57121-113">This method returns **S_OK** on success or one of the standard COM **HRESULT** values on error.</span></span>

## <a name="remarks"></a><span data-ttu-id="57121-114">Notes</span><span class="sxs-lookup"><span data-stu-id="57121-114">Remarks</span></span>

<span data-ttu-id="57121-115">Le service génère l’identificateur lorsque vous [créez](ibackgroundcopymanager-createjob.md) le travail.</span><span class="sxs-lookup"><span data-stu-id="57121-115">The service generates the identifier when you [create](ibackgroundcopymanager-createjob.md) the job.</span></span> <span data-ttu-id="57121-116">Pour utiliser l’identificateur pour récupérer un pointeur d’interface [**méthode ibackgroundcopyjob**](ibackgroundcopyjob-.md) pour le travail, appelez la méthode [**IBackgroundCopyManager :: GetJob**](ibackgroundcopymanager-getjob.md) .</span><span class="sxs-lookup"><span data-stu-id="57121-116">To use the identifier to retrieve an [**IBackgroundCopyJob**](ibackgroundcopyjob-.md) interface pointer for the job, call the [**IBackgroundCopyManager::GetJob**](ibackgroundcopymanager-getjob.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="57121-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="57121-117">Requirements</span></span>



| <span data-ttu-id="57121-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="57121-118">Requirement</span></span> | <span data-ttu-id="57121-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="57121-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="57121-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="57121-120">Minimum supported client</span></span><br/> | <span data-ttu-id="57121-121">Applications de bureau Windows 10, version 1709 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="57121-121">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="57121-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="57121-122">Minimum supported server</span></span><br/> | <span data-ttu-id="57121-123">Windows Server, version 1709, \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="57121-123">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="57121-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="57121-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="57121-125"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="57121-125"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="57121-126">MIDL</span><span class="sxs-lookup"><span data-stu-id="57121-126">IDL</span></span><br/>                      | <dl> <span data-ttu-id="57121-127"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="57121-127"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="57121-128">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="57121-128">Library</span></span><br/>                  | <dl> <span data-ttu-id="57121-129"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="57121-129"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="57121-130">DLL</span><span class="sxs-lookup"><span data-stu-id="57121-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="57121-131"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="57121-131"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="57121-132">IID</span><span class="sxs-lookup"><span data-stu-id="57121-132">IID</span></span><br/>                      | <span data-ttu-id="57121-133">IID_IBackgroundCopyJob est défini en tant que 37668D37-507E-4160-9316-26306D150B12</span><span class="sxs-lookup"><span data-stu-id="57121-133">IID_IBackgroundCopyJob is defined as 37668D37-507E-4160-9316-26306D150B12</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="57121-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="57121-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57121-135">**Méthode ibackgroundcopyjob**</span><span class="sxs-lookup"><span data-stu-id="57121-135">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> <dt>

[<span data-ttu-id="57121-136">**IBackgroundCopyManager :: CreateJob**</span><span class="sxs-lookup"><span data-stu-id="57121-136">**IBackgroundCopyManager::CreateJob**</span></span>](ibackgroundcopymanager-createjob.md)
</dt> <dt>

[<span data-ttu-id="57121-137">**IBackgroundCopyManager::GetJob**</span><span class="sxs-lookup"><span data-stu-id="57121-137">**IBackgroundCopyManager::GetJob**</span></span>](ibackgroundcopymanager-getjob.md)
</dt> </dl>

 

 





