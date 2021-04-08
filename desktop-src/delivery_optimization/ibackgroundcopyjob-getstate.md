---
title: Méthode méthode ibackgroundcopyjob GetState (Deliveryoptimization. h)
description: Récupère l’état du travail.
ms.assetid: 975AF0FB-37AE-4CE8-9EC1-35A972E422D8
keywords:
- Méthode GetState
- Méthode GetState, interface méthode ibackgroundcopyjob
- Interface méthode ibackgroundcopyjob, méthode GetState
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.GetState
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5b195377a44cab8f336bae8090bacc5ca5624d7c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741717"
---
# <a name="ibackgroundcopyjobgetstate-method"></a><span data-ttu-id="d3335-106">Méthode ibackgroundcopyjob :: GetState, méthode</span><span class="sxs-lookup"><span data-stu-id="d3335-106">IBackgroundCopyJob::GetState method</span></span>

<span data-ttu-id="d3335-107">Récupère l’état du travail.</span><span class="sxs-lookup"><span data-stu-id="d3335-107">Retrieves the state of the job.</span></span>

## <a name="syntax"></a><span data-ttu-id="d3335-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d3335-108">Syntax</span></span>


```C++
HRESULT GetState(
  [out] BG_JOB_STATE *pJobState
);
```



## <a name="parameters"></a><span data-ttu-id="d3335-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d3335-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d3335-110">*pJobState* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="d3335-110">*pJobState* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d3335-111">État du travail.</span><span class="sxs-lookup"><span data-stu-id="d3335-111">The state of the job.</span></span> <span data-ttu-id="d3335-112">Par exemple, l’état indique si le travail est erroné, s’il est en cours de transfert de données ou s’il est suspendu.</span><span class="sxs-lookup"><span data-stu-id="d3335-112">For example, the state reflects whether the job is in error, transferring data, or suspended.</span></span> <span data-ttu-id="d3335-113">Pour obtenir la liste des États de travail, consultez l’énumération [**BG_JOB_STATE**](bg-job-state-.md) .</span><span class="sxs-lookup"><span data-stu-id="d3335-113">For a list of job states, see the [**BG_JOB_STATE**](bg-job-state-.md) enumeration.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d3335-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d3335-114">Return value</span></span>

<span data-ttu-id="d3335-115">Cette méthode retourne les valeurs **HRESULT** suivantes, ainsi que d’autres.</span><span class="sxs-lookup"><span data-stu-id="d3335-115">This method returns the following **HRESULT** values, as well as others.</span></span>



| <span data-ttu-id="d3335-116">Code de retour</span><span class="sxs-lookup"><span data-stu-id="d3335-116">Return code</span></span>                                                                              | <span data-ttu-id="d3335-117">Description</span><span class="sxs-lookup"><span data-stu-id="d3335-117">Description</span></span>                                                 |
|------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <dl> <span data-ttu-id="d3335-118"><dt>S_OK \* \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="d3335-118"><dt>\*\*\*\*S_OK\*\*\*\*</dt></span></span> </dl> | <span data-ttu-id="d3335-119">L’état de la tâche a été récupéré avec succès.</span><span class="sxs-lookup"><span data-stu-id="d3335-119">The state of the job was successfully retrieved.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="d3335-120">Notes</span><span class="sxs-lookup"><span data-stu-id="d3335-120">Remarks</span></span>

<span data-ttu-id="d3335-121">Si vous souhaitez savoir quand un travail est en erreur ou si a transféré tous les fichiers du travail, vous pouvez utiliser cette méthode pour interroger l’état du travail ou vous pouvez vous inscrire pour recevoir une notification lorsque des événements se produisent.</span><span class="sxs-lookup"><span data-stu-id="d3335-121">If you want to know when a job is in error or has transferred all the files in the job, you can use this method to poll for the state of the job or you can register to receive notification when events occur.</span></span> <span data-ttu-id="d3335-122">Pour plus d’informations sur l’inscription à la réception d’une notification d’événement, consultez l’interface [**IBackgroundCopyCallback**](ibackgroundcopycallback.md) .</span><span class="sxs-lookup"><span data-stu-id="d3335-122">For details on registering to receive event notification, see the [**IBackgroundCopyCallback**](ibackgroundcopycallback.md) interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="d3335-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d3335-123">Requirements</span></span>



| <span data-ttu-id="d3335-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d3335-124">Requirement</span></span> | <span data-ttu-id="d3335-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="d3335-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d3335-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d3335-126">Minimum supported client</span></span><br/> | <span data-ttu-id="d3335-127">Applications de bureau Windows 10, version 1709 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d3335-127">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="d3335-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d3335-128">Minimum supported server</span></span><br/> | <span data-ttu-id="d3335-129">Windows Server, version 1709, \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d3335-129">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="d3335-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="d3335-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="d3335-131"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="d3335-131"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="d3335-132">MIDL</span><span class="sxs-lookup"><span data-stu-id="d3335-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d3335-133"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="d3335-133"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="d3335-134">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="d3335-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="d3335-135"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d3335-135"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="d3335-136">DLL</span><span class="sxs-lookup"><span data-stu-id="d3335-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d3335-137"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d3335-137"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="d3335-138">IID</span><span class="sxs-lookup"><span data-stu-id="d3335-138">IID</span></span><br/>                      | <span data-ttu-id="d3335-139">IID_IBackgroundCopyJob est défini en tant que 37668D37-507E-4160-9316-26306D150B12</span><span class="sxs-lookup"><span data-stu-id="d3335-139">IID_IBackgroundCopyJob is defined as 37668D37-507E-4160-9316-26306D150B12</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="d3335-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d3335-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3335-141">**Méthode ibackgroundcopyjob**</span><span class="sxs-lookup"><span data-stu-id="d3335-141">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> <dt>

[<span data-ttu-id="d3335-142">**BG_JOB_STATE**</span><span class="sxs-lookup"><span data-stu-id="d3335-142">**BG_JOB_STATE**</span></span>](bg-job-state-.md)
</dt> <dt>

[<span data-ttu-id="d3335-143">**IBackgroundCopyCallback**</span><span class="sxs-lookup"><span data-stu-id="d3335-143">**IBackgroundCopyCallback**</span></span>](ibackgroundcopycallback.md)
</dt> </dl>

 

 





